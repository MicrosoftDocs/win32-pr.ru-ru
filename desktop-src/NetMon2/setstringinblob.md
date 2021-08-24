---
description: Задает строку в указанном месте в большом двоичном объекте.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Функция Сетстрингинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363683"
---
# <a name="setstringinblob-function"></a>Функция Сетстрингинблоб

Функция **сетстрингинблоб** задает строку в заданном месте в большом двоичном объекте.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
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

Указатель на раздел **owner** большого двоичного объекта, где задана строка.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Указатель на раздел **категории** большого двоичного объекта, где задана строка.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

Указатель на **тег** запрошенной строки.

</dd> <dt>

*пстринг* \[ окне\]
</dt> <dd>

Указатель на переменную, в которой будет возвращен указатель на строку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на проблему.

Если указанные сведения о **владельце**, **категории** или **теге** не существуют, возвращаемое значение является \_ записью большого двоичного объекта нмерр \_ \_ \_ \_ .

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

[жетстрингфромблоб](getstringfromblob.md)
</dt> <dt>

[сетбулинблоб](setboolinblob.md)
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
</dt> </dl>

 

 




