---
description: Каждый процесс в 32-разрядной версии Microsoft Windows имеет собственное виртуальное адресное пространство, которое позволяет адресовать до 4 гигабайт памяти.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Управление памятью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682718"
---
# <a name="about-memory-management"></a><span data-ttu-id="612fb-103">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="612fb-103">About Memory Management</span></span>

<span data-ttu-id="612fb-104">Каждый процесс в 32-разрядной версии Microsoft Windows имеет собственное виртуальное адресное пространство, которое позволяет адресовать до 4 гигабайт памяти.</span><span class="sxs-lookup"><span data-stu-id="612fb-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="612fb-105">Каждый процесс в 64-разрядном Windows имеет виртуальное адресное пространство, равное 8 терабайтам.</span><span class="sxs-lookup"><span data-stu-id="612fb-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="612fb-106">Все потоки процесса могут обращаться к своему виртуальному адресному пространству.</span><span class="sxs-lookup"><span data-stu-id="612fb-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="612fb-107">Однако потоки не могут получить доступ к памяти, принадлежащей другому процессу, что защищает процесс от повреждения другим процессом.</span><span class="sxs-lookup"><span data-stu-id="612fb-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="612fb-108">Сведения о пространстве виртуальных адресов и функциях управления памятью см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="612fb-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="612fb-109">Виртуальное адресное пространство</span><span class="sxs-lookup"><span data-stu-id="612fb-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="612fb-110">Пулы памяти</span><span class="sxs-lookup"><span data-stu-id="612fb-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="612fb-111">Сведения о производительности памяти</span><span class="sxs-lookup"><span data-stu-id="612fb-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="612fb-112">Функции виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="612fb-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="612fb-113">Функции кучи</span><span class="sxs-lookup"><span data-stu-id="612fb-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="612fb-114">Сопоставление файлов</span><span class="sxs-lookup"><span data-stu-id="612fb-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="612fb-115">Поддержка больших объемов памяти</span><span class="sxs-lookup"><span data-stu-id="612fb-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="612fb-116">Глобальные и локальные функции</span><span class="sxs-lookup"><span data-stu-id="612fb-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="612fb-117">Функции стандартной библиотеки C</span><span class="sxs-lookup"><span data-stu-id="612fb-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="612fb-118">Сравнение методов выделения памяти</span><span class="sxs-lookup"><span data-stu-id="612fb-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



