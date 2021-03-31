---
description: Сравнивает две строки в Юникоде.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Функция Ртлкомпареуникодестринг (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895825"
---
# <a name="rtlcompareunicodestring-function"></a>Функция Ртлкомпареуникодестринг

Сравнивает две строки в Юникоде.

## <a name="syntax"></a>Синтаксис


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Строка1* \[ окне\]
</dt> <dd>

Указатель на первую строку.

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

Значение со знаком, которое дает результаты сравнения:



| Код возврата                                                                               | Описание                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Ноль**</dt> </dl>       | *Строка1* равна *строка2*.<br/>          |
| <dl> <dt>**< ноль**</dt> </dl>  | *Строка1* меньше, чем *строка2*.<br/>    |
| <dl> <dt>**> ноль**</dt> </dl> | *Строка1* больше, чем *строка2*.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                    |
| Целевая платформа<br/>          | <dl> <dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>WDM. h (включает WDM. h, Нтддк. h или Нтифс. h)</dt> </dl>                   |
| Библиотека<br/>                  | <dl> <dt>NTDLL. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ртлкомпарестринг**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**ртлекуалстринг**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
