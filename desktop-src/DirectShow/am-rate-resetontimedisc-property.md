---
description: Применяется к Windows Vista и более поздним версиям.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Свойство AM_RATE_ResetOnTimeDisc (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910252"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="9e202-103">\_ \_ Свойство ресетонтимедиск Rate</span><span class="sxs-lookup"><span data-stu-id="9e202-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="9e202-104">Применяется к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="9e202-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="9e202-105">Это свойство запрашивает, будет ли декодер повторно синхронизировать метки времени вывода со штампами времени ввода, когда декодер получает пример с флагом небесперебойности.</span><span class="sxs-lookup"><span data-stu-id="9e202-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="9e202-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9e202-106">This property is read/write.</span></span>



| <span data-ttu-id="9e202-107">Метка</span><span class="sxs-lookup"><span data-stu-id="9e202-107">Label</span></span> | <span data-ttu-id="9e202-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9e202-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="9e202-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="9e202-109">Property Set GUID</span></span> | <span data-ttu-id="9e202-110">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="9e202-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="9e202-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="9e202-111">Property ID</span></span>       | <span data-ttu-id="9e202-112">\_Ставка \_ ресетонтимедиск</span><span class="sxs-lookup"><span data-stu-id="9e202-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="9e202-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e202-113">Data Type</span></span>         | <span data-ttu-id="9e202-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e202-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="9e202-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e202-115">Remarks</span></span>

<span data-ttu-id="9e202-116">Это свойство поддерживает плавные изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="9e202-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="9e202-117">Если значение этого свойства равно **true** и декодер получает образец входных данных с \_ \_ флагом тимедисконтинуити, декодированный кадр должен иметь ту же метку времени, что и входной фрейм.</span><span class="sxs-lookup"><span data-stu-id="9e202-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="9e202-118">Чтобы получить \_ пример \_ флага тимедисконтинуити, вызовите [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) в примере.</span><span class="sxs-lookup"><span data-stu-id="9e202-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="9e202-119">Флаг задается в элементе **двсамплефлагс** структуры [**\_ \_ свойств SAMPLE2 AM**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="9e202-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="9e202-120">Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="9e202-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e202-121">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="9e202-121">Requirements</span></span>



| <span data-ttu-id="9e202-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9e202-122">Requirement</span></span> | <span data-ttu-id="9e202-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9e202-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e202-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9e202-124">Header</span></span><br/> | <dl> <span data-ttu-id="9e202-125"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e202-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e202-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9e202-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e202-127">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="9e202-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




