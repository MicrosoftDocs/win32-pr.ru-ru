---
description: Извлекает сведения об указанном объекте каталога.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Функция Нткуеридиректорйобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648063"
---
# <a name="ntquerydirectoryobject-function"></a>Функция Нткуеридиректорйобжект

\[Эта функция может быть изменена или недоступна в будущем.\]

Извлекает сведения об указанном объекте каталога.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Директорихандле* \[ окне\]
</dt> <dd>

Маркер объекта каталога.

</dd> <dt>

*Буфер* \[ out, необязательно\]
</dt> <dd>

Указатель на буфер, который получает сведения о каталоге. Этот буфер получает одну или несколько **\_ \_ информационных структур каталога объектов** , последний из которых **равен null**, а затем строки, содержащие имена записей каталога. Дополнительные сведения см. в подразделе "Примечания".

</dd> <dt>

*Длина* \[ окне\]
</dt> <dd>

Размер предоставляемого пользователем выходного буфера в байтах.

</dd> <dt>

*Ретурнсинглинтри* \[ окне\]
</dt> <dd>

Указывает, должна ли функция возвращать только одну запись.

</dd> <dt>

*Рестартскан* \[ окне\]
</dt> <dd>

Указывает, следует ли перезапустить сканирование или продолжить перечисление, используя сведения, переданные в параметре *контекста* .

</dd> <dt>

*Контекст* \[ в, out\]
</dt> <dd>

Контекст перечисления.

</dd> <dt>

*Ретурнленгс* \[ out, необязательно\]
</dt> <dd>

Указатель на переменную, которая получает длину сведений о каталоге, возвращаемых в буфере вывода, в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает состояние **\_ Success** или Error.

## <a name="remarks"></a>Комментарии

Ниже приведено определение **\_ \_ информационной структуры каталога объектов** .

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**нтопендиректорйобжект**](ntopendirectoryobject.md)
</dt> </dl>

 

 
