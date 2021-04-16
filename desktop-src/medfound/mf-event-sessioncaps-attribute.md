---
description: Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Атрибут MF_EVENT_SESSIONCAPS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656577"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="ce14d-103">\_ \_ Атрибут СЕССИОНКАПС события MF</span><span class="sxs-lookup"><span data-stu-id="ce14d-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="ce14d-104">Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="ce14d-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce14d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce14d-105">Data type</span></span>

<span data-ttu-id="ce14d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce14d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ce14d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce14d-107">Remarks</span></span>

<span data-ttu-id="ce14d-108">Этот атрибут содержит побитовое **или** с нулевым или более флагами.</span><span class="sxs-lookup"><span data-stu-id="ce14d-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="ce14d-109">Список возможных флагов см. в разделе [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="ce14d-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="ce14d-110">Этот атрибут используется с событием [месессионкапабилитиесчанжед](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="ce14d-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="ce14d-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ce14d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce14d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ce14d-112">Requirements</span></span>



| <span data-ttu-id="ce14d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ce14d-113">Requirement</span></span> | <span data-ttu-id="ce14d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ce14d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce14d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce14d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ce14d-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce14d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce14d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce14d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ce14d-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce14d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ce14d-119">Header</span><span class="sxs-lookup"><span data-stu-id="ce14d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce14d-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce14d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce14d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce14d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce14d-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce14d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce14d-123">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="ce14d-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce14d-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce14d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ce14d-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ce14d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




