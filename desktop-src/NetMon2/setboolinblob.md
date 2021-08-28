---
description: Функция Сетбулинблоб задает логическое значение в указанном месте в большом двоичном объекте.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Функция Сетбулинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 95785714919ad99026c8e179c11f992a79efc4d99d0de4caab20fd00f63cbffc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128824"
---
# <a name="setboolinblob-function"></a>Функция Сетбулинблоб

Функция **сетбулинблоб** задает логическое значение в указанном месте в большом двоичном объекте.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> <dt>

*повнернаме* \[ окне\]
</dt> <dd>

Указатель на имя **владельца** большого двоичного объекта.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Указатель на имя **категории** BLOB-объектов.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

Указатель на имя **тега** большого двоичного объекта.

</dd> <dt>

*Bool (логическое* \[ ) окне\]
</dt> <dd>

Логическое значение, заданное в заданном месте.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[жетбулфромблоб](getboolfromblob.md)
</dt> <dt>

[сетклассидинблоб](setclassidinblob.md)
</dt> <dt>

[сетдвординблоб](setdwordinblob.md)
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

 

 




