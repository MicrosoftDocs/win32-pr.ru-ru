---
title: Метод BasicDevice.add_ConnectionStatusChanged
description: Регистрирует обработчик событий для события Коннектионстатусчанжед. | Метод BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API потоковой передачи мультимедиа add_ConnectionStatusChanged метода
- API потоковой передачи add_ConnectionStatusChanged метода, интерфейс Басикдевице
- API потоковой передачи мультимедиа интерфейса Басикдевице, метод add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a416770a0ea3a4d317a2308fc9f5c9d940e89900aabbc7651ceb93b789454338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462264"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a>Басикдевице. Add \_ коннектионстатусчанжед, метод

Регистрирует обработчик событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обработчик событий* \[ окне\]
</dt> <dd>

Функция обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .

</dd> <dt>

*токен* \[ out, retval\]
</dt> <dd>

Ссылка на токен, который можно использовать для отмены регистрации обработчика событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Чтобы отменить регистрацию обработчика событий, зарегистрированного этим методом, передайте значение *токена* методу [**Remove \_ коннектионстатусчанжед**](basicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**басикдевице**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

