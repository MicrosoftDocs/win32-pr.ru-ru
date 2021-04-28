---
description: AM_RATE_ReverseMaxFullDataRate свойство — применяется к Windows Vista и более поздним версиям.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Свойство AM_RATE_ReverseMaxFullDataRate (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099972"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="88089-103">\_ \_ Свойство реверсемаксфуллдатарате Rate</span><span class="sxs-lookup"><span data-stu-id="88089-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="88089-104">Применяется к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="88089-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="88089-105">Возвращает максимальную частоту обратных воспроизведений декодера.</span><span class="sxs-lookup"><span data-stu-id="88089-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="88089-106">Значением свойства является абсолютное значение максимальной скорости на обратную скорость x 10000.</span><span class="sxs-lookup"><span data-stu-id="88089-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="88089-107">Например, если максимальная обратная скорость равна-2,0, значение этого свойства равно 20000.</span><span class="sxs-lookup"><span data-stu-id="88089-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="88089-108">Тип данных для этого свойства — **\_ максфуллдатарате**, то есть `typedef` для типа **Long**.</span><span class="sxs-lookup"><span data-stu-id="88089-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="88089-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88089-109">This property is read-only.</span></span>



| <span data-ttu-id="88089-110">Метка</span><span class="sxs-lookup"><span data-stu-id="88089-110">Label</span></span> | <span data-ttu-id="88089-111">Значение</span><span class="sxs-lookup"><span data-stu-id="88089-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="88089-112">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="88089-112">Property Set GUID</span></span> | <span data-ttu-id="88089-113">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="88089-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="88089-114">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="88089-114">Property ID</span></span>       | <span data-ttu-id="88089-115">\_Ставка \_ реверсемаксфуллдатарате</span><span class="sxs-lookup"><span data-stu-id="88089-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="88089-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="88089-116">Data Type</span></span>         | <span data-ttu-id="88089-117">**\_Максфуллдатарате**</span><span class="sxs-lookup"><span data-stu-id="88089-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="88089-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="88089-118">Remarks</span></span>

<span data-ttu-id="88089-119">Это свойство должно предоставлять декодеры, поддерживающие плавный обратный воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="88089-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="88089-120">Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="88089-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88089-121">Требования</span><span class="sxs-lookup"><span data-stu-id="88089-121">Requirements</span></span>



| <span data-ttu-id="88089-122">Требование</span><span class="sxs-lookup"><span data-stu-id="88089-122">Requirement</span></span> | <span data-ttu-id="88089-123">Значение</span><span class="sxs-lookup"><span data-stu-id="88089-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88089-124">Header</span><span class="sxs-lookup"><span data-stu-id="88089-124">Header</span></span><br/> | <dl> <span data-ttu-id="88089-125"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="88089-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88089-126">См. также</span><span class="sxs-lookup"><span data-stu-id="88089-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88089-127">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="88089-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




