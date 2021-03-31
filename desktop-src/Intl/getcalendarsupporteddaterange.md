---
description: Не рекомендуется. Возвращает поддерживаемый диапазон дат для указанного календаря.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Функция Жеткалендарсуппортеддатеранже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998925"
---
# <a name="getcalendarsupporteddaterange-function"></a>Функция Жеткалендарсуппортеддатеранже

Не рекомендуется. Возвращает поддерживаемый диапазон дат для указанного календаря.

## <a name="syntax"></a>Синтаксис


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Календарь* \[ окне\]
</dt> <dd>

[Идентификатор календаря](calendar-identifiers.md) , для которого требуется получить поддерживаемый диапазон дат.

</dd> <dt>

*лпкалминдатетиме* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**калдатетиме**](caldatetime.md) , определяющую минимальную поддерживаемую дату.

</dd> <dt>

*лпкалмаксдатетиме* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**калдатетиме**](caldatetime.md) , определяющую максимальную поддерживаемую дату.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Комментарии

Самая ранняя дата, поддерживаемая этой функцией, — 1 января 1601 г.

Эта функция не имеет связанного файла заголовка или файла библиотеки. Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля. Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля и имя этой функции, чтобы получить адрес функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка национальных языков](national-language-support.md)
</dt> <dt>

[Функции поддержки национальных языков](national-language-support-functions.md)
</dt> <dt>

[NLS: пример API-интерфейсов на основе имен](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
