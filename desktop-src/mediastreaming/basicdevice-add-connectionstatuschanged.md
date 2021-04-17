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
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703569"
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



 

## <a name="remarks"></a>Комментарии

Чтобы отменить регистрацию обработчика событий, зарегистрированного этим методом, передайте значение *токена* методу [**Remove \_ коннектионстатусчанжед**](basicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**басикдевице**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

