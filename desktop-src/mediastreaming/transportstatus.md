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
ms.openlocfilehash: e96b7d3892d0344b166665426c66313da370aed1abbdb80c17037ea6aeb44e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473000"
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
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (ссылка Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





