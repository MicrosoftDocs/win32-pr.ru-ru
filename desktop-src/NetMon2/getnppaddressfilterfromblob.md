---
description: Функция Жетнппаддрессфилтерфромблоб заполняет заданный фильтр адресов данными, хранящимися в большом двоичном объекте.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Функция Жетнппаддрессфилтерфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999397"
---
# <a name="getnppaddressfilterfromblob-function"></a>Функция Жетнппаддрессфилтерфромблоб

Функция **жетнппаддрессфилтерфромблоб** заполняет заданный фильтр адресов данными, хранящимися в большом двоичном объекте.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> <dt>

*паддресстабле* \[ в, out\]
</dt> <dd>

Указатель на выделенную пользователем таблицу адресов.

</dd> <dt>

*херрорблоб* \[ заполняет\]
</dt> <dd>

Обработайте с большим ДВОИЧным объектом ошибки, который указывает, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.

## <a name="remarks"></a>Комментарии

Сведения об адресе хранятся в разделе **config** категории **владельца** BLOB-объекта НПП.

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

[сетнппаддрессфилтеринблоб](setnppaddressfilterinblob.md)
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

[жетнпппаттернфилтерфромблоб](getnpppatternfilterfromblob.md)
</dt> <dt>

[жетнпптригжерфромблоб](getnpptriggerfromblob.md)
</dt> <dt>

[жетстрингфромблоб](getstringfromblob.md)
</dt> <dt>

[жетстрингсфромблоб](getstringsfromblob.md)
</dt> </dl>

 

 




