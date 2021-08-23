---
description: Не рекомендуется. Преобразует указанную структуру КАЛДАТЕТИМЕ в структуру SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: Функция Конверткалдатетиметосистемтиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: cb579eb80c421d6f206045889edfe3f1b64130f58d02d96c61b3867abcaabb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631934"
---
# <a name="convertcaldatetimetosystemtime-function"></a>Функция Конверткалдатетиметосистемтиме

Не рекомендуется. Преобразует указанную структуру [**калдатетиме**](caldatetime.md) в структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпкалдатетиме* \[ окне\]
</dt> <dd>

Указатель на структуру [**калдатетиме**](caldatetime.md) для преобразования.

</dd> <dt>

*лпсистиме* \[ заполняет\]
</dt> <dd>

Указатель на эквивалентную структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   \_Дата ошибки \_ за пределами \_ \_ диапазона. Указанная дата находится за пределами диапазона.
-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного файла заголовка или файла библиотеки. Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля. Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка национальных языков](national-language-support.md)
</dt> <dt>

[Функции поддержки национальных языков](national-language-support-functions.md)
</dt> <dt>

[Получение сведений о времени и дате](time-and-date.md)
</dt> </dl>

 

 
