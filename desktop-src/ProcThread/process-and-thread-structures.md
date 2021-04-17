---
description: В этом разделе перечислены структуры, которые используются с процессами, потоками, процессорами, объектами заданий и планированием пользовательского режима (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Структуры процессов и потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673750"
---
# <a name="process-and-thread-structures"></a><span data-ttu-id="db02b-103">Структуры процессов и потоков</span><span class="sxs-lookup"><span data-stu-id="db02b-103">Process and Thread Structures</span></span>

<span data-ttu-id="db02b-104">В этом разделе перечислены структуры, которые используются с процессами, потоками, процессорами, объектами заданий и планированием пользовательского режима (UMS).</span><span class="sxs-lookup"><span data-stu-id="db02b-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="db02b-105">Структуры процессов и потоков</span><span class="sxs-lookup"><span data-stu-id="db02b-105">Process and Thread Structures</span></span>

<span data-ttu-id="db02b-106">Для процессов и потоков используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="db02b-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="db02b-107">**\_ \_ сведения о памяти приложения**</span><span class="sxs-lookup"><span data-stu-id="db02b-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="db02b-108">**\_состояние AR**</span><span class="sxs-lookup"><span data-stu-id="db02b-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="db02b-109">**\_дескриптор кэша**</span><span class="sxs-lookup"><span data-stu-id="db02b-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="db02b-110">**Счетчики ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="db02b-111">**\_предпочтения ориентации**</span><span class="sxs-lookup"><span data-stu-id="db02b-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="db02b-112">**пеб**</span><span class="sxs-lookup"><span data-stu-id="db02b-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="db02b-113">**\_данные пеб LDR \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="db02b-114">**\_сведения о процессе**</span><span class="sxs-lookup"><span data-stu-id="db02b-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="db02b-115">**\_ \_ \_ сведения о НЕхватке памяти процесса**</span><span class="sxs-lookup"><span data-stu-id="db02b-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="db02b-116">**\_ \_ Политика ASLR для обработки \_ рисков**</span><span class="sxs-lookup"><span data-stu-id="db02b-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="db02b-117">**\_ \_ Политика двоичной \_ подписи для процесса устранения рисков \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="db02b-118">**\_ \_ \_ \_ Политика защиты потока управления для процесса устранения рисков \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="db02b-119">**\_Политика DEP для устранения рисков \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="db02b-120">**\_ \_ \_ Политика динамического кода для устранения \_ рисков**</span><span class="sxs-lookup"><span data-stu-id="db02b-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="db02b-121">**\_ \_ \_ \_ Политика отключения точки расширения процесса устранения рисков \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="db02b-122">**\_ \_ \_ Политика отключения шрифтов для преодоления процессов \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="db02b-123">**\_ \_ \_ Политика загрузки образа для устранения рисков процесса \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="db02b-124">**\_ \_ Политика проверки ограниченного \_ управления процессами устранения рисков \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="db02b-125">**\_ \_ Политика отключения обработки системных \_ вызовов \_ для устранения рисков \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="db02b-126">**\_Параметры пользовательского \_ процесса \_ RTL**</span><span class="sxs-lookup"><span data-stu-id="db02b-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="db02b-127">**стартупинфо**</span><span class="sxs-lookup"><span data-stu-id="db02b-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="db02b-128">**стартупинфоекс**</span><span class="sxs-lookup"><span data-stu-id="db02b-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="db02b-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="db02b-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="db02b-130">Структуры процессора</span><span class="sxs-lookup"><span data-stu-id="db02b-130">Processor Structures</span></span>

<span data-ttu-id="db02b-131">Для процессоров и групп процессоров используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="db02b-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="db02b-132">**\_связь кэша**</span><span class="sxs-lookup"><span data-stu-id="db02b-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="db02b-133">**\_сходство групп**</span><span class="sxs-lookup"><span data-stu-id="db02b-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="db02b-134">**\_отношение группы**</span><span class="sxs-lookup"><span data-stu-id="db02b-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="db02b-135">**\_отношение узла \_ NUMA**</span><span class="sxs-lookup"><span data-stu-id="db02b-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="db02b-136">**\_сведения о группе процессоров \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="db02b-137">**\_номер процессора**</span><span class="sxs-lookup"><span data-stu-id="db02b-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="db02b-138">**связь ПРОЦЕССОРов \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="db02b-139">**\_ \_ сведения о настройке ЦП системы \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="db02b-140">**\_ \_ сведения о логическом ПРОЦЕССОРе системы \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="db02b-141">**\_ \_ сведения о логическом ПРОЦЕССОРе системы, \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="db02b-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="db02b-142">Структура очереди диспетчера</span><span class="sxs-lookup"><span data-stu-id="db02b-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="db02b-143">Для создания [диспатчеркуеуеконтроллер](/uwp/api/windows.system.dispatcherqueuecontroller)используется следующая структура.</span><span class="sxs-lookup"><span data-stu-id="db02b-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="db02b-144">**диспатчеркуеуеоптионс**</span><span class="sxs-lookup"><span data-stu-id="db02b-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="db02b-145">Структуры объектов заданий</span><span class="sxs-lookup"><span data-stu-id="db02b-145">Job Object Structures</span></span>

<span data-ttu-id="db02b-146">Для объектов заданий используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="db02b-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="db02b-147">**\_ \_ порт завершения привязки \_ жобобжект**</span><span class="sxs-lookup"><span data-stu-id="db02b-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="db02b-148">**ЖОБОБЖЕКТ \_ основные \_ \_ сведения о учете**</span><span class="sxs-lookup"><span data-stu-id="db02b-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="db02b-149">**\_ \_ \_ \_ учетные данные жобобжект Basic и IO \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="db02b-150">**\_ \_ сведения о базовом ОГРАНИЧЕНии жобобжект \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="db02b-151">**\_ \_ \_ список идентификаторов процессов жобобжект Basic \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="db02b-152">**\_базовые \_ ограничения ПОЛЬЗОВАТЕЛЬСКОГО интерфейса \_ жобобжект**</span><span class="sxs-lookup"><span data-stu-id="db02b-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="db02b-153">**ЖОБОБЖЕКТ \_ конец \_ \_ \_ сведений о времени выполнения задания \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="db02b-154">**\_ \_ сведения о расширенном ОГРАНИЧЕНии жобобжект \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="db02b-155">**\_ \_ сведения об ограничении безопасности жобобжект \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="db02b-156">Структуры планирования User-Mode</span><span class="sxs-lookup"><span data-stu-id="db02b-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="db02b-157">С UMS используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="db02b-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="db02b-158">**\_Создание \_ атрибутов потока \_ для UMS**</span><span class="sxs-lookup"><span data-stu-id="db02b-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="db02b-159">**\_ \_ сведения о запуске ПЛАНИРОВЩИКа UMS \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="db02b-160">**\_ \_ сведения о системном ПОТОКе UMS \_**</span><span class="sxs-lookup"><span data-stu-id="db02b-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
