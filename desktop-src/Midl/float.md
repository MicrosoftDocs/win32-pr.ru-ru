---
title: float, атрибут
description: Ключевое слово float обозначает 32-разрядное число с плавающей запятой.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- атрибут float с плавающей запятой
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 096bd5488335d59944b03815184735a4530b20310ddc7c21389e86fac1997eec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040093"
---
# <a name="float-attribute"></a>float, атрибут

Ключевое слово **float** обозначает 32-разрядное число с плавающей запятой.

``` syntax
float identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Remarks

Тип **float** является одним из базовых типов языка определения интерфейса (IDL). Тип **float** может отображаться в виде спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и описателя типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

Тип **float** не может использоваться в объявлениях [**const**](const.md) .

## <a name="see-also"></a>См. также

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**Дважды**](double.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 




