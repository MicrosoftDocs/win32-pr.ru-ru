---
title: string - атрибут
description: Атрибут \ String \ указывает, что одномерный массив char, WCHAR \_ t, Byte (или эквивалентный) или указатель на такой массив должен рассматриваться как строка.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- строковый атрибут MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987460"
---
# <a name="string-attribute"></a>string - атрибут

Атрибут **\[ String \]** указывает, что одномерный массив [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Byte**](byte.md) (или эквивалентный) или указатель на такой массив должен рассматриваться как строка. Строка может также быть массивом (или указателем на массив) конструкций, поля которых имеют тип **Byte**.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Type-Attribute-List* 
</dt> <dd>

Указывает один или несколько атрибутов, применяемых к типу. К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[ String \]** и **\[** [**Ignore**](ignore.md) **\]** . Несколько атрибутов разделяются запятыми.

</dd> <dt>

*Описатель типа* 
</dt> <dd>

Указывает [базовый тип](midl-base-types.md), тип [**структуры**](struct.md) или идентификатор типа. Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.

</dd> <dt>

*стандартные-деклараторы* 
</dt> <dd>

Задает стандартный декларатор C, например идентификатор, декларатор указателя или декларатор массива. Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*декларатор-список* 
</dt> <dd>

Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов. Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers). *Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми. Идентификатор параметра-Name в деклараторе функции является необязательным.

</dd> <dt>

*Список атрибутов Field* 
</dt> <dd>

Указывает ноль или более атрибутов полей, применимых к структуре, члену объединения или параметру функции. Два допустимых атрибута поля — **\[** [**это \_ Max**](max-is.md) , **\]** а **\[** [**размер \_ —**](size-is.md) **\]** **\[ \] строка** атрибутов **\[ \] использования, атрибут Ignore**, модификатор **\[ контекста \_ , тип указателя ref, UNIQUE или PTR, а также переключатель атрибута Union. \]** **\[** [](ref.md) **\]** **\[ \]** **\[** [](ptr.md) **\]** **\[ \_ \]** Несколько атрибутов полей разделяются запятыми.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к функции. Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[ \] ref**, **\[ Unique \]** или **\[ ptr \]**; и атрибуты использования **\[ строка \]**, **\[ Ignore \]** и **\[ Контекстный \_ маркер \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Задает необязательный декларатор указателя, к которому применяется атрибут **\[ String \]** . Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).

</dd> <dt>

*имя функции* 
</dt> <dd>

Задает имя удаленной процедуры.

</dd> <dt>

*Parameter-список атрибутов* 
</dt> <dd>

Состоит из нуля или более атрибутов, подходящих для указанного типа параметра. Атрибуты параметров могут **\[ \]** принимать и отменять **\[ атрибуты \]** направления; атрибуты поля **\[** [**Max \_ имеют**](max-is.md) значение, **\]** а **\[** [**размер \_ —**](size-is.md) **\]** атрибут указателя **\[ ref \]**, **\[ Unique \]** или **\[ ptr \]**, а также **\[ \_ маркер \] контекста** атрибутов использования и **\[ строка \]**. Атрибут использования **\[ Ignore \]** не может использоваться в качестве атрибута параметра. Несколько атрибутов разделяются запятыми.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если **\[ строковый \]** атрибут используется с массивом, границы которого определяются во время выполнения, необходимо также указать атрибут **\[ \_ \]** **\[ size \_ \]** или Max, как показано в следующем примере:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

Атрибут **\[ String \]** не может использоваться с атрибутами, задающих диапазон переданных элементов, например **\[ First \_ — \]**, **\[ Last \_ — \]** и **\[ length \_ — \]**.

При использовании в многомерных массивах атрибут **\[ String \]** применяется к крайнему справа массиву.

Чтобы определить подсчитанную строку, не используйте атрибут **\[ String \]** . Используйте массив символов или символьный указатель, подобный следующему:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

Атрибут **\[ String \]** указывает, что заглушка должна использовать предоставляемый языком метод для определения длины строк.

При объявлении строк в языке C необходимо выделить место для дополнительного символа, который обозначает конец строки.

## <a name="examples"></a>Примеры

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**массивы**](arrays-1.md)
</dt> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**обратный вызов**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Контекстный \_ маркер**](context-handle.md)
</dt> <dt>

[**перечисления**](enum.md)
</dt> <dt>

[**первый \_ —**](first-is.md)
</dt> <dt>

[**справиться**](handle.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**обращать**](ignore.md)
</dt> <dt>

[**Последний \_ —**](last-is.md)
</dt> <dt>

[**Длина \_ равна**](length-is.md)
</dt> <dt>

[**Языковые**](local.md)
</dt> <dt>

[**Максимальное \_ число**](max-is.md)
</dt> <dt>

[**Указатель \_ по умолчанию**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**размер \_ равен**](size-is.md)
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
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 