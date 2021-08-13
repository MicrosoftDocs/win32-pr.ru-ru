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
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642970"
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

## <a name="remarks"></a>Remarks

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

 

 