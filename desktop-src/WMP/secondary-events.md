---
title: Вторичные события
description: Вторичные события
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Обложки проигрывателя Windows Media, вторичные события
- обложки, вторичные события
- события, вторичные
- Написание кода для обложек, вторичных событий
- Вторичные события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486960"
---
# <a name="secondary-events"></a><span data-ttu-id="9d14e-108">Вторичные события</span><span class="sxs-lookup"><span data-stu-id="9d14e-108">Secondary Events</span></span>

<span data-ttu-id="9d14e-109">Вы можете определить, какие другие события выполняются при срабатывании определенного события.</span><span class="sxs-lookup"><span data-stu-id="9d14e-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="9d14e-110">Например, при нажатии кнопки мыши может потребоваться определить, была ли нажата клавиша ALT в то же время.</span><span class="sxs-lookup"><span data-stu-id="9d14e-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="9d14e-111">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="9d14e-111">Event Attributes</span></span>

<span data-ttu-id="9d14e-112">Для обложек поддерживаются следующие атрибуты событий:</span><span class="sxs-lookup"><span data-stu-id="9d14e-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="9d14e-113">**алткэй**</span><span class="sxs-lookup"><span data-stu-id="9d14e-113">**altKey**</span></span>
-   <span data-ttu-id="9d14e-114">**переключатель**</span><span class="sxs-lookup"><span data-stu-id="9d14e-114">**button**</span></span>
-   <span data-ttu-id="9d14e-115">**клиенткс**</span><span class="sxs-lookup"><span data-stu-id="9d14e-115">**clientX**</span></span>
-   <span data-ttu-id="9d14e-116">**Клиентская**</span><span class="sxs-lookup"><span data-stu-id="9d14e-116">**clientY**</span></span>
-   <span data-ttu-id="9d14e-117">**ктрлкэй**</span><span class="sxs-lookup"><span data-stu-id="9d14e-117">**ctrlKey**</span></span>
-   <span data-ttu-id="9d14e-118">**фромелемент**</span><span class="sxs-lookup"><span data-stu-id="9d14e-118">**fromElement**</span></span>
-   <span data-ttu-id="9d14e-119">**оффсеткс**</span><span class="sxs-lookup"><span data-stu-id="9d14e-119">**offsetX**</span></span>
-   <span data-ttu-id="9d14e-120">**смещение**</span><span class="sxs-lookup"><span data-stu-id="9d14e-120">**offsetY**</span></span>
-   <span data-ttu-id="9d14e-121">**скринкс**</span><span class="sxs-lookup"><span data-stu-id="9d14e-121">**screenX**</span></span>
-   <span data-ttu-id="9d14e-122">**экран**</span><span class="sxs-lookup"><span data-stu-id="9d14e-122">**screenY**</span></span>
-   <span data-ttu-id="9d14e-123">**шифткэй**</span><span class="sxs-lookup"><span data-stu-id="9d14e-123">**shiftKey**</span></span>
-   <span data-ttu-id="9d14e-124">**срцелемент**</span><span class="sxs-lookup"><span data-stu-id="9d14e-124">**srcElement**</span></span>
-   <span data-ttu-id="9d14e-125">**тоелемент**</span><span class="sxs-lookup"><span data-stu-id="9d14e-125">**toElement**</span></span>
-   <span data-ttu-id="9d14e-126">**x**</span><span class="sxs-lookup"><span data-stu-id="9d14e-126">**x**</span></span>
-   <span data-ttu-id="9d14e-127">**y**</span><span class="sxs-lookup"><span data-stu-id="9d14e-127">**y**</span></span>
-   <span data-ttu-id="9d14e-128">**keyCode**</span><span class="sxs-lookup"><span data-stu-id="9d14e-128">**keyCode**</span></span>

<span data-ttu-id="9d14e-129">Дополнительные сведения об этих атрибутах см. в [справочнике по программированию для обложки](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9d14e-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="9d14e-130">Использование дополнительных событий</span><span class="sxs-lookup"><span data-stu-id="9d14e-130">Using Secondary Events</span></span>

<span data-ttu-id="9d14e-131">Обрабатывать атрибуты событий можно только в коде JScript.</span><span class="sxs-lookup"><span data-stu-id="9d14e-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="9d14e-132">Необходимо использовать следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="9d14e-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="9d14e-133">*евентаттрибутенаме* — имя атрибута события.</span><span class="sxs-lookup"><span data-stu-id="9d14e-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="9d14e-134">Например, чтобы определить, была ли нажата клавиша ALT во время события щелчка, можно использовать следующие строки в коде JScript:</span><span class="sxs-lookup"><span data-stu-id="9d14e-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="9d14e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9d14e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d14e-136">**Обработка событий**</span><span class="sxs-lookup"><span data-stu-id="9d14e-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




