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
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714079"
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
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





