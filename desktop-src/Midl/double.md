---
title: Double, атрибут
description: Ключевое слово Double обозначает 64-разрядное число с плавающей запятой.
ms.assetid: a235e9c5-90b3-4fa4-9154-06511abcccd0
keywords:
- двойной атрибут MIDL
topic_type:
- apiref
api_name:
- double
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f14f4906de9e843c9413411c9d45ba927cc40ee4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532744"
---
# <a name="double-attribute"></a>Double, атрибут

Ключевое слово **Double** обозначает 64-разрядное число с плавающей запятой.

``` syntax
double identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Тип **Double** является одним из базовых типов языка определения интерфейса (IDL). Этот тип может использоваться в качестве спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в качестве спецификатора возвращаемого типа функции и описателя типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

Тип **Double** не может использоваться в объявлениях [**const**](const.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**сделать**](float.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 




