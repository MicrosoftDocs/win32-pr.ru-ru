---
title: Внутренние события
description: Внутренние события
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Обложки проигрывателя Windows Media, внутренние события
- обложки, внутренние события
- события, внутренние
- Написание кода для обложек, внутренние события
- внутренние события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986260"
---
# <a name="internal-events"></a><span data-ttu-id="1eb08-108">Внутренние события</span><span class="sxs-lookup"><span data-stu-id="1eb08-108">Internal Events</span></span>

<span data-ttu-id="1eb08-109">Можно обнаружить изменения, происходящие в проигрывателе Windows Media, или изменения в собственной обложке.</span><span class="sxs-lookup"><span data-stu-id="1eb08-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="1eb08-110">Это могут быть изменения в свойствах или методах объекта проигрывателя Windows Media, изменениях в атрибутах обложки и т. д.</span><span class="sxs-lookup"><span data-stu-id="1eb08-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="1eb08-111">Изменения свойств проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="1eb08-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="1eb08-112">Вы можете обрабатывать изменения в проигрывателе Windows Media с помощью прослушивателя вмппроп.</span><span class="sxs-lookup"><span data-stu-id="1eb08-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="1eb08-113">Необходимо настроить прослушиватель как значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="1eb08-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="1eb08-114">Вставьте значение в двойные кавычки и начните со слова «вмппроп», за которым следует двоеточие.</span><span class="sxs-lookup"><span data-stu-id="1eb08-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="1eb08-115">Затем укажите свойство, которое нужно прослушать.</span><span class="sxs-lookup"><span data-stu-id="1eb08-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="1eb08-116">При изменении свойства значение атрибута также изменится.</span><span class="sxs-lookup"><span data-stu-id="1eb08-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="1eb08-117">Например, чтобы изменить значение элемента Slider при каждом изменении значения атрибута **CurrentPosition** , введите следующее:</span><span class="sxs-lookup"><span data-stu-id="1eb08-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="1eb08-118">**Важно!** Не используйте вмппроп в методах проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1eb08-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="1eb08-119">Могут возникнуть непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="1eb08-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="1eb08-120">Изменения методов проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="1eb08-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="1eb08-121">Можно сделать так, чтобы Обложка отвечала на доступность методов в проигрывателе Windows Media с помощью вмпенаблед и вмпдисаблед.</span><span class="sxs-lookup"><span data-stu-id="1eb08-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="1eb08-122">Они используются аналогично прослушивателю вмппроп, за исключением того, что их можно использовать только в методах **управляющего** объекта, которые поддерживаются методом **Available** .</span><span class="sxs-lookup"><span data-stu-id="1eb08-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="1eb08-123">Например, можно включить кнопку только в том случае, если включен метод **Play** , используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="1eb08-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="1eb08-124">**Важно!** Не используйте вмпенаблед или вмпдисаблед в свойствах проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1eb08-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="1eb08-125">Могут возникнуть непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="1eb08-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="1eb08-126">Изменения атрибутов обложки</span><span class="sxs-lookup"><span data-stu-id="1eb08-126">Skin Attribute Changes</span></span>

<span data-ttu-id="1eb08-127">Вы можете реагировать на изменения в атрибутах обложки одним из двух способов: с помощью вмппроп или события **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="1eb08-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="1eb08-128">Вмппроп можно использовать для прослушивания изменений в собственной обложке.</span><span class="sxs-lookup"><span data-stu-id="1eb08-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="1eb08-129">Например, чтобы отобразить значение ползунка в текстовом поле, можно ввести следующее:</span><span class="sxs-lookup"><span data-stu-id="1eb08-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="1eb08-130">Для обработки событий внутри элемента можно использовать событие **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="1eb08-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="1eb08-131">Необходимо прикрепить имя атрибута, который необходимо отложить для **\_ изменения**.</span><span class="sxs-lookup"><span data-stu-id="1eb08-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="1eb08-132">Например, если нужно отвести значение текстового поля, введите:</span><span class="sxs-lookup"><span data-stu-id="1eb08-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="1eb08-133">Затем можно присвоить строку JScript, которая будет выполняться при изменении значения.</span><span class="sxs-lookup"><span data-stu-id="1eb08-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="1eb08-134">Например, чтобы ответить на изменение в значении текстового поля, которое можно использовать для настройки громкости проигрывателя Windows Media, введите следующий текст внутри элемента **Text** в качестве атрибута:</span><span class="sxs-lookup"><span data-stu-id="1eb08-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="1eb08-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1eb08-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eb08-136">**Обработка событий**</span><span class="sxs-lookup"><span data-stu-id="1eb08-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




