---
description: Применяется к Windows Vista и более поздним версиям.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Свойство AM_RATE_ReverseMaxFullDataRate (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657673"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="77e6b-103">\_ \_ Свойство реверсемаксфуллдатарате Rate</span><span class="sxs-lookup"><span data-stu-id="77e6b-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="77e6b-104">Применяется к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="77e6b-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="77e6b-105">Возвращает максимальную частоту обратных воспроизведений декодера.</span><span class="sxs-lookup"><span data-stu-id="77e6b-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="77e6b-106">Значением свойства является абсолютное значение максимальной скорости на обратную скорость x 10000.</span><span class="sxs-lookup"><span data-stu-id="77e6b-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="77e6b-107">Например, если максимальная обратная скорость равна-2,0, значение этого свойства равно 20000.</span><span class="sxs-lookup"><span data-stu-id="77e6b-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="77e6b-108">Тип данных для этого свойства — **\_ максфуллдатарате**, то есть `typedef` для типа **Long**.</span><span class="sxs-lookup"><span data-stu-id="77e6b-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="77e6b-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="77e6b-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="77e6b-110">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="77e6b-110">Property Set GUID</span></span> | <span data-ttu-id="77e6b-111">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="77e6b-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="77e6b-112">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="77e6b-112">Property ID</span></span>       | <span data-ttu-id="77e6b-113">\_Ставка \_ реверсемаксфуллдатарате</span><span class="sxs-lookup"><span data-stu-id="77e6b-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="77e6b-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="77e6b-114">Data Type</span></span>         | <span data-ttu-id="77e6b-115">**\_Максфуллдатарате**</span><span class="sxs-lookup"><span data-stu-id="77e6b-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="77e6b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77e6b-116">Remarks</span></span>

<span data-ttu-id="77e6b-117">Это свойство должно предоставлять декодеры, поддерживающие плавный обратный воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="77e6b-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="77e6b-118">Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="77e6b-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77e6b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="77e6b-119">Requirements</span></span>



| <span data-ttu-id="77e6b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="77e6b-120">Requirement</span></span> | <span data-ttu-id="77e6b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="77e6b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77e6b-122">Header</span><span class="sxs-lookup"><span data-stu-id="77e6b-122">Header</span></span><br/> | <dl> <span data-ttu-id="77e6b-123"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e6b-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e6b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77e6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e6b-125">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="77e6b-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




