---
description: Добавляет альтернативное имя локальной сети для компьютера, с которого он вызывается.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Функция Аддлокалалтернатекомпутернаме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 90945188209abdcaf16a7250e43db2af9a99ab4a3fbb55b8baabf0ea610c99e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668686"
---
# <a name="addlocalalternatecomputername-function"></a>Функция Аддлокалалтернатекомпутернаме

Добавляет альтернативное имя локальной сети для компьютера, с которого он вызывается.

## <a name="syntax"></a>Синтаксис


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпднсфкхостнаме* \[ окне\]
</dt> <dd>

Добавляемое альтернативное имя. Имя должно быть в формате **компутернамеднсфулликуалифиед** , как определено в перечислении [**\_ \_ форматов имен компьютеров**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , а функция [**днсвалидатенаме \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) должна иметь возможность проверить ее, указав для ее формата значение **днснамехостнамефулл**.

</dd> <dt>

*улфлагс* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован и должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает **ошибку \_ Success**. Если функция завершается ошибкой, она возвращает ненулевой код ошибки. К возвращенным им кодам ошибок относятся следующие:



| Код возврата                                                                                               | Описание                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ошибка \_ недопустимого \_ параметра**</dt> </dl>  | Указывает, что параметр *лпднсфкхостнаме* не указывает на допустимое DNS-имя или что параметр *улфлагс* не равен нулю.<br/> |
| <dl> <dt>**Ошибка \_ не \_ хватает \_ памяти**</dt> </dl> | Недостаточно памяти для выполнения запроса.<br/>                                                                                    |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Библиотека<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Имя в кодировке Юникод и ANSI<br/> | **Аддлокалалтернатекомпутернамев** (Юникод) и **аддлокалалтернатекомпутернамеа** (ANSI)<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Формат имени \_ компьютера**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**Днсвалидатенаме \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
