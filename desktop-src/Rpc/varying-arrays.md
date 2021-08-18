---
title: Различные массивы
description: В MIDL различные массивы имеют фиксированный размер. Они позволяют клиентам передавать различные части массивов с клиентов на серверы. Размер части массива может изменяться в зависимости от вызова вызова. Однако размер всего массива фиксирован.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3919eed28ef7a9c888d7c23e4ebe12a1db39c97b18fa325c6daf8a4cd62d6554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010552"
---
# <a name="varying-arrays"></a>Различные массивы

В MIDL различные массивы имеют фиксированный размер. Они позволяют клиентам передавать различные части массивов с клиентов на серверы. Размер части массива может изменяться в зависимости от вызова вызова. Однако размер всего массива фиксирован.

Например, в следующем примере показано определение удаленной процедуры в интерфейсе в файле MIDL. Размер массива, переданного клиентом на сервер, исправляется по размеру массива констант \_ . Интерфейс указывает часть массива, которую клиент передает на сервер в параметрах Фирстелемент и chunkSize.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

В определении интерфейса сначала используется атрибут MIDL, \[ [**\_**](/windows/desktop/Midl/first-is) \] указывающий номер индекса первого элемента в части массива, который клиент передает на сервер. Атрибут \[ [**length \_**](/windows/desktop/Midl/length-is) \] указывает общее количество элементов массива, которые передает клиент. Дополнительные сведения об этих атрибутах MIDL см. в разделе [атрибуты массива](array-attributes.md).

В следующем фрагменте кода показано, как клиент может вызвать удаленную процедуру, определенную в предыдущем файле MIDL.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Этот фрагмент вызывает удаленную процедуру Миремотепрок дважды. При первом вызове он передает элементы массива с номерами от 20 до 119, как показано в значениях переменных Фирстаррайелементнумбер и Тоталелементспассед. При втором вызове клиент передает элементы массива с номерами 120 по 319.

 

 