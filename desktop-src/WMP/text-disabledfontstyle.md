---
title: TEXT. Дисабледфонтстиле
description: Атрибут Дисабледфонтстиле указывает или получает стиль шрифта, используемый для элемента управления "текст", когда он отключен.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Проигрыватель Windows Media TEXT. Дисабледфонтстиле
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717971"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="ee6d2-104">TEXT. Дисабледфонтстиле</span><span class="sxs-lookup"><span data-stu-id="ee6d2-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="ee6d2-105">Атрибут **дисабледфонтстиле** указывает или получает стиль шрифта, используемый для элемента управления "текст", когда он отключен.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="ee6d2-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ee6d2-106">Possible Values</span></span>

<span data-ttu-id="ee6d2-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="ee6d2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ee6d2-108">Value</span></span>     | <span data-ttu-id="ee6d2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ee6d2-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="ee6d2-110">Жирный</span><span class="sxs-lookup"><span data-stu-id="ee6d2-110">Bold</span></span>      | <span data-ttu-id="ee6d2-111">Начертание шрифта полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-111">Bold font style.</span></span>      |
| <span data-ttu-id="ee6d2-112">Курсив</span><span class="sxs-lookup"><span data-stu-id="ee6d2-112">Italic</span></span>    | <span data-ttu-id="ee6d2-113">Стиль шрифта курсивом.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-113">Italic font style.</span></span>    |
| <span data-ttu-id="ee6d2-114">Underline</span><span class="sxs-lookup"><span data-stu-id="ee6d2-114">Underline</span></span> | <span data-ttu-id="ee6d2-115">Подчеркнуть стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-115">Underline font style.</span></span> |
| <span data-ttu-id="ee6d2-116">Перечеркивание</span><span class="sxs-lookup"><span data-stu-id="ee6d2-116">Strikeout</span></span> | <span data-ttu-id="ee6d2-117">Зачеркивание стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-117">Strikeout font style.</span></span> |
| <span data-ttu-id="ee6d2-118">Норм.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-118">Normal</span></span>    | <span data-ttu-id="ee6d2-119">Обычный стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="ee6d2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee6d2-120">Remarks</span></span>

<span data-ttu-id="ee6d2-121">Можно использовать любое сочетание значений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="ee6d2-122">Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="ee6d2-123">Если **дисабледфонтстиле** не указан, используется **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="ee6d2-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="ee6d2-124">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="ee6d2-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee6d2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ee6d2-125">Requirements</span></span>



| <span data-ttu-id="ee6d2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ee6d2-126">Requirement</span></span> | <span data-ttu-id="ee6d2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ee6d2-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ee6d2-128">Версия</span><span class="sxs-lookup"><span data-stu-id="ee6d2-128">Version</span></span><br/> | <span data-ttu-id="ee6d2-129">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ee6d2-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee6d2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee6d2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6d2-131">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="ee6d2-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ee6d2-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="ee6d2-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





