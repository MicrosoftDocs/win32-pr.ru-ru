---
title: max_is - атрибут
description: Атрибут \ Max = \_ \ задает максимальное значение для допустимого индекса массива.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is атрибута MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337044"
---
# <a name="max_is-attribute"></a>Max \_ — атрибут

Атрибут **\[ Max \_ — \]** указывает максимальное значение для допустимого индекса массива.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*список ограниченных выражений* 
</dt> <dd>

Указывает одно или несколько выражений языка C. Каждое выражение оценивается как целое число, представляющее наибольший допустимый индекс массива. Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения. MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента. Несколько выражений разделяются запятыми.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ \_ Max \]** не обязательно соответствует количеству элементов в массиве. Для массива размером *n* в C, где первый элемент массива является нулевым числом элементов, максимальное значение для допустимого индекса массива равно *n*– 1.

Атрибут **\[ Max \_ не \]** может использоваться в качестве атрибута поля одновременно с **\[** [**\_**](size-is.md) **\]** атрибутом Size.

Хотя допускается использование атрибута **\[ Max \_ \]** с константным выражением, это неэффективно и не требуется. Например, используйте массив фиксированного размера:

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

вместо

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Примеры

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты поля](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**min \_ —**](min-is.md)
</dt> <dt>

[**размер \_ равен**](size-is.md)
</dt> </dl>

 

 