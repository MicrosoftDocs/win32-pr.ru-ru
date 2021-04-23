---
description: Задает текущие характеристики источника мультимедиа.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Атрибут MF_EVENT_SOURCE_CHARACTERISTICS (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656544"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="ed111-103">\_ \_ Атрибут характеристик источника события MF \_</span><span class="sxs-lookup"><span data-stu-id="ed111-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="ed111-104">Задает текущие характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed111-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed111-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ed111-105">Data type</span></span>

<span data-ttu-id="ed111-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ed111-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ed111-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed111-107">Remarks</span></span>

<span data-ttu-id="ed111-108">Значение этого атрибута является побитовым оператором **or** для флагов [**перечисления \_ мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="ed111-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="ed111-109">Этот атрибут используется с событием [месаурцечарактеристиксчанжед](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="ed111-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="ed111-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ed111-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed111-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ed111-111">Requirements</span></span>



| <span data-ttu-id="ed111-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ed111-112">Requirement</span></span> | <span data-ttu-id="ed111-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ed111-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed111-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed111-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ed111-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed111-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ed111-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed111-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ed111-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed111-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed111-118">Header</span><span class="sxs-lookup"><span data-stu-id="ed111-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed111-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed111-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed111-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed111-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed111-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed111-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed111-122">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="ed111-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed111-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ed111-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ed111-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ed111-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




