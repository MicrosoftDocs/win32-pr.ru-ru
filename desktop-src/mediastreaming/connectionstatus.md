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
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721254"
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
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (ссылка Windows. Media. Streaming. IDL)</dt> </dl> |



 

 





