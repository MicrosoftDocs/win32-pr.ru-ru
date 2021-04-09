---
title: Согласованные массивы
description: Размер согласованного массива может различаться или соответствовать каждый раз, когда клиент передает его удаленной процедуре на сервере.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070455"
---
# <a name="conformant-arrays"></a>Согласованные массивы

Размер согласованного массива может различаться или соответствовать каждый раз, когда клиент передает его удаленной процедуре на сервере. Определение интерфейса в файле MIDL приложения позволяет клиенту указывать размер массива при каждом вызове удаленной процедуры. Используйте пустые квадратные скобки ( \[ \] ) или звездочку в квадратных скобках ( \[ \* \] ) в определении массива, чтобы обозначить согласованный массив.

Следующий пример содержит определение удаленной процедуры в интерфейсе в файле MIDL. Клиент указывает размер массива, который он передает серверу, с помощью параметра *размера массива*.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

Определение интерфейса использует \[ [**размер \_**](/windows/desktop/Midl/size-is) атрибута MIDL \] для указания размера массива, который клиент передает на сервер. Если вместо этого указать максимальное значение номеров индексов массива, используйте \[ атрибут [**Max \_**](/windows/desktop/Midl/max-is) \] . Дополнительные сведения об этих атрибутах MIDL см. в разделе [атрибуты массива](array-attributes.md).

В следующем фрагменте кода показано, как клиент может вызвать удаленную процедуру, определенную в предыдущем файле MIDL.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Этот фрагмент вызывает удаленную процедуру Миремотепрок дважды. При первом вызове он передает массив из 20 элементов. При втором вызове клиент передает массив элементов 200.

 

 