---
title: " в, out, size_is prototype"
description: в \_ качестве размера \ prototype использует одномерный массив символов, передаваемый от клиента серверу и от сервера к клиенту.
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337793"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="ff676-103">\[в, out и Size \_ — \] прототип</span><span class="sxs-lookup"><span data-stu-id="ff676-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="ff676-104">В следующем прототипе функции используется массив символов с одной подсчетностью, который передается обоими способами: от клиента к серверу и от сервера к клиенту:</span><span class="sxs-lookup"><span data-stu-id="ff676-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="ff676-105">В качестве \[ параметра [**в**](/windows/desktop/Midl/in) \] параметре *ачинаут* должен указывать на допустимое хранилище на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="ff676-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="ff676-106">Разработчик выделяет память, связанную с массивом, на стороне клиента перед выполнением удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="ff676-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="ff676-107">Заглушки используют \[ [**размер \_ —**](/windows/desktop/Midl/size-is) \] параметр *стрсизе* для выделения памяти на сервере, а для \[ [**\_**](/windows/desktop/Midl/length-is) \] передачи элементов массива в эту память используется параметр length *пкбсизе* .</span><span class="sxs-lookup"><span data-stu-id="ff676-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="ff676-108">Разработчик должен убедиться, что код клиента задает **\[ длину \_ \]** переменной перед вызовом удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="ff676-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="ff676-109">В некоторых ситуациях использование отдельных параметров вместо одной строки для ввода и вывода является более эффективным и обеспечивает гибкость.</span><span class="sxs-lookup"><span data-stu-id="ff676-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="ff676-110">Это продемонстрировано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ff676-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="ff676-111">В предыдущем примере массив символов Ачинаут также используется в качестве \[ [**выходного**](/windows/desktop/Midl/out-idl) \] параметра.</span><span class="sxs-lookup"><span data-stu-id="ff676-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="ff676-112">В C имя массива эквивалентно использованию указателя.</span><span class="sxs-lookup"><span data-stu-id="ff676-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="ff676-113">По умолчанию все указатели верхнего уровня являются ссылочными указателями — они не меняются в значении и указывают на одну и ту же область памяти на клиенте до и после вызова.</span><span class="sxs-lookup"><span data-stu-id="ff676-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="ff676-114">Вся память, к которой обращаются удаленные процедуры, должна соответствовать размеру, указанному клиентом перед вызовом, или заглушкам будет выдаваться исключение.</span><span class="sxs-lookup"><span data-stu-id="ff676-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="ff676-115">Перед возвращением функция Analyze на сервере должна сбросить параметр *пкбсизе* , чтобы указать количество элементов, которые сервер будет передавать клиенту, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ff676-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 