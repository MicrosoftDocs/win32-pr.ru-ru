---
title: Функция Str_GetPtr
description: Копирует строку из одного буфера в другой.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtrные элементы управления Windows функции
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77c76ad276f6cb6dfc12bc272fbbc86c83617a0d00d36d77cf2ab0ca113811d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919454"
---
# <a name="str_getptr-function"></a>Str \_ жетптр, функция

\[эта функция доступна в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows.\]

Копирует строку из одного буфера в другой.

## <a name="syntax"></a>Синтаксис


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзсаурце* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Указатель на исходную строку.

</dd> <dt>

*псздест* \[ в, out\]
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Указатель на целевой буфер. Это значение может быть **равно NULL**.

</dd> <dt>

*кчдест* \[ окне\]
</dt> <dd>

Тип: **int**

Размер *псздест* в символах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Если *псздест* имеет **значение NULL** или *кчдест* равен нулю, возвращает размер буфера (в символах), который должен содержать завершающуюся нулем копию строки, на которую указывает *псзсаурце*.

Если *псздест* имеет значение, отличное от **null**, возвращает число успешно скопированных символов, включая завершающий нуль-символ.

Если *псздест* не может вместить всю строку, на которую указывает *псзсаурце*, то символы (*кчдест*-1) копируются, строка, заканчивающаяся нулем, и *кчдест* возвращается.

## <a name="remarks"></a>Remarks

**Str \_ Жетптр** доступен в виде версий ANSI (**str \_ Жетптра**) и Unicode (**str \_ жетптрв**). Эти функции не экспортируются по имени или объявляются в общедоступном файле заголовка. Чтобы использовать их, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 233 (**str \_ жетптра**) или 235 (**str \_ жетптрв**) из ComCtl32.dll, чтобы получить указатель на функцию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Str \_ Жетптрв** (Юникод) и **str \_ жетптра** (ANSI)<br/>                       |



 

