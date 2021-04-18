---
title: LISTBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "список".
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- Проигрыватель Windows Media LISTBOX. fontStyle
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694971"
---
# <a name="listboxfontstyle"></a><span data-ttu-id="2460f-104">LISTBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="2460f-104">LISTBOX.fontStyle</span></span>

<span data-ttu-id="2460f-105">Атрибут **FontStyle** указывает или получает стиль шрифта для элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="2460f-105">The **fontStyle** attribute specifies or retrieves the font style for the list box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="2460f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2460f-106">Possible Values</span></span>

<span data-ttu-id="2460f-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2460f-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="2460f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2460f-108">Value</span></span>     | <span data-ttu-id="2460f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2460f-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="2460f-110">Жирный</span><span class="sxs-lookup"><span data-stu-id="2460f-110">Bold</span></span>      | <span data-ttu-id="2460f-111">Начертание шрифта полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="2460f-111">Bold font style.</span></span>      |
| <span data-ttu-id="2460f-112">Курсив</span><span class="sxs-lookup"><span data-stu-id="2460f-112">Italic</span></span>    | <span data-ttu-id="2460f-113">Стиль шрифта курсивом.</span><span class="sxs-lookup"><span data-stu-id="2460f-113">Italic font style.</span></span>    |
| <span data-ttu-id="2460f-114">Underline</span><span class="sxs-lookup"><span data-stu-id="2460f-114">Underline</span></span> | <span data-ttu-id="2460f-115">Подчеркнуть стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="2460f-115">Underline font style.</span></span> |
| <span data-ttu-id="2460f-116">Перечеркивание</span><span class="sxs-lookup"><span data-stu-id="2460f-116">Strikeout</span></span> | <span data-ttu-id="2460f-117">Зачеркивание стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="2460f-117">Strikeout font style.</span></span> |
| <span data-ttu-id="2460f-118">Норм.</span><span class="sxs-lookup"><span data-stu-id="2460f-118">Normal</span></span>    | <span data-ttu-id="2460f-119">Обычный стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="2460f-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="2460f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2460f-120">Remarks</span></span>

<span data-ttu-id="2460f-121">Можно использовать любое сочетание значений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="2460f-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="2460f-122">Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="2460f-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="2460f-123">Для целей отрисовки используется обычный стиль шрифта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2460f-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="2460f-124">Значение по умолчанию, полученное из этого атрибута, — "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="2460f-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="2460f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2460f-125">Requirements</span></span>



| <span data-ttu-id="2460f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2460f-126">Requirement</span></span> | <span data-ttu-id="2460f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2460f-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="2460f-128">Версия</span><span class="sxs-lookup"><span data-stu-id="2460f-128">Version</span></span><br/> | <span data-ttu-id="2460f-129">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2460f-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2460f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2460f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2460f-131">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="2460f-131">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="2460f-132">**Список LISTBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="2460f-132">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> </dl>

 

 





