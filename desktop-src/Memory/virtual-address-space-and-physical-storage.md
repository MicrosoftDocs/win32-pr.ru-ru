---
description: Максимальный объем физической памяти, поддерживаемой Microsoft Windows, составляет от 2 ГБ до 2 ТБ в зависимости от версии Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Виртуальное адресное пространство и физическое хранилище
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545210"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="d2d6f-103">Виртуальное адресное пространство и физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="d2d6f-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="d2d6f-104">Максимальный объем физической памяти, поддерживаемой Microsoft Windows, составляет от 2 ГБ до 24 ТБ в зависимости от версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="d2d6f-105">Дополнительные сведения см. в разделе [ограничения памяти для выпусков Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="d2d6f-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="d2d6f-106">Виртуальное адресное пространство каждого процесса может быть меньше или больше, чем общая физическая память, доступная на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="d2d6f-107">Подмножество виртуального адресного пространства процесса, находящегося в физической памяти, называется *рабочим набором*.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="d2d6f-108">Если потоки процесса пытаются использовать больше физической памяти, чем доступно в данный момент, система замещает часть содержимого памяти на диск.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="d2d6f-109">Общий объем виртуального адресного пространства, доступного для процесса, ограничен физической памятью и свободным местом на диске, доступным для файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="d2d6f-110">Физическое хранилище и виртуальное адресное пространство каждого процесса организованы в виде *страниц*, единиц памяти, размер которых зависит от главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="d2d6f-111">Например, на компьютерах x86 размер страницы узла составляет 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="d2d6f-112">Чтобы максимально повысить гибкость управления памятью, система может перемещать страницы физической памяти в файл подкачки на диске и из него.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="d2d6f-113">При перемещении страницы в физической памяти система обновляет карты страниц затрагиваемых процессов.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="d2d6f-114">Когда системе требуется место в физической памяти, она перемещает наименее недавно использованные страницы физической памяти в файл подкачки.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="d2d6f-115">Обработка физической памяти системой полностью прозрачна для приложений, которые работают только в своих виртуальных адресных пространствах.</span><span class="sxs-lookup"><span data-stu-id="d2d6f-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



