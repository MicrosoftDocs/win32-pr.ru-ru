---
title: TEXT. Ховерфонтстиле
description: Атрибут Ховерфонтстиле указывает или получает стиль шрифта, используемый для текстового элемента управления при наведении на него курсора мыши.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Проигрыватель Windows Media TEXT. Ховерфонтстиле
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648076"
---
# <a name="texthoverfontstyle"></a><span data-ttu-id="6a750-104">TEXT. Ховерфонтстиле</span><span class="sxs-lookup"><span data-stu-id="6a750-104">TEXT.hoverFontStyle</span></span>

<span data-ttu-id="6a750-105">Атрибут **ховерфонтстиле** указывает или получает стиль шрифта, используемый для текстового элемента управления при наведении на него курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="6a750-105">The **hoverFontStyle** attribute specifies or retrieves the font style used for the Text control when the mouse cursor hovers over it.</span></span>

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="6a750-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6a750-106">Possible Values</span></span>

<span data-ttu-id="6a750-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6a750-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="6a750-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6a750-108">Value</span></span>     | <span data-ttu-id="6a750-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6a750-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="6a750-110">Жирный</span><span class="sxs-lookup"><span data-stu-id="6a750-110">Bold</span></span>      | <span data-ttu-id="6a750-111">Начертание шрифта полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="6a750-111">Bold font style.</span></span>      |
| <span data-ttu-id="6a750-112">Курсив</span><span class="sxs-lookup"><span data-stu-id="6a750-112">Italic</span></span>    | <span data-ttu-id="6a750-113">Стиль шрифта курсивом.</span><span class="sxs-lookup"><span data-stu-id="6a750-113">Italic font style.</span></span>    |
| <span data-ttu-id="6a750-114">Underline</span><span class="sxs-lookup"><span data-stu-id="6a750-114">Underline</span></span> | <span data-ttu-id="6a750-115">Подчеркнуть стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="6a750-115">Underline font style.</span></span> |
| <span data-ttu-id="6a750-116">Перечеркивание</span><span class="sxs-lookup"><span data-stu-id="6a750-116">Strikeout</span></span> | <span data-ttu-id="6a750-117">Зачеркивание стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="6a750-117">Strikeout font style.</span></span> |
| <span data-ttu-id="6a750-118">Норм.</span><span class="sxs-lookup"><span data-stu-id="6a750-118">Normal</span></span>    | <span data-ttu-id="6a750-119">Обычный стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="6a750-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="6a750-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a750-120">Remarks</span></span>

<span data-ttu-id="6a750-121">Можно использовать любое сочетание значений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="6a750-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="6a750-122">Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="6a750-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="6a750-123">Если **ховерфонтстиле** не указан, используется **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="6a750-123">If **hoverFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="6a750-124">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="6a750-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a750-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6a750-125">Requirements</span></span>



| <span data-ttu-id="6a750-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6a750-126">Requirement</span></span> | <span data-ttu-id="6a750-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6a750-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6a750-128">Версия</span><span class="sxs-lookup"><span data-stu-id="6a750-128">Version</span></span><br/> | <span data-ttu-id="6a750-129">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6a750-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a750-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a750-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a750-131">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="6a750-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="6a750-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="6a750-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





