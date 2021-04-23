---
description: Описывает содержимое простейшего потока в транспортном потоке MPEG-2. Это перечисление используется в интерфейсе IMPEG2PIDMap, который реализуется на выходных контактах демультиплексора MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Перечисление MEDIA_SAMPLE_CONTENT (Бдатипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675117"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="c46a8-104">\_ \_ Перечисление примеров содержимого мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c46a8-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="c46a8-105">Описывает содержимое простейшего потока в транспортном потоке MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="c46a8-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="c46a8-106">Это перечисление используется в интерфейсе [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , который реализуется на выходных контактах [демультиплексора MPEG-2](mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="c46a8-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c46a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c46a8-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="c46a8-108">Константы</span><span class="sxs-lookup"><span data-stu-id="c46a8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c46a8-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_пакет транспорта \_ носителя**</span><span class="sxs-lookup"><span data-stu-id="c46a8-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="c46a8-110">Указывает полный пакет транспортного потока, который будет передан без обработки.</span><span class="sxs-lookup"><span data-stu-id="c46a8-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="c46a8-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_простейший \_ поток мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="c46a8-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="c46a8-112">Указывает полезные данные аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="c46a8-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="c46a8-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ psi**</span><span class="sxs-lookup"><span data-stu-id="c46a8-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="c46a8-114">Указывает поток данных PAT, ПЛТ, CAT или Private.</span><span class="sxs-lookup"><span data-stu-id="c46a8-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="c46a8-115">Это полные разделы PSI, которые не нужно собирать заново.</span><span class="sxs-lookup"><span data-stu-id="c46a8-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="c46a8-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_ \_ полезные данные транспорта носителей**</span><span class="sxs-lookup"><span data-stu-id="c46a8-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="c46a8-117">Указывает собранные полезные данные пакетов служб терминалов, такие как PES.</span><span class="sxs-lookup"><span data-stu-id="c46a8-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c46a8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c46a8-118">Requirements</span></span>



| <span data-ttu-id="c46a8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c46a8-119">Requirement</span></span> | <span data-ttu-id="c46a8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c46a8-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="c46a8-121">Header</span></span><br/> | <dl> <span data-ttu-id="c46a8-122"><dt>Бдатипес. h (включение Бдаифаце. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c46a8-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46a8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c46a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46a8-124">Перечислимые типы DirectShow</span><span class="sxs-lookup"><span data-stu-id="c46a8-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




