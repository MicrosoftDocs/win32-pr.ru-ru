---
title: Метод add_ConnectionStatusChanged Ибасикдевице
description: Регистрирует обработчик событий для события Коннектионстатусчанжед. | Метод add_ConnectionStatusChanged Ибасикдевице
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API потоковой передачи мультимедиа add_ConnectionStatusChanged метода
- API потоковой передачи add_ConnectionStatusChanged метода, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e90ea1f90ccd5b1e141b0e4071213abfe6f4a05a85d3c0d4ced505e1b0f164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952664"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>Метод Ибасикдевице:: Add \_ коннектионстатусчанжед

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

Чтобы отменить регистрацию обработчика событий, зарегистрированного этим методом, передайте значение *токена* методу [**Remove \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) .

## <a name="see-also"></a>См. также

<dl> <dt>

[**ибасикдевице**](ibasicdevice.md)
</dt> </dl>

 

