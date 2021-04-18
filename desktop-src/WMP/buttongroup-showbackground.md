---
title: BUTTONGROUP. Шовбаккграунд
description: Атрибут Шовбаккграунд указывает или получает значение, указывающее, отображает ли BUTTONGROUP только кнопки, или отображает полный точечный рисунок, указанный в атрибуте Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Шовбаккграунд
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694854"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="e0089-104">BUTTONGROUP. Шовбаккграунд</span><span class="sxs-lookup"><span data-stu-id="e0089-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="e0089-105">Атрибут **шовбаккграунд** указывает или получает значение, указывающее, отображает ли **BUTTONGROUP** только кнопки, или отображает полный точечный рисунок, указанный в атрибуте **Image** .</span><span class="sxs-lookup"><span data-stu-id="e0089-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="e0089-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e0089-106">Possible Values</span></span>

<span data-ttu-id="e0089-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e0089-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e0089-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e0089-108">Value</span></span> | <span data-ttu-id="e0089-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e0089-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0089-110">true</span><span class="sxs-lookup"><span data-stu-id="e0089-110">true</span></span>  | <span data-ttu-id="e0089-111">Отображаются кнопки, а область, не занятая кнопками, рисуется из растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="e0089-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="e0089-112">false</span><span class="sxs-lookup"><span data-stu-id="e0089-112">false</span></span> | <span data-ttu-id="e0089-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0089-113">Default.</span></span> <span data-ttu-id="e0089-114">Отображаются только кнопки.</span><span class="sxs-lookup"><span data-stu-id="e0089-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e0089-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0089-115">Remarks</span></span>

<span data-ttu-id="e0089-116">Если **шовбаккграунд** имеет значение true, будет виден весь основной **образ** .</span><span class="sxs-lookup"><span data-stu-id="e0089-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="e0089-117">Если **шовбаккграунд** имеет значение false, будут подготавливаться только области, соответствующие назначенным цветам **маппингимаже** .</span><span class="sxs-lookup"><span data-stu-id="e0089-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="e0089-118">Иными словами, будут видны только **буттонелементс** с назначенными **маппингколор** .</span><span class="sxs-lookup"><span data-stu-id="e0089-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="e0089-119">Если указано недопустимое значение, сохраняется предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="e0089-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0089-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e0089-120">Requirements</span></span>



| <span data-ttu-id="e0089-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e0089-121">Requirement</span></span> | <span data-ttu-id="e0089-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e0089-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e0089-123">Версия</span><span class="sxs-lookup"><span data-stu-id="e0089-123">Version</span></span><br/> | <span data-ttu-id="e0089-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e0089-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0089-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0089-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0089-126">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="e0089-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="e0089-127">**БУТТОНЕЛЕМЕНТ. Маппингколор**</span><span class="sxs-lookup"><span data-stu-id="e0089-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="e0089-128">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="e0089-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="e0089-129">**BUTTONGROUP. Маппингимаже**</span><span class="sxs-lookup"><span data-stu-id="e0089-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





