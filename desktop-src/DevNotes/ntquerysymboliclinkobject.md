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
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648062"
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

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**нтопенсимболиклинкобжект**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
