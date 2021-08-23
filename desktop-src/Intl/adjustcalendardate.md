---
description: Не рекомендуется. Корректирует дату на указанное число лет, месяцев, недель или дней.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Функция Аджусткалендардате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520624"
---
# <a name="adjustcalendardate-function"></a>Функция Аджусткалендардате

Не рекомендуется. Корректирует дату на указанное число лет, месяцев, недель или дней.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпкалдатетиме* \[ в, out\]
</dt> <dd>

Указатель на структуру [**калдатетиме**](caldatetime.md) , которая содержит дату и сведения о календаре для корректировки.

</dd> <dt>

*калунит* \[ окне\]
</dt> <dd>

Значение перечисления [**калдатетиме \_ датеунит**](caldatetime-dateunit.md) , указывающее единицу даты, например дайунит.

</dd> <dt>

*Сумма* \[ заполняет\]
</dt> <dd>

Величина, на которую нужно скорректировать указанную дату.

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

[NLS: пример API-интерфейсов на основе имен](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
