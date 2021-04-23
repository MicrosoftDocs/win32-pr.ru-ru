---
title: Амбиентаттрибутес. verticalAlignment
description: Атрибут verticalAlignment указывает или получает значение, обозначающее вертикальное расположение элемента управления при растяжении представления или родительского подпредставления.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699055"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="144aa-104">Амбиентаттрибутес. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="144aa-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="144aa-105">Атрибут **verticalAlignment** указывает или получает значение, обозначающее вертикальное расположение элемента управления при растяжении **представления** или родительского **подпредставления** .</span><span class="sxs-lookup"><span data-stu-id="144aa-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="144aa-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="144aa-106">Possible Values</span></span>

<span data-ttu-id="144aa-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="144aa-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="144aa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="144aa-108">Value</span></span>   | <span data-ttu-id="144aa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="144aa-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144aa-110">top</span><span class="sxs-lookup"><span data-stu-id="144aa-110">top</span></span>     | <span data-ttu-id="144aa-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="144aa-111">Default.</span></span> <span data-ttu-id="144aa-112">Сохраняет положение элемента управления относительно верхнего края **представления** или родительского **подпредставления** при изменении размера представления.</span><span class="sxs-lookup"><span data-stu-id="144aa-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="144aa-113">снизу</span><span class="sxs-lookup"><span data-stu-id="144aa-113">bottom</span></span>  | <span data-ttu-id="144aa-114">Сохраняет положение элемента управления относительно нижней границы **представления** или родительского **подпредставления** при изменении размера представления.</span><span class="sxs-lookup"><span data-stu-id="144aa-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="144aa-115">центр</span><span class="sxs-lookup"><span data-stu-id="144aa-115">center</span></span>  | <span data-ttu-id="144aa-116">Сохраняет расположение элемента управления относительно вертикальной центральной области **представления** **или родительского представления при изменении размера** представления.</span><span class="sxs-lookup"><span data-stu-id="144aa-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="144aa-117">растяжение</span><span class="sxs-lookup"><span data-stu-id="144aa-117">stretch</span></span> | <span data-ttu-id="144aa-118">Сохраняет положение элемента управления относительно верхнего и нижнего полей представления при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="144aa-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="144aa-119">Элемент управления растягивается в соответствии с тем, как будет растягиваться **представление** или родительское **Подпредставление** .</span><span class="sxs-lookup"><span data-stu-id="144aa-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="144aa-120">Фактическое изображение не увеличивается или сжимается, если его размер не изменяется, но при щелчке область расширяется или сжимается, если она не ограничена **клиппингимаже**.</span><span class="sxs-lookup"><span data-stu-id="144aa-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="144aa-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="144aa-121">Remarks</span></span>

<span data-ttu-id="144aa-122">Если **verticalAlignment** не имеет значение "Center", элемент управления оставляет свое исходное расстояние от указанного края или на обоих краях, если задано "Stretch", и размер элемента управления ограничен.</span><span class="sxs-lookup"><span data-stu-id="144aa-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="144aa-123">Если размер элемента управления не может быть увеличен и указан параметр "Stretch", то область, которую вы щелкнули, растягивается.</span><span class="sxs-lookup"><span data-stu-id="144aa-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="144aa-124">Можно задать любое сочетание атрибутов **horizontalAlignment** и **verticalAlignment** .</span><span class="sxs-lookup"><span data-stu-id="144aa-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="144aa-125">Например, если необходимо центрировать элемент управления как по горизонтали, так и по вертикали, установите для параметра **horizontalAlignment** значение Center, а для **verticalAlignment** — значение Center.</span><span class="sxs-lookup"><span data-stu-id="144aa-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="144aa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="144aa-126">Requirements</span></span>



| <span data-ttu-id="144aa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="144aa-127">Requirement</span></span> | <span data-ttu-id="144aa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="144aa-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="144aa-129">Версия</span><span class="sxs-lookup"><span data-stu-id="144aa-129">Version</span></span><br/> | <span data-ttu-id="144aa-130">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="144aa-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="144aa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="144aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144aa-132">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="144aa-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="144aa-133">**Амбиентаттрибутес. horizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="144aa-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





