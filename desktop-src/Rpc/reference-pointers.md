---
title: Ссылочные указатели
description: Ссылочные указатели — это самые простые указатели, требующие минимального объема обработки клиентской заглушкой.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070504"
---
# <a name="reference-pointers"></a><span data-ttu-id="bc840-103">Ссылочные указатели</span><span class="sxs-lookup"><span data-stu-id="bc840-103">Reference Pointers</span></span>

<span data-ttu-id="bc840-104">Ссылочные указатели — это самые простые указатели, требующие минимального объема обработки клиентской заглушкой.</span><span class="sxs-lookup"><span data-stu-id="bc840-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="bc840-105">Когда клиентская программа передает указатель ссылки на удаленную процедуру, указатель ссылки всегда содержит адрес допустимого блока памяти.</span><span class="sxs-lookup"><span data-stu-id="bc840-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="bc840-106">При завершении удаленной процедуры она по-прежнему будет указывать на тот же блок памяти.</span><span class="sxs-lookup"><span data-stu-id="bc840-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="bc840-107">Эти указатели в основном используются для реализации семантики ссылок и для разрешения параметров \[ [**out**](/windows/desktop/Midl/out-idl) \] в C.</span><span class="sxs-lookup"><span data-stu-id="bc840-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="bc840-108">В следующем примере значение указателя не изменяется во время вызова, хотя содержимое данных по адресу, указанному указателем, может измениться.</span><span class="sxs-lookup"><span data-stu-id="bc840-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![изменение данных по адресу статического указателя ссылки](images/prog-a07.png)

<span data-ttu-id="bc840-110">Ссылочный указатель имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="bc840-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="bc840-111">Он всегда указывает на допустимое хранилище и никогда не имеет значения **null**.</span><span class="sxs-lookup"><span data-stu-id="bc840-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="bc840-112">Он никогда не изменяется во время вызова и всегда указывает на то же хранилище до и после вызова.</span><span class="sxs-lookup"><span data-stu-id="bc840-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="bc840-113">Данные, возвращаемые удаленной процедурой, записываются в существующее хранилище.</span><span class="sxs-lookup"><span data-stu-id="bc840-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="bc840-114">Доступ к хранилищу, на который указывает указатель ссылки, невозможен любым другим указателем или любым другим именем в функции.</span><span class="sxs-lookup"><span data-stu-id="bc840-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="bc840-115">Используйте атрибут \[ [**ref**](/windows/desktop/Midl/ref) \] для указания ссылочных указателей в определениях интерфейса, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="bc840-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="bc840-116">В этом примере параметр *пчар* определяется как указатель на один символ, а не на массив символов.</span><span class="sxs-lookup"><span data-stu-id="bc840-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="bc840-117">Это \[ **выходной** \] параметр и указатель на ссылку, указывающий на память, которую Серверная подпрограммы ремотефн будет заполнять данными.</span><span class="sxs-lookup"><span data-stu-id="bc840-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 