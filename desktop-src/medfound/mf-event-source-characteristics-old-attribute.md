---
description: Задает предыдущие характеристики источника мультимедиа.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Атрибут MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656578"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="dbf7d-103">\_ \_ \_ Старый атрибут характеристик для источника события MF \_</span><span class="sxs-lookup"><span data-stu-id="dbf7d-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="dbf7d-104">Задает предыдущие характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dbf7d-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="dbf7d-105">Данные атрибута являются **побитовыми флагами из перечисления** [**\_ характеристик мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="dbf7d-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="dbf7d-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dbf7d-106">Data type</span></span>

<span data-ttu-id="dbf7d-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbf7d-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf7d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf7d-108">Remarks</span></span>

<span data-ttu-id="dbf7d-109">Этот атрибут используется с событием [месаурцечарактеристиксчанжед](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf7d-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="dbf7d-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="dbf7d-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf7d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf7d-111">Requirements</span></span>



| <span data-ttu-id="dbf7d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf7d-112">Requirement</span></span> | <span data-ttu-id="dbf7d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf7d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf7d-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbf7d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf7d-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbf7d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dbf7d-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbf7d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf7d-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbf7d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dbf7d-118">Header</span><span class="sxs-lookup"><span data-stu-id="dbf7d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf7d-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf7d-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf7d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf7d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf7d-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbf7d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbf7d-122">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="dbf7d-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbf7d-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbf7d-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dbf7d-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dbf7d-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dbf7d-125">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="dbf7d-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




