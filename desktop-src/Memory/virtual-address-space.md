---
description: Виртуальным адресным пространством для процесса является набор адресов виртуальной памяти, который можно использовать. Адресное пространство для каждого процесса является закрытым и не может быть доступно другим процессам, если он не является общим.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Виртуальное адресное пространство (управление памятью)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991270"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="6a313-104">Виртуальное адресное пространство (управление памятью)</span><span class="sxs-lookup"><span data-stu-id="6a313-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="6a313-105">Виртуальным адресным пространством для процесса является набор адресов виртуальной памяти, который можно использовать.</span><span class="sxs-lookup"><span data-stu-id="6a313-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="6a313-106">Адресное пространство для каждого процесса является закрытым и не может быть доступно другим процессам, если он не является общим.</span><span class="sxs-lookup"><span data-stu-id="6a313-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="6a313-107">Виртуальный адрес не представляет фактическое физическое расположение объекта в памяти; Вместо этого система ведет *таблицу страниц* для каждого процесса, который представляет собой внутреннюю структуру данных, используемую для преобразования виртуальных адресов в соответствующие физические адреса.</span><span class="sxs-lookup"><span data-stu-id="6a313-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="6a313-108">Каждый раз, когда поток ссылается на адрес, система преобразует виртуальный адрес в физический адрес.</span><span class="sxs-lookup"><span data-stu-id="6a313-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="6a313-109">Виртуальное адресное пространство для 32-разрядной версии Windows имеет размер 4 гигабайта (ГБ) и делится на две секции: одна для использования процессом, а другая зарезервирована для использования системой.</span><span class="sxs-lookup"><span data-stu-id="6a313-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="6a313-110">Дополнительные сведения о пространстве виртуальных адресов в 64-разрядных Windows см. в разделе [виртуальное адресное пространство в 64-разрядной версии Windows](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="6a313-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="6a313-111">Дополнительные сведения о виртуальной памяти см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6a313-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="6a313-112">Виртуальное адресное пространство и физическое хранилище</span><span class="sxs-lookup"><span data-stu-id="6a313-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="6a313-113">Рабочий набор</span><span class="sxs-lookup"><span data-stu-id="6a313-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="6a313-114">Состояние страницы</span><span class="sxs-lookup"><span data-stu-id="6a313-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="6a313-115">Область выделенной памяти</span><span class="sxs-lookup"><span data-stu-id="6a313-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="6a313-116">Предотвращение выполнения данных</span><span class="sxs-lookup"><span data-stu-id="6a313-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="6a313-117">Защита памяти</span><span class="sxs-lookup"><span data-stu-id="6a313-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="6a313-118">Ограничения памяти для выпусков Windows</span><span class="sxs-lookup"><span data-stu-id="6a313-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="6a313-119">Виртуальное адресное пространство по умолчанию для 32-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="6a313-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="6a313-120">В следующей таблице показан диапазон памяти по умолчанию для каждой секции.</span><span class="sxs-lookup"><span data-stu-id="6a313-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="6a313-121">Диапазон памяти</span><span class="sxs-lookup"><span data-stu-id="6a313-121">Memory range</span></span>                             | <span data-ttu-id="6a313-122">Использование</span><span class="sxs-lookup"><span data-stu-id="6a313-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="6a313-123">Низкая 2 ГБ (от 0x00000000 до 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="6a313-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="6a313-124">Используется процессом.</span><span class="sxs-lookup"><span data-stu-id="6a313-124">Used by the process.</span></span> |
| <span data-ttu-id="6a313-125">Высокий 2 ГБ (от 0x80000000 до 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="6a313-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="6a313-126">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="6a313-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="6a313-127">Виртуальное адресное пространство для 32-разрядной версии Windows с 4GT</span><span class="sxs-lookup"><span data-stu-id="6a313-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="6a313-128">Если включена [Настройка 4 гигабайта](4-gigabyte-tuning.md) (4GT), диапазон памяти для каждой секции выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6a313-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="6a313-129">Диапазон памяти</span><span class="sxs-lookup"><span data-stu-id="6a313-129">Memory range</span></span>                             | <span data-ttu-id="6a313-130">Использование</span><span class="sxs-lookup"><span data-stu-id="6a313-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="6a313-131">С низким 3 ГБ (0x00000000 до 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="6a313-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="6a313-132">Используется процессом.</span><span class="sxs-lookup"><span data-stu-id="6a313-132">Used by the process.</span></span> |
| <span data-ttu-id="6a313-133">Высокий 1 ГБ (0xC0000000 до 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="6a313-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="6a313-134">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="6a313-134">Used by the system.</span></span>  |



 

<span data-ttu-id="6a313-135">После включения 4GT процесс, имеющий установленный в заголовке изображения флаг с большим количеством [**\_ файлов \_ \_ \_ изображений**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) , будет иметь доступ к дополнительному объему памяти (1 ГБ), превышающему младшие 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="6a313-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="6a313-136">Настройка виртуального адресного пространства для 32-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="6a313-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="6a313-137">Можно использовать следующую команду, чтобы задать параметр записи загрузки, который настраивает размер раздела, который может использоваться процессом, в диапазоне от 2048 (2 ГБ) до 3072 (3 ГБ):</span><span class="sxs-lookup"><span data-stu-id="6a313-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="6a313-138">[BCDEdit/Set](/windows-hardware/drivers/devtest/bcdedit--set) **инкреасеусерва** *мегабайт*</span><span class="sxs-lookup"><span data-stu-id="6a313-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="6a313-139">После установки параметра загрузочной записи диапазон памяти для каждой секции выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6a313-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="6a313-140">Диапазон памяти</span><span class="sxs-lookup"><span data-stu-id="6a313-140">Memory range</span></span>                            | <span data-ttu-id="6a313-141">Использование</span><span class="sxs-lookup"><span data-stu-id="6a313-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="6a313-142">Низкая (0x00000000 до *мегабайт*)</span><span class="sxs-lookup"><span data-stu-id="6a313-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="6a313-143">Используется процессом.</span><span class="sxs-lookup"><span data-stu-id="6a313-143">Used by the process.</span></span> |
| <span data-ttu-id="6a313-144">Высокий (в *мегабайтах*+ 1 – 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="6a313-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="6a313-145">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="6a313-145">Used by the system.</span></span>  |



 

<span data-ttu-id="6a313-146">**Windows Server 2003:** Задайте для параметра **/USERVA** в boot.ini значение от 2048 до 3072.</span><span class="sxs-lookup"><span data-stu-id="6a313-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
