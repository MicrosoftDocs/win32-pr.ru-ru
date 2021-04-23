---
description: Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Атрибут MF_EVENT_SESSIONCAPS_DELTA (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423801"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="d39dc-103">\_ \_ \_ Разностный атрибут сессионкапс события MF</span><span class="sxs-lookup"><span data-stu-id="d39dc-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="d39dc-104">Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="d39dc-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d39dc-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d39dc-105">Data type</span></span>

<span data-ttu-id="d39dc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d39dc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d39dc-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d39dc-107">Remarks</span></span>

<span data-ttu-id="d39dc-108">Этот атрибут содержит битовую маску, указывающую, какие флаги возможностей изменились.</span><span class="sxs-lookup"><span data-stu-id="d39dc-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="d39dc-109">Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="d39dc-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="d39dc-110">Биты имеют значение 1 в битовой маске по любой из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="d39dc-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="d39dc-111">Соответствующий бит для возможностей изменился с 0 на 1.</span><span class="sxs-lookup"><span data-stu-id="d39dc-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="d39dc-112">Соответствующий бит возможностей изменился с 1 на 0.</span><span class="sxs-lookup"><span data-stu-id="d39dc-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="d39dc-113">Соответствующий бит остался 1, но подробные сведения об этой возможности изменились.</span><span class="sxs-lookup"><span data-stu-id="d39dc-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="d39dc-114">Например, изменена максимальная скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d39dc-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="d39dc-115">Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d39dc-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="d39dc-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d39dc-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39dc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d39dc-117">Requirements</span></span>



| <span data-ttu-id="d39dc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d39dc-118">Requirement</span></span> | <span data-ttu-id="d39dc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d39dc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d39dc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d39dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d39dc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d39dc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d39dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d39dc-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d39dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="d39dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d39dc-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d39dc-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39dc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d39dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39dc-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d39dc-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d39dc-128">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="d39dc-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d39dc-129">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="d39dc-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d39dc-130">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d39dc-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




