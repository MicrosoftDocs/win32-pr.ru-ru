---
title: Поставщики систем
description: Включите события поставщика трассировки системы с помощью EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387817"
---
# <a name="system-providers"></a><span data-ttu-id="47000-103">Поставщики систем</span><span class="sxs-lookup"><span data-stu-id="47000-103">System Providers</span></span>
 
<span data-ttu-id="47000-104">Начиная с Windows 10 SDK Build 20348 события поставщика трассировки системы могут быть включены так же, как другие поставщики ETW с [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span><span class="sxs-lookup"><span data-stu-id="47000-104">Beginning in Windows 10 SDK build 20348, the System Trace Provider's events can be enabled in the same way that other ETW providers are, with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span></span>  <span data-ttu-id="47000-105">Различные флаги и [маски групп](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , связанные с системным поставщиком трассировки, были сопоставлены с новыми поставщиками трассировки, называемыми поставщиками систем, и совпадающими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="47000-105">The different flags and [group masks](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associated with the System Trace Provider have been mapped to new trace providers, called System Providers, and matching keywords.</span></span>  
 
<span data-ttu-id="47000-106">Как и непосредственное включение поставщика трассировки системы, поставщики систем можно включить только с помощью сеанса с набором [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) .</span><span class="sxs-lookup"><span data-stu-id="47000-106">Like enabling the System Trace Provider directly, the System Providers can only be enabled by a session with the [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) set.</span></span>

## <a name="system-provider-reference"></a><span data-ttu-id="47000-107">Справочник по поставщику систем</span><span class="sxs-lookup"><span data-stu-id="47000-107">System Provider reference</span></span>

* [<span data-ttu-id="47000-108">Поставщик System ALPC</span><span class="sxs-lookup"><span data-stu-id="47000-108">System ALPC Provider</span></span>](#system-alpc-provider)
* [<span data-ttu-id="47000-109">Поставщик системных конфигураций</span><span class="sxs-lookup"><span data-stu-id="47000-109">System Config Provider</span></span>](#system-config-provider)
* [<span data-ttu-id="47000-110">Поставщик системных ЦП</span><span class="sxs-lookup"><span data-stu-id="47000-110">System CPU Provider</span></span>](#system-cpu-provider)
* [<span data-ttu-id="47000-111">Поставщик низкоуровневой оболочки системы</span><span class="sxs-lookup"><span data-stu-id="47000-111">System Hypervisor Provider</span></span>](#system-hypervisor-provider)
* [<span data-ttu-id="47000-112">Поставщик системных прерываний</span><span class="sxs-lookup"><span data-stu-id="47000-112">System Interrupt Provider</span></span>](#system-interrupt-provider)
* [<span data-ttu-id="47000-113">Поставщик системных операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="47000-113">System IO Provider</span></span>](#system-io-provider)
* [<span data-ttu-id="47000-114">Поставщик фильтра ввода-вывода системы</span><span class="sxs-lookup"><span data-stu-id="47000-114">System IO Filter Provider</span></span>](#system-io-filter-provider)
* [<span data-ttu-id="47000-115">Поставщик блокировки системы</span><span class="sxs-lookup"><span data-stu-id="47000-115">System Lock Provider</span></span>](#system-lock-provider)
* [<span data-ttu-id="47000-116">Поставщик системной памяти</span><span class="sxs-lookup"><span data-stu-id="47000-116">System Memory Provider</span></span>](#system-memory-provider)
* [<span data-ttu-id="47000-117">Поставщик системных объектов</span><span class="sxs-lookup"><span data-stu-id="47000-117">System Object Provider</span></span>](#system-object-provider)
* [<span data-ttu-id="47000-118">Системный поставщик питания</span><span class="sxs-lookup"><span data-stu-id="47000-118">System Power Provider</span></span>](#system-power-provider)
* [<span data-ttu-id="47000-119">Поставщик системных процессов</span><span class="sxs-lookup"><span data-stu-id="47000-119">System Process Provider</span></span>](#system-process-provider)
* [<span data-ttu-id="47000-120">Поставщик системного профиля</span><span class="sxs-lookup"><span data-stu-id="47000-120">System Profile Provider</span></span>](#system-profile-provider)
* [<span data-ttu-id="47000-121">Поставщик системного реестра</span><span class="sxs-lookup"><span data-stu-id="47000-121">System Registry Provider</span></span>](#system-registry-provider)
* [<span data-ttu-id="47000-122">Поставщик системного планировщика</span><span class="sxs-lookup"><span data-stu-id="47000-122">System Scheduler Provider</span></span>](#system-scheduler-provider)
* [<span data-ttu-id="47000-123">Системный поставщик syscall</span><span class="sxs-lookup"><span data-stu-id="47000-123">System Syscall Provider</span></span>](#system-syscall-provider)
* [<span data-ttu-id="47000-124">Поставщик системного таймера</span><span class="sxs-lookup"><span data-stu-id="47000-124">System Timer Provider</span></span>](#system-timer-provider)
 
### <a name="system-alpc-provider"></a><span data-ttu-id="47000-125">Поставщик System ALPC</span><span class="sxs-lookup"><span data-stu-id="47000-125">System ALPC Provider</span></span>

<span data-ttu-id="47000-126">Предоставляет события, связанные с системой ALPC.</span><span class="sxs-lookup"><span data-stu-id="47000-126">Provides events related to the ALPC system.</span></span>

<span data-ttu-id="47000-127">GUID: Системалпкпровидергуид {fcb9baaf-E529-4980-92e9-ced1a6aadfdf}</span><span class="sxs-lookup"><span data-stu-id="47000-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span></span>

| <span data-ttu-id="47000-128">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-128">Keyword</span></span> | <span data-ttu-id="47000-129">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-129">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-130">SYSTEM_ALPC_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-130">SYSTEM_ALPC_KW_GENERAL</span></span> | <span data-ttu-id="47000-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span><span class="sxs-lookup"><span data-stu-id="47000-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span></span> |
 
### <a name="system-config-provider"></a><span data-ttu-id="47000-132">Поставщик системных конфигураций</span><span class="sxs-lookup"><span data-stu-id="47000-132">System Config Provider</span></span> 

<span data-ttu-id="47000-133">Предоставляет события конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="47000-133">Provides system configuration events.</span></span>

<span data-ttu-id="47000-134">GUID: Системконфигпровидергуид {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span><span class="sxs-lookup"><span data-stu-id="47000-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span></span>

| <span data-ttu-id="47000-135">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-135">Keyword</span></span> | <span data-ttu-id="47000-136">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-136">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-137">SYSTEM_CONFIG_KW_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="47000-137">SYSTEM_CONFIG_KW_SYSTEM</span></span> | <span data-ttu-id="47000-138">PERF_SYSCFG_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="47000-138">PERF_SYSCFG_SYSTEM</span></span> |
| <span data-ttu-id="47000-139">SYSTEM_CONFIG_KW_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="47000-139">SYSTEM_CONFIG_KW_GRAPHICS</span></span> | <span data-ttu-id="47000-140">PERF_SYSCFG_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="47000-140">PERF_SYSCFG_GRAPHICS</span></span> |
| <span data-ttu-id="47000-141">SYSTEM_CONFIG_KW_STORAGE</span><span class="sxs-lookup"><span data-stu-id="47000-141">SYSTEM_CONFIG_KW_STORAGE</span></span> | <span data-ttu-id="47000-142">PERF_SYSCFG_STORAGE</span><span class="sxs-lookup"><span data-stu-id="47000-142">PERF_SYSCFG_STORAGE</span></span> |
| <span data-ttu-id="47000-143">SYSTEM_CONFIG_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="47000-143">SYSTEM_CONFIG_KW_NETWORK</span></span> | <span data-ttu-id="47000-144">PERF_SYSCFG_NETWORK</span><span class="sxs-lookup"><span data-stu-id="47000-144">PERF_SYSCFG_NETWORK</span></span> |
| <span data-ttu-id="47000-145">SYSTEM_CONFIG_KW_SERVICES</span><span class="sxs-lookup"><span data-stu-id="47000-145">SYSTEM_CONFIG_KW_SERVICES</span></span> | <span data-ttu-id="47000-146">PERF_SYSCFG_SERVICES</span><span class="sxs-lookup"><span data-stu-id="47000-146">PERF_SYSCFG_SERVICES</span></span> |
| <span data-ttu-id="47000-147">SYSTEM_CONFIG_KW_PNP</span><span class="sxs-lookup"><span data-stu-id="47000-147">SYSTEM_CONFIG_KW_PNP</span></span> | <span data-ttu-id="47000-148">PERF_SYSCFG_PNP</span><span class="sxs-lookup"><span data-stu-id="47000-148">PERF_SYSCFG_PNP</span></span> |
| <span data-ttu-id="47000-149">SYSTEM_CONFIG_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="47000-149">SYSTEM_CONFIG_KW_OPTICAL</span></span> | <span data-ttu-id="47000-150">PERF_SYSCFG_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="47000-150">PERF_SYSCFG_OPTICAL</span></span> |
 
### <a name="system-cpu-provider"></a><span data-ttu-id="47000-151">Поставщик системных ЦП</span><span class="sxs-lookup"><span data-stu-id="47000-151">System CPU Provider</span></span> 

<span data-ttu-id="47000-152">Предоставляет события, связанные с ЦП.</span><span class="sxs-lookup"><span data-stu-id="47000-152">Provides events related to the CPU.</span></span>

<span data-ttu-id="47000-153">GUID: Системкпупровидергуид {c6c5265f-eae8-4650-AAE4-9d48603d8510}</span><span class="sxs-lookup"><span data-stu-id="47000-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span></span>

| <span data-ttu-id="47000-154">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-154">Keyword</span></span> | <span data-ttu-id="47000-155">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-155">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-156">SYSTEM_CPU_KW_CONFIG</span><span class="sxs-lookup"><span data-stu-id="47000-156">SYSTEM_CPU_KW_CONFIG</span></span> | <span data-ttu-id="47000-157">PERF_CPU_CONFIG</span><span class="sxs-lookup"><span data-stu-id="47000-157">PERF_CPU_CONFIG</span></span> |
| <span data-ttu-id="47000-158">SYSTEM_CPU_KW_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="47000-158">SYSTEM_CPU_KW_CACHE_FLUSH</span></span> | <span data-ttu-id="47000-159">PERF_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="47000-159">PERF_CACHE_FLUSH</span></span> |
| <span data-ttu-id="47000-160">SYSTEM_CPU_KW_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="47000-160">SYSTEM_CPU_KW_SPEC_CONTROL</span></span> | <span data-ttu-id="47000-161">PERF_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="47000-161">PERF_SPEC_CONTROL</span></span> |
 
### <a name="system-hypervisor-provider"></a><span data-ttu-id="47000-162">Поставщик низкоуровневой оболочки системы</span><span class="sxs-lookup"><span data-stu-id="47000-162">System Hypervisor Provider</span></span> 

<span data-ttu-id="47000-163">Предоставляет события, связанные с гипервизором.</span><span class="sxs-lookup"><span data-stu-id="47000-163">Provides events relating to the hypervisor.</span></span>

<span data-ttu-id="47000-164">GUID: Системхипервисорпровидергуид {bafa072a-918a-4bed-B622-bc152097098f}</span><span class="sxs-lookup"><span data-stu-id="47000-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span></span>

| <span data-ttu-id="47000-165">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-165">Keyword</span></span> | <span data-ttu-id="47000-166">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-166">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-167">SYSTEM_HYPERVISOR_KW_PROFILE</span><span class="sxs-lookup"><span data-stu-id="47000-167">SYSTEM_HYPERVISOR_KW_PROFILE</span></span> | <span data-ttu-id="47000-168">PERF_HV_PROFILE</span><span class="sxs-lookup"><span data-stu-id="47000-168">PERF_HV_PROFILE</span></span> |
| <span data-ttu-id="47000-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="47000-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span></span> | <span data-ttu-id="47000-170">PERF_HV_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="47000-170">PERF_HV_CALLOUTS</span></span> |
| <span data-ttu-id="47000-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="47000-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span></span> | <span data-ttu-id="47000-172">PERF_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="47000-172">PERF_VTL_CHANGE</span></span> |
 
### <a name="system-interrupt-provider"></a><span data-ttu-id="47000-173">Поставщик системных прерываний</span><span class="sxs-lookup"><span data-stu-id="47000-173">System Interrupt Provider</span></span> 

<span data-ttu-id="47000-174">Предоставляет события, связанные с DPC и прерываниями.</span><span class="sxs-lookup"><span data-stu-id="47000-174">Provides events relating to DPCs and interrupts.</span></span>

<span data-ttu-id="47000-175">GUID: Системинтерруптпровидергуид {d4bbee17-b545-4888-858b-744169015b25}</span><span class="sxs-lookup"><span data-stu-id="47000-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span></span>

| <span data-ttu-id="47000-176">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-176">Keyword</span></span> | <span data-ttu-id="47000-177">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-177">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-178">SYSTEM_INTERRUPT_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-178">SYSTEM_INTERRUPT_KW_GENERAL</span></span> | <span data-ttu-id="47000-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="47000-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span></span> |
| <span data-ttu-id="47000-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="47000-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span></span> | <span data-ttu-id="47000-181">PERF_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="47000-181">PERF_CLOCK_INTERRUPT</span></span> |
| <span data-ttu-id="47000-182">SYSTEM_INTERRUPT_KW_DPC</span><span class="sxs-lookup"><span data-stu-id="47000-182">SYSTEM_INTERRUPT_KW_DPC</span></span> | <span data-ttu-id="47000-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span><span class="sxs-lookup"><span data-stu-id="47000-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span></span> |
| <span data-ttu-id="47000-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="47000-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span></span> | <span data-ttu-id="47000-185">PERF_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="47000-185">PERF_DPC_QUEUE</span></span> |
| <span data-ttu-id="47000-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="47000-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span></span> | <span data-ttu-id="47000-187">PERF_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="47000-187">PERF_WDF_DPC</span></span> |
| <span data-ttu-id="47000-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="47000-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span></span> | <span data-ttu-id="47000-189">PERF_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="47000-189">PERF_WDF_INTERRUPT</span></span> |
| <span data-ttu-id="47000-190">SYSTEM_INTERRUPT_KW_IPI</span><span class="sxs-lookup"><span data-stu-id="47000-190">SYSTEM_INTERRUPT_KW_IPI</span></span> | <span data-ttu-id="47000-191">PERF_IPI</span><span class="sxs-lookup"><span data-stu-id="47000-191">PERF_IPI</span></span> |
 
 
### <a name="system-io-provider"></a><span data-ttu-id="47000-192">Поставщик системных операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="47000-192">System IO Provider</span></span> 

<span data-ttu-id="47000-193">Предоставляет события, связанные с несколькими типами операций ввода-вывода, включая диск, кэш и сеть.</span><span class="sxs-lookup"><span data-stu-id="47000-193">Provides events relating to multiple kinds of IO including disk, cache, and network.</span></span>

<span data-ttu-id="47000-194">GUID: Системиопровидергуид {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span><span class="sxs-lookup"><span data-stu-id="47000-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span></span>

| <span data-ttu-id="47000-195">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-195">Keyword</span></span> | <span data-ttu-id="47000-196">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-196">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-197">SYSTEM_IO_KW_DISK</span><span class="sxs-lookup"><span data-stu-id="47000-197">SYSTEM_IO_KW_DISK</span></span> | <span data-ttu-id="47000-198">EVENT_TRACE_FLAG_DISK_IO</span><span class="sxs-lookup"><span data-stu-id="47000-198">EVENT_TRACE_FLAG_DISK_IO</span></span> |
| <span data-ttu-id="47000-199">SYSTEM_IO_KW_DISK_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-199">SYSTEM_IO_KW_DISK_INIT</span></span> | <span data-ttu-id="47000-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span></span> |
| <span data-ttu-id="47000-201">SYSTEM_IO_KW_FILENAME</span><span class="sxs-lookup"><span data-stu-id="47000-201">SYSTEM_IO_KW_FILENAME</span></span> | <span data-ttu-id="47000-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="47000-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span></span> |
| <span data-ttu-id="47000-203">SYSTEM_IO_KW_SPLIT</span><span class="sxs-lookup"><span data-stu-id="47000-203">SYSTEM_IO_KW_SPLIT</span></span> | <span data-ttu-id="47000-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span><span class="sxs-lookup"><span data-stu-id="47000-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span></span> |
| <span data-ttu-id="47000-205">SYSTEM_IO_KW_FILE</span><span class="sxs-lookup"><span data-stu-id="47000-205">SYSTEM_IO_KW_FILE</span></span> | <span data-ttu-id="47000-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="47000-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span></span> |
| <span data-ttu-id="47000-207">SYSTEM_IO_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="47000-207">SYSTEM_IO_KW_OPTICAL</span></span> | <span data-ttu-id="47000-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span></span> |
| <span data-ttu-id="47000-209">SYSTEM_IO_KW_OPTICAL_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-209">SYSTEM_IO_KW_OPTICAL_INIT</span></span> | <span data-ttu-id="47000-210">PERF_OPTICAL_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-210">PERF_OPTICAL_IO_INIT</span></span> |
| <span data-ttu-id="47000-211">SYSTEM_IO_KW_DRIVERS</span><span class="sxs-lookup"><span data-stu-id="47000-211">SYSTEM_IO_KW_DRIVERS</span></span> | <span data-ttu-id="47000-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span><span class="sxs-lookup"><span data-stu-id="47000-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span></span> |
| <span data-ttu-id="47000-213">SYSTEM_IO_KW_CC</span><span class="sxs-lookup"><span data-stu-id="47000-213">SYSTEM_IO_KW_CC</span></span> | <span data-ttu-id="47000-214">PERF_CC</span><span class="sxs-lookup"><span data-stu-id="47000-214">PERF_CC</span></span> |
| <span data-ttu-id="47000-215">SYSTEM_IO_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="47000-215">SYSTEM_IO_KW_NETWORK</span></span> | <span data-ttu-id="47000-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span><span class="sxs-lookup"><span data-stu-id="47000-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span></span> |

<span data-ttu-id="47000-217">Примечание. Включение ключевого слова SYSTEM_IO_KW_DRIVERS автоматически включит SYSTEM_IO_KW_FILENAME.</span><span class="sxs-lookup"><span data-stu-id="47000-217">Note: Enabling the SYSTEM_IO_KW_DRIVERS keyword will automatically enable SYSTEM_IO_KW_FILENAME as well.</span></span>  <span data-ttu-id="47000-218">SYSTEM_IO_KW_FILENAME также автоматически включается при включении поставщика системной памяти с ключевым словом SYSTEM_MEMORY_KW_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="47000-218">The SYSTEM_IO_KW_FILENAME is also automatically turned on when the System Memory Provider is enabled with the SYSTEM_MEMORY_KW_MEMORY keyword.</span></span>
 
### <a name="system-io-filter-provider"></a><span data-ttu-id="47000-219">Поставщик фильтра ввода-вывода системы</span><span class="sxs-lookup"><span data-stu-id="47000-219">System IO Filter Provider</span></span> 

<span data-ttu-id="47000-220">Предоставляет события, связанные с фильтрацией операций ввода-вывода, включая время и сбои.</span><span class="sxs-lookup"><span data-stu-id="47000-220">Provides events related to IO filtering including timing and failures.</span></span>

<span data-ttu-id="47000-221">GUID: Системиофилтерпровидергуид {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span><span class="sxs-lookup"><span data-stu-id="47000-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span></span>

| <span data-ttu-id="47000-222">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-222">Keyword</span></span> | <span data-ttu-id="47000-223">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-223">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-224">SYSTEM_IOFILTER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-224">SYSTEM_IOFILTER_KW_GENERAL</span></span> | <span data-ttu-id="47000-225">PERF_FLT_IO</span><span class="sxs-lookup"><span data-stu-id="47000-225">PERF_FLT_IO</span></span> |
| <span data-ttu-id="47000-226">SYSTEM_IOFILTER_KW_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-226">SYSTEM_IOFILTER_KW_INIT</span></span> | <span data-ttu-id="47000-227">PERF_FLT_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="47000-227">PERF_FLT_IO_INIT</span></span> |
| <span data-ttu-id="47000-228">SYSTEM_IOFILTER_KW_FASTIO</span><span class="sxs-lookup"><span data-stu-id="47000-228">SYSTEM_IOFILTER_KW_FASTIO</span></span> | <span data-ttu-id="47000-229">PERF_FLT_FASTIO</span><span class="sxs-lookup"><span data-stu-id="47000-229">PERF_FLT_FASTIO</span></span> |
| <span data-ttu-id="47000-230">SYSTEM_IOFILTER_KW_FAILURE</span><span class="sxs-lookup"><span data-stu-id="47000-230">SYSTEM_IOFILTER_KW_FAILURE</span></span> | <span data-ttu-id="47000-231">PERF_FLT_IO_FAILURE</span><span class="sxs-lookup"><span data-stu-id="47000-231">PERF_FLT_IO_FAILURE</span></span> |
 
### <a name="system-lock-provider"></a><span data-ttu-id="47000-232">Поставщик блокировки системы</span><span class="sxs-lookup"><span data-stu-id="47000-232">System Lock Provider</span></span> 

<span data-ttu-id="47000-233">Предоставляет события, относящиеся к механизмам блокировки ядра.</span><span class="sxs-lookup"><span data-stu-id="47000-233">Provides events relating to kernel locking mechanisms.</span></span>

<span data-ttu-id="47000-234">GUID: Системлоккпровидергуид {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span><span class="sxs-lookup"><span data-stu-id="47000-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span></span>

| <span data-ttu-id="47000-235">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-235">Keyword</span></span> | <span data-ttu-id="47000-236">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-236">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-237">SYSTEM_LOCK_KW_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="47000-237">SYSTEM_LOCK_KW_SPINLOCK</span></span> | <span data-ttu-id="47000-238">PERF_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="47000-238">PERF_SPINLOCK</span></span> |
| <span data-ttu-id="47000-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="47000-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span></span> | <span data-ttu-id="47000-240">PERF_SPINLOCK_CNTRS</span><span class="sxs-lookup"><span data-stu-id="47000-240">PERF_SPINLOCK_CNTRS</span></span> |
| <span data-ttu-id="47000-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="47000-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span></span> | <span data-ttu-id="47000-242">PERF_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="47000-242">PERF_SYNC_OBJECTS</span></span> |
 
### <a name="system-memory-provider"></a><span data-ttu-id="47000-243">Поставщик системной памяти</span><span class="sxs-lookup"><span data-stu-id="47000-243">System Memory Provider</span></span> 

<span data-ttu-id="47000-244">Предоставляет события, относящиеся к диспетчеру памяти.</span><span class="sxs-lookup"><span data-stu-id="47000-244">Provides events relating to the memory manager.</span></span>

<span data-ttu-id="47000-245">GUID: Системмеморипровидергуид {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span><span class="sxs-lookup"><span data-stu-id="47000-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span></span>

| <span data-ttu-id="47000-246">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-246">Keyword</span></span> | <span data-ttu-id="47000-247">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-247">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-248">SYSTEM_MEMORY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-248">SYSTEM_MEMORY_KW_GENERAL</span></span> | <span data-ttu-id="47000-249">PERF_MEMORY</span><span class="sxs-lookup"><span data-stu-id="47000-249">PERF_MEMORY</span></span> |
| <span data-ttu-id="47000-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="47000-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span></span> | <span data-ttu-id="47000-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="47000-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span></span> |
| <span data-ttu-id="47000-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span><span class="sxs-lookup"><span data-stu-id="47000-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span></span> | <span data-ttu-id="47000-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span><span class="sxs-lookup"><span data-stu-id="47000-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span></span> |
| <span data-ttu-id="47000-254">SYSTEM_MEMORY_KW_POOL</span><span class="sxs-lookup"><span data-stu-id="47000-254">SYSTEM_MEMORY_KW_POOL</span></span> | <span data-ttu-id="47000-255">PERF_POOL</span><span class="sxs-lookup"><span data-stu-id="47000-255">PERF_POOL</span></span> |
| <span data-ttu-id="47000-256">SYSTEM_MEMORY_KW_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="47000-256">SYSTEM_MEMORY_KW_MEMINFO</span></span> | <span data-ttu-id="47000-257">PERF_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="47000-257">PERF_MEMINFO</span></span> |
| <span data-ttu-id="47000-258">SYSTEM_MEMORY_KW_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="47000-258">SYSTEM_MEMORY_KW_PFSECTION</span></span> | <span data-ttu-id="47000-259">PERF_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="47000-259">PERF_PFSECTION</span></span> |
| <span data-ttu-id="47000-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="47000-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span></span> | <span data-ttu-id="47000-261">PERF_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="47000-261">PERF_MEMINFO_WS</span></span> |
| <span data-ttu-id="47000-262">SYSTEM_MEMORY_KW_HEAP</span><span class="sxs-lookup"><span data-stu-id="47000-262">SYSTEM_MEMORY_KW_HEAP</span></span> | <span data-ttu-id="47000-263">PERF_HEAP</span><span class="sxs-lookup"><span data-stu-id="47000-263">PERF_HEAP</span></span> |
| <span data-ttu-id="47000-264">SYSTEM_MEMORY_KW_WS</span><span class="sxs-lookup"><span data-stu-id="47000-264">SYSTEM_MEMORY_KW_WS</span></span> | <span data-ttu-id="47000-265">PERF_WS</span><span class="sxs-lookup"><span data-stu-id="47000-265">PERF_WS</span></span> |
| <span data-ttu-id="47000-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="47000-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span></span> | <span data-ttu-id="47000-267">PERF_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="47000-267">PERF_CONTMEM_GEN</span></span> |
| <span data-ttu-id="47000-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="47000-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span></span> | <span data-ttu-id="47000-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="47000-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span></span> |
| <span data-ttu-id="47000-270">SYSTEM_MEMORY_KW_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="47000-270">SYSTEM_MEMORY_KW_FOOTPRINT</span></span> | <span data-ttu-id="47000-271">PERF_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="47000-271">PERF_FOOTPRINT</span></span> |
| <span data-ttu-id="47000-272">SYSTEM_MEMORY_KW_SESSION</span><span class="sxs-lookup"><span data-stu-id="47000-272">SYSTEM_MEMORY_KW_SESSION</span></span> | <span data-ttu-id="47000-273">PERF_SESSION</span><span class="sxs-lookup"><span data-stu-id="47000-273">PERF_SESSION</span></span> |
| <span data-ttu-id="47000-274">SYSTEM_MEMORY_KW_REFSET</span><span class="sxs-lookup"><span data-stu-id="47000-274">SYSTEM_MEMORY_KW_REFSET</span></span> | <span data-ttu-id="47000-275">PERF_REFSET</span><span class="sxs-lookup"><span data-stu-id="47000-275">PERF_REFSET</span></span> |
| <span data-ttu-id="47000-276">SYSTEM_MEMORY_KW_VAMAP</span><span class="sxs-lookup"><span data-stu-id="47000-276">SYSTEM_MEMORY_KW_VAMAP</span></span> | <span data-ttu-id="47000-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span><span class="sxs-lookup"><span data-stu-id="47000-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span></span> |

<span data-ttu-id="47000-278">Примечания.</span><span class="sxs-lookup"><span data-stu-id="47000-278">Notes:</span></span> 
* <span data-ttu-id="47000-279">Включение ключевого слова SYSTEM_MEMORY_KW_MEMORY автоматически включит SYSTEM_IO_KW_FILENAME в системном поставщике ввода и вывода.</span><span class="sxs-lookup"><span data-stu-id="47000-279">Enabling the SYSTEM_MEMORY_KW_MEMORY keyword will automatically enable SYSTEM_IO_KW_FILENAME on the System IO Provider as well.</span></span>
* <span data-ttu-id="47000-280">События, включенные SYSTEM_MEMORY_KW_POOL, поддерживают фильтр тегов пула, чтобы выборочно записывать события только для определенных тегов пула.</span><span class="sxs-lookup"><span data-stu-id="47000-280">The events enabled by the SYSTEM_MEMORY_KW_POOL support a Pool Tag Filter, to selectively write events only for certain pool tags.</span></span>  <span data-ttu-id="47000-281">Он настраивается в качестве [фильтра схематизированных](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) для поставщика системной памяти.</span><span class="sxs-lookup"><span data-stu-id="47000-281">This is configured as a [Schematized Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) on the System Memory Provider.</span></span>  <span data-ttu-id="47000-282">Фильтр Пултаг создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="47000-282">The PoolTag filter is constructed as follows:</span></span>

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* <span data-ttu-id="47000-283">[EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) должны быть инициализированы с идентификатором, имеющим значение SYSTEM_MEMORY_POOL_FILTER_ID, а поле Size — размером заголовка и используемой части массива пултагс.</span><span class="sxs-lookup"><span data-stu-id="47000-283">The [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) should be initialized with Id set to SYSTEM_MEMORY_POOL_FILTER_ID and the size field set to the size of Header plus the used portion of the PoolTags array.</span></span>  

* <span data-ttu-id="47000-284">Каждый тег пула — это 4-символьная строка, которая хранится в фильтре в виде ULONG.</span><span class="sxs-lookup"><span data-stu-id="47000-284">Each Pool Tag is a 4 character string that is stored as a ULONG in the filter.</span></span>  
 
 
### <a name="system-object-provider"></a><span data-ttu-id="47000-285">Поставщик системных объектов</span><span class="sxs-lookup"><span data-stu-id="47000-285">System Object Provider</span></span> 

<span data-ttu-id="47000-286">Предоставляет события, относящиеся к диспетчеру объектов.</span><span class="sxs-lookup"><span data-stu-id="47000-286">Provides events relating to the Object Manager.</span></span>

<span data-ttu-id="47000-287">GUID: Системобжектпровидергуид {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span><span class="sxs-lookup"><span data-stu-id="47000-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span></span>

| <span data-ttu-id="47000-288">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-288">Keyword</span></span> | <span data-ttu-id="47000-289">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-289">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-290">SYSTEM_OBJECT_KW_HANDLE</span><span class="sxs-lookup"><span data-stu-id="47000-290">SYSTEM_OBJECT_KW_HANDLE</span></span> | <span data-ttu-id="47000-291">PERF_OB_HANDLE</span><span class="sxs-lookup"><span data-stu-id="47000-291">PERF_OB_HANDLE</span></span> |
| <span data-ttu-id="47000-292">SYSTEM_OBJECT_KW_OBJECT</span><span class="sxs-lookup"><span data-stu-id="47000-292">SYSTEM_OBJECT_KW_OBJECT</span></span> | <span data-ttu-id="47000-293">PERF_OB_OBJECT</span><span class="sxs-lookup"><span data-stu-id="47000-293">PERF_OB_OBJECT</span></span> |
 
### <a name="system-power-provider"></a><span data-ttu-id="47000-294">Системный поставщик питания</span><span class="sxs-lookup"><span data-stu-id="47000-294">System Power Provider</span></span> 

<span data-ttu-id="47000-295">Предоставляет события, относящиеся к системному состоянию питания.</span><span class="sxs-lookup"><span data-stu-id="47000-295">Provides events relating to the system's power state.</span></span>

<span data-ttu-id="47000-296">GUID: Системповерпровидергуид {c134884a-32d5-4488-80e5-14ed7abb8269}</span><span class="sxs-lookup"><span data-stu-id="47000-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span></span>

| <span data-ttu-id="47000-297">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-297">Keyword</span></span> | <span data-ttu-id="47000-298">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-298">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-299">SYSTEM_POWER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-299">SYSTEM_POWER_KW_GENERAL</span></span> | <span data-ttu-id="47000-300">PERF_POWER</span><span class="sxs-lookup"><span data-stu-id="47000-300">PERF_POWER</span></span> |
| <span data-ttu-id="47000-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="47000-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span></span> | <span data-ttu-id="47000-302">PERF_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="47000-302">PERF_HIBER_RUNDOWN</span></span> |
| <span data-ttu-id="47000-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="47000-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span></span> | <span data-ttu-id="47000-304">PERF_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="47000-304">PERF_PROCESSOR_IDLE</span></span> |
| <span data-ttu-id="47000-305">SYSTEM_POWER_KW_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="47000-305">SYSTEM_POWER_KW_IDLE_SELECTION</span></span> | <span data-ttu-id="47000-306">PERF_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="47000-306">PERF_IDLE_SELECTION</span></span> |
| <span data-ttu-id="47000-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="47000-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span></span> | <span data-ttu-id="47000-308">PERF_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="47000-308">PERF_PPM_EXIT_LATENCY</span></span> |
 
### <a name="system-process-provider"></a><span data-ttu-id="47000-309">Поставщик системных процессов</span><span class="sxs-lookup"><span data-stu-id="47000-309">System Process Provider</span></span> 

<span data-ttu-id="47000-310">Предоставляет события, связанные с процессом, включая сведения о времени существования, событиях загрузки изображения и событиях, связанных с потоком.</span><span class="sxs-lookup"><span data-stu-id="47000-310">Provides events relating to the process, including lifetime information, image load events, and thread related events.</span></span>

<span data-ttu-id="47000-311">GUID: Системпроцесспровидергуид {151f55dc-467d-471f-83b5-5f889d46ff66}</span><span class="sxs-lookup"><span data-stu-id="47000-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span></span>

| <span data-ttu-id="47000-312">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-312">Keyword</span></span> | <span data-ttu-id="47000-313">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-313">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-314">SYSTEM_PROCESS_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-314">SYSTEM_PROCESS_KW_GENERAL</span></span> | <span data-ttu-id="47000-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span><span class="sxs-lookup"><span data-stu-id="47000-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span></span> |
| <span data-ttu-id="47000-316">SYSTEM_PROCESS_KW_INSWAP</span><span class="sxs-lookup"><span data-stu-id="47000-316">SYSTEM_PROCESS_KW_INSWAP</span></span> | <span data-ttu-id="47000-317">PERF_PROCESS_INSWAP</span><span class="sxs-lookup"><span data-stu-id="47000-317">PERF_PROCESS_INSWAP</span></span> |
| <span data-ttu-id="47000-318">SYSTEM_PROCESS_KW_FREEZE</span><span class="sxs-lookup"><span data-stu-id="47000-318">SYSTEM_PROCESS_KW_FREEZE</span></span> | <span data-ttu-id="47000-319">PERF_PROCESS_FREEZE</span><span class="sxs-lookup"><span data-stu-id="47000-319">PERF_PROCESS_FREEZE</span></span> |
| <span data-ttu-id="47000-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span><span class="sxs-lookup"><span data-stu-id="47000-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span></span> | <span data-ttu-id="47000-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="47000-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span></span> |
| <span data-ttu-id="47000-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="47000-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span></span> | <span data-ttu-id="47000-323">PERF_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="47000-323">PERF_WAKE_COUNTER</span></span> |
| <span data-ttu-id="47000-324">SYSTEM_PROCESS_KW_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="47000-324">SYSTEM_PROCESS_KW_WAKE_DROP</span></span> | <span data-ttu-id="47000-325">PERF_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="47000-325">PERF_WAKE_DROP</span></span> |
| <span data-ttu-id="47000-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="47000-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span></span> | <span data-ttu-id="47000-327">PERF_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="47000-327">PERF_WAKE_EVENT</span></span> |
| <span data-ttu-id="47000-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="47000-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span></span> | <span data-ttu-id="47000-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="47000-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span></span> |
| <span data-ttu-id="47000-330">SYSTEM_PROCESS_KW_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="47000-330">SYSTEM_PROCESS_KW_DBGPRINT</span></span> | <span data-ttu-id="47000-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="47000-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span></span> |
| <span data-ttu-id="47000-332">SYSTEM_PROCESS_KW_JOB</span><span class="sxs-lookup"><span data-stu-id="47000-332">SYSTEM_PROCESS_KW_JOB</span></span> | <span data-ttu-id="47000-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span><span class="sxs-lookup"><span data-stu-id="47000-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span></span> |
| <span data-ttu-id="47000-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="47000-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span></span> | <span data-ttu-id="47000-335">PERF_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="47000-335">PERF_WORKER_THREAD</span></span> |
| <span data-ttu-id="47000-336">SYSTEM_PROCESS_KW_THREAD</span><span class="sxs-lookup"><span data-stu-id="47000-336">SYSTEM_PROCESS_KW_THREAD</span></span> | <span data-ttu-id="47000-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span><span class="sxs-lookup"><span data-stu-id="47000-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span></span> |
| <span data-ttu-id="47000-338">SYSTEM_PROCESS_KW_LOADER</span><span class="sxs-lookup"><span data-stu-id="47000-338">SYSTEM_PROCESS_KW_LOADER</span></span> | <span data-ttu-id="47000-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span><span class="sxs-lookup"><span data-stu-id="47000-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span></span> |
 
### <a name="system-profile-provider"></a><span data-ttu-id="47000-340">Поставщик системного профиля</span><span class="sxs-lookup"><span data-stu-id="47000-340">System Profile Provider</span></span> 

<span data-ttu-id="47000-341">Предоставляет события профилирования.</span><span class="sxs-lookup"><span data-stu-id="47000-341">Provides profiling events.</span></span>

<span data-ttu-id="47000-342">GUID: Системпрофилепровидергуид {bfeb0324-1cee-496f-A409-2ac2b48a6322}</span><span class="sxs-lookup"><span data-stu-id="47000-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span></span>

| <span data-ttu-id="47000-343">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-343">Keyword</span></span> | <span data-ttu-id="47000-344">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-344">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-345">SYSTEM_PROFILE_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-345">SYSTEM_PROFILE_KW_GENERAL</span></span> | <span data-ttu-id="47000-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span><span class="sxs-lookup"><span data-stu-id="47000-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span></span> |
| <span data-ttu-id="47000-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="47000-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span></span> | <span data-ttu-id="47000-348">PERF_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="47000-348">PERF_PMC_PROFILE</span></span> |
 
### <a name="system-registry-provider"></a><span data-ttu-id="47000-349">Поставщик системного реестра</span><span class="sxs-lookup"><span data-stu-id="47000-349">System Registry Provider</span></span> 

<span data-ttu-id="47000-350">Предоставляет события, относящиеся к реестру.</span><span class="sxs-lookup"><span data-stu-id="47000-350">Provides events relating to the registry.</span></span>

<span data-ttu-id="47000-351">GUID: Системрегистрипровидергуид {16156bd9-fab4-4cfa-a232-89d1099058e3}</span><span class="sxs-lookup"><span data-stu-id="47000-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span></span>

| <span data-ttu-id="47000-352">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-352">Keyword</span></span> | <span data-ttu-id="47000-353">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-353">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-354">SYSTEM_REGISTRY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-354">SYSTEM_REGISTRY_KW_GENERAL</span></span> | <span data-ttu-id="47000-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="47000-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span></span> |
| <span data-ttu-id="47000-356">SYSTEM_REGISTRY_KW_HIVE</span><span class="sxs-lookup"><span data-stu-id="47000-356">SYSTEM_REGISTRY_KW_HIVE</span></span> | <span data-ttu-id="47000-357">PERF_REG_HIVE</span><span class="sxs-lookup"><span data-stu-id="47000-357">PERF_REG_HIVE</span></span> |
| <span data-ttu-id="47000-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="47000-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span></span> | <span data-ttu-id="47000-359">PERF_REG_NOTIF</span><span class="sxs-lookup"><span data-stu-id="47000-359">PERF_REG_NOTIF</span></span> |
 
### <a name="system-scheduler-provider"></a><span data-ttu-id="47000-360">Поставщик системного планировщика</span><span class="sxs-lookup"><span data-stu-id="47000-360">System Scheduler Provider</span></span> 

<span data-ttu-id="47000-361">Предоставляет события, связанные с планировщиком.</span><span class="sxs-lookup"><span data-stu-id="47000-361">Provides events relating to the scheduler.</span></span>

<span data-ttu-id="47000-362">GUID: Системсчедулерпровидергуид {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span><span class="sxs-lookup"><span data-stu-id="47000-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span></span>

| <span data-ttu-id="47000-363">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-363">Keyword</span></span> | <span data-ttu-id="47000-364">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-364">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="47000-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span></span> | <span data-ttu-id="47000-366">PERF_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="47000-366">PERF_XSCHEDULER</span></span> |
| <span data-ttu-id="47000-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="47000-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span></span> | <span data-ttu-id="47000-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="47000-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span></span> |
| <span data-ttu-id="47000-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="47000-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span></span> | <span data-ttu-id="47000-370">PERF_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="47000-370">PERF_KERNEL_QUEUE</span></span> |
| <span data-ttu-id="47000-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="47000-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span></span> | <span data-ttu-id="47000-372">PERF_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="47000-372">PERF_SHOULD_YIELD</span></span> |
| <span data-ttu-id="47000-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="47000-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span></span> | <span data-ttu-id="47000-374">PERF_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="47000-374">PERF_ANTI_STARVATION</span></span> |
| <span data-ttu-id="47000-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="47000-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span></span> | <span data-ttu-id="47000-376">PERF_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="47000-376">PERF_LOAD_BALANCER</span></span> |
| <span data-ttu-id="47000-377">SYSTEM_SCHEDULER_KW_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="47000-377">SYSTEM_SCHEDULER_KW_AFFINITY</span></span> | <span data-ttu-id="47000-378">PERF_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="47000-378">PERF_AFFINITY</span></span> |
| <span data-ttu-id="47000-379">SYSTEM_SCHEDULER_KW_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="47000-379">SYSTEM_SCHEDULER_KW_PRIORITY</span></span> | <span data-ttu-id="47000-380">PERF_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="47000-380">PERF_PRIORITY</span></span> |
| <span data-ttu-id="47000-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="47000-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span></span> | <span data-ttu-id="47000-382">PERF_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="47000-382">PERF_IDEAL_PROCESSOR</span></span> |
| <span data-ttu-id="47000-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span><span class="sxs-lookup"><span data-stu-id="47000-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span></span> | <span data-ttu-id="47000-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span><span class="sxs-lookup"><span data-stu-id="47000-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span></span> |
 
### <a name="system-syscall-provider"></a><span data-ttu-id="47000-385">Системный поставщик syscall</span><span class="sxs-lookup"><span data-stu-id="47000-385">System Syscall Provider</span></span> 

<span data-ttu-id="47000-386">Предоставляет события со сведениями о системных вызовах.</span><span class="sxs-lookup"><span data-stu-id="47000-386">Provides events with information about system calls.</span></span>

<span data-ttu-id="47000-387">GUID: Системсискаллпровидергуид {434286f7-6f1b-45bb-b37e-95f623046c7c}</span><span class="sxs-lookup"><span data-stu-id="47000-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span></span>

| <span data-ttu-id="47000-388">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-388">Keyword</span></span> | <span data-ttu-id="47000-389">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-389">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-390">SYSTEM_SYSCALL_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-390">SYSTEM_SYSCALL_KW_GENERAL</span></span> | <span data-ttu-id="47000-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span><span class="sxs-lookup"><span data-stu-id="47000-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span></span> |
 
### <a name="system-timer-provider"></a><span data-ttu-id="47000-392">Поставщик системного таймера</span><span class="sxs-lookup"><span data-stu-id="47000-392">System Timer Provider</span></span> 

<span data-ttu-id="47000-393">Предоставляет события, относящиеся к таймерам в ядре.</span><span class="sxs-lookup"><span data-stu-id="47000-393">Provides events relating to timers in the kernel.</span></span>

<span data-ttu-id="47000-394">GUID: Системтимерпровидергуид {4f061568-e215-499f-ab2e-eda0ae890a5b}</span><span class="sxs-lookup"><span data-stu-id="47000-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span></span>

| <span data-ttu-id="47000-395">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="47000-395">Keyword</span></span> | <span data-ttu-id="47000-396">Соответствующие устаревшие флаги и группы</span><span class="sxs-lookup"><span data-stu-id="47000-396">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="47000-397">SYSTEM_TIMER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="47000-397">SYSTEM_TIMER_KW_GENERAL</span></span> | <span data-ttu-id="47000-398">PERF_TIMER</span><span class="sxs-lookup"><span data-stu-id="47000-398">PERF_TIMER</span></span> |
| <span data-ttu-id="47000-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="47000-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span></span> | <span data-ttu-id="47000-400">PERF_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="47000-400">PERF_CLOCK_TIMER</span></span> |
 
## <a name="remarks"></a><span data-ttu-id="47000-401">Remarks</span><span class="sxs-lookup"><span data-stu-id="47000-401">Remarks</span></span>

<span data-ttu-id="47000-402">Этот новый механизм включения является дополнением к уже существующим методам для включения этих событий.</span><span class="sxs-lookup"><span data-stu-id="47000-402">This new enablement mechanism is in addition to the pre-existing methods for enabling these events.</span></span>  <span data-ttu-id="47000-403">Любой код, который использовался для работы, продолжит это.</span><span class="sxs-lookup"><span data-stu-id="47000-403">Any code that used to work, will continue to do so.</span></span>
 
<span data-ttu-id="47000-404">События, создаваемые поставщиком трассировки системы, не изменяются из-за этой новой функции.</span><span class="sxs-lookup"><span data-stu-id="47000-404">The events generated by the System Trace Provider are not changing due to this new feature.</span></span>  <span data-ttu-id="47000-405">Это означает, что выводимые события не помечаются как порожденные от поставщиков отдельных систем.</span><span class="sxs-lookup"><span data-stu-id="47000-405">This means that the outputted events are not marked as being emitted from the individual system providers.</span></span>
 
<span data-ttu-id="47000-406">Дополнительные сведения о GUID поставщика и определениях ключевых слов см. в разделе [евнтраце. h](/windows/win32/api/evntrace/).</span><span class="sxs-lookup"><span data-stu-id="47000-406">For more information on provider GUID and keyword definitions see [evntrace.h](/windows/win32/api/evntrace/).</span></span>

## <a name="see-also"></a><span data-ttu-id="47000-407">См. также:</span><span class="sxs-lookup"><span data-stu-id="47000-407">See Also</span></span>

[<span data-ttu-id="47000-408">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="47000-408">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)

[<span data-ttu-id="47000-409">заголовок евнтраце. h</span><span class="sxs-lookup"><span data-stu-id="47000-409">evntrace.h header</span></span>](/windows/win32/api/evntrace/)