---
title: EDITBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "поле ввода".
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- FontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694537"
---
# <a name="editboxfontstyle"></a><span data-ttu-id="b1b5a-104">EDITBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="b1b5a-104">EDITBOX.fontStyle</span></span>

<span data-ttu-id="b1b5a-105">Атрибут **FontStyle** указывает или получает стиль шрифта для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="b1b5a-105">The **fontStyle** attribute specifies or retrieves the font style for the edit box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="b1b5a-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b1b5a-106">Possible Values</span></span>

<span data-ttu-id="b1b5a-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="b1b5a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b1b5a-108">Value</span></span>     | <span data-ttu-id="b1b5a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b1b5a-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="b1b5a-110">Жирный</span><span class="sxs-lookup"><span data-stu-id="b1b5a-110">Bold</span></span>      | <span data-ttu-id="b1b5a-111">Начертание шрифта полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-111">Bold font style.</span></span>      |
| <span data-ttu-id="b1b5a-112">Курсив</span><span class="sxs-lookup"><span data-stu-id="b1b5a-112">Italic</span></span>    | <span data-ttu-id="b1b5a-113">Стиль шрифта курсивом.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-113">Italic font style.</span></span>    |
| <span data-ttu-id="b1b5a-114">Underline</span><span class="sxs-lookup"><span data-stu-id="b1b5a-114">Underline</span></span> | <span data-ttu-id="b1b5a-115">Подчеркнуть стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-115">Underline font style.</span></span> |
| <span data-ttu-id="b1b5a-116">Перечеркивание</span><span class="sxs-lookup"><span data-stu-id="b1b5a-116">Strikeout</span></span> | <span data-ttu-id="b1b5a-117">Зачеркивание стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-117">Strikeout font style.</span></span> |
| <span data-ttu-id="b1b5a-118">Норм.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-118">Normal</span></span>    | <span data-ttu-id="b1b5a-119">Обычный стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="b1b5a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1b5a-120">Remarks</span></span>

<span data-ttu-id="b1b5a-121">Можно использовать любое сочетание значений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="b1b5a-122">Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="b1b5a-123">Для целей отрисовки используется обычный стиль шрифта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1b5a-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="b1b5a-124">Значение по умолчанию, полученное из этого атрибута, — "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="b1b5a-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b5a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b1b5a-125">Requirements</span></span>



| <span data-ttu-id="b1b5a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b1b5a-126">Requirement</span></span> | <span data-ttu-id="b1b5a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b1b5a-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="b1b5a-128">Версия</span><span class="sxs-lookup"><span data-stu-id="b1b5a-128">Version</span></span><br/> | <span data-ttu-id="b1b5a-129">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b1b5a-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1b5a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1b5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b5a-131">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="b1b5a-131">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="b1b5a-132">**EDITBOX. Фонтфаце**</span><span class="sxs-lookup"><span data-stu-id="b1b5a-132">**EDITBOX.fontFace**</span></span>](editbox-fontface.md)
</dt> <dt>

[<span data-ttu-id="b1b5a-133">**EDITBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="b1b5a-133">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> </dl>

 

 





