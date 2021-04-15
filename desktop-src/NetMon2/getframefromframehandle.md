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
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662188"
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

## <a name="remarks"></a>Комментарии

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



 

 




