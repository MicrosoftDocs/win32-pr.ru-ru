---
title: Объект запроса
description: Объект запроса
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700849"
---
# <a name="the-request-object"></a><span data-ttu-id="3fb14-103">Объект запроса</span><span class="sxs-lookup"><span data-stu-id="3fb14-103">The Request Object</span></span>

<span data-ttu-id="3fb14-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3fb14-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3fb14-105">Сервер обрабатывает некоторые методы асинхронно.</span><span class="sxs-lookup"><span data-stu-id="3fb14-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="3fb14-106">Это позволяет коду приложения продолжать работу во время выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="3fb14-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="3fb14-107">Когда клиентское приложение вызывает один из этих методов, элемент управления создает и возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) для запроса.</span><span class="sxs-lookup"><span data-stu-id="3fb14-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="3fb14-108">Объект **request** можно использовать для наблюдения за состоянием метода путем назначения объектной переменной для метода.</span><span class="sxs-lookup"><span data-stu-id="3fb14-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="3fb14-109">В Visual Basic сначала объявите объектную переменную:</span><span class="sxs-lookup"><span data-stu-id="3fb14-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="3fb14-110">В VBScript вы не включаете тип переменной в объявление:</span><span class="sxs-lookup"><span data-stu-id="3fb14-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="3fb14-111">И используйте инструкцию SET Visual Basic, чтобы присвоить переменную вызову метода:</span><span class="sxs-lookup"><span data-stu-id="3fb14-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="3fb14-112">При этом добавляется ссылка на объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="3fb14-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="3fb14-113">Объект **запроса** будет уничтожен, если на него больше нет ссылок.</span><span class="sxs-lookup"><span data-stu-id="3fb14-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="3fb14-114">Место объявления объекта **запроса** и его использование определяет время его существования.</span><span class="sxs-lookup"><span data-stu-id="3fb14-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="3fb14-115">Если объект объявлен как локальный для подпрограммы или функции, он будет разрушен при выходе за пределы области действия. то есть при завершении подпрограммы или функции.</span><span class="sxs-lookup"><span data-stu-id="3fb14-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="3fb14-116">Если объект объявлен глобально, он не уничтожается до тех пор, пока не будет выполнено завершение программы или для объекта будет назначено новое значение (или значение, заданное как пустое).</span><span class="sxs-lookup"><span data-stu-id="3fb14-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="3fb14-117">Объект [**request**](/windows/desktop/lwef/the-request-object) предоставляет несколько свойств, которые можно запросить.</span><span class="sxs-lookup"><span data-stu-id="3fb14-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="3fb14-118">Например, свойство [**Status**](status-property.md) возвращает текущее состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="3fb14-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="3fb14-119">Это свойство можно использовать для проверки состояния запроса:</span><span class="sxs-lookup"><span data-stu-id="3fb14-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="3fb14-120">Свойство [**Status**](status-property.md) возвращает состояние объекта [**запроса**](/windows/desktop/lwef/the-request-object) в виде длинного целого значения.</span><span class="sxs-lookup"><span data-stu-id="3fb14-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="3fb14-121">Состояние</span><span class="sxs-lookup"><span data-stu-id="3fb14-121">Status</span></span> | <span data-ttu-id="3fb14-122">Определение</span><span class="sxs-lookup"><span data-stu-id="3fb14-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="3fb14-123">0</span><span class="sxs-lookup"><span data-stu-id="3fb14-123">0</span></span>      | <span data-ttu-id="3fb14-124">Запрос успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3fb14-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="3fb14-125">1</span><span class="sxs-lookup"><span data-stu-id="3fb14-125">1</span></span>      | <span data-ttu-id="3fb14-126">Сбой запроса.</span><span class="sxs-lookup"><span data-stu-id="3fb14-126">Request failed.</span></span>                                   |
| <span data-ttu-id="3fb14-127">2</span><span class="sxs-lookup"><span data-stu-id="3fb14-127">2</span></span>      | <span data-ttu-id="3fb14-128">Ожидание запроса (в очереди, но не завершено).</span><span class="sxs-lookup"><span data-stu-id="3fb14-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="3fb14-129">3</span><span class="sxs-lookup"><span data-stu-id="3fb14-129">3</span></span>      | <span data-ttu-id="3fb14-130">Запрос прерван.</span><span class="sxs-lookup"><span data-stu-id="3fb14-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="3fb14-131">4</span><span class="sxs-lookup"><span data-stu-id="3fb14-131">4</span></span>      | <span data-ttu-id="3fb14-132">Запрос выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fb14-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="3fb14-133">Объект [**request**](/windows/desktop/lwef/the-request-object) также содержит длинное целое значение в свойстве [**Number**](https://www.bing.com/search?q=**Number**) , которое возвращает ошибку или причину кода [**состояния**](status-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb14-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="3fb14-134">Если нет, это значение равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="3fb14-134">If none, this value is zero (0).</span></span> <span data-ttu-id="3fb14-135">Свойство [**Description**](description-property.md) содержит строковое значение, соответствующее номеру ошибки.</span><span class="sxs-lookup"><span data-stu-id="3fb14-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="3fb14-136">Если строка не существует, **Описание** содержит сообщение об ошибке, определяемое приложением или объектом.</span><span class="sxs-lookup"><span data-stu-id="3fb14-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="3fb14-137">Значения и значение, возвращаемое свойством [**Number**](https://www.bing.com/search?q=**Number**) , см. в разделе [коды ошибок](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3fb14-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="3fb14-138">Сервер размещает запросы анимации в очереди указанного символа.</span><span class="sxs-lookup"><span data-stu-id="3fb14-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="3fb14-139">Это позволяет серверу воспроизводить анимацию в отдельном потоке, и код приложения может продолжаться во время воспроизведения анимации.</span><span class="sxs-lookup"><span data-stu-id="3fb14-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="3fb14-140">При создании ссылки на объект [**запроса**](/windows/desktop/lwef/the-request-object) сервер автоматически оповещает вас о начале или завершении запроса анимации с помощью событий [**рекуестстарт**](https://www.bing.com/search?q=**RequestStart**) и [**рекуесткомплете**](https://www.bing.com/search?q=**RequestComplete**) .</span><span class="sxs-lookup"><span data-stu-id="3fb14-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="3fb14-141">Поскольку методы, возвращающие объекты **запроса** , являются асинхронными и могут не завершиться в области вызывающей функции, объявите ссылку на объект **запроса** глобально.</span><span class="sxs-lookup"><span data-stu-id="3fb14-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="3fb14-142">Для возврата объекта [**запроса**](/windows/desktop/lwef/the-request-object) можно использовать следующие методы: [**жестуреат**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Показать**](show-method.md), [**говорите**](speak-method.md)и [**Wait**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="3fb14-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 