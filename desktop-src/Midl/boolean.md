---
title: логический атрибут
description: Ключевое слово Boolean указывает, что выражение или константное выражение, связанное с идентификатором, принимает только значения TRUE и FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- логический атрибут MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411865"
---
# <a name="boolean-attribute"></a>логический атрибут

Ключевое слово **Boolean** указывает, что выражение или константное выражение, связанное с идентификатором, принимает только значения **true** и **false**.

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Логический** тип является одним из базовых типов языка IDL. **Логический** тип может использоваться в качестве спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и в качестве описателя типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

> [!Note]  
> Базовый тип **Boolean** несовместим с атрибутом [**oleautomation**](oleautomation.md) . Используйте вариант \_ bool в интерфейсах, совместимых с автоматизацией.

 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 




