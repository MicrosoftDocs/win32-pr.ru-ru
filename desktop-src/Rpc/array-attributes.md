---
title: Атрибуты массивов
description: Между массивами и указателями в языке C существует замкнутая связь.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793225"
---
# <a name="array-attributes"></a><span data-ttu-id="f5be0-103">Атрибуты массивов</span><span class="sxs-lookup"><span data-stu-id="f5be0-103">Array Attributes</span></span>

<span data-ttu-id="f5be0-104">Между массивами и указателями в языке C существует замкнутая связь.</span><span class="sxs-lookup"><span data-stu-id="f5be0-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="f5be0-105">При передаче в функцию в качестве параметра имя массива рассматривается как указатель на первый элемент массива, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="f5be0-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="f5be0-106">При локальном вызове можно использовать параметр указателя с марта по памяти и исследовать содержимое других адресов:</span><span class="sxs-lookup"><span data-stu-id="f5be0-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="f5be0-107">Когда клиент передает указатель на удаленную процедуру, заглушка клиента передает как указатель, так и данные, на которые он указывает.</span><span class="sxs-lookup"><span data-stu-id="f5be0-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="f5be0-108">Если указатель не ограничен соответствующими данными, вся память клиента должна передаваться при каждом удаленном вызове.</span><span class="sxs-lookup"><span data-stu-id="f5be0-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="f5be0-109">Применяя строгую типизацию в определении интерфейса, MIDL ограничивает обработку заглушки клиента данными, которые соответствуют указанному указателю.</span><span class="sxs-lookup"><span data-stu-id="f5be0-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="f5be0-110">Размер массива и диапазон элементов массива, передаваемых на удаленный компьютер, могут быть постоянными или переменными.</span><span class="sxs-lookup"><span data-stu-id="f5be0-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="f5be0-111">Если эти значения являются переменными и, таким способом, определяются во время выполнения, необходимо использовать атрибуты в IDL-файле, чтобы указать, сколько элементов массива передавать.</span><span class="sxs-lookup"><span data-stu-id="f5be0-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="f5be0-112">Следующие атрибуты MIDL поддерживают границы массивов.</span><span class="sxs-lookup"><span data-stu-id="f5be0-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="f5be0-113">attribute</span><span class="sxs-lookup"><span data-stu-id="f5be0-113">Attribute</span></span>                             | <span data-ttu-id="f5be0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f5be0-114">Description</span></span>                                             | <span data-ttu-id="f5be0-115">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f5be0-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="f5be0-116">\[[ **первый \_ —**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="f5be0-117">Индекс первого переданного элемента массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="f5be0-118">0</span><span class="sxs-lookup"><span data-stu-id="f5be0-118">0</span></span>       |
| <span data-ttu-id="f5be0-119">\[[ **последний \_ —**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="f5be0-120">Индекс последнего переданного элемента массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="f5be0-121">\[[ **длина \_ равна**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="f5be0-122">Общее число переданных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="f5be0-123">\[[ **Максимальное \_ число**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="f5be0-124">Наибольшее допустимое значение индекса массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="f5be0-125">\[[ **min \_ —**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="f5be0-126">Наименьшее допустимое значение индекса массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="f5be0-127">0</span><span class="sxs-lookup"><span data-stu-id="f5be0-127">0</span></span>       |
| <span data-ttu-id="f5be0-128">\[[ **размер \_ равен**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="f5be0-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="f5be0-129">Общее число элементов массива, выделенных для массива.</span><span class="sxs-lookup"><span data-stu-id="f5be0-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="f5be0-130">Атрибут **min \_ не** реализован в RPC.</span><span class="sxs-lookup"><span data-stu-id="f5be0-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="f5be0-131">Минимальный индекс массива всегда обрабатывается как ноль.</span><span class="sxs-lookup"><span data-stu-id="f5be0-131">The minimum array index is always treated as zero.</span></span>

 

 

 