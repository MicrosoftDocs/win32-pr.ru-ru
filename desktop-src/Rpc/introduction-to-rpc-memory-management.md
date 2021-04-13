---
title: Общие сведения об управлении памятью RPC
description: Общие сведения об управлении памятью удаленного вызова процедур (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338713"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="5668a-103">Общие сведения об управлении памятью RPC</span><span class="sxs-lookup"><span data-stu-id="5668a-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="5668a-104">В контексте RPC управление памятью включает в себя:</span><span class="sxs-lookup"><span data-stu-id="5668a-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="5668a-105">Выделение и освобождение памяти, необходимой для имитации одного концептуального адресного пространства между клиентом и сервером в различных адресных пространствах потоков клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="5668a-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="5668a-106">Определение того, какой программный компонент отвечает за управление памятью — это приложение или заглушка, созданная с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="5668a-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="5668a-107">Выбор атрибутов MIDL, влияющих на управление памятью: атрибуты направления, атрибуты указателя, атрибуты массива и атрибуты ACF, \[ [ \_ количество байт](/windows/desktop/Midl/byte-count) \] , \[ [выделение](/windows/desktop/Midl/allocate) \] и \[ [Включение \_ выделения](/windows/desktop/Midl/enable-allocate) \] .</span><span class="sxs-lookup"><span data-stu-id="5668a-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="5668a-108">Когда программа вызывает функцию или процедуру в адресном пространстве, управление памятью является более простым, чем в распределенном приложении.</span><span class="sxs-lookup"><span data-stu-id="5668a-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="5668a-109">Для иллюстрации на следующей схеме показано двоичное дерево.</span><span class="sxs-lookup"><span data-stu-id="5668a-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="5668a-110">Чтобы передать эту структуру данных процедуре в адресном пространстве, программа просто передает указатель на корень дерева.</span><span class="sxs-lookup"><span data-stu-id="5668a-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![Двоичное дерево с указателями на данные структуры, размещенные в корне дерева](images/bintree.png)

<span data-ttu-id="5668a-112">Клиентские и серверные приложения RPC совместно используют данные в двух разных пространствах памяти.</span><span class="sxs-lookup"><span data-stu-id="5668a-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="5668a-113">Эти пространства памяти могут быть или не находиться на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5668a-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="5668a-114">В любом случае клиент и сервер не имеют прямого доступа к пространству памяти друг друга.</span><span class="sxs-lookup"><span data-stu-id="5668a-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="5668a-115">RPC зависит от возможности имитировать адресное пространство клиентской программы в адресном пространстве серверной программы.</span><span class="sxs-lookup"><span data-stu-id="5668a-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="5668a-116">Он также должен возвращать данные, включая новые и измененные данные, с сервера в память клиента.</span><span class="sxs-lookup"><span data-stu-id="5668a-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="5668a-117">В таких случаях, как двоичное дерево, представленное на предыдущей схеме, недостаточно передать указатель на корневой узел удаленной процедуре.</span><span class="sxs-lookup"><span data-stu-id="5668a-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="5668a-118">Либо программа, либо заглушки должны передать полное дерево в адресное пространство сервера, чтобы Удаленная процедура работала с ней.</span><span class="sxs-lookup"><span data-stu-id="5668a-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 