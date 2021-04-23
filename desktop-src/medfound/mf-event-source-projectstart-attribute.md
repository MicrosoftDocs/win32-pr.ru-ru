---
description: Указывает время начала для топологии сегмента.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Атрибут MF_EVENT_SOURCE_PROJECTSTART (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913735"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="33200-103">\_ \_ Атрибут прожектстарт источника события MF \_</span><span class="sxs-lookup"><span data-stu-id="33200-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="33200-104">Указывает время начала для топологии сегмента.</span><span class="sxs-lookup"><span data-stu-id="33200-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="33200-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="33200-105">Data type</span></span>

<span data-ttu-id="33200-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="33200-106">**UINT64**</span></span>

<span data-ttu-id="33200-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="33200-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33200-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33200-108">Remarks</span></span>

<span data-ttu-id="33200-109">Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="33200-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="33200-110">Источник Sequencer задает этот атрибут, если топология текущего сегмента имеет атрибут [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="33200-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="33200-111">Два атрибута имеют одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="33200-111">The two attributes have the same value.</span></span>

<span data-ttu-id="33200-112">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="33200-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="33200-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="33200-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="33200-114">Требования</span><span class="sxs-lookup"><span data-stu-id="33200-114">Requirements</span></span>



| <span data-ttu-id="33200-115">Требование</span><span class="sxs-lookup"><span data-stu-id="33200-115">Requirement</span></span> | <span data-ttu-id="33200-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33200-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33200-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33200-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33200-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33200-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="33200-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33200-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33200-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33200-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="33200-121">Header</span><span class="sxs-lookup"><span data-stu-id="33200-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33200-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="33200-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33200-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33200-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33200-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33200-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33200-125">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="33200-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="33200-126">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="33200-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="33200-127">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="33200-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




