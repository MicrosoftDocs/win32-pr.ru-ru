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
ms.openlocfilehash: d6dfd50856202e78177d2ad259b16638f466d9bca236a691c65802ce2758c948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012320"
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



 

 




