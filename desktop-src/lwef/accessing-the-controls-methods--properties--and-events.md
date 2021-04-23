---
title: Доступ к методам, свойствам и событиям элементов управления
description: Доступ к методам, свойствам и событиям элементов управления
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410881"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="e1bf1-103">Доступ к методам, свойствам и событиям элементов управления</span><span class="sxs-lookup"><span data-stu-id="e1bf1-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="e1bf1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1bf1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e1bf1-105">Использование управления Microsoft Agent с Visual Basic очень похоже на использование элемента управления с помощью VBScript, за исключением того, что события в Visual Basic должны включать тип данных передаваемых параметров.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="e1bf1-106">Добавление элемента управления Microsoft Agent в форму автоматически включит события Microsoft Agent с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="e1bf1-107">При запуске приложения также будет автоматически создано соединение с сервером агента.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="e1bf1-108">Вы также можете использовать синтаксис создания обжект'с языка программирования для создания экземпляра элемента управления во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="e1bf1-109">Например, в Visual Basic (5,0 или более поздней версии) при включении элемента управления Microsoft Agent 2,0 в ссылки проекта можно использовать [**с событиями**](https://www.bing.com/search?q=**With+Events**). [**Новое**](https://www.bing.com/search?q=**New**) объявление.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="e1bf1-110">Если ссылка не включена, VB выдает ошибку, указывающую на то, что не удалось запустить Microsoft Agent (код ошибки 80042502).</span><span class="sxs-lookup"><span data-stu-id="e1bf1-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="e1bf1-111">Для версий Visual Basic, предшествовавших 5,0, можно использовать ключевое слово [**New**](https://www.bing.com/search?q=**New**) в VB без объявления [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) или функции [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) VB, но эти соглашения не будут предоставлять события элемента управления агента.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="e1bf1-112">Также необходимо использовать свойство [**Connected**](https://www.bing.com/search?q=**Connected**) , прежде чем ссылаться на любые методы или свойства агента.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="e1bf1-113">Если этого не сделать, VB выдаст ошибку, указывающую, что не удалось запустить агент Майкрософт (код ошибки 80042502).</span><span class="sxs-lookup"><span data-stu-id="e1bf1-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="e1bf1-114">Аналогичным образом для других языков программирования может потребоваться использовать свойство [**Connected**](https://www.bing.com/search?q=**Connected**) , чтобы установить соединение с сервером модели COM, прежде чем ваш код сможет вызывать методы или свойства элемента управления агента.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="e1bf1-115">Кроме того, для некоторых языков программирования методы и свойства агента не могут быть предоставлены напрямую, если не объявить элемент управления агента с помощью его типа.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="e1bf1-116">Например, в Microsoft Access 97 необходимо объявить объект как агент типа, чтобы увидеть методы и свойства, отображаемые в раскрывающемся списке "автоматическое отображение членов" при вводе.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="e1bf1-117">Большинство языков программирования, поддерживающих элементы управления ActiveX, следуют соглашениям, похожим на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="e1bf1-118">Для языков программирования, которые не поддерживают коллекции объектов, можно использовать метод [**символов**](https://www.bing.com/search?q=**Character**) и [**Командный**](https://www.bing.com/search?q=**Command**) метод для доступа к методам и свойствам элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="e1bf1-119">Языки программирования, такие как Visual Basic, которые предоставляют доступ к типам объектов, предоставляемым элементом управления агента, позволяют использовать их в объявлениях объектов.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="e1bf1-120">Например, вместо объявления объекта как универсального типа:</span><span class="sxs-lookup"><span data-stu-id="e1bf1-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="e1bf1-121">Можно объявить объект как конкретный тип:</span><span class="sxs-lookup"><span data-stu-id="e1bf1-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="e1bf1-122">Это может повысить общую производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="e1bf1-123">Для некоторых типов объектов можно обнаружить два одинаковых типа, за исключением суффикса "ex".</span><span class="sxs-lookup"><span data-stu-id="e1bf1-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="e1bf1-124">Если оба существуют, используйте тип "ex", так как это обеспечивает все функции агента.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="e1bf1-125">Аналоги, отличные от "ex", включены только в целях обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="e1bf1-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




