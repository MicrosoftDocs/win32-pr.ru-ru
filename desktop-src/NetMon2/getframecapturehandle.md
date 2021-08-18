---
description: Функция Жетфрамекаптурехандле возвращает маркер записи на основе данного кадра.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Функция Жетфрамекаптурехандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9e7bf14cd7eae73ac1e5c8e21f8036574628932032a1545f8ac1c653dbbf8adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910754"
---
# <a name="getframecapturehandle-function"></a>Функция Жетфрамекаптурехандле

Функция **жетфрамекаптурехандле** возвращает маркер записи на основе данного кадра.

## <a name="syntax"></a>Синтаксис


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
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

Если функция выполнена успешно, возвращаемое значение является маркером записи.

Если функция завершается неудачно, возвращается значение 0.

## <a name="remarks"></a>Remarks

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамекаптурехандле** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




