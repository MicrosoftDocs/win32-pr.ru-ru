---
description: Атрибут частоты кадров указывает частоту кадров в секунду.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Атрибут частоты кадров (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990091"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="78e1a-103">Атрибут частоты кадров (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="78e1a-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="78e1a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="78e1a-104">\[Deprecated.</span></span> <span data-ttu-id="78e1a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="78e1a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="78e1a-106">Атрибут указывает частоту кадров `framerate` в секунду.</span><span class="sxs-lookup"><span data-stu-id="78e1a-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="78e1a-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="78e1a-107">Possible Values</span></span>

<span data-ttu-id="78e1a-108">Значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="78e1a-108">Floating-point value.</span></span> <span data-ttu-id="78e1a-109">Значение должно включать начальный ноль перед десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="78e1a-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="78e1a-110">Например, 0,3, а не. 3.</span><span class="sxs-lookup"><span data-stu-id="78e1a-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="78e1a-111">Не используйте более семи десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="78e1a-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="78e1a-112">Применение</span><span class="sxs-lookup"><span data-stu-id="78e1a-112">Applies To</span></span>

<span data-ttu-id="78e1a-113">[**клип**](clip-element.md), [**Группа**](group-element.md), [**временная шкала**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="78e1a-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="78e1a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78e1a-114">Remarks</span></span>

<span data-ttu-id="78e1a-115">Для элемента **Clip** этот атрибут указывает частоту кадров источника по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78e1a-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="78e1a-116">Укажите атрибут для Анддиб последовательностей изображений.</span><span class="sxs-lookup"><span data-stu-id="78e1a-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="78e1a-117">Для неподвижных изображений установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="78e1a-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="78e1a-118">Для последовательности DIB используйте ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="78e1a-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="78e1a-119">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78e1a-119">The default value is zero.</span></span>

<span data-ttu-id="78e1a-120">Для элемента **Group** этот атрибут указывает частоту выходных кадров для группы.</span><span class="sxs-lookup"><span data-stu-id="78e1a-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="78e1a-121">Для элемента **временной шкалы** этот атрибут задает частоту кадров по умолчанию для всех групп.</span><span class="sxs-lookup"><span data-stu-id="78e1a-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="78e1a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78e1a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e1a-123">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="78e1a-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="78e1a-124">**Иамтимелинесрк:: Сетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="78e1a-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="78e1a-125">**Иамтимелинеграуп:: Сетаутпутфпс**</span><span class="sxs-lookup"><span data-stu-id="78e1a-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="78e1a-126">**Иамтимелине:: Сетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="78e1a-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



