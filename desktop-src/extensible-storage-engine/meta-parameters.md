---
description: Дополнительные сведения о параметрах meta.
title: Параметры Meta
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650494"
---
# <a name="meta-parameters"></a><span data-ttu-id="9211c-103">Параметры Meta</span><span class="sxs-lookup"><span data-stu-id="9211c-103">Meta Parameters</span></span>


<span data-ttu-id="9211c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9211c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="9211c-105">Параметры Meta</span><span class="sxs-lookup"><span data-stu-id="9211c-105">Meta Parameters</span></span>

<span data-ttu-id="9211c-106">Этот раздел содержит параметры, используемые для управления другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9211c-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="9211c-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="9211c-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="9211c-108">129</span><span class="sxs-lookup"><span data-stu-id="9211c-108">129</span></span>  
<span data-ttu-id="9211c-109">Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="9211c-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="9211c-110">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9211c-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="9211c-111">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9211c-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="9211c-112">Кроме того, сам параметр может иметь другие последствия поведения ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="9211c-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="9211c-113">В настоящее время существует две поддерживаемые конфигурации:</span><span class="sxs-lookup"><span data-stu-id="9211c-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="9211c-114">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="9211c-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="9211c-115">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9211c-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="9211c-116">При небольшой конфигурации по умолчанию для следующих системных параметров задаются указанные значения:</span><span class="sxs-lookup"><span data-stu-id="9211c-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9211c-117">Системный параметр</span><span class="sxs-lookup"><span data-stu-id="9211c-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="9211c-118">Новое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9211c-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9211c-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="9211c-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="9211c-120">30 000</span><span class="sxs-lookup"><span data-stu-id="9211c-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="9211c-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="9211c-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="9211c-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="9211c-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="9211c-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="9211c-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="9211c-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="9211c-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="9211c-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="9211c-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="9211c-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="9211c-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="9211c-130">64</span><span class="sxs-lookup"><span data-stu-id="9211c-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="9211c-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="9211c-132">1</span><span class="sxs-lookup"><span data-stu-id="9211c-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="9211c-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="9211c-134">16</span><span class="sxs-lookup"><span data-stu-id="9211c-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="9211c-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="9211c-136">14</span><span class="sxs-lookup"><span data-stu-id="9211c-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="9211c-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="9211c-138">16</span><span class="sxs-lookup"><span data-stu-id="9211c-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="9211c-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="9211c-140">65536</span><span class="sxs-lookup"><span data-stu-id="9211c-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="9211c-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="9211c-142">10</span><span class="sxs-lookup"><span data-stu-id="9211c-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="9211c-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="9211c-144">16</span><span class="sxs-lookup"><span data-stu-id="9211c-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="9211c-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="9211c-146">1</span><span class="sxs-lookup"><span data-stu-id="9211c-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="9211c-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="9211c-148">2</span><span class="sxs-lookup"><span data-stu-id="9211c-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="9211c-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="9211c-150">1</span><span class="sxs-lookup"><span data-stu-id="9211c-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="9211c-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="9211c-152">16</span><span class="sxs-lookup"><span data-stu-id="9211c-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="9211c-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="9211c-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="9211c-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="9211c-156">0</span><span class="sxs-lookup"><span data-stu-id="9211c-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="9211c-158">1</span><span class="sxs-lookup"><span data-stu-id="9211c-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="9211c-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="9211c-160">32</span><span class="sxs-lookup"><span data-stu-id="9211c-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="9211c-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="9211c-162">1</span><span class="sxs-lookup"><span data-stu-id="9211c-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="9211c-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="9211c-164">1</span><span class="sxs-lookup"><span data-stu-id="9211c-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="9211c-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="9211c-166">1</span><span class="sxs-lookup"><span data-stu-id="9211c-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="9211c-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="9211c-168">1024</span><span class="sxs-lookup"><span data-stu-id="9211c-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="9211c-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="9211c-170">0</span><span class="sxs-lookup"><span data-stu-id="9211c-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="9211c-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="9211c-172">8</span><span class="sxs-lookup"><span data-stu-id="9211c-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9211c-173">Небольшая конфигурация также имеет ряд других изменений в ядре СУБД, в том числе:</span><span class="sxs-lookup"><span data-stu-id="9211c-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="9211c-174">Все ресурсы, управляемые системными параметрами, выделяются из кучи по мере необходимости</span><span class="sxs-lookup"><span data-stu-id="9211c-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="9211c-175">Другие внутренние ресурсы, используемые ядром СУБД, масштабируются по размеру.</span><span class="sxs-lookup"><span data-stu-id="9211c-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="9211c-176">Различные операции обслуживания масштабируются обратно во избежание фонового действия потока.</span><span class="sxs-lookup"><span data-stu-id="9211c-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9211c-177">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="9211c-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="9211c-178">1 (устаревший)</span><span class="sxs-lookup"><span data-stu-id="9211c-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-179">Тип:</span><span class="sxs-lookup"><span data-stu-id="9211c-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="9211c-180">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="9211c-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-181">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="9211c-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="9211c-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="9211c-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-183">Область.</span><span class="sxs-lookup"><span data-stu-id="9211c-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="9211c-184">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="9211c-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-185">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="9211c-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="9211c-186">Да</span><span class="sxs-lookup"><span data-stu-id="9211c-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-187">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="9211c-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="9211c-188">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-189">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="9211c-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="9211c-190">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-191">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="9211c-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="9211c-192">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-193">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="9211c-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="9211c-194">Да</span><span class="sxs-lookup"><span data-stu-id="9211c-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-195">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="9211c-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="9211c-196">Да</span><span class="sxs-lookup"><span data-stu-id="9211c-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-197">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="9211c-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="9211c-198">Начиная с Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9211c-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9211c-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="9211c-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="9211c-200">130</span><span class="sxs-lookup"><span data-stu-id="9211c-200">130</span></span>  
<span data-ttu-id="9211c-201">Этот параметр используется для управления тем, когда ядро СУБД принимает или отклоняет изменения в подмножестве системных параметров.</span><span class="sxs-lookup"><span data-stu-id="9211c-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="9211c-202">Этот параметр используется совместно с JET_paramConfiguration, чтобы предотвратить установку некоторых системных параметров из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9211c-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="9211c-203">Следующие системные параметры будут защищены от установки, если этот параметр имеет значение false:</span><span class="sxs-lookup"><span data-stu-id="9211c-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="9211c-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="9211c-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="9211c-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="9211c-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="9211c-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="9211c-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="9211c-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="9211c-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="9211c-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="9211c-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="9211c-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="9211c-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="9211c-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="9211c-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="9211c-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="9211c-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="9211c-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="9211c-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="9211c-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="9211c-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="9211c-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="9211c-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="9211c-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="9211c-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="9211c-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="9211c-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="9211c-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="9211c-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="9211c-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="9211c-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="9211c-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="9211c-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="9211c-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="9211c-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="9211c-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="9211c-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="9211c-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="9211c-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="9211c-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="9211c-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="9211c-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="9211c-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="9211c-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="9211c-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="9211c-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="9211c-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="9211c-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="9211c-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="9211c-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="9211c-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="9211c-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="9211c-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="9211c-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="9211c-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="9211c-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="9211c-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="9211c-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="9211c-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="9211c-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="9211c-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="9211c-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="9211c-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="9211c-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="9211c-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="9211c-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="9211c-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="9211c-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="9211c-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="9211c-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="9211c-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="9211c-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="9211c-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="9211c-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="9211c-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="9211c-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="9211c-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="9211c-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="9211c-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9211c-244">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="9211c-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="9211c-245">True</span><span class="sxs-lookup"><span data-stu-id="9211c-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-246">Тип:</span><span class="sxs-lookup"><span data-stu-id="9211c-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="9211c-247">Логическое</span><span class="sxs-lookup"><span data-stu-id="9211c-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-248">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="9211c-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="9211c-249">False, true</span><span class="sxs-lookup"><span data-stu-id="9211c-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-250">Область.</span><span class="sxs-lookup"><span data-stu-id="9211c-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="9211c-251">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="9211c-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-252">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="9211c-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="9211c-253">Да</span><span class="sxs-lookup"><span data-stu-id="9211c-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-254">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="9211c-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="9211c-255">Да</span><span class="sxs-lookup"><span data-stu-id="9211c-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-256">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="9211c-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="9211c-257">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-258">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="9211c-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="9211c-259">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-260">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="9211c-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="9211c-261">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-262">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="9211c-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="9211c-263">Нет</span><span class="sxs-lookup"><span data-stu-id="9211c-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-264">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="9211c-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="9211c-265">Начиная с Windows Server 2008 и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9211c-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="9211c-266">Требования</span><span class="sxs-lookup"><span data-stu-id="9211c-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9211c-267"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9211c-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9211c-268">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9211c-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9211c-269"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9211c-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9211c-270">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9211c-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9211c-271"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9211c-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9211c-272">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9211c-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9211c-273">См. также:</span><span class="sxs-lookup"><span data-stu-id="9211c-273">See Also</span></span>

[<span data-ttu-id="9211c-274">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="9211c-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="9211c-275">жетинит</span><span class="sxs-lookup"><span data-stu-id="9211c-275">JetInit</span></span>](./jetinit-function.md)
