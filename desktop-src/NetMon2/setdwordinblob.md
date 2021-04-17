---
description: Функция Сетдвординблоб задает именованное значение DWORD большого двоичного объекта.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Функция Сетдвординблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673544"
---
# <a name="setdwordinblob-function"></a>Функция Сетдвординблоб

Функция **сетдвординблоб** задает именованное значение **DWORD** большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обрабатываемый набор больших двоичных объектов.

</dd> <dt>

*повнернаме* \[ окне\]
</dt> <dd>

Указатель на устанавливаемое имя **владельца** большого двоичного объекта.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Указатель на устанавливаемое имя **категории** BLOB-объектов.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

Указатель на заданный имя **тега** большого двоичного объекта.

</dd> <dt>

*Параметр DWORD* \[ окне\]
</dt> <dd>

Значение **DWORD** УСТАНАВЛИВАЕМОГО большого двоичного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

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

[жетдвордфромблоб](getdwordfromblob.md)
</dt> <dt>

[сетбулинблоб](setboolinblob.md)
</dt> <dt>

[сетклассидинблоб](setclassidinblob.md)
</dt> <dt>

[сетмакаддрессинблоб](setmacaddressinblob.md)
</dt> <dt>

[сетнетворкинфоинблоб](setnetworkinfoinblob.md)
</dt> <dt>

[сетнппаддрессфилтеринблоб](setnppaddressfilterinblob.md)
</dt> <dt>

[сетнпппаттернфилтеринблоб](setnpppatternfilterinblob.md)
</dt> <dt>

[сетнпптригжеринблоб](setnpptriggerinblob.md)
</dt> <dt>

[сетстрингинблоб](setstringinblob.md)
</dt> </dl>

 

 




