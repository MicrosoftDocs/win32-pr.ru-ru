---
description: 'Диспетчер памяти создает следующие пулы памяти, используемые системой для выделения памяти: невыгружаемого пула и выгружаемого пула.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Пулы памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674435"
---
# <a name="memory-pools"></a><span data-ttu-id="9a2d7-103">Пулы памяти</span><span class="sxs-lookup"><span data-stu-id="9a2d7-103">Memory Pools</span></span>

<span data-ttu-id="9a2d7-104">Диспетчер памяти создает следующие пулы памяти, используемые системой для выделения памяти: невыгружаемого пула и выгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="9a2d7-105">Оба пула памяти находятся в регионе адресного пространства, зарезервированного для системы и сопоставленного с виртуальным адресным пространством каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="9a2d7-106">Невыгружаемого пула состоит из адресов виртуальной памяти, которые гарантированно находятся в физической памяти, при условии, что соответствующие объекты ядра выделены.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="9a2d7-107">Выгружаемого пула состоит из виртуальной памяти, которая может быть помещена в систему и из нее.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="9a2d7-108">Для повышения производительности системы с одним процессором имеют три выгружаемого пула, и многопроцессорные системы имеют пять выгружаемого страничных пулов.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="9a2d7-109">Дескрипторы [объектов ядра](../sysinfo/kernel-objects.md) хранятся в выгружаемом пуле, поэтому количество создаваемых дескрипторов зависит от объема доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="9a2d7-110">Система записывает ограничения и текущие значения для нестраничного пула, выгружаемого пула и использования файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="9a2d7-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="9a2d7-111">Дополнительные сведения см. в разделе [сведения о производительности памяти](memory-performance-information.md).</span><span class="sxs-lookup"><span data-stu-id="9a2d7-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
