---
description: Не рекомендуется. Определяет, является ли указанный год високосным годом в заданной эре для конкретного календаря.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Функция Искалендарлеапеар
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: fe89f11bbaf41235449e882626680cf4d4af075d93f76c2d2aacd90d8d38707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948738"
---
# <a name="iscalendarleapyear-function"></a>Функция Искалендарлеапеар

Не рекомендуется. Определяет, является ли указанный год високосным годом в заданной эре для конкретного календаря.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Калид* \[ окне\]
</dt> <dd>

[Идентификатор календаря](calendar-identifiers.md) , используемый для проверки високосного года.

</dd> <dt>

*year (год* \[ ) окне\]
</dt> <dd>

Год для проверки.

</dd> <dt>

*эра* \[ окне\]
</dt> <dd>

Эпоха для проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если указанный год является високосным годом, или **false** в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного файла заголовка или файла библиотеки. Приложение может вызвать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Kernel32.dll) для получения маркера модуля. Затем он может вызвать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и именем этой функции, чтобы получить адрес функции.

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
</dt> </dl>

 

 
