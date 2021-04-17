---
title: Амбиентаттрибутес. Алфаблендто
description: Метод Алфаблендто корректирует свойство Алфабленд за определенный период времени.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Алфаблендто
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694877"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="ab2c2-104">Амбиентаттрибутес. Алфаблендто</span><span class="sxs-lookup"><span data-stu-id="ab2c2-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="ab2c2-105">Метод **алфаблендто** корректирует свойство **алфабленд** за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="ab2c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab2c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab2c2-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*неввал*</span><span class="sxs-lookup"><span data-stu-id="ab2c2-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="ab2c2-108">**Число** (длинное), указывающее новое значение непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="ab2c2-109">Диапазон от 0 (без непрозрачности) до 255 (полная непрозрачность).</span><span class="sxs-lookup"><span data-stu-id="ab2c2-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="ab2c2-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*алфатиме*</span><span class="sxs-lookup"><span data-stu-id="ab2c2-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="ab2c2-111">**Число** (**длинное**), указывающее время в миллисекундах, которое принимает элемент на изменение непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab2c2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab2c2-112">Return Value</span></span>

<span data-ttu-id="ab2c2-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab2c2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab2c2-114">Remarks</span></span>

<span data-ttu-id="ab2c2-115">Этот метод полезен для постепенного отображения или исчезновения элементов.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="ab2c2-116">При использовании **алфаблендто** с **текстовым** элементом, для которого не указан **backgroundColor** , будет использоваться цвет фона черного цвета.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="ab2c2-117">Если цвет переднего плана также является черным (значением по умолчанию для *текста*).**foregroundColor**), текст может стать нечитаемым.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="ab2c2-118">Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="ab2c2-119">Этот атрибут не поддерживается в Windows 98.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab2c2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ab2c2-120">Requirements</span></span>



| <span data-ttu-id="ab2c2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ab2c2-121">Requirement</span></span> | <span data-ttu-id="ab2c2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ab2c2-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ab2c2-123">Версия</span><span class="sxs-lookup"><span data-stu-id="ab2c2-123">Version</span></span><br/> | <span data-ttu-id="ab2c2-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ab2c2-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab2c2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab2c2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2c2-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab2c2-127">**Амбиентаттрибутес. Алфабленд**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="ab2c2-128">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ab2c2-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="ab2c2-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





