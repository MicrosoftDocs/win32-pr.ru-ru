---
title: Элемент VIDEO
description: Элемент VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Обложки проигрывателя Windows Media, элемент VIDEO
- обложки, элемент VIDEO
- Элемент VIDEO
- Справочник по обложкам, элементу VIDEO
- элементы, видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776640"
---
# <a name="video-element"></a><span data-ttu-id="f4c89-108">Элемент VIDEO</span><span class="sxs-lookup"><span data-stu-id="f4c89-108">VIDEO Element</span></span>

<span data-ttu-id="f4c89-109">Элемент **Video** предоставляет способ управления видеоокном в обложке с помощью следующих атрибутов и событий.</span><span class="sxs-lookup"><span data-stu-id="f4c89-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="f4c89-110">Для удобства также предоставляется предварительно определенный элемент **Video** .</span><span class="sxs-lookup"><span data-stu-id="f4c89-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="f4c89-111">Элемент **Video** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f4c89-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="f4c89-112">attribute</span><span class="sxs-lookup"><span data-stu-id="f4c89-112">Attribute</span></span>                                            | <span data-ttu-id="f4c89-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f4c89-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c89-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f4c89-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="f4c89-115">Указывает или получает цвет фона элемента управления видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="f4c89-116">курсор</span><span class="sxs-lookup"><span data-stu-id="f4c89-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="f4c89-117">Указывает или получает значение курсора, которое используется при наведении мыши на область видео, доступную для щелчка.</span><span class="sxs-lookup"><span data-stu-id="f4c89-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="f4c89-118">fullScreen</span><span class="sxs-lookup"><span data-stu-id="f4c89-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="f4c89-119">Указывает или получает значение, указывающее, отображается ли видео в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="f4c89-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="f4c89-120">Можно задать только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4c89-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="f4c89-121">маинтаинаспектратио</span><span class="sxs-lookup"><span data-stu-id="f4c89-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="f4c89-122">Указывает или получает значение, указывающее, будет ли видео поддерживать пропорции при попытке разместить его в пределах ширины и высоты, определенных для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f4c89-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="f4c89-123">шринктофит</span><span class="sxs-lookup"><span data-stu-id="f4c89-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="f4c89-124">Указывает или получает значение, указывающее, будет ли видео уменьшаться до ширины и высоты, определенных для элемента управления видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="f4c89-125">стретчтофит</span><span class="sxs-lookup"><span data-stu-id="f4c89-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="f4c89-126">Указывает или получает значение, указывающее, будет ли видео растягиваться по ширине и высоте, определенным для элемента управления видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="f4c89-127">Сказок</span><span class="sxs-lookup"><span data-stu-id="f4c89-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="f4c89-128">Указывает или получает текст подсказки для окна видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="f4c89-129">без окон</span><span class="sxs-lookup"><span data-stu-id="f4c89-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="f4c89-130">Указывает или получает значение, указывающее, будет ли элемент управления видео отображаться в окне или без окон. то есть независимо от того, будет ли весь прямоугольник элемента управления видимым в любое время или же его можно обрезать.</span><span class="sxs-lookup"><span data-stu-id="f4c89-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="f4c89-131">Можно задать только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="f4c89-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="f4c89-132">масштаб</span><span class="sxs-lookup"><span data-stu-id="f4c89-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="f4c89-133">Указывает процент, на который масштабируется видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="f4c89-134">Элемент **Video** может реализовывать следующие обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="f4c89-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="f4c89-135">Обработчик событий</span><span class="sxs-lookup"><span data-stu-id="f4c89-135">Event handler</span></span>                          | <span data-ttu-id="f4c89-136">Описание</span><span class="sxs-lookup"><span data-stu-id="f4c89-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c89-137">онвидеоенд</span><span class="sxs-lookup"><span data-stu-id="f4c89-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="f4c89-138">Обрабатывает событие, возникающее, когда видео останавливает отрисовку и выгружается.</span><span class="sxs-lookup"><span data-stu-id="f4c89-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="f4c89-139">онвидеостарт</span><span class="sxs-lookup"><span data-stu-id="f4c89-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="f4c89-140">Обрабатывает событие, возникающее при загрузке видео и начале его подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="f4c89-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="f4c89-141">Элемент **Video** поддерживает атрибуты окружения и может реализовывать обработчики событий окружения, за исключением случаев, когда отмечено.</span><span class="sxs-lookup"><span data-stu-id="f4c89-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="f4c89-142">Дополнительные сведения см. в разделе [атрибуты окружения](ambient-attributes.md) и [обработчики событий окружения](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f4c89-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="f4c89-143">Стандартные элементы видео — это обычные элементы **видео** с различными параметрами общих атрибутов, заданных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4c89-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="f4c89-144">Доступны следующие предварительно определенные элементы видео.</span><span class="sxs-lookup"><span data-stu-id="f4c89-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="f4c89-145">Предопределенное видео</span><span class="sxs-lookup"><span data-stu-id="f4c89-145">Predefined VIDEO</span></span>         | <span data-ttu-id="f4c89-146">Описание</span><span class="sxs-lookup"><span data-stu-id="f4c89-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="f4c89-147">вмпвидео</span><span class="sxs-lookup"><span data-stu-id="f4c89-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="f4c89-148">Элемент **видео** , который растягивает видео при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="f4c89-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4c89-149">См. также</span><span class="sxs-lookup"><span data-stu-id="f4c89-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c89-150">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="f4c89-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




