---
description: Применяется к Windows Vista и более поздним версиям.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Свойство AM_RATE_ResetOnTimeDisc (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689052"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="42e2d-103">\_ \_ Свойство ресетонтимедиск Rate</span><span class="sxs-lookup"><span data-stu-id="42e2d-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="42e2d-104">Применяется к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="42e2d-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="42e2d-105">Это свойство запрашивает, будет ли декодер повторно синхронизировать метки времени вывода со штампами времени ввода, когда декодер получает пример с флагом небесперебойности.</span><span class="sxs-lookup"><span data-stu-id="42e2d-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="42e2d-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="42e2d-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="42e2d-107">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="42e2d-107">Property Set GUID</span></span> | <span data-ttu-id="42e2d-108">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="42e2d-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="42e2d-109">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="42e2d-109">Property ID</span></span>       | <span data-ttu-id="42e2d-110">\_Ставка \_ ресетонтимедиск</span><span class="sxs-lookup"><span data-stu-id="42e2d-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="42e2d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42e2d-111">Data Type</span></span>         | <span data-ttu-id="42e2d-112">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="42e2d-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="42e2d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42e2d-113">Remarks</span></span>

<span data-ttu-id="42e2d-114">Это свойство поддерживает плавные изменения скорости.</span><span class="sxs-lookup"><span data-stu-id="42e2d-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="42e2d-115">Если значение этого свойства равно **true** и декодер получает образец входных данных с \_ \_ флагом тимедисконтинуити, декодированный кадр должен иметь ту же метку времени, что и входной фрейм.</span><span class="sxs-lookup"><span data-stu-id="42e2d-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="42e2d-116">Чтобы получить \_ пример \_ флага тимедисконтинуити, вызовите [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) в примере.</span><span class="sxs-lookup"><span data-stu-id="42e2d-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="42e2d-117">Флаг задается в элементе **двсамплефлагс** структуры [**\_ \_ свойств SAMPLE2 AM**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="42e2d-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="42e2d-118">Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="42e2d-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42e2d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="42e2d-119">Requirements</span></span>



| <span data-ttu-id="42e2d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="42e2d-120">Requirement</span></span> | <span data-ttu-id="42e2d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="42e2d-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42e2d-122">Header</span><span class="sxs-lookup"><span data-stu-id="42e2d-122">Header</span></span><br/> | <dl> <span data-ttu-id="42e2d-123"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e2d-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e2d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42e2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e2d-125">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="42e2d-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




