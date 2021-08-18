---
description: Не рекомендуется. Преобразует указанную структуру SYSTEMTIME в структуру КАЛДАТЕТИМЕ.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Функция Конвертсистемтиметокалдатетиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746044"
---
# <a name="convertsystemtimetocaldatetime-function"></a>Функция Конвертсистемтиметокалдатетиме

Не рекомендуется. Преобразует указанную структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) в структуру [**калдатетиме**](caldatetime.md) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсистиме* \[ окне\]
</dt> <dd>

Указатель на структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) для преобразования.

</dd> <dt>

*Калид* \[ окне\]
</dt> <dd>

Идентификатор системного [календаря](calendar-identifiers.md) , используемый при преобразовании.

</dd> <dt>

*лпкалдатетиме* \[ заполняет\]
</dt> <dd>

Указатель на эквивалентную структуру [**калдатетиме**](caldatetime.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Remarks

Самая ранняя дата, поддерживаемая этой функцией, — 1 января 1601 г.

Эта функция не имеет связанного файла заголовка или файла библиотеки. Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля. Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка национальных языков](national-language-support.md)
</dt> <dt>

[Функции поддержки национальных языков](national-language-support-functions.md)
</dt> <dt>

[Получение сведений о времени и дате](time-and-date.md)
</dt> </dl>

 

 
