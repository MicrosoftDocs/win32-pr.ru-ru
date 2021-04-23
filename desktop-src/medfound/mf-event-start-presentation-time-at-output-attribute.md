---
description: Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Атрибут MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910807"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="ec182-103">\_Событие MF \_ Начало \_ презентации \_ время показа \_ с \_ выходным атрибутом</span><span class="sxs-lookup"><span data-stu-id="ec182-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="ec182-104">Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.</span><span class="sxs-lookup"><span data-stu-id="ec182-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec182-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ec182-105">Data type</span></span>

<span data-ttu-id="ec182-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ec182-106">**UINT64**</span></span>

<span data-ttu-id="ec182-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="ec182-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec182-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec182-108">Remarks</span></span>

<span data-ttu-id="ec182-109">Если какие-либо объекты конвейера в предыдущей топологии буферизованных данных, это значение будет немного меньше значения атрибута [**\_ \_ \_ \_ смещения времени представления событий MF**](mf-event-presentation-time-offset-attribute.md) , так как приемники должны визуализировать буферизованные данные.</span><span class="sxs-lookup"><span data-stu-id="ec182-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="ec182-110">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="ec182-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="ec182-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ec182-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec182-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ec182-112">Requirements</span></span>



| <span data-ttu-id="ec182-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ec182-113">Requirement</span></span> | <span data-ttu-id="ec182-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ec182-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec182-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec182-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec182-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec182-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ec182-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec182-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec182-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec182-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ec182-119">Header</span><span class="sxs-lookup"><span data-stu-id="ec182-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec182-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec182-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec182-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec182-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec182-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec182-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec182-123">Атрибуты событий</span><span class="sxs-lookup"><span data-stu-id="ec182-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec182-124">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="ec182-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ec182-125">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ec182-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




