---
description: Извлекает именованное логическое значение из большого двоичного объекта.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Функция Жетбулфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673190"
---
# <a name="getboolfromblob-function"></a>Функция Жетбулфромблоб

Функция **жетбулфромблоб** Извлекает именованное логическое значение из большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Маркер для большого двоичного объекта.

</dd> <dt>

*повнернаме* \[ окне\]
</dt> <dd>

Указатель на имя владельца большого двоичного объекта.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Указатель на имя категории BLOB-объектов.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

Указатель на имя тега большого двоичного объекта.

</dd> <dt>

*пбул* \[ заполняет\]
</dt> <dd>

Указатель на логическое значение большого двоичного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[сетбулинблоб](setboolinblob.md)
</dt> <dt>

[жетклассидфромблоб](getclassidfromblob.md)
</dt> <dt>

[жетдвордфромблоб](getdwordfromblob.md)
</dt> <dt>

[жетмакаддрессфромблоб](getmacaddressfromblob.md)
</dt> <dt>

[жетнетворкинфофромблоб](getnetworkinfofromblob.md)
</dt> <dt>

[жетнппаддрессфилтерфромблоб](getnppaddressfilterfromblob.md)
</dt> <dt>

[жетнпппаттернфилтерфромблоб](getnpppatternfilterfromblob.md)
</dt> <dt>

[жетнпптригжерфромблоб](getnpptriggerfromblob.md)
</dt> <dt>

[жетстрингфромблоб](getstringfromblob.md)
</dt> <dt>

[жетстрингсфромблоб](getstringsfromblob.md)
</dt> </dl>

 

 




