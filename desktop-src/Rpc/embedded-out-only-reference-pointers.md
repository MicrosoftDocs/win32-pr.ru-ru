---
title: Внедренные Out-Only указатели ссылок
description: Внедренные Out-Only указатели ссылок
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672379"
---
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="f095c-103">Внедренные Out-Only указатели ссылок</span><span class="sxs-lookup"><span data-stu-id="f095c-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="f095c-104">При использовании \[ [](/windows/desktop/Midl/out-idl) \] ссылочных указателей в Microsoft RPC, созданные заглушки сервера выделяют только первый уровень указателей, доступных из указателя ссылки.</span><span class="sxs-lookup"><span data-stu-id="f095c-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="f095c-105">Указатели на более глубоких уровнях не выделяются заглушками, но должны выделяться уровнем серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="f095c-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="f095c-106">Например, предположим, что интерфейс указывает только недопустимый \[  \] массив указателей ссылок:</span><span class="sxs-lookup"><span data-stu-id="f095c-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="f095c-107">В этом примере заглушка сервера выделяет память для 10 указателей и присваивает каждому указателю значение null.</span><span class="sxs-lookup"><span data-stu-id="f095c-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="f095c-108">Серверное приложение должно выделить память для 10 [**коротких**](/windows/desktop/Midl/short) целых чисел, на которые ссылаются указатели, а затем установить 10 указателей для указания на целые числа.</span><span class="sxs-lookup"><span data-stu-id="f095c-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="f095c-109">Если в \[ [](/windows/desktop/Midl/out-idl) \] структуре данных только для выхода включены вложенные указатели на ссылки, то заглушки сервера выделяют только первый указатель, доступный из указателя ссылки.</span><span class="sxs-lookup"><span data-stu-id="f095c-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="f095c-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="f095c-110">For example:</span></span>

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

<span data-ttu-id="f095c-111">В предыдущем примере заглушки сервера распределяют указатель *пстоп* и **\_ \_ тип Top структуры** Structure.</span><span class="sxs-lookup"><span data-stu-id="f095c-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="f095c-112">Указатель ссылки *PS1* в **типе структуры \_ Top \_** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="f095c-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="f095c-113">Заглушка сервера не выделяет каждый уровень структуры данных, а также не выделяет **\_ тип STRUCT1** или внедренный указатель *псвалуе*.</span><span class="sxs-lookup"><span data-stu-id="f095c-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 