---
description: Приложения могут безопасно использовать функции управления памятью библиотеки времени выполнения C (malloc, Free и т. д.) и C++ (создать, удалить и т. д.).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Функции стандартной библиотеки C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662593"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="ca188-103">Функции стандартной библиотеки C</span><span class="sxs-lookup"><span data-stu-id="ca188-103">Standard C Library Functions</span></span>

<span data-ttu-id="ca188-104">Приложения могут безопасно использовать функции управления памятью библиотеки времени выполнения C (**malloc**, **Free** и т. д.) и C++ (**создать**, **Удалить** и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ca188-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="ca188-105">Функции библиотеки времени выполнения C не имеют потенциальных проблем в 16-разрядных Windows.</span><span class="sxs-lookup"><span data-stu-id="ca188-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="ca188-106">Управление памятью больше не является проблемой, поскольку система может управлять памятью, перемещая страницы физической памяти, не влияя на виртуальные адреса.</span><span class="sxs-lookup"><span data-stu-id="ca188-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="ca188-107">Аналогично различие между близкими и дальнеими указателями больше не имеет отношения к.</span><span class="sxs-lookup"><span data-stu-id="ca188-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="ca188-108">Таким образом, можно использовать стандартные функции библиотеки C для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="ca188-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="ca188-109">Однако функции управления памятью предоставляют функциональные возможности, недоступные в библиотеке времени выполнения C.</span><span class="sxs-lookup"><span data-stu-id="ca188-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



