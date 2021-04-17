---
description: Функция Сетклассидинблоб задает значение идентификатора именованного класса для большого двоичного объекта.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Функция Сетклассидинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673543"
---
# <a name="setclassidinblob-function"></a>Функция Сетклассидинблоб

Функция **сетклассидинблоб** задает значение идентификатора именованного класса для большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
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

Указатель на заданное имя **владельца** большого двоичного объекта.

</dd> <dt>

*пкатегоринаме* \[ окне\]
</dt> <dd>

Указатель на заданное имя **категории** BLOB-объектов.

</dd> <dt>

*птагнаме* \[ окне\]
</dt> <dd>

Указатель на заданное имя **ТЕГА** BLOB-объекта.

</dd> <dt>

*пклсид* \[ окне\]
</dt> <dd>

Указатель на идентификатор класса заданного большого двоичного объекта.

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

[жетклассидфромблоб](getclassidfromblob.md)
</dt> <dt>

[сетбулинблоб](setboolinblob.md)
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

 

 




