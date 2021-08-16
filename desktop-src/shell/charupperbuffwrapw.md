---
description: Преобразует символы нижнего регистра в буфере в символы верхнего регистра.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Функция Чаруппербуффврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861559"
---
# <a name="charupperbuffwrapw-function"></a>Функция Чаруппербуффврапв

\[**чаруппербуффврапв** доступен для использования в Windows XP. Она может быть недоступна в последующих версиях. На своем месте следует использовать [**чаруппербуффв**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .\]

Преобразует символы нижнего регистра в буфере в символы верхнего регистра. Функция преобразует символы на месте.

> [!Note]  
> **Чаруппербуффврапв** — это оболочка для функции **чаруппербуффв** . Дополнительные сведения об использовании см. на странице [**чаруппербуфф**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .

 

## <a name="syntax"></a>Синтаксис


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PCH* \[ окне\]
</dt> <dd>

Тип: **LPWSTR**

Указатель на буфер, содержащий один или несколько символов Юникода для обработки.

</dd> <dt>

*кчленгс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Задает размер (в символах) буфера, на который указывает *PCH*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **DWORD**

Число обработанных символов.

## <a name="remarks"></a>Remarks

Предпочтительным методом является использование [**чаруппербуффв**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Чаруппербуффврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 44.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**чаруппербуфф**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
