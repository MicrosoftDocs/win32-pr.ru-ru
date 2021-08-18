---
title: Перечисление Девицетипес
description: Описание типов устройств DLNA, поддерживаемых API потоковой передачи мультимедиа.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API потоковой передачи мультимедиа для перечисления Девицетипес
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969eb389a1216ec0e30f27a938ca4f5382397ac5489f87add87731b69824b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100658"
---
# <a name="devicetypes-enumeration"></a>Перечисление Девицетипес

Описание типов устройств DLNA, поддерживаемых API потоковой передачи мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**
</dt> <dd>

Неизвестный тип устройства.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**дигиталмедиарендерер**
</dt> <dd>

Модуль подготовки цифрового мультимедиа DLNA (ДМР). Значение эквивалентно типу устройства **urn: schemas-UPnP-org: Device: медиарендерер: 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**дигиталмедиасервер**
</dt> <dd>

Сервер цифрового мультимедиа DLNA (DMS). Значение эквивалентно типу устройства **urn: schemas-UPnP-org: Device: медиасервер: 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**дигиталмедиаплайер**
</dt> <dd>

Проигрыватель DLNA Digital Media Player

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (ссылка Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





