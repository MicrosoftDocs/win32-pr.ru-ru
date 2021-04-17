---
title: Перечисление ConnectionStatus
description: Представляет состояние устройства в сети как Последнее появление.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API потоковой передачи мультимедиа для перечисления ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717919"
---
# <a name="connectionstatus-enumeration"></a>Перечисление ConnectionStatus

Представляет состояние устройства в сети как Последнее появление.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Онлайн**
</dt> <dd>

Устройство подключено и активно в сети.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Работа**
</dt> <dd>

устройство вне сети;

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Сна**
</dt> <dd>

Устройство находится в автономном режиме, но может автоматически выходить из системы при попытке взаимодействия с ним.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Reference Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





