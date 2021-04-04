---
title: Доступ к службам с помощью Java
description: Доступ к службам с помощью Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987416"
---
# <a name="accessing-services-using-java"></a><span data-ttu-id="10d27-103">Доступ к службам с помощью Java</span><span class="sxs-lookup"><span data-stu-id="10d27-103">Accessing Services Using Java</span></span>

<span data-ttu-id="10d27-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10d27-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="10d27-105">Вы также можете получить доступ к службам Microsoft Agent из Java-приложения.</span><span class="sxs-lookup"><span data-stu-id="10d27-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="10d27-106">Многие функции, доступные через интерфейсы Microsoft Agent, возвращают значения через параметры, передаваемые по ссылке.</span><span class="sxs-lookup"><span data-stu-id="10d27-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="10d27-107">Чтобы передать эти параметры из Java, необходимо создать одноэлементные массивы в коде и передать их в качестве параметров в соответствующую функцию.</span><span class="sxs-lookup"><span data-stu-id="10d27-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="10d27-108">Если вы используете Microsoft Visual J++ и запускаете мастер библиотеки типов Java на сервере Microsoft Agent, обратитесь к файлу summary.txt, чтобы узнать, какие функции требуются для аргументов массива.</span><span class="sxs-lookup"><span data-stu-id="10d27-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="10d27-109">Процедура аналогична этой процедуре в C; для создания экземпляра сервера используется интерфейс [**иажентекс**](https://www.bing.com/search?q=**IAgentEx**) , а затем загружается символ:</span><span class="sxs-lookup"><span data-stu-id="10d27-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



<span data-ttu-id="10d27-110">При загрузке символов из удаленного расположения HTTP, такого как веб-сайт, процедура немного отличается.</span><span class="sxs-lookup"><span data-stu-id="10d27-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="10d27-111">В этом случае метод [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) является асинхронным и вызовет исключение COM \_ в ожидании ожидания (0x8000000a).</span><span class="sxs-lookup"><span data-stu-id="10d27-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="10d27-112">Необходимо перехватить это исключение и правильно обработайте его, как это делается в следующих функциях:</span><span class="sxs-lookup"><span data-stu-id="10d27-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



<span data-ttu-id="10d27-113">Затем получите интерфейс [**иажентчарактерекс**](https://www.bing.com/search?q=**IAgentCharacterEx**) , который позволяет получить доступ к его методам:</span><span class="sxs-lookup"><span data-stu-id="10d27-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="10d27-114">Аналогично, чтобы получать уведомления о событиях, необходимо реализовать интерфейс [**иажентнотифисинк**](https://www.bing.com/search?q=**IAgentNotifySink**) или [**иажентнотифисинкекс**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , создав и зарегистрировав объект этого типа:</span><span class="sxs-lookup"><span data-stu-id="10d27-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



<span data-ttu-id="10d27-115">Чтобы получить доступ к Microsoft Agent из Java-приложения, необходимо создать классы Java, которые устанавливаются вместе с приложением.</span><span class="sxs-lookup"><span data-stu-id="10d27-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="10d27-116">Для создания этих файлов можно использовать мастер библиотек типов Visual J++ Java, например.</span><span class="sxs-lookup"><span data-stu-id="10d27-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="10d27-117">Если вы планируете разместить приложение на веб-странице, необходимо создать подписанный CAB-файл Java, включающий созданные файлы классов, загружаемые вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="10d27-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="10d27-118">Файлы классов необходимы для доступа к серверу Microsoft Agent Server, поскольку он является COM-объектом, который выполняется за пределами песочницы Java.</span><span class="sxs-lookup"><span data-stu-id="10d27-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="10d27-119">Дополнительные сведения о Trust-Based безопасности для Java см. в разделе <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="10d27-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 