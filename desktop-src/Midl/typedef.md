---
title: typedef, атрибут
description: Ключевое слово IDL typedef позволяет объявлять typedef, которые очень похожи на объявления typedef языка C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef с атрибутом MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790008"
---
# <a name="typedef-attribute"></a>typedef, атрибут

Ключевое слово IDL **typedef** позволяет объявлять **typedef** , которые очень похожи на объявления **typedef** языка C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Список IDL-Type-Attribute-List* 
</dt> <dd>

Указывает один или несколько атрибутов, применяемых к типу. Допустимые атрибуты типа в IDL-файле включают в себя **\[** [**Handle**](handle.md) **\]** , **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md), **\]** а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** . Несколько атрибутов разделяются запятыми.

</dd> <dt>

*Описатель типа* 
</dt> <dd>

Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа. Дополнительная спецификация хранилища может предшествовать *спецификатору типа*. Ключевое слово [**const**](const.md) может предшествовать *спецификатору типа*.

</dd> <dt>

*декларатор-список* 
</dt> <dd>

Задает стандартные деклараторы MIDL, такие как идентификаторы, деклараторы указателей и деклараторы массивов. Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers). *Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.

</dd> <dt>

*ACF-Type-Attribute-List* 
</dt> <dd>

Указывает один или несколько атрибутов, применяемых к типу. Допустимые атрибуты типа в ACF включают **\[** [**выделение**](allocate.md) **\]** , **\[** [**кодирование**](encode.md) **\]** и **\[** [**декодирование**](decode.md) **\]** .

</dd> <dt>

*имени* 
</dt> <dd>

Указывает тип, определенный в IDL-файле.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Объявление **TYPEDEF** IDL дополняется, позволяя связывать атрибуты типа с определенными типами. К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .

Ключевое слово **typedef** в ACF применяет атрибуты к типам, определенным в СООТВЕТСТВУЮЩем IDL-файле. Например, атрибут [**выделения**](allocate.md) типа позволяет настраивать выделение и освобождение памяти как приложением, так и заглушками.

Инструкция ACF **typedef** отображается как часть тела ACF. Обратите внимание, что синтаксис **TYPEDEF** ACF отличается от синтаксиса **typedef языка IDL и** синтаксиса **typedef** языка C. Новые типы не могут быть введены в ACF.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**массивы**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Контекстный \_ маркер**](context-handle.md)
</dt> <dt>

[**декодировать**](decode.md)
</dt> <dt>

[**шифровать**](encode.md)
</dt> <dt>

[**перечисления**](enum.md)
</dt> <dt>

[**справиться**](handle.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**обращать**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Строка**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Тип коммутатора \_**](switch-type.md)
</dt> <dt>

[**передать \_ как**](transmit-as.md)
</dt> <dt>

[**наборов**](union.md)
</dt> <dt>

[**однозначно**](unique.md)
</dt> </dl>

 

 