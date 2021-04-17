---
description: Функция Варленсмаллинттодворд преобразует однострочное целое число с переменной длиной в тип DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Функция Варленсмаллинттодворд (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673575"
---
# <a name="varlensmallinttodword-function"></a>Функция Варленсмаллинттодворд

Функция **варленсмаллинттодворд** преобразует однострочное целое число с переменной длиной в тип **DWORD**.

## <a name="syntax"></a>Синтаксис


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pValue* 
</dt> <dd>

Указатель на однострочное целое число с переменной длиной.

</dd> <dt>

*валуелен* 
</dt> <dd>

Длина (в байтах) переменной длины с малым числом.

</dd> <dt>

*фисбитесваппед* 
</dt> <dd>

Флаг, указывающий, является ли маленькое целое число переменной длины байтовым.

</dd> <dt>

*лпдворд* 
</dt> <dd>

Значение **типа DWORD** , в которое преобразуется целое число.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является указателем на **DWORD**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




