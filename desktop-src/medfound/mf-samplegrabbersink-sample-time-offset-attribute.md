---
description: Смещение между отметкой времени в каждом примере, полученным с помощью образца области захвата, и времени, в котором этот пример представляет образец.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Атрибут MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647207"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="9d5a6-103">\_ \_ \_ Атрибут смещения времени выборки MF самплеграбберсинк \_</span><span class="sxs-lookup"><span data-stu-id="9d5a6-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="9d5a6-104">Смещение между отметкой времени в каждом примере, полученным с помощью образца области захвата, и времени, в котором этот пример представляет образец.</span><span class="sxs-lookup"><span data-stu-id="9d5a6-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d5a6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9d5a6-105">Data type</span></span>

<span data-ttu-id="9d5a6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="9d5a6-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5a6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d5a6-107">Remarks</span></span>

<span data-ttu-id="9d5a6-108">Этот атрибут можно задать для объекта [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемого функцией [**мфкреатесамплеграбберсинкактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="9d5a6-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="9d5a6-109">Этот атрибут позволяет функции обратного вызова образца захвата получать примеры, предшествующие времени презентации.</span><span class="sxs-lookup"><span data-stu-id="9d5a6-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="9d5a6-110">Когда образец захвата получает новый пример, он представляет пример на время *t* −, где *t* — это метка времени в *примере, а* *offset* — значение этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="9d5a6-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="9d5a6-111">Если этот атрибут не задан, значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9d5a6-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="9d5a6-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9d5a6-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5a6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9d5a6-113">Requirements</span></span>



| <span data-ttu-id="9d5a6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9d5a6-114">Requirement</span></span> | <span data-ttu-id="9d5a6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5a6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5a6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d5a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5a6-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d5a6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9d5a6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d5a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5a6-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d5a6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9d5a6-120">Header</span><span class="sxs-lookup"><span data-stu-id="9d5a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5a6-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5a6-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5a6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d5a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5a6-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d5a6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d5a6-124">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="9d5a6-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="9d5a6-125">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="9d5a6-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="9d5a6-126">**имфсамплеграбберсинккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9d5a6-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="9d5a6-127">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d5a6-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




