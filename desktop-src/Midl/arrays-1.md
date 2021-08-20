---
title: Array, атрибут
description: Массивы представляют собой однородные коллекции данных, доступ к которым осуществляется по индексу или номеру элемента.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- массив с атрибутом MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57682252c36284a89a3fb659c69446902c3d0181cbf82d494b200b5769e087e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808282"
---
# <a name="arrays-attribute"></a>Array, атрибут

Массивы представляют собой однородные коллекции данных, доступ к которым осуществляется по индексу или номеру элемента.

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип-attr-список* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к типу. К допустимым атрибутам типа относятся [**\[ \] Handle**](handle.md), [**\[ Switch \_ Type \]**](switch-type.md), [**\[ передает \_ As \]**](transmit-as.md); атрибут указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md);, а также [**\[ \_ маркер \] контекста**](context-handle.md)атрибутов использования, [**\[ String \]**](string.md)и [**\[ Ignore \]**](ignore.md). Несколько атрибутов разделяются запятыми.

</dd> <dt>

*Описатель типа* 
</dt> <dd>

Задает идентификатор типа, базовый тип, [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) . Спецификация типа может включать в себя дополнительную спецификацию хранилища.

</dd> <dt>

*pointer-decl* 
</dt> <dd>

Указывает ноль или несколько деклараторов указателей. Декларатор указателя аналогичен декларатору указателя, используемому в языке C, созданному из **\* *_ обозначения, модификаторов, таких как _* FAR**, и квалификатора [**const**](const.md).

</dd> <dt>

*декларатор массива* 
</dt> <dd>

Задает имя массива, за которым следуют одна из следующих конструкций для каждого измерения массива: "**\[ \]**", " **\[\*\]** ", " **\[** _Const1_ *_\]_* " или " **\[** _Lower... Upper_ *_\]_* ", где" *снизу* "и" *верхний* "являются константными значениями, представляющими нижнюю и верхнюю границы. Константа *ниже* должна иметь значение 0.

</dd> <dt>

*тегами* 
</dt> <dd>

Указывает необязательный тег для структуры или объединения.

</dd> <dt>

*Список атрибутов Field* 
</dt> <dd>

Указывает ноль или более атрибутов полей, применимых к структуре, члену объединения или параметру функции. К допустимым атрибутам полей относятся: [**\[ \_ \] First**](first-is.md)—, [**\[ Last \_ — \]**](last-is.md), [**\[ length \_ — \]**](length-is.md), [**\[ Max \_ — \]**](max-is.md), [**\[ size \_ — \]**](size-is.md), [**\[ строка \]**](string.md)атрибутов использования и [**\[ игнорируется \]**](ignore.md); атрибуты указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)и [**\[ ptr \]**](ptr.md); и [**\[ \_ тип \] переключателя**](switch-type.md)атрибута объединения. Несколько атрибутов полей разделяются запятыми. Обратите внимание, что из перечисленных выше атрибутов, « **\[ первый \_ \]**», « **\[ последний \_ \]**» и « [**\[ игнорирует \]**](ignore.md) », недопустимы для объединений.

</dd> <dt>

*ограниченное выражение* 
</dt> <dd>

Указывает выражение языка C. Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения. MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к функции. Допустимые атрибуты функции — [**\[ обратный \] вызов**](callback.md), [**\[ локальный \]**](local.md)объект, атрибут указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md), а также [**\[ строка \]**](string.md)атрибутов использования и [**\[ Контекстный \_ маркер \]**](context-handle.md).

</dd> <dt>

*имя функции* 
</dt> <dd>

Задает имя удаленной процедуры.

</dd> <dt>

*Param-attr-список* 
</dt> <dd>

Задает атрибуты направления и один или несколько необязательных атрибутов поля, которые применяются к параметру массива. Допустимые атрибуты поля включают [**\[ Max \_ — \]**](max-is.md), [**\[ size \_ \] —**](size-is.md), [**\[ length \_ — \]**](length-is.md), [**\[ First \_ — \]**](first-is.md), а [**\[ Last \_ — \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Массивы в MIDL используют стиль, похожий на, но не точно такой же, как C и C++. Дополнительные сведения см. в разделе [MIDL Arrays](midl-arrays.md).

## <a name="see-also"></a>См. также

<dl> <dt>

[**обратный вызов**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Контекстный \_ маркер**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**первый \_ —**](first-is.md)
</dt> <dt>

[**handle**](handle.md)
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

[**указатель**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**размер \_ равен**](size-is.md)
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

 

 




