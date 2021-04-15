---
description: Для трассировки событий в DirectShow используются следующие идентификаторы GUID.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: Идентификаторы GUID трассировки (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669103"
---
# <a name="trace-guids"></a><span data-ttu-id="70385-103">Идентификаторы GUID трассировки</span><span class="sxs-lookup"><span data-stu-id="70385-103">Trace GUIDs</span></span>

<span data-ttu-id="70385-104">Для трассировки событий в DirectShow используются следующие идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="70385-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="70385-105">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="70385-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="70385-106">Описание</span><span class="sxs-lookup"><span data-stu-id="70385-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="70385-107"><dt>**GUID \_ аудиобреак**</dt></span><span class="sxs-lookup"><span data-stu-id="70385-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="70385-108">Событие разрыва звука.</span><span class="sxs-lookup"><span data-stu-id="70385-108">Audio break event.</span></span> <span data-ttu-id="70385-109">События этого типа используют структуру [**перфинфо \_ DSHOW \_ аудиобреак**](perfinfo-dshow-audiobreak.md) для данных событий.</span><span class="sxs-lookup"><span data-stu-id="70385-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="70385-110"><dt>**CTL с GUID \_ DSHOW \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70385-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="70385-111">Поставщик событий DirectShow.</span><span class="sxs-lookup"><span data-stu-id="70385-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="70385-112"><dt>**GUID \_ стреамтраце**</dt></span><span class="sxs-lookup"><span data-stu-id="70385-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="70385-113">Общее событие потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="70385-113">General streaming event.</span></span> <span data-ttu-id="70385-114">События этого типа используют структуру [**перфинфо \_ DSHOW \_ стреамтраце**](perfinfo-dshow-streamtrace.md) для данных событий.</span><span class="sxs-lookup"><span data-stu-id="70385-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="70385-115"><dt>**GUID \_ видеоренд**</dt></span><span class="sxs-lookup"><span data-stu-id="70385-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="70385-116">Событие отрисовки видео.</span><span class="sxs-lookup"><span data-stu-id="70385-116">Video rendering event.</span></span> <span data-ttu-id="70385-117">События этого типа используют структуру [**перфинфо \_ DSHOW \_ авренд**](perfinfo-dshow-avrend.md) для данных событий.</span><span class="sxs-lookup"><span data-stu-id="70385-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="70385-118">Требования</span><span class="sxs-lookup"><span data-stu-id="70385-118">Requirements</span></span>



| <span data-ttu-id="70385-119">Требование</span><span class="sxs-lookup"><span data-stu-id="70385-119">Requirement</span></span> | <span data-ttu-id="70385-120">Значение</span><span class="sxs-lookup"><span data-stu-id="70385-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70385-121">Header</span><span class="sxs-lookup"><span data-stu-id="70385-121">Header</span></span><br/> | <dl> <span data-ttu-id="70385-122"><dt>Перфструкт. h</dt></span><span class="sxs-lookup"><span data-stu-id="70385-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70385-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70385-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70385-124">Трассировка событий в DirectShow</span><span class="sxs-lookup"><span data-stu-id="70385-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




