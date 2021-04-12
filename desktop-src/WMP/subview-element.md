---
title: Элемент вложенного представления
description: Элемент вложенного представления
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Обложки проигрывателя Windows Media, элемент вложенного представления
- обложки, элемент вложенного представления
- Элемент вложенного представления
- Справочник по обложкам, элементу вложенного представления
- элементы, вложенное представление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331859"
---
# <a name="subview-element"></a><span data-ttu-id="98d10-108">Элемент вложенного представления</span><span class="sxs-lookup"><span data-stu-id="98d10-108">SUBVIEW Element</span></span>

<span data-ttu-id="98d10-109">Элемент вложенного **представления** предоставляет способ управления частью обложки, например, для предоставления панели управления, которая может быть скрыта, когда она не используется.</span><span class="sxs-lookup"><span data-stu-id="98d10-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="98d10-110">Элементы вложенного **представления** всегда являются дочерними элементами родительского **представления** и могут содержать другой элемент обложки, кроме **представлений**, **тем** и **других элементов вложенного представления.**</span><span class="sxs-lookup"><span data-stu-id="98d10-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="98d10-111">Элемент вложенного **представления** поддерживает следующие атрибуты, которые определены в элементе **View** .</span><span class="sxs-lookup"><span data-stu-id="98d10-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="98d10-112">attribute</span><span class="sxs-lookup"><span data-stu-id="98d10-112">Attribute</span></span>                                                       | <span data-ttu-id="98d10-113">Описание</span><span class="sxs-lookup"><span data-stu-id="98d10-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98d10-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="98d10-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="98d10-115">Указывает или получает цвет фона для элемента управления " **Подпредставление** ".</span><span class="sxs-lookup"><span data-stu-id="98d10-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="98d10-116">Значение по умолчанию — None.</span><span class="sxs-lookup"><span data-stu-id="98d10-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="98d10-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="98d10-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="98d10-118">Указывает или получает фоновое изображение для элемента управления " **Подпредставление** ".</span><span class="sxs-lookup"><span data-stu-id="98d10-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="98d10-119">баккграундимажехуешифт</span><span class="sxs-lookup"><span data-stu-id="98d10-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="98d10-120">Указывает или получает величину, на которую смещается цветовой тон фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="98d10-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="98d10-121">баккграундимажесатуратион</span><span class="sxs-lookup"><span data-stu-id="98d10-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="98d10-122">Указывает или получает значение насыщенности фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="98d10-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="98d10-123">баккграундтилед</span><span class="sxs-lookup"><span data-stu-id="98d10-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="98d10-124">Указывает или получает значение, указывающее, находится ли мозаичное изображение элемента управления " **ПОДпредставление** ".</span><span class="sxs-lookup"><span data-stu-id="98d10-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="98d10-125">ресизебаккграундимаже</span><span class="sxs-lookup"><span data-stu-id="98d10-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="98d10-126">Указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="98d10-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="98d10-127">транспаренциколор</span><span class="sxs-lookup"><span data-stu-id="98d10-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="98d10-128">Указывает или получает цвет прозрачности фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="98d10-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="98d10-129">Элемент вложенного **представления** поддерживает атрибуты окружения, за исключением случаев, где указано.</span><span class="sxs-lookup"><span data-stu-id="98d10-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="98d10-130">Дополнительные сведения см. в разделе [атрибуты окружения](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="98d10-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="98d10-131">Элемент вложенного **представления** может реализовывать следующие внешние обработчики событий: [онендмове](onendmove.md) и [онресизе](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="98d10-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98d10-132">См. также</span><span class="sxs-lookup"><span data-stu-id="98d10-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98d10-133">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="98d10-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="98d10-134">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="98d10-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




