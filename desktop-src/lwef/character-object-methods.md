---
title: Методы символьных объектов
description: Методы символьных объектов
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987375"
---
# <a name="character-object-methods"></a><span data-ttu-id="6a073-103">Методы символьных объектов</span><span class="sxs-lookup"><span data-stu-id="6a073-103">Character Object Methods</span></span>

<span data-ttu-id="6a073-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a073-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6a073-105">Сервер также предоставляет методы для каждого символа в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="6a073-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="6a073-106">Поддерживаются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="6a073-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="6a073-107">**Вызова**</span><span class="sxs-lookup"><span data-stu-id="6a073-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="6a073-108">**жестуреат**</span><span class="sxs-lookup"><span data-stu-id="6a073-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="6a073-109">**Получить**</span><span class="sxs-lookup"><span data-stu-id="6a073-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="6a073-110">**Скрыть**</span><span class="sxs-lookup"><span data-stu-id="6a073-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="6a073-111">**Прервать**</span><span class="sxs-lookup"><span data-stu-id="6a073-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="6a073-112">**Прослушивание**</span><span class="sxs-lookup"><span data-stu-id="6a073-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="6a073-113">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="6a073-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="6a073-114">**Воспроизведение**</span><span class="sxs-lookup"><span data-stu-id="6a073-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="6a073-115">**Казывающи**</span><span class="sxs-lookup"><span data-stu-id="6a073-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="6a073-116">**шовпопупмену**</span><span class="sxs-lookup"><span data-stu-id="6a073-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="6a073-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="6a073-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="6a073-118">**Stop**</span><span class="sxs-lookup"><span data-stu-id="6a073-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="6a073-119">**стопалл**</span><span class="sxs-lookup"><span data-stu-id="6a073-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="6a073-120">**Ситуацию**</span><span class="sxs-lookup"><span data-stu-id="6a073-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="6a073-121">**Ожидание**</span><span class="sxs-lookup"><span data-stu-id="6a073-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="6a073-122">Чтобы использовать метод, сослаться на символ в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a073-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="6a073-123">В VBScript и Visual Basic это можно сделать, указав идентификатор символа:</span><span class="sxs-lookup"><span data-stu-id="6a073-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



<span data-ttu-id="6a073-124">Чтобы упростить синтаксис кода, можно определить переменную объекта и задать для нее ссылку на символьный объект в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) . Затем можно использовать переменную для ссылки на методы или свойства символа.</span><span class="sxs-lookup"><span data-stu-id="6a073-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="6a073-125">В следующем примере показано, как это можно сделать с помощью инструкции Visual Basic Set:</span><span class="sxs-lookup"><span data-stu-id="6a073-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



<span data-ttu-id="6a073-126">В Visual Basic 5,0 можно также создать ссылку, объявляя переменную как [**символьный**](/windows/desktop/lwef/the-characters-object)объект:</span><span class="sxs-lookup"><span data-stu-id="6a073-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



<span data-ttu-id="6a073-127">Объявление объекта типа Иажентктлчарактерекс делает возможным раннее связывание объекта, что приводит к лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="6a073-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="6a073-128">В VBScript нельзя объявлять ссылку как конкретный тип.</span><span class="sxs-lookup"><span data-stu-id="6a073-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="6a073-129">Однако можно просто объявить ссылку на переменную:</span><span class="sxs-lookup"><span data-stu-id="6a073-129">However, you can simply declare the variable reference:</span></span>


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



<span data-ttu-id="6a073-130">Некоторые языки программирования не поддерживают коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a073-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="6a073-131">Однако доступ к методам [**символьного**](/windows/desktop/lwef/the-characters-object) объекта можно получить с помощью [**символьного**](character-method.md) метода:</span><span class="sxs-lookup"><span data-stu-id="6a073-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="6a073-132">Кроме того, можно создать ссылку на объект [**character**](/windows/desktop/lwef/the-characters-object) , чтобы упростить выполнение кода скрипта:</span><span class="sxs-lookup"><span data-stu-id="6a073-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 