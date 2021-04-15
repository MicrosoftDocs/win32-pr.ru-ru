---
description: Возвращает строку, расположенную в заданной позиции в большом двоичном объекте.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Функция Жетстрингфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496995"
---
# <a name="getstringfromblob-function"></a>Функция Жетстрингфромблоб

Функция **жетстрингфромблоб** возвращает строку, расположенную в заданной позиции в большом двоичном объекте.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
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

Раздел **владельца** большого двоичного объекта, где находится строка.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Раздел **категории** BLOB-объектов, в котором находится строка.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

**Тег** запрошенной строки.

</dd> <dt>

*ппстринг* \[ заполняет\]
</dt> <dd>

Указатель на переменную, указывающую на возвращаемую строку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

Если указанный **владелец**, **Категория** или данные **тега** не существуют, функция возвращает **\_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**.

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

[сетстрингинблоб](setstringinblob.md)
</dt> <dt>

[жетбулфромблоб](getboolfromblob.md)
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

[жетстрингсфромблоб](getstringsfromblob.md)
</dt> </dl>

 

 




