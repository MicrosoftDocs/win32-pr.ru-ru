---
description: Определяет, соответствует ли строка Юникода указанному шаблону.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Функция Ртлиснамеинекспрессион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662081"
---
# <a name="rtlisnameinexpression-function"></a>Функция Ртлиснамеинекспрессион

Определяет, соответствует ли строка Юникода указанному шаблону.

## <a name="syntax"></a>Синтаксис


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Выражение* \[ окне\]
</dt> <dd>

Указатель на строку шаблона. Эта строка может содержать подстановочные знаки. Если параметр *ignoreCase* имеет значение true, строка должна содержать только символы верхнего регистра.

</dd> <dt>

*Имя* \[ окне\]
</dt> <dd>

Указатель на строку, сравниваемую с шаблоном. Эта строка не может содержать подстановочные знаки.

</dd> <dt>

*IgnoreCase* \[ окне\]
</dt> <dd>

**Значение true** для сопоставления без учета регистра или **false** для сопоставления с учетом регистра.

</dd> <dt>

*Упкасетабле* \[ в необязательное\]
</dt> <dd>

Необязательный указатель на таблицу символов в верхнем регистре, используемую для сопоставления без учета регистра. Если этот параметр имеет значение NULL, используется таблица символов верхнего регистра системы по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если строка соответствует шаблону. Если строка не соответствует шаблону, эта функция возвращает **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанного файла заголовка. Связанная библиотека импорта, NTDLL. lib, доступна в наборе драйверов Microsoft Windows (WDK). Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                           |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
