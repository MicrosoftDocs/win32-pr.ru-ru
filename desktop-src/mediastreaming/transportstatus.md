---
title: Перечисление Транспортстатус
description: Определяет доступное состояние транспорта, определенное правилами UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API потоковой передачи мультимедиа для перечисления Транспортстатус
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718131"
---
# <a name="transportstatus-enumeration"></a>Перечисление Транспортстатус

Определяет доступное состояние транспорта, определенное правилами UPnP.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**
</dt> <dd>

Ошибочное состояние устройства.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Хорошо**
</dt> <dd>

Устройство имеет хорошее состояние.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ерророккурред**
</dt> <dd>

На устройстве произошла ошибка.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Последняя**
</dt> <dd>

Предыдущее состояние устройства — текущее состояние транспорта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





