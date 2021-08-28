---
title: Перечисление Транспортстате
description: Определяет доступные состояния транспорта, определенные правилами UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API потоковой передачи мультимедиа для перечисления Транспортстате
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a21fc8d0f2799cfba734d605d0c4d2835744ddeb130327ea39a22090d13464f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663095"
---
# <a name="transportstate-enumeration"></a>Перечисление Транспортстате

Определяет доступные состояния транспорта, определенные правилами UPnP.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**
</dt> <dd>

Ошибочное состояние устройства.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлена**
</dt> <dd>

Транспорт устройства находится в остановленном состоянии.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Игре**
</dt> <dd>

Транспорт устройства находится в воспроизводимом состоянии.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход**
</dt> <dd>

Транспорт устройства находится в состоянии перехода, что приведет к другому значению состояния.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлена**
</dt> <dd>

Транспортное устройство s находится в приостановленном состоянии.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Запись**
</dt> <dd>

Транспорт устройства находится в состоянии записи.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**номедиапресент**
</dt> <dd>

Для транспорта устройства не задан универсальный код ресурса (URI) для воспроизведения.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Последняя**
</dt> <dd>

Предыдущее состояние устройства в текущее состояние транспорта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (ссылка Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





