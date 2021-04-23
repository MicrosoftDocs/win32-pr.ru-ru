---
description: Системный виртуальный адрес (ва) в 32-разрядных системах может стать недоступным из-за фрагментации. Для настройки ограничений памяти в 32-разрядных системах, которые сталкиваются с этой проблемой, можно использовать несколько разделов реестра.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Разделы реестра для управления памятью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913683"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="17c57-104">Разделы реестра для управления памятью</span><span class="sxs-lookup"><span data-stu-id="17c57-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="17c57-105">Системный виртуальный адрес (ва) в 32-разрядных системах может стать недоступным из-за фрагментации.</span><span class="sxs-lookup"><span data-stu-id="17c57-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="17c57-106">Для настройки ограничений памяти в 32-разрядных системах, которые сталкиваются с этой проблемой, можно использовать несколько разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="17c57-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="17c57-107">Системное пространство на 64-разрядных системах не зависит от фрагментации. Поэтому эти ключи не оказывают влияния на 64-разрядные системы.</span><span class="sxs-lookup"><span data-stu-id="17c57-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="17c57-108">Для 32-разрядных систем эти разделы реестра управления памятью должны быть явно созданы в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="17c57-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="17c57-109">**HKey \_ \_** \\  \\ **Текущий набор параметров** \\ **управления** \\  \\ **памятью** диспетчера сеансов локального компьютера</span><span class="sxs-lookup"><span data-stu-id="17c57-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="17c57-110">**Windows Server 2008 и Windows Vista:** Эти разделы реестра доступны в 32-разрядных системах, начиная с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="17c57-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="17c57-111">Сведения об ограничениях памяти и адресного пространства по умолчанию для 32-разрядных и 64-разрядных систем см. в разделе [ограничения памяти для выпусков Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="17c57-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="17c57-112">В следующей таблице описаны разделы реестра управления памятью, которые можно использовать для настройки ограничений памяти в 32-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="17c57-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="17c57-113">Все эти ключи имеют \_ тип DWORD с параметром reg и возможные значения в диапазоне от 0 до 2 048 МБ.</span><span class="sxs-lookup"><span data-stu-id="17c57-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="17c57-114">Значение по умолчанию — 0. Это означает, что ограничения не применяются.</span><span class="sxs-lookup"><span data-stu-id="17c57-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="17c57-115">Значения автоматически округляются до следующей границы размещения системы, что составляет 2 МБ в 32-разрядных системах с включенным [расширением физических адресов](physical-address-extension.md) (PAE) и 4 мб на 32-разрядных системах, для которых не включен PAE.</span><span class="sxs-lookup"><span data-stu-id="17c57-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="17c57-116">Ключ</span><span class="sxs-lookup"><span data-stu-id="17c57-116">Key</span></span>                   | <span data-ttu-id="17c57-117">Описание</span><span class="sxs-lookup"><span data-stu-id="17c57-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c57-118">**нонпажедпуллимит**</span><span class="sxs-lookup"><span data-stu-id="17c57-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="17c57-119">Указывает максимальный объем системного пространства, который может использоваться невыгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="17c57-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="17c57-120">При определенных условиях это ограничение может быть превышено на небольшое количество.</span><span class="sxs-lookup"><span data-stu-id="17c57-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="17c57-121">**пажедпуллимит**</span><span class="sxs-lookup"><span data-stu-id="17c57-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="17c57-122">Указывает максимальный объем системного пространства, который может использоваться выгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="17c57-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="17c57-123">**сессионспацелимит**</span><span class="sxs-lookup"><span data-stu-id="17c57-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="17c57-124">Указывает максимальный объем системного пространства, который может использоваться при выделении пространства сеанса.</span><span class="sxs-lookup"><span data-stu-id="17c57-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="17c57-125">**системкачелимит**</span><span class="sxs-lookup"><span data-stu-id="17c57-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="17c57-126">Указывает максимальный объем системного пространства, который может использоваться системным кэшем.</span><span class="sxs-lookup"><span data-stu-id="17c57-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="17c57-127">При определенных условиях это ограничение может быть превышено на небольшое количество.</span><span class="sxs-lookup"><span data-stu-id="17c57-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="17c57-128">**системптеслимит**</span><span class="sxs-lookup"><span data-stu-id="17c57-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="17c57-129">Указывает максимальный объем системного пространства, который может использоваться сопоставлениями ввода-вывода и другими ресурсами, использующими записи системной таблицы страниц (PTE).</span><span class="sxs-lookup"><span data-stu-id="17c57-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="17c57-130">Чтобы определить, исчерпано ли системное пространство, необходимо использовать отладчик ядра.</span><span class="sxs-lookup"><span data-stu-id="17c57-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="17c57-131">Дополнительные сведения см. в разделе [Debugging Tools for Windows (на английском языке)](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="17c57-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



