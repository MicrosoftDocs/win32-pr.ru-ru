---
description: Извлекает целевой объект символьной ссылки.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Функция Нткуерисимболиклинкобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 805f3de5da380c4749e58dd7467f1f4ccb2471119ffed81b79695a98feb1b090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003634"
---
# <a name="ntquerysymboliclinkobject-function"></a>Функция Нткуерисимболиклинкобжект

\[Эта функция может быть изменена или недоступна в будущем.\]

Извлекает целевой объект символьной ссылки.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Линкхандле* \[ окне\]
</dt> <dd>

Маркер объекта символьной ссылки.

</dd> <dt>

*LinkTarget* \[ в, out\]
</dt> <dd>

Указатель на инициализированную строку Юникода, которая получает целевой объект символьной ссылки. Если вызов завершается неудачей, необходимо задать элементы **MaximumLength** и **buffer** .

</dd> <dt>

*Ретурнедленгс* \[ out, необязательно\]
</dt> <dd>

Указатель на переменную, которая получает длину строки Юникода, возвращаемую в параметре *LinkTarget* . Если функция возвращает **буфер состояния \_ \_ слишком \_ мал**, эта переменная получает требуемый размер буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает состояние **\_ Success** или Error.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**нтопенсимболиклинкобжект**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
