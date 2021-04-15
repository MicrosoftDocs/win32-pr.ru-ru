---
title: Свойство сервера Девицепаир (Асптлб. h)
description: Возвращает сервер для пары "активный базовый устройство".
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API потоковой передачи свойства сервера
- API потоковой передачи свойства сервера, интерфейс Девицепаир
- API потоковой передачи мультимедиа интерфейса Девицепаир, свойство сервера
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714080"
---
# <a name="devicepairserver-property"></a>Свойство Девицепаир:: Server

Возвращает сервер для пары "активный базовый устройство".

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Значение свойства

Получает объект [**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) , представляющий серверное устройство.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Асптлб. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**девицепаир**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

