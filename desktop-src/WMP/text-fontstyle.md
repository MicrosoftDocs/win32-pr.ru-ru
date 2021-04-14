---
title: TEXT. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "текст".
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Проигрыватель Windows Media TEXT. fontStyle
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647985"
---
# <a name="textfontstyle"></a><span data-ttu-id="e091e-104">TEXT. fontStyle</span><span class="sxs-lookup"><span data-stu-id="e091e-104">TEXT.fontStyle</span></span>

<span data-ttu-id="e091e-105">Атрибут **FontStyle** указывает или получает стиль шрифта для элемента управления "текст".</span><span class="sxs-lookup"><span data-stu-id="e091e-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="e091e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e091e-106">Possible Values</span></span>

<span data-ttu-id="e091e-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e091e-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="e091e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e091e-108">Value</span></span>     | <span data-ttu-id="e091e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e091e-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="e091e-110">Жирный</span><span class="sxs-lookup"><span data-stu-id="e091e-110">Bold</span></span>      | <span data-ttu-id="e091e-111">Начертание шрифта полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="e091e-111">Bold font style.</span></span>            |
| <span data-ttu-id="e091e-112">Курсив</span><span class="sxs-lookup"><span data-stu-id="e091e-112">Italic</span></span>    | <span data-ttu-id="e091e-113">Стиль шрифта курсивом.</span><span class="sxs-lookup"><span data-stu-id="e091e-113">Italic font style.</span></span>          |
| <span data-ttu-id="e091e-114">Underline</span><span class="sxs-lookup"><span data-stu-id="e091e-114">Underline</span></span> | <span data-ttu-id="e091e-115">Подчеркнуть стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="e091e-115">Underline font style.</span></span>       |
| <span data-ttu-id="e091e-116">Перечеркивание</span><span class="sxs-lookup"><span data-stu-id="e091e-116">Strikeout</span></span> | <span data-ttu-id="e091e-117">Зачеркивание стиля шрифта.</span><span class="sxs-lookup"><span data-stu-id="e091e-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="e091e-118">Норм.</span><span class="sxs-lookup"><span data-stu-id="e091e-118">Normal</span></span>    | <span data-ttu-id="e091e-119">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e091e-119">Default.</span></span> <span data-ttu-id="e091e-120">Обычный стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="e091e-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e091e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e091e-121">Remarks</span></span>

<span data-ttu-id="e091e-122">Можно использовать любое сочетание значений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="e091e-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="e091e-123">Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="e091e-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="e091e-124">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="e091e-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e091e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e091e-125">Requirements</span></span>



| <span data-ttu-id="e091e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e091e-126">Requirement</span></span> | <span data-ttu-id="e091e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e091e-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e091e-128">Версия</span><span class="sxs-lookup"><span data-stu-id="e091e-128">Version</span></span><br/> | <span data-ttu-id="e091e-129">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e091e-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e091e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e091e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e091e-131">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="e091e-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





