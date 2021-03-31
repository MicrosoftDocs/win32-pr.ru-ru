---
description: Функция Бержетинтежер декодирует целое число ЛИЧЕСТВО в кодировке.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Функция Бержетинтежер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911644"
---
# <a name="bergetinteger-function"></a>Функция Бержетинтежер

Функция **бержетинтежер** декодирует целое число личество в кодировке.

## <a name="syntax"></a>Синтаксис


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррентпоинтер* 
</dt> <dd>

Указатель на декодированное целое число.

</dd> <dt>

*ппвалуепоинтер* 
</dt> <dd>

Указатель на возвращаемое значение указателя.

</dd> <dt>

*феадерленгс* 
</dt> <dd>

Указатель на возвращаемую длину заголовка.

</dd> <dt>

*пдаталенгс* 
</dt> <dd>

Указатель на длину данных.

</dd> <dt>

*ппнекст* 
</dt> <dd>

Указатель на указатель на следующую запись ЛИЧЕСТВО.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно (то есть при обнаружении и преобразовании допустимого целого числа в кодировке ЛИЧЕСТВО), возвращается значение **true**.

Если функция завершилась неудачно, возвращается значение **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




