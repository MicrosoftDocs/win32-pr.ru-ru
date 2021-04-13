---
description: Сравнивает две строки в Юникоде, чтобы определить, является ли одна строка префиксом другой.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Функция Ртлпрефиксуникодестринг (Нтддк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496104"
---
# <a name="rtlprefixunicodestring-function"></a>Функция Ртлпрефиксуникодестринг

Сравнивает две строки в Юникоде, чтобы определить, является ли одна строка префиксом другой.

## <a name="syntax"></a>Синтаксис


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Строка1* \[ окне\]
</dt> <dd>

Указатель на первую строку, которая может быть префиксом буферизованной строки Юникода в строке *строка2*.

</dd> <dt>

*Строка2* \[ окне\]
</dt> <dd>

Указатель на вторую строку.

</dd> <dt>

*Без* \[ окне\]
</dt> <dd>

Если **значение — true**, при выполнении сравнения регистр следует игнорировать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если *строка1* является префиксом *строка_замены*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                    |
| Целевая платформа<br/>          | <dl> <dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Нтддк. h (включение Нтддк. h)</dt> </dl>                                    |
| Библиотека<br/>                  | <dl> <dt>NTDLL. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ртлкомпареуникодестринг**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




