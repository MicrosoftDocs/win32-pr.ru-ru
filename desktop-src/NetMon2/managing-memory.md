---
description: В случае сбоя эксперта во время выполнения, если для управления памятью используются функции сетевой монитор, сетевой монитор освобождает выделенную память.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Управление памятью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991208"
---
# <a name="managing-memory"></a><span data-ttu-id="e1472-103">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="e1472-103">Managing Memory</span></span>

<span data-ttu-id="e1472-104">В случае сбоя эксперта во время выполнения, если для управления памятью используются функции сетевой монитор, сетевой монитор освобождает выделенную память.</span><span class="sxs-lookup"><span data-stu-id="e1472-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="e1472-105">Однако при написании эксперта может потребоваться получить сведения о системных ресурсах и структуре данных.</span><span class="sxs-lookup"><span data-stu-id="e1472-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="e1472-106">Например, эксперт по Объединенному протоколу сетевой монитор получит описатель файла для создания новой записи.</span><span class="sxs-lookup"><span data-stu-id="e1472-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="e1472-107">Каждый эксперт должен создать собственную обработку **try/catch** , чтобы эксперт мог высвободить приобретенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e1472-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="e1472-108">При выделении памяти используйте следующие существующие функции памяти:</span><span class="sxs-lookup"><span data-stu-id="e1472-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="e1472-109">**експерталлокмемори**</span><span class="sxs-lookup"><span data-stu-id="e1472-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="e1472-110">**експертреаллокмемори**</span><span class="sxs-lookup"><span data-stu-id="e1472-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



