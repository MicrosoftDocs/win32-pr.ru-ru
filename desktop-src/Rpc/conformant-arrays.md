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
# <a name="conformant-arrays"></a><span data-ttu-id="d35a7-103">Согласованные массивы</span><span class="sxs-lookup"><span data-stu-id="d35a7-103">Conformant Arrays</span></span>

<span data-ttu-id="d35a7-104">Размер согласованного массива может различаться или соответствовать каждый раз, когда клиент передает его удаленной процедуре на сервере.</span><span class="sxs-lookup"><span data-stu-id="d35a7-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="d35a7-105">Определение интерфейса в файле MIDL приложения позволяет клиенту указывать размер массива при каждом вызове удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="d35a7-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="d35a7-106">Используйте пустые квадратные скобки ( \[ \] ) или звездочку в квадратных скобках ( \[ \* \] ) в определении массива, чтобы обозначить согласованный массив.</span><span class="sxs-lookup"><span data-stu-id="d35a7-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="d35a7-107">Следующий пример содержит определение удаленной процедуры в интерфейсе в файле MIDL.</span><span class="sxs-lookup"><span data-stu-id="d35a7-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="d35a7-108">Клиент указывает размер массива, который он передает серверу, с помощью параметра *размера массива*.</span><span class="sxs-lookup"><span data-stu-id="d35a7-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

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

<span data-ttu-id="d35a7-109">Определение интерфейса использует \[ [**размер \_**](/windows/desktop/Midl/size-is) атрибута MIDL \] для указания размера массива, который клиент передает на сервер.</span><span class="sxs-lookup"><span data-stu-id="d35a7-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="d35a7-110">Если вместо этого указать максимальное значение номеров индексов массива, используйте \[ атрибут [**Max \_**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="d35a7-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="d35a7-111">Дополнительные сведения об этих атрибутах MIDL см. в разделе [атрибуты массива](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d35a7-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="d35a7-112">В следующем фрагменте кода показано, как клиент может вызвать удаленную процедуру, определенную в предыдущем файле MIDL.</span><span class="sxs-lookup"><span data-stu-id="d35a7-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="d35a7-113">Этот фрагмент вызывает удаленную процедуру Миремотепрок дважды.</span><span class="sxs-lookup"><span data-stu-id="d35a7-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="d35a7-114">При первом вызове он передает массив из 20 элементов.</span><span class="sxs-lookup"><span data-stu-id="d35a7-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="d35a7-115">При втором вызове клиент передает массив элементов 200.</span><span class="sxs-lookup"><span data-stu-id="d35a7-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 