---
title: атрибут wchar_t
description: '\_Ключевое слово WCHAR t обозначает тип расширенных символов.'
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t атрибута MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "104069660"
---
# <a name="wchar_t-attribute"></a>\_атрибут WCHAR t

Ключевое слово **WCHAR \_ t** обозначает тип расширенных символов.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Тип **WCHAR \_ t** определяется MIDL как [**неподписанный**](unsigned.md) [**короткий**](short.md) (16-разрядный) объект данных.

Компилятор MIDL допускает переопределение **WCHAR \_ t**, но только в том случае, если он согласуется с предыдущим определением.

Тип расширенных символов является одним из предопределенных типов MIDL. Тип расширенных символов может отображаться как описатель типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (как спецификатор типа возвращаемого значения функции и как спецификатор типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

**\[ Строковый \]** атрибут может быть применен к указателю или массиву типа **WCHAR \_ t**.

Используйте символ **L** перед символом или строковой константой, чтобы обозначить константу расширенного типа символа.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> <dt>

[**без знака**](unsigned.md)
</dt> </dl>

 

 




