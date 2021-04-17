---
description: Не рекомендуется. Возвращает день недели, соответствующий указанному дню, и заполняет элемент DayOfWeek в указанной структуре КАЛДАТЕТИМЕ этим значением.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Функция Упдатекалендардайофвик
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684609"
---
# <a name="updatecalendardayofweek-function"></a>Функция Упдатекалендардайофвик

Не рекомендуется. Возвращает день недели, соответствующий указанному дню, и заполняет элемент **DayOfWeek** в указанной структуре [**калдатетиме**](caldatetime.md) этим значением.

## <a name="syntax"></a>Синтаксис


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпкалдатетиме* \[ в, out\]
</dt> <dd>

Указатель на структуру [**калдатетиме**](caldatetime.md) , содержащую дату, для которой необходимо задать день недели.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   \_Дата ошибки \_ за пределами \_ \_ диапазона. Указанная дата находится за пределами диапазона.
-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанного файла заголовка или файла библиотеки. Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля. Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и именем этой функции, чтобы получить адрес функции.

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

[**калдатетиме**](caldatetime.md)
</dt> </dl>

 

 
