---
title: Указатели и RPC
description: Использование указателей в качестве параметров C-Function очень эффективно.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888872"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="dc199-103">Указатели и RPC</span><span class="sxs-lookup"><span data-stu-id="dc199-103">Pointers and RPC</span></span>

<span data-ttu-id="dc199-104">Использование указателей в качестве параметров C-Function очень эффективно.</span><span class="sxs-lookup"><span data-stu-id="dc199-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="dc199-105">Указатель принимает только несколько байтов и может использоваться для доступа к большому объему памяти.</span><span class="sxs-lookup"><span data-stu-id="dc199-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="dc199-106">Однако в распределенном приложении процедуры клиента и сервера находятся в разных адресных пространствах — они могут находиться на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="dc199-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="dc199-107">Таким образом, клиент и сервер обычно не имеют доступа к одному и тому же пространству памяти.</span><span class="sxs-lookup"><span data-stu-id="dc199-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="dc199-108">Если одна из параметров удаленной процедуры является указателем на объект, клиент должен передать копию этого объекта и его указатель на сервер.</span><span class="sxs-lookup"><span data-stu-id="dc199-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="dc199-109">Если удаленная процедура изменяет объект с помощью его указателя, сервер возвращает указатель и его измененную копию.</span><span class="sxs-lookup"><span data-stu-id="dc199-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="dc199-110">MIDL предоставляет атрибуты указателя, чтобы сократить объем необходимых затрат и размер приложения.</span><span class="sxs-lookup"><span data-stu-id="dc199-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="dc199-111">В этом разделе рассматривается назначение и использование атрибутов указателя MIDL.</span><span class="sxs-lookup"><span data-stu-id="dc199-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="dc199-112">В нем также представлены сведения об обработке указателей в приложениях RPC.</span><span class="sxs-lookup"><span data-stu-id="dc199-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="dc199-113">Он разделен на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="dc199-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="dc199-114">Виды указателей</span><span class="sxs-lookup"><span data-stu-id="dc199-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="dc199-115">Указатели и выделение памяти</span><span class="sxs-lookup"><span data-stu-id="dc199-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="dc199-116">Типы указателей по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc199-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="dc199-117">Наследование типа атрибута указателя</span><span class="sxs-lookup"><span data-stu-id="dc199-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




