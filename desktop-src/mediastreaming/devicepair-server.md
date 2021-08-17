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
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100728"
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
| Заголовок<br/> | <dl> <dt>Асптлб. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**девицепаир**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

