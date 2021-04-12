---
title: Подключенное свойство
description: Подключенное свойство
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331088"
---
# <a name="connected-property"></a><span data-ttu-id="69766-103">Подключенное свойство</span><span class="sxs-lookup"><span data-stu-id="69766-103">Connected Property</span></span>

<span data-ttu-id="69766-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69766-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="69766-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="69766-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="69766-106">Возвращает или задает значение, указывающее, подключен ли текущий элемент управления к серверу Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="69766-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="69766-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="69766-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="69766-108">*агент. \* \* подключен* \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="69766-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="69766-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="69766-109">Part</span></span>      | <span data-ttu-id="69766-110">Описание</span><span class="sxs-lookup"><span data-stu-id="69766-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69766-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="69766-111">*boolean*</span></span> | <span data-ttu-id="69766-112">Логическое выражение, указывающее, подключен ли элемент управления.</span><span class="sxs-lookup"><span data-stu-id="69766-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="69766-113">**Значение true** Элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="69766-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69766-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69766-114">Remarks</span></span>

<span data-ttu-id="69766-115">Во многих случаях при указании элемента управления автоматически создается подключение к серверу Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="69766-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="69766-116">Например, при указании идентификатора CLSID элемента управления Microsoft Agent в <OBJECT> теге на веб-странице автоматически открывается соединение с сервером, а при выходе из страницы закрывается соединение.</span><span class="sxs-lookup"><span data-stu-id="69766-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="69766-117">Аналогичным образом, для Visual Basic или других языков, позволяющих удалить элемент управления в форме, при запуске программы автоматически открывается подключение, и при выходе из программы закрывается подключение.</span><span class="sxs-lookup"><span data-stu-id="69766-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="69766-118">Если сервер в данный момент не запущен, он запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="69766-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="69766-119">Однако если вы хотите создать элемент управления агента во время выполнения, вам также может потребоваться явно открыть новое соединение с сервером с помощью свойства **Connected** .</span><span class="sxs-lookup"><span data-stu-id="69766-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="69766-120">Например, в Visual Basic можно создать объект ActiveX во время выполнения с помощью инструкции SET с ключевым словом **New** (или функцией CreateObject).</span><span class="sxs-lookup"><span data-stu-id="69766-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="69766-121">При этом создается объект, который не может создать соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="69766-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="69766-122">Можно использовать свойство **Connected** перед любым кодом, который вызывает интерфейс программирования Microsoft Agent, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="69766-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="69766-123">Создание элемента управления с помощью этого метода не предоставляет события элемента управления агента.</span><span class="sxs-lookup"><span data-stu-id="69766-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="69766-124">В Visual Basic 5,0 (и более поздних версиях) можно получить доступ к событиям элемента управления, включив элемент управления в ссылки проекта, и использовать ключевое слово **WithEvents** в объявлении переменной:</span><span class="sxs-lookup"><span data-stu-id="69766-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="69766-125">При использовании **WithEvents** для создания экземпляра элемента управления агента во время выполнения автоматически открывается подключение к серверу Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="69766-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="69766-126">Поэтому нет необходимости включать **подключенную** инструкцию.</span><span class="sxs-lookup"><span data-stu-id="69766-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="69766-127">Можно закрыть подключение к серверу, освобождая все созданные ссылки на объекты агента, такие как Иажентктлчарактерекс и Иажентктлкоммандекс.</span><span class="sxs-lookup"><span data-stu-id="69766-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="69766-128">Необходимо также освободить ссылку на сам элемент управления агента.</span><span class="sxs-lookup"><span data-stu-id="69766-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="69766-129">В Visual Basic можно освободить ссылку на объект, присвоив его переменной значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="69766-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="69766-130">Если вы загрузили символы, выгрузите их перед освобождением объекта символов.</span><span class="sxs-lookup"><span data-stu-id="69766-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="69766-131">Невозможно закрыть подключение к серверу, освобождая ссылки, в которых был добавлен компонент.</span><span class="sxs-lookup"><span data-stu-id="69766-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="69766-132">Например, невозможно закрыть подключение к серверу на веб-страницах, где используется <OBJECT> тег для объявления элемента управления или в Visual Basic приложении, в котором элемент управления перекрывается в форме.</span><span class="sxs-lookup"><span data-stu-id="69766-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="69766-133">При освобождении всех ссылок на агенты будет уменьшен рабочий набор агента, подключение останется до перехода на следующую страницу или выхода из приложения.</span><span class="sxs-lookup"><span data-stu-id="69766-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





