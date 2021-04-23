---
description: Указывает, пуста ли текущая топология сегмента.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Атрибут MF_EVENT_SOURCE_FAKE_START (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913736"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="aec1b-103">\_Источник события \_ MF \_ поддельный \_ атрибут запуска</span><span class="sxs-lookup"><span data-stu-id="aec1b-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="aec1b-104">Указывает, пуста ли текущая топология сегмента.</span><span class="sxs-lookup"><span data-stu-id="aec1b-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="aec1b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aec1b-105">Data type</span></span>

<span data-ttu-id="aec1b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="aec1b-106">**UINT32**</span></span>

<span data-ttu-id="aec1b-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="aec1b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec1b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aec1b-108">Remarks</span></span>

<span data-ttu-id="aec1b-109">Этот атрибут используется с событием [месаурцестартед](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="aec1b-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="aec1b-110">Источник Sequencer задает для этого атрибута **значение true** , если текущая топология сегмента пуста.</span><span class="sxs-lookup"><span data-stu-id="aec1b-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="aec1b-111">Если этот атрибут имеет **значение true**, воспроизведение еще не началось.</span><span class="sxs-lookup"><span data-stu-id="aec1b-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="aec1b-112">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="aec1b-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="aec1b-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="aec1b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec1b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aec1b-114">Requirements</span></span>



| <span data-ttu-id="aec1b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aec1b-115">Requirement</span></span> | <span data-ttu-id="aec1b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aec1b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aec1b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aec1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aec1b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aec1b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aec1b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aec1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aec1b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aec1b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aec1b-121">Header</span><span class="sxs-lookup"><span data-stu-id="aec1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aec1b-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec1b-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec1b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aec1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec1b-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aec1b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aec1b-125">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="aec1b-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="aec1b-126">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="aec1b-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="aec1b-127">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aec1b-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




