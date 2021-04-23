---
description: Расширение физических адресов (PAE) — это компонент процессора, который позволяет процессорам x86 получать доступ к более чем 4 ГБ физической памяти в поддерживающих версиях Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Расширение физических адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081611"
---
# <a name="physical-address-extension"></a><span data-ttu-id="6cdc0-103">Расширение физических адресов</span><span class="sxs-lookup"><span data-stu-id="6cdc0-103">Physical Address Extension</span></span>

<span data-ttu-id="6cdc0-104">Расширение физических адресов (PAE) — это компонент процессора, который позволяет процессорам x86 получать доступ к более чем 4 ГБ физической памяти в поддерживающих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-104">Physical Address Extension (PAE) is a processor feature that enables x86 processors to access more than 4 GB of physical memory on capable versions of Windows.</span></span> <span data-ttu-id="6cdc0-105">Некоторые 32-разрядные версии Windows Server, работающие на системах на базе x86, могут использовать PAE для доступа до 64 ГБ или 128 ГБ физической памяти в зависимости от размера физического адреса процессора.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-105">Certain 32-bit versions of Windows Server running on x86-based systems can use PAE to access up to 64 GB or 128 GB of physical memory, depending on the physical address size of the processor.</span></span> <span data-ttu-id="6cdc0-106">Дополнительные сведения см. в разделе [ограничения памяти для выпусков Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="6cdc0-106">For details, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="6cdc0-107">Архитектуры процессоров Intel Itanium и x64 могут получить доступ к более чем 4 ГБ физической памяти в собственном виде и, следовательно, не предоставляют эквиваленты PAE.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-107">The Intel Itanium and x64 processor architectures can access more than 4 GB of physical memory natively and therefore do not provide the equivalent of PAE.</span></span> <span data-ttu-id="6cdc0-108">PAE используется только в 32-разрядных версиях Windows, работающих в системах на базе x86.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-108">PAE is used only by 32-bit versions of Windows running on x86-based systems.</span></span>

<span data-ttu-id="6cdc0-109">При использовании PAE операционная система перемещается из преобразования линейного адреса из двух уровней в преобразование адресов, сопоставленное с тремя уровнями.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-109">With PAE, the operating system moves from two-level linear address translation to three-level address translation.</span></span> <span data-ttu-id="6cdc0-110">Вместо линейного адреса, разбитого на три отдельных поля для индексирования в таблицах памяти, оно делится на четыре отдельных поля: 2-разрядное битовое значение, 2 9-разрядное битовых полей и 12-разрядное битовое значение, соответствующее размеру страницы, реализованному в архитектуре Intel (4 КБ).</span><span class="sxs-lookup"><span data-stu-id="6cdc0-110">Instead of a linear address being split into three separate fields for indexing into memory tables, it is split into four separate fields: a 2-bit bitfield, two 9-bit bitfields, and a 12-bit bitfield that corresponds to the page size implemented by Intel architecture (4 KB).</span></span> <span data-ttu-id="6cdc0-111">Размер записей в таблице страниц (PTE) и записей каталога страниц (Пдес) в режиме PAE увеличивается с 32 до 64 бит.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-111">The size of page table entries (PTEs) and page directory entries (PDEs) in PAE mode is increased from 32 to 64 bits.</span></span> <span data-ttu-id="6cdc0-112">Дополнительные биты позволяют операционной системе PTE или ПДЕ ссылаться на физическую память свыше 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-112">The additional bits allow an operating system PTE or PDE to reference physical memory above 4 GB.</span></span>

<span data-ttu-id="6cdc0-113">В 32-разрядной системе Windows, работающей в системах на базе x64, PAE также обеспечивает несколько дополнительных функций системы и процессоров, включая [предотвращение выполнения данных](data-execution-prevention.md) с аппаратным обеспечением (DEP), [неоднородный доступ к памяти (NUMA)](../procthread/numa-support.md)и возможность добавлять память в систему во время ее работы (память с горячим добавлением).</span><span class="sxs-lookup"><span data-stu-id="6cdc0-113">In 32-bit Windows running on x64-based systems, PAE also enables several advanced system and processor features, including hardware-enabled [Data Execution Prevention](data-execution-prevention.md) (DEP), [non-uniform memory access (NUMA)](../procthread/numa-support.md), and the ability to add memory to a system while it is running (hot-add memory).</span></span>

<span data-ttu-id="6cdc0-114">PAE не изменяет объем виртуального адресного пространства, доступного процессу.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-114">PAE does not change the amount of virtual address space available to a process.</span></span> <span data-ttu-id="6cdc0-115">Каждый процесс, выполняемый в 32-разрядной версии Windows, по-прежнему ограничен виртуальным адресным пространством размером 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-115">Each process running in 32-bit Windows is still limited to a 4 GB virtual address space.</span></span>

## <a name="system-support-for-pae"></a><span data-ttu-id="6cdc0-116">Системная поддержка PAE</span><span class="sxs-lookup"><span data-stu-id="6cdc0-116">System Support for PAE</span></span>

<span data-ttu-id="6cdc0-117">PAE поддерживается только в следующих 32-разрядных версиях Windows, работающих в системах на базе x86:</span><span class="sxs-lookup"><span data-stu-id="6cdc0-117">PAE is supported only on the following 32-bit versions of Windows running on x86-based systems:</span></span>

-   <span data-ttu-id="6cdc0-118">Windows 7 (только бит 32)</span><span class="sxs-lookup"><span data-stu-id="6cdc0-118">Windows 7 (32 bit only)</span></span>
-   <span data-ttu-id="6cdc0-119">Windows Server 2008 (только 32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="6cdc0-119">Windows Server 2008 (32-bit only)</span></span>
-   <span data-ttu-id="6cdc0-120">Windows Vista (только 32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="6cdc0-120">Windows Vista (32-bit only)</span></span>
-   <span data-ttu-id="6cdc0-121">Windows Server 2003 (только 32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="6cdc0-121">Windows Server 2003 (32-bit only)</span></span>
-   <span data-ttu-id="6cdc0-122">Windows XP (только 32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="6cdc0-122">Windows XP (32-bit only)</span></span>

## <a name="enabling-pae"></a><span data-ttu-id="6cdc0-123">Включение PAE</span><span class="sxs-lookup"><span data-stu-id="6cdc0-123">Enabling PAE</span></span>

<span data-ttu-id="6cdc0-124">Windows автоматически включает PAE, если функция DEP включена на компьютере, поддерживающем DEP с аппаратной поддержкой, или если компьютер настроен для устройств памяти с горячим добавлением в памяти за пределами 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-124">Windows automatically enables PAE if DEP is enabled on a computer that supports hardware-enabled DEP, or if the computer is configured for hot-add memory devices in memory ranges beyond 4 GB.</span></span> <span data-ttu-id="6cdc0-125">Если компьютер не поддерживает DEP, поддерживающий аппаратную поддержку, или не настроен для устройств памяти с горячим добавлением в памяти, превышающих 4 ГБ, PAE необходимо явно включить.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-125">If the computer does not support hardware-enabled DEP or is not configured for hot-add memory devices in memory ranges beyond 4 GB, PAE must be explicitly enabled.</span></span>

<span data-ttu-id="6cdc0-126">Чтобы явно включить PAE, используйте следующую команду [**BCDEdit/Set**](/windows-hardware/drivers/devtest/bcdedit--set) , чтобы задать параметр загрузочной записи **PAE** :</span><span class="sxs-lookup"><span data-stu-id="6cdc0-126">To explicitly enable PAE, use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) command to set the **pae** boot entry option:</span></span>

 <span data-ttu-id="6cdc0-127">**BCDEdit/Set \[ {ID} \] PAE форцеенабле**</span><span class="sxs-lookup"><span data-stu-id="6cdc0-127">**bcdedit /set \[{ID}\] pae ForceEnable**</span></span>  


<span data-ttu-id="6cdc0-128">Если функция DEP включена, PAE невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-128">IF DEP is enabled, PAE cannot be disabled.</span></span> <span data-ttu-id="6cdc0-129">Используйте следующие команды [**BCDEdit/Set**](/windows-hardware/drivers/devtest/bcdedit--set) для отключения DEP и PAE:</span><span class="sxs-lookup"><span data-stu-id="6cdc0-129">Use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) commands to disable both DEP and PAE:</span></span>

 <span data-ttu-id="6cdc0-130">**BCDEdit/Set \[ {ID} \] NX алвайсофф**</span><span class="sxs-lookup"><span data-stu-id="6cdc0-130">**bcdedit /set \[{ID}\] nx AlwaysOff**</span></span>  
<span data-ttu-id="6cdc0-131">**BCDEdit/Set \[ {ID} \] PAE форцедисабле**</span><span class="sxs-lookup"><span data-stu-id="6cdc0-131">**bcdedit /set \[{ID}\] pae ForceDisable**</span></span>  


<span data-ttu-id="6cdc0-132">**Windows Server 2003 и Windows XP:** Чтобы включить PAE, используйте параметр **/PAE** в файле [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) .</span><span class="sxs-lookup"><span data-stu-id="6cdc0-132">**Windows Server 2003 and Windows XP:** To enable PAE, use the **/PAE** switch in the [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) file.</span></span> <span data-ttu-id="6cdc0-133">Чтобы отключить PAE, используйте параметр **/нопае** .</span><span class="sxs-lookup"><span data-stu-id="6cdc0-133">To disable PAE, use the **/NOPAE** switch.</span></span> <span data-ttu-id="6cdc0-134">Чтобы отключить DEP, используйте параметр **/EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="6cdc0-134">To disable DEP, use the **/EXECUTE** switch.</span></span>

## <a name="comparing-pae-and-other-large-memory-support"></a><span data-ttu-id="6cdc0-135">Сравнение PAE и другой поддержки больших объемов памяти</span><span class="sxs-lookup"><span data-stu-id="6cdc0-135">Comparing PAE and other Large Memory Support</span></span>

<span data-ttu-id="6cdc0-136">PAE, [4-Гигабайтная настройка](4-gigabyte-tuning.md) (4GT) и [расширения](address-windowing-extensions.md) AWE служат для разных целей и могут использоваться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-136">PAE, [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT), and [Address Windowing Extensions](address-windowing-extensions.md) (AWE) serve different purposes and can be used independently of each other:</span></span>

-   <span data-ttu-id="6cdc0-137">PAE позволяет операционной системе получать доступ и использовать более 4 ГБ физической памяти.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-137">PAE allows the operating system to access and use more than 4 GB of physical memory.</span></span>
-   <span data-ttu-id="6cdc0-138">4GT увеличивает часть виртуального адресного пространства, доступного для процесса от 2 ГБ до 3 ГБ.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-138">4GT increases the portion of the virtual address space that is available to a process from 2 GB to up to 3 GB.</span></span>
-   <span data-ttu-id="6cdc0-139">Расширения AWE — это набор API-интерфейсов, который позволяет процессу выделить нестраничную физическую память, а затем динамически сопоставлять части этой памяти с виртуальным адресным пространством процесса.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-139">AWE is a set of APIs that allows a process to allocate nonpaged physical memory and then dynamically map portions of this memory into the virtual address space of the process.</span></span>

<span data-ttu-id="6cdc0-140">Если не используются ни 4GT, ни AWE, объем физической памяти, который может использовать один 32-разрядный процесс, ограничен размером его адресного пространства (2 ГБ).</span><span class="sxs-lookup"><span data-stu-id="6cdc0-140">When neither 4GT nor AWE are being used, the amount of physical memory that a single 32-bit process can use is limited by the size of its address space (2 GB).</span></span> <span data-ttu-id="6cdc0-141">В этом случае система, поддерживающая PAE, по-прежнему может использовать более 4 ГБ ОЗУ для одновременного выполнения нескольких процессов или кэширования данных файлов в памяти.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-141">In this case, a PAE-enabled system can still make use of more than 4 GB of RAM to run multiple processes at the same time or to cache file data in memory.</span></span>

<span data-ttu-id="6cdc0-142">4GT можно использовать с PAE или без него.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-142">4GT can be used with or without PAE.</span></span> <span data-ttu-id="6cdc0-143">Однако некоторые версии Windows ограничивают максимальный объем физической памяти, который может поддерживаться при использовании 4GT.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-143">However, some versions of Windows limit the maximum amount of physical memory that can be supported when 4GT is used.</span></span> <span data-ttu-id="6cdc0-144">В таких системах Загрузка с помощью 4GT Enabled приводит к тому, что операционная система будет игнорировать любую память, превышающую ограничение.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-144">On such systems, booting with 4GT enabled causes the operating system to ignore any memory in excess of the limit.</span></span>

<span data-ttu-id="6cdc0-145">AWE не требует PAE или 4GT, но часто используется вместе с PAE, чтобы выделить более 4 ГБ физической памяти из одного 32-разрядного процесса.</span><span class="sxs-lookup"><span data-stu-id="6cdc0-145">AWE does not require PAE or 4GT but is often used together with PAE to allocate more than 4 GB of physical memory from a single 32-bit process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cdc0-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6cdc0-146">Related topics</span></span>



[<span data-ttu-id="6cdc0-147">**испроцессорфеатурепресент**</span><span class="sxs-lookup"><span data-stu-id="6cdc0-147">**IsProcessorFeaturePresent**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

<span data-ttu-id="6cdc0-148">[Техническое руководство по PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6cdc0-148">[PAE X86 Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span></span>
</dt> </dl>

 

 
