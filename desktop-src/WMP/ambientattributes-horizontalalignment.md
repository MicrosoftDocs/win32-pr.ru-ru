---
title: Амбиентаттрибутес. horizontalAlignment
description: Атрибут horizontalAlignment указывает или получает значение, указывающее горизонтальное расположение элемента управления при изменении размера представления или родительского подпредставления.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694541"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="5ec7d-104">Амбиентаттрибутес. horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="5ec7d-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="5ec7d-105">Атрибут **horizontalAlignment** указывает или получает значение, указывающее горизонтальное расположение элемента управления при изменении размера **представления** или родительского **подпредставления** .</span><span class="sxs-lookup"><span data-stu-id="5ec7d-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="5ec7d-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5ec7d-106">Possible Values</span></span>

<span data-ttu-id="5ec7d-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="5ec7d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5ec7d-108">Value</span></span>   | <span data-ttu-id="5ec7d-109">Описание:</span><span class="sxs-lookup"><span data-stu-id="5ec7d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec7d-110">Левое</span><span class="sxs-lookup"><span data-stu-id="5ec7d-110">left</span></span>    | <span data-ttu-id="5ec7d-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-111">Default.</span></span> <span data-ttu-id="5ec7d-112">Сохраняет положение элемента управления относительно левого края **представления** или родительского **подпредставления** при изменении размера представления.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="5ec7d-113">right</span><span class="sxs-lookup"><span data-stu-id="5ec7d-113">right</span></span>   | <span data-ttu-id="5ec7d-114">Сохраняет положение элемента управления относительно правого **представления** или родительского **подпредставления** при изменении размера представления.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="5ec7d-115">центр</span><span class="sxs-lookup"><span data-stu-id="5ec7d-115">center</span></span>  | <span data-ttu-id="5ec7d-116">Сохраняет расположение элемента управления относительно горизонтального центра **представления** или родительского **подпредставления** при изменении размера представления.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="5ec7d-117">растяжение</span><span class="sxs-lookup"><span data-stu-id="5ec7d-117">stretch</span></span> | <span data-ttu-id="5ec7d-118">Сохраняет положение элемента управления относительно левого и правого полей **представления** или родительского **подпредставления** при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="5ec7d-119">Элемент управления растягивается в соответствии с растяжением **представления** или **подпредставления** .</span><span class="sxs-lookup"><span data-stu-id="5ec7d-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="5ec7d-120">Фактическое изображение не увеличивается или сжимается, если его размер не изменяется, но при щелчке область расширяется или сжимается, если она не ограничена **клиппингимаже**.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5ec7d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ec7d-121">Remarks</span></span>

<span data-ttu-id="5ec7d-122">Если **horizontalAlignment** не имеет значение "Center", элемент управления оставляет свое исходное расстояние от указанного края или на обоих краях, если задано "Stretch", и размер элемента управления ограничен.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="5ec7d-123">Если размер элемента управления не может быть увеличен и указан параметр "Stretch", то область, которую вы щелкнули, растягивается.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="5ec7d-124">Можно задать любое сочетание **horizontalAlignment** и **verticalAlignment**.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="5ec7d-125">Например, если нужно центрировать элемент управления как по горизонтали, так и по вертикали, задайте horizontalAlignment = "Center" verticalAlignment = "Center".</span><span class="sxs-lookup"><span data-stu-id="5ec7d-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec7d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5ec7d-126">Requirements</span></span>



| <span data-ttu-id="5ec7d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5ec7d-127">Requirement</span></span> | <span data-ttu-id="5ec7d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5ec7d-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5ec7d-129">Версия</span><span class="sxs-lookup"><span data-stu-id="5ec7d-129">Version</span></span><br/> | <span data-ttu-id="5ec7d-130">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="5ec7d-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ec7d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ec7d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec7d-132">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="5ec7d-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ec7d-133">**Амбиентаттрибутес. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="5ec7d-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="5ec7d-134">**Амбиентаттрибутес. Клиппингимаже**</span><span class="sxs-lookup"><span data-stu-id="5ec7d-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





