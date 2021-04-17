---
description: Функция Бержесеадер декодирует заголовок Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Функция Бержесеадер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673645"
---
# <a name="bergetheader-function"></a>Функция Бержесеадер

Функция **бержесеадер** декодирует заголовок Choice.

## <a name="syntax"></a>Синтаксис


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррентпоинтер* 
</dt> <dd>

Указатель на заголовок Choice.

</dd> <dt>

*птаг* 
</dt> <dd>

Указатель на возвращаемый тег.

</dd> <dt>

*феадерленгс* 
</dt> <dd>

Указатель на возвращаемую длину заголовка.

</dd> <dt>

*пдаталенгс* 
</dt> <dd>

Указатель на возвращаемую длину данных.

</dd> <dt>

*ппнекст* 
</dt> <dd>

Указатель на содержимое заголовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно (то есть найден допустимый заголовок выбора ЛИЧЕСТВО), возвращается значение **true**.

Если функция завершается неудачно, возвращается значение **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




