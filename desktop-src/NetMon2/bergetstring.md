---
description: Функция Бержетстринг декодирует строку в кодировке ЛИЧЕСТВО.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Функция Бержетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909423"
---
# <a name="bergetstring-function"></a>Функция Бержетстринг

Функция **бержетстринг** декодирует строку в кодировке личество.

## <a name="syntax"></a>Синтаксис


```C++
BOOL BERGetString(
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

Указатель на декодированную строку.

</dd> <dt>

*ппвалуепоинтер* 
</dt> <dd>

Указатель на указатель декодированной строки.

</dd> <dt>

*феадерленгс* 
</dt> <dd>

Указатель на возвращаемую длину заголовка.

</dd> <dt>

*пдаталенгс* 
</dt> <dd>

Указатель на длину строки.

</dd> <dt>

*ппнекст* 
</dt> <dd>

Указатель на указатель следующей записи ЛИЧЕСТВО.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно (то есть при декодировании допустимой строки с ЛИЧЕСТВО кодировкой), возвращается значение **true**.

Если функция завершилась неудачно, возвращается значение **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




