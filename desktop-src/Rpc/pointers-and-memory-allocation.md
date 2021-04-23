---
title: Указатели и выделение памяти
description: Возможность изменения памяти с помощью указателей часто требует, чтобы сервер и клиент выделили достаточно памяти для элементов массива.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134355"
---
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="15703-103">Указатели и выделение памяти</span><span class="sxs-lookup"><span data-stu-id="15703-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="15703-104">Возможность изменения памяти с помощью указателей часто требует, чтобы сервер и клиент выделили достаточно памяти для элементов массива.</span><span class="sxs-lookup"><span data-stu-id="15703-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="15703-105">Когда заглушка должна выделить или освободить память, она вызывает функции библиотеки времени выполнения, которые, в свою очередь, вызывают функции [**MIDL для \_ пользовательского \_ выделения**](/windows/desktop/Midl/midl-user-allocate-1) и [**MIDL \_ \_**](/windows/desktop/Midl/midl-user-free-1).</span><span class="sxs-lookup"><span data-stu-id="15703-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="15703-106">Эти функции не включаются в библиотеку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="15703-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="15703-107">Вам необходимо написать собственные версии этих функций и связать их с приложением.</span><span class="sxs-lookup"><span data-stu-id="15703-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="15703-108">Таким образом можно решить, как управлять памятью.</span><span class="sxs-lookup"><span data-stu-id="15703-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="15703-109">При компиляции файла IDL в режиме использование-Compatibility (**/ОСФ**) не требуется реализовывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="15703-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="15703-110">Эти функции необходимо записать в следующие прототипы:</span><span class="sxs-lookup"><span data-stu-id="15703-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="15703-111">Например, версии этих функций для приложения могут просто вызывать стандартные функции библиотеки:</span><span class="sxs-lookup"><span data-stu-id="15703-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 