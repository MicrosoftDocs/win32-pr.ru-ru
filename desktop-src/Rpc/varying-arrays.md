---
title: Различные массивы
description: В MIDL различные массивы имеют фиксированный размер. Они позволяют клиентам передавать различные части массивов с клиентов на серверы. Размер части массива может изменяться в зависимости от вызова вызова. Однако размер всего массива фиксирован.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488101"
---
# <a name="varying-arrays"></a><span data-ttu-id="6b456-106">Различные массивы</span><span class="sxs-lookup"><span data-stu-id="6b456-106">Varying Arrays</span></span>

<span data-ttu-id="6b456-107">В MIDL различные массивы имеют фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="6b456-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="6b456-108">Они позволяют клиентам передавать различные части массивов с клиентов на серверы.</span><span class="sxs-lookup"><span data-stu-id="6b456-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="6b456-109">Размер части массива может изменяться в зависимости от вызова вызова.</span><span class="sxs-lookup"><span data-stu-id="6b456-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="6b456-110">Однако размер всего массива фиксирован.</span><span class="sxs-lookup"><span data-stu-id="6b456-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="6b456-111">Например, в следующем примере показано определение удаленной процедуры в интерфейсе в файле MIDL.</span><span class="sxs-lookup"><span data-stu-id="6b456-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="6b456-112">Размер массива, переданного клиентом на сервер, исправляется по размеру массива констант \_ .</span><span class="sxs-lookup"><span data-stu-id="6b456-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="6b456-113">Интерфейс указывает часть массива, которую клиент передает на сервер в параметрах Фирстелемент и chunkSize.</span><span class="sxs-lookup"><span data-stu-id="6b456-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

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

<span data-ttu-id="6b456-114">В определении интерфейса сначала используется атрибут MIDL, \[ [**\_**](/windows/desktop/Midl/first-is) \] указывающий номер индекса первого элемента в части массива, который клиент передает на сервер.</span><span class="sxs-lookup"><span data-stu-id="6b456-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="6b456-115">Атрибут \[ [**length \_**](/windows/desktop/Midl/length-is) \] указывает общее количество элементов массива, которые передает клиент.</span><span class="sxs-lookup"><span data-stu-id="6b456-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="6b456-116">Дополнительные сведения об этих атрибутах MIDL см. в разделе [атрибуты массива](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6b456-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="6b456-117">В следующем фрагменте кода показано, как клиент может вызвать удаленную процедуру, определенную в предыдущем файле MIDL.</span><span class="sxs-lookup"><span data-stu-id="6b456-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="6b456-118">Этот фрагмент вызывает удаленную процедуру Миремотепрок дважды.</span><span class="sxs-lookup"><span data-stu-id="6b456-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="6b456-119">При первом вызове он передает элементы массива с номерами от 20 до 119, как показано в значениях переменных Фирстаррайелементнумбер и Тоталелементспассед.</span><span class="sxs-lookup"><span data-stu-id="6b456-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="6b456-120">При втором вызове клиент передает элементы массива с номерами 120 по 319.</span><span class="sxs-lookup"><span data-stu-id="6b456-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 