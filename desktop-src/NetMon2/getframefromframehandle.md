---
description: Функция Жетфрамефромфрамехандле возвращает указатель на кадр из маркера кадра.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Функция Жетфрамефромфрамехандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 56ee96fd04d4860648dac2ec6b20a537ba420beb070c8f9b7248d9e3b4acd184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366548"
---
# <a name="getframefromframehandle-function"></a>Функция Жетфрамефромфрамехандле

Функция **жетфрамефромфрамехандле** возвращает указатель на кадр из маркера кадра.

## <a name="syntax"></a>Синтаксис


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на кадр.

Если функция завершается неудачно, возвращается значение 0.

## <a name="remarks"></a>Remarks

Функция **жетфрамефромфрамехандле** извлекает данные, которые не могут быть извлечены другими вспомогательными функциями, предоставляемыми сетевой монитор. При возможности используйте следующие функции.

<dl>

[**жетфрамедстаддрессоффсет**](getframedstaddressoffset.md)  
[**жетфрамесркаддрессоффсет**](getframesrcaddressoffset.md)  
[**жетфрамекаптурехандле**](getframecapturehandle.md)  
[**жетфрамедестаддресс**](getframedestaddress.md)  
[**жетфрамесаурцеаддресс**](getframesourceaddress.md)  
[**жетфрамемачеадерленгс**](getframemacheaderlength.md)  
[**жетфрамеленгс**](getframelength.md)  
[**жетфраместоредленгс**](getframestoredlength.md)  
[**жетфрамемактипе**](getframemactype.md)  
[**жетфраменумбер**](getframenumber.md)  
[**жетфраметиместамп**](getframetimestamp.md)  
</dl>

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамефромфрамехандле** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




