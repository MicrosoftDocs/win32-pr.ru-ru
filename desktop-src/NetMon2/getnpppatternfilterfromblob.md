---
description: Функция Жетнпппаттернфилтерфромблоб извлекает фильтр соответствия шаблонов из определенного большого двоичного объекта.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Функция Жетнпппаттернфилтерфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808711"
---
# <a name="getnpppatternfilterfromblob-function"></a>Функция Жетнпппаттернфилтерфромблоб

Функция **жетнпппаттернфилтерфромблоб** извлекает фильтр соответствия шаблонов из определенного большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> <dt>

*пекспрессион* \[ окне\]
</dt> <dd>

Указатель на критерий фильтра.

</dd> <dt>

*херрорблоб* \[ заполняет\]
</dt> <dd>

Обработайте с большим ДВОИЧным объектом ошибки, который указывает, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="remarks"></a>Комментарии

Сведения о фильтре соответствия шаблону хранятся в категории **конфигурации** большого двоичного объекта.

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

[сетнпппаттернфилтеринблоб](setnpppatternfilterinblob.md)
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

[жетнпптригжерфромблоб](getnpptriggerfromblob.md)
</dt> <dt>

[жетстрингфромблоб](getstringfromblob.md)
</dt> <dt>

[жетстрингсфромблоб](getstringsfromblob.md)
</dt> </dl>

 

 




