---
description: AM_RATE_ResetOnTimeDisc свойство — применяется к Windows Vista и более поздним версиям.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Свойство AM_RATE_ResetOnTimeDisc (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096612"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="cb1b5-103">\_ \_ Свойство ресетонтимедиск Rate</span><span class="sxs-lookup"><span data-stu-id="cb1b5-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="cb1b5-104">Применяется к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="cb1b5-105">Это свойство запрашивает, будет ли декодер повторно синхронизировать метки времени вывода со штампами времени ввода, когда декодер получает пример с флагом небесперебойности.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="cb1b5-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-106">This property is read/write.</span></span>



| <span data-ttu-id="cb1b5-107">Метка</span><span class="sxs-lookup"><span data-stu-id="cb1b5-107">Label</span></span> | <span data-ttu-id="cb1b5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cb1b5-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="cb1b5-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="cb1b5-109">Property Set GUID</span></span> | <span data-ttu-id="cb1b5-110">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="cb1b5-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="cb1b5-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="cb1b5-111">Property ID</span></span>       | <span data-ttu-id="cb1b5-112">\_Ставка \_ ресетонтимедиск</span><span class="sxs-lookup"><span data-stu-id="cb1b5-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="cb1b5-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cb1b5-113">Data Type</span></span>         | <span data-ttu-id="cb1b5-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="cb1b5-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="cb1b5-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb1b5-115">Remarks</span></span>

<span data-ttu-id="cb1b5-116">Это свойство поддерживает плавные изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="cb1b5-117">Если значение этого свойства равно **true** и декодер получает образец входных данных с \_ \_ флагом тимедисконтинуити, декодированный кадр должен иметь ту же метку времени, что и входной фрейм.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="cb1b5-118">Чтобы получить \_ пример \_ флага тимедисконтинуити, вызовите [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) в примере.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="cb1b5-119">Флаг задается в элементе **двсамплефлагс** структуры [**\_ \_ свойств SAMPLE2 AM**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="cb1b5-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="cb1b5-120">Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="cb1b5-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb1b5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cb1b5-121">Requirements</span></span>



| <span data-ttu-id="cb1b5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cb1b5-122">Requirement</span></span> | <span data-ttu-id="cb1b5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cb1b5-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1b5-124">Header</span><span class="sxs-lookup"><span data-stu-id="cb1b5-124">Header</span></span><br/> | <dl> <span data-ttu-id="cb1b5-125"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb1b5-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb1b5-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cb1b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1b5-127">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="cb1b5-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




