---
title: Тип кнопки
description: Тип кнопки
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Обложки Windows Media Player для мобильных устройств, типы кнопок
- обложки, типы кнопок
- Справочник по обложкам, кнопкам
- кнопки в обложках, типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887919"
---
# <a name="button-type"></a><span data-ttu-id="1f526-107">Тип кнопки</span><span class="sxs-lookup"><span data-stu-id="1f526-107">Button Type</span></span>

<span data-ttu-id="1f526-108">Кнопки бывают двух общих типов: расположение и регион.</span><span class="sxs-lookup"><span data-stu-id="1f526-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="1f526-109">Каждый общий тип имеет три конкретных типа, что делает шесть типов кнопок полностью.</span><span class="sxs-lookup"><span data-stu-id="1f526-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="1f526-110">Типы кнопок являются устаревшими в обложках проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1f526-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="1f526-111">Типы кнопок расположения</span><span class="sxs-lookup"><span data-stu-id="1f526-111">Location Button Types</span></span>

<span data-ttu-id="1f526-112">Кнопки расположения используют координаты для определения их расположений относительно фона.</span><span class="sxs-lookup"><span data-stu-id="1f526-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="1f526-113">В следующей таблице приведены значения, допустимые для типов кнопок расположения.</span><span class="sxs-lookup"><span data-stu-id="1f526-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="1f526-114">Не нужно определять значения для типов, которые не будут использоваться в обложке.</span><span class="sxs-lookup"><span data-stu-id="1f526-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="1f526-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1f526-115">Value</span></span>  | <span data-ttu-id="1f526-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1f526-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f526-117">push</span><span class="sxs-lookup"><span data-stu-id="1f526-117">Push</span></span>   | <span data-ttu-id="1f526-118">Определяет кнопку, которая запускает событие один раз.</span><span class="sxs-lookup"><span data-stu-id="1f526-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="1f526-119">Кнопка должна быть отправлена каждый раз, чтобы активировать дальнейшие события.</span><span class="sxs-lookup"><span data-stu-id="1f526-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="1f526-120">Примером может быть кнопка, которая перемещается на следующий элемент в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1f526-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="1f526-121">Расположение кнопки определяется ее координатами.</span><span class="sxs-lookup"><span data-stu-id="1f526-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1f526-122">Переключение</span><span class="sxs-lookup"><span data-stu-id="1f526-122">Toggle</span></span> | <span data-ttu-id="1f526-123">Определяет кнопку, которая активирует событие, которое изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="1f526-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="1f526-124">Состояние остается до тех пор, пока кнопка не будет отправлена снова.</span><span class="sxs-lookup"><span data-stu-id="1f526-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="1f526-125">Примером является кнопка, которая перемещает список воспроизведения в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="1f526-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="1f526-126">Когда список воспроизведения перемещается в случайное состояние, он остается в случайном порядке, пока кнопка не будет снова отправлена.</span><span class="sxs-lookup"><span data-stu-id="1f526-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="1f526-127">Расположение кнопки определяется ее координатами.</span><span class="sxs-lookup"><span data-stu-id="1f526-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1f526-128">2Push</span><span class="sxs-lookup"><span data-stu-id="1f526-128">2Push</span></span>  | <span data-ttu-id="1f526-129">Определяет кнопку, которая запускает событие, а затем переходит в состояние, готовое к запуску другого события.</span><span class="sxs-lookup"><span data-stu-id="1f526-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="1f526-130">Эти два состояния переключаются при каждом нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="1f526-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="1f526-131">Примером является кнопка, которая использует функцию **плайпаусе** для переключения между воспроизведением и приостановкой текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f526-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="1f526-132">Когда кнопка помещается в первый раз, запускается основное состояние воспроизведения и отображается дополнительное изображение, указывающее, что можно запустить событие **паузы** .</span><span class="sxs-lookup"><span data-stu-id="1f526-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="1f526-133">При повторном нажатии кнопки происходит состояние приостановки и отображается исходное изображение, указывающее, что можно запустить событие **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="1f526-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="1f526-134">Расположение кнопки определяется ее координатами.</span><span class="sxs-lookup"><span data-stu-id="1f526-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="1f526-135">Типы кнопок региона</span><span class="sxs-lookup"><span data-stu-id="1f526-135">Region Button Types</span></span>

<span data-ttu-id="1f526-136">Кнопки области используют цветовые области в изображении региона, чтобы определить, где будут обрабатываться касания для определенной кнопки.</span><span class="sxs-lookup"><span data-stu-id="1f526-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="1f526-137">В следующей таблице приведены значения, допустимые для типов кнопок Region.</span><span class="sxs-lookup"><span data-stu-id="1f526-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="1f526-138">Не нужно определять значения для типов, которые не будут использоваться в обложке.</span><span class="sxs-lookup"><span data-stu-id="1f526-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="1f526-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1f526-139">Value</span></span>     | <span data-ttu-id="1f526-140">Описание</span><span class="sxs-lookup"><span data-stu-id="1f526-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f526-141">пушхит</span><span class="sxs-lookup"><span data-stu-id="1f526-141">PushHit</span></span>   | <span data-ttu-id="1f526-142">Аналогично значению кнопки отправки, за исключением того, что область попадания кнопки определяется значением цвета в изображении региона.</span><span class="sxs-lookup"><span data-stu-id="1f526-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="1f526-143">тогглехит</span><span class="sxs-lookup"><span data-stu-id="1f526-143">ToggleHit</span></span> | <span data-ttu-id="1f526-144">Аналогично значению переключателя, за исключением того, что область попадания кнопки определяется значением цвета в изображении региона.</span><span class="sxs-lookup"><span data-stu-id="1f526-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="1f526-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="1f526-145">2PushHit</span></span>  | <span data-ttu-id="1f526-146">Аналогично значению кнопки 2Push, за исключением того, что область попадания кнопки определяется значением цвета в изображении региона.</span><span class="sxs-lookup"><span data-stu-id="1f526-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="1f526-147">См. также</span><span class="sxs-lookup"><span data-stu-id="1f526-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f526-148">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="1f526-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




