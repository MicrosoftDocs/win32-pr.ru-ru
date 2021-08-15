---
description: Задает фильтр соответствия шаблону большого двоичного объекта.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Функция Сетнпппаттернфилтеринблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a920d6ffc135855826719e31613119a27671e334d5a75ce7dba29c2b140816fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363755"
---
# <a name="setnpppatternfilterinblob-function"></a>Функция Сетнпппаттернфилтеринблоб

Функция **сетнпппаттернфилтеринблоб** задает фильтр соответствия ШАБЛОНУ большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Маркер для большого двоичного объекта.

</dd> <dt>

*пекспрессион* \[ окне\]
</dt> <dd>

Указатель на структуру [выражения](expression.md) , определяющую устанавливаемое выражение фильтра.

</dd> <dt>

*херрорблоб* \[ заполняет\]
</dt> <dd>

Маркер для большого двоичного объекта ошибки, указывающий, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция **сетнпппаттернфилтеринблоб** выполнена успешно, возвращается значение нмерр \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="remarks"></a>Remarks

Шаблон соответствует данным фильтра, хранящимся в категории **конфигурации** большого двоичного объекта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[жетнппаддрессфилтерфромблоб](getnppaddressfilterfromblob.md)
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

[сетнпптригжеринблоб](setnpptriggerinblob.md)
</dt> <dt>

[сетстрингинблоб](setstringinblob.md)
</dt> </dl>

 

 




