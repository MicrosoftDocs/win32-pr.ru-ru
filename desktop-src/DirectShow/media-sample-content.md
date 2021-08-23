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
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684994"
---
# <a name="media_sample_content-enumeration"></a>\_ \_ Перечисление примеров содержимого мультимедиа

Описывает содержимое простейшего потока в транспортном потоке MPEG-2. Это перечисление используется в интерфейсе [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , который реализуется на выходных контактах [демультиплексора MPEG-2](mpeg-2-demultiplexer.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_пакет транспорта \_ носителя**
</dt> <dd>

Указывает полный пакет транспортного потока, который будет передан без обработки.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_простейший \_ поток мультимедиа**
</dt> <dd>

Указывает полезные данные аудио или видео.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ psi**
</dt> <dd>

Указывает поток данных PAT, ПЛТ, CAT или Private. Это полные разделы PSI, которые не нужно собирать заново.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_ \_ полезные данные транспорта носителей**
</dt> <dd>

Указывает собранные полезные данные пакетов служб терминалов, такие как PES.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Бдатипес. h (включение Бдаифаце. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Перечислимые типы](directshow-enumerated-types.md)
</dt> </dl>

 

 




