---
title: Соответствие процессоров в WOW64
description: 32-разрядная версия Windows поддерживает не более 32 процессоров. Таким образом, такие функции, как Жетпроцессаффинитимаск, имитируют компьютер с 32 процессоров при вызове в эмуляторе WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- соответствие процессоров в 64-разрядном программировании Windows
- WOW64 64-разрядное программирование Windows, соответствие процессоров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792457"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="dc963-106">Соответствие процессоров в WOW64</span><span class="sxs-lookup"><span data-stu-id="dc963-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="dc963-107">32-разрядная версия Windows поддерживает не более 32 процессоров.</span><span class="sxs-lookup"><span data-stu-id="dc963-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="dc963-108">Таким образом, такие функции, как [**жетпроцессаффинитимаск**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) , имитируют компьютер с 32 процессоров при вызове в эмуляторе WOW64.</span><span class="sxs-lookup"><span data-stu-id="dc963-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="dc963-109">Маска сходства получается путем выполнения побитовой операции OR для старших 32 бит маски с младшими 32 битами.</span><span class="sxs-lookup"><span data-stu-id="dc963-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="dc963-110">Таким образом, если поток имеет сходство для процессоров 0, 1 и 32, Подсистема WOW64 сообщает о сходстве как 0 и 1, так как процессор 32 сопоставляется с процессором 0.</span><span class="sxs-lookup"><span data-stu-id="dc963-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="dc963-111">Функции, устанавливающие сходство процессоров, например [**сетсреадаффинитимаск**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), ограничивают процессоры первыми 32 процессоров в эмуляторе WOW64.</span><span class="sxs-lookup"><span data-stu-id="dc963-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="dc963-112">Дополнительные сведения о сходстве процессоров см. в разделе [несколько процессоров](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="dc963-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 