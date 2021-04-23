---
description: 'Дополнительные сведения: параметры кэша базы данных'
title: Параметры кэша базы данных
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711319"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="c1260-103">Параметры кэша базы данных</span><span class="sxs-lookup"><span data-stu-id="c1260-103">Database Cache Parameters</span></span>


<span data-ttu-id="c1260-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c1260-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="c1260-105">Параметры кэша базы данных</span><span class="sxs-lookup"><span data-stu-id="c1260-105">Database Cache Parameters</span></span>

<span data-ttu-id="c1260-106">Этот раздел содержит параметры, используемые для кэша базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="c1260-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="c1260-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="c1260-108">22</span><span class="sxs-lookup"><span data-stu-id="c1260-108">22</span></span>  

<span data-ttu-id="c1260-109">Этот параметр определяет размер вспомогательной части кэша страниц базы данных, которая используется для имитации операций ввода-вывода при недоступности.</span><span class="sxs-lookup"><span data-stu-id="c1260-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="c1260-110">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-110">The size is in database pages.</span></span>

<span data-ttu-id="c1260-111">**Windows XP и более поздние версии:**  Этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c1260-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-112">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-113">256</span><span class="sxs-lookup"><span data-stu-id="c1260-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-114">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-115">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-116">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-117">0, 2 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1260-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-118">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-119">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-120">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-121">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-122">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-123">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-124">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-125">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-126">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-128">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-129">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-130">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-131">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-132">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-133">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="c1260-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="c1260-135">41</span><span class="sxs-lookup"><span data-stu-id="c1260-135">41</span></span>  

<span data-ttu-id="c1260-136">Этот параметр можно использовать для управления размером кэша страниц базы данных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c1260-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="c1260-137">Обычно кэш автоматически настраивает свой размер в виде функции уровней активности базы данных и компьютера.</span><span class="sxs-lookup"><span data-stu-id="c1260-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="c1260-138">Если приложение устанавливает для этого параметра значение 0, то кэш будет настраивать свой собственный размер таким образом.</span><span class="sxs-lookup"><span data-stu-id="c1260-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="c1260-139">Однако если приложение задает для этого параметра ненулевое значение, то кэш будет настроен таким же целевым размером (на страницах базы данных).</span><span class="sxs-lookup"><span data-stu-id="c1260-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="c1260-140">Кэш будет храниться в этом пороговом значении до получения нового размера или до тех пор, пока не будет выбран его собственный размер.</span><span class="sxs-lookup"><span data-stu-id="c1260-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="c1260-141">**Примечание**  .  Размер кэша по-прежнему подчиняется ограничениям, наложенным **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="c1260-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="c1260-142">При чтении этого параметра возвращается фактический размер кэша на страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="c1260-143">Этот размер может использоваться приложением в качестве входных данных для выполнения ручной настройки размера кэша.</span><span class="sxs-lookup"><span data-stu-id="c1260-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-144">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-145">Специальные функции</span><span class="sxs-lookup"><span data-stu-id="c1260-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-146">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-147">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-148">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-149"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="c1260-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="c1260-150"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-151">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-152">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-153">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-154">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-155">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-156">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-157">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-158">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-159">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-160">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-161">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-162">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-163">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-164">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-165">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-166">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="c1260-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="c1260-168">60</span><span class="sxs-lookup"><span data-stu-id="c1260-168">60</span></span>  

<span data-ttu-id="c1260-169">Этот параметр задает минимальный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="c1260-170">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-170">The size is in database pages.</span></span>

<span data-ttu-id="c1260-171">По умолчанию кэш базы данных автоматически подстраивает свой размер между ограничениями, заданными **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="c1260-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="c1260-172">**Windows 2000:**  В Windows 2000 этому параметру должно быть присвоено значение примерно равное четырем количеству потоков, которые будут находиться внутри API ESE одновременно.</span><span class="sxs-lookup"><span data-stu-id="c1260-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="c1260-173">Это необходимо, чтобы избежать взаимоблокировок, вызванных недостаточным количеством буферов кэша страниц базы данных для выполнения сложных операций, таких как разбиение дерева B +.</span><span class="sxs-lookup"><span data-stu-id="c1260-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="c1260-174">**Windows XP и более поздние версии:**  Диспетчер кэша автоматически установит свой минимальный размер кэша, чтобы избежать взаимоблокировок.</span><span class="sxs-lookup"><span data-stu-id="c1260-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-175">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-176"><strong>Windows 2000:</strong>  64</span><span class="sxs-lookup"><span data-stu-id="c1260-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="c1260-177"><strong>Windows XP:</strong>  1</span><span class="sxs-lookup"><span data-stu-id="c1260-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-178">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-179">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-180">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-181"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="c1260-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="c1260-182"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-183">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-184">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-185">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-186"><strong>Windows 2000:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="c1260-187"><strong>Windows XP:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="c1260-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-188">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-189"><strong>Windows 2000:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="c1260-190"><strong>Windows XP:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="c1260-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-191">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-192">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-193">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-194">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-195">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-196">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-197">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-198">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-199">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-200">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="c1260-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="c1260-202">23</span><span class="sxs-lookup"><span data-stu-id="c1260-202">23</span></span>  

<span data-ttu-id="c1260-203">Этот параметр задает максимальный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="c1260-204">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-204">The size is in database pages.</span></span>

<span data-ttu-id="c1260-205">По умолчанию кэш базы данных автоматически подстраивает свой размер между ограничениями, заданными **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="c1260-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="c1260-206">**Примечание**   .   Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c1260-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="c1260-207">**Windows Vista:**  Начиная с Windows Vista, значение этого параметра по умолчанию изменилось, чтобы объяснить это поведение.</span><span class="sxs-lookup"><span data-stu-id="c1260-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-208">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-209"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  512</span><span class="sxs-lookup"><span data-stu-id="c1260-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="c1260-210"><strong>Windows Vista:</strong>  2000000000</span><span class="sxs-lookup"><span data-stu-id="c1260-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-211">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-212">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-213">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-214"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="c1260-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="c1260-215"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-216">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-217">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-218">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-219"><strong>Windows 2000:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="c1260-220"><strong>Windows XP:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="c1260-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-221">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-222"><strong>Windows XP и windows 2000:</strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="c1260-223"><strong>Windows Vista и Windows Server 2003:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="c1260-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-224">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-225">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-226">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-227">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-228">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-229">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-230">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-231">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-232">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-233">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="c1260-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="c1260-235">24</span><span class="sxs-lookup"><span data-stu-id="c1260-235">24</span></span> 

<span data-ttu-id="c1260-236">Этот параметр определяет, как агрессивные страницы базы данных очищаются из кэша страниц базы данных, чтобы максимально сокращать время, необходимое для восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="c1260-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="c1260-237">Параметр — это пороговое значение в байтах, необходимое для того, сколько файлов журнала транзакций потребуется воспроизвести после сбоя.</span><span class="sxs-lookup"><span data-stu-id="c1260-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="c1260-238">Если циклическое ведение журнала включено с помощью [JET_paramCircularLog](./transaction-log-parameters.md) то этот параметр также будет управлять приблизительным объемом файлов журнала транзакций, которые будут храниться на диске.</span><span class="sxs-lookup"><span data-stu-id="c1260-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="c1260-239">Важно, чтобы этот параметр не был задан слишком низким.</span><span class="sxs-lookup"><span data-stu-id="c1260-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="c1260-240">Поскольку значение этого параметра приближается к нулю, кэш становится более и более агрессивным при сбросе страниц базы данных на диск.</span><span class="sxs-lookup"><span data-stu-id="c1260-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="c1260-241">Это не только увеличивает число операций записи в файлы базы данных, но и косвенно приводит к увеличению числа операций чтения этих файлов.</span><span class="sxs-lookup"><span data-stu-id="c1260-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="c1260-242">В некоторых случаях это может привести к очень значительным проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="c1260-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="c1260-243">К сожалению, установка наименьшего оптимального значения для этого параметра может быть выполнена только с помощью эксперимента с целевым приложением.</span><span class="sxs-lookup"><span data-stu-id="c1260-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-244">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-245">20971520</span><span class="sxs-lookup"><span data-stu-id="c1260-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-246">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-247">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-248">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-249"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1260-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="c1260-250"><strong>Windows Vista:</strong>  Все значения</span><span class="sxs-lookup"><span data-stu-id="c1260-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-251">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-252">Windows <strong>2000, Windows XP и Windows Server 2003:</strong> Этот параметр является глобальным.</span><span class="sxs-lookup"><span data-stu-id="c1260-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="c1260-253"><strong>Windows Vista:</strong>  Этот параметр задан для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c1260-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-254">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-255">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-256">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-257">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-258">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-259">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-260">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-261">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-262">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-263">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-264">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-265">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-266">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-267">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="c1260-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="c1260-269">135</span><span class="sxs-lookup"><span data-stu-id="c1260-269">135</span></span>  

<span data-ttu-id="c1260-270">Этот параметр управляет максимальным числом одновременных операций записи, которые ядро СУБД будет использовать для сброса измененных страниц базы данных с целью перемещения контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="c1260-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="c1260-271">Значение этого параметра можно использовать для балансировки скорости, с которой может быть расширена контрольная точка, а также отрицательного воздействия на то, что этот процесс будет иметь время отклика для других операций ввода-вывода на дисках, где находится база данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-272">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-273">96</span><span class="sxs-lookup"><span data-stu-id="c1260-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-274">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-275">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-276">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-277">8 — 1024</span><span class="sxs-lookup"><span data-stu-id="c1260-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-278">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-279">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-280">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-281">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-282">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-283">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-284">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-285">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-286">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-287">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-288">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-289">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-290">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-291">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-292">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-293">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="c1260-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="c1260-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="c1260-295">127</span><span class="sxs-lookup"><span data-stu-id="c1260-295">127</span></span>  

<span data-ttu-id="c1260-296">Если этот параметр имеет **значение true**, ядро СУБД будет использовать данные базы данных непосредственно из кэша файлов Windows, а не копировать кэшированные данные в собственную частную память.</span><span class="sxs-lookup"><span data-stu-id="c1260-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="c1260-297">Все измененные данные базы данных по-прежнему будут кэшироваться в частной памяти.</span><span class="sxs-lookup"><span data-stu-id="c1260-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="c1260-298">Цель этого режима — еще больше уменьшить объем памяти, используемой ядром СУБД для кэширования данных базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="c1260-299">Кэш представлений может использоваться только в том случае, если использование кэша файлов Windows включено путем установки JET_paramEnableFileCache в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="c1260-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-300">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-301">Неверно</span><span class="sxs-lookup"><span data-stu-id="c1260-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-302">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-303">Логическое</span><span class="sxs-lookup"><span data-stu-id="c1260-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-304">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-305">False, true</span><span class="sxs-lookup"><span data-stu-id="c1260-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-306">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-307">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-308">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-309">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-310">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-311">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-312">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-313">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-314">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-315">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-316">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-317">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-318">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-319">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-320">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-321">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="c1260-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="c1260-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="c1260-323">25</span><span class="sxs-lookup"><span data-stu-id="c1260-323">25</span></span>  

<span data-ttu-id="c1260-324">Этот параметр задает интервал времени в микросекундах, в течение которого два доступа к странице базы данных считаются коррелированными.</span><span class="sxs-lookup"><span data-stu-id="c1260-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="c1260-325">Этот интервал корреляции управляет чувствительностью алгоритма замены страниц кэша (LRU-K) к последовательному доступу к странице.</span><span class="sxs-lookup"><span data-stu-id="c1260-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="c1260-326">Это, в свою очередь, повлияет на то, какие страницы он выбирает для сохранения кэширования.</span><span class="sxs-lookup"><span data-stu-id="c1260-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-327">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-328">128 000</span><span class="sxs-lookup"><span data-stu-id="c1260-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-329">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-330">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-331">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-332"><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1260-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="c1260-333"><strong>Windows Vista:</strong>  Все значения</span><span class="sxs-lookup"><span data-stu-id="c1260-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-334">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-335">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-336">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-337">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-338">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-339">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-340">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-341">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-342">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-343">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-344">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-345">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-346">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-347">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-348">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-349">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="c1260-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="c1260-351">26</span><span class="sxs-lookup"><span data-stu-id="c1260-351">26</span></span>  

<span data-ttu-id="c1260-352">Этот параметр задает максимальное количество некэшированных страниц базы данных, для которых будет храниться время доступа к странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="c1260-353">Эти записи журнала позволяют алгоритму замены страниц кэша (LRU-K) более точно обнаруживать популярные страницы, которые были неправильно исключены из кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="c1260-354">**Windows XP и Windows Server 2003:**  Этот параметр не учитывается в Windows XP и Windows Server 2003 и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c1260-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-355">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-356"><strong>Windows 2000:</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="c1260-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="c1260-357"><strong>Windows Vista:</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="c1260-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-358">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-359">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-360">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-361"><strong>Windows 2000:</strong>  0 – 4194303</span><span class="sxs-lookup"><span data-stu-id="c1260-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="c1260-362"><strong>Windows Vista:</strong>  Все значения</span><span class="sxs-lookup"><span data-stu-id="c1260-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-363">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-364">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-365">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-366">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-367">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-368">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-369">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-370">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-371">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-372">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-373">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-374">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-375">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-376">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-377">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-378">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="c1260-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="c1260-380">27</span><span class="sxs-lookup"><span data-stu-id="c1260-380">27</span></span>  

<span data-ttu-id="c1260-381">Этот параметр задает количество обращений к странице базы данных, которые учитываются при определении полезности страницы.</span><span class="sxs-lookup"><span data-stu-id="c1260-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="c1260-382">Этот параметр по сути является K в LRU-K, алгоритмом замены страниц кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1260-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-383">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-384">2</span><span class="sxs-lookup"><span data-stu-id="c1260-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-385">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-386">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-387">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-388">1–2</span><span class="sxs-lookup"><span data-stu-id="c1260-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-389">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-390">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-391">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-392">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-393">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-394">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-395">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-396">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-397">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-398">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-399">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-400">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-401">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-402">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-403">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-404">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="c1260-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="c1260-406">28</span><span class="sxs-lookup"><span data-stu-id="c1260-406">28</span></span>

<span data-ttu-id="c1260-407">Этот параметр указывает период времени (в секундах), по истечении которого считается, что страница в кэше страниц базы данных потеряла доступ к странице для учета полезности страницы.</span><span class="sxs-lookup"><span data-stu-id="c1260-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-408">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-409">100</span><span class="sxs-lookup"><span data-stu-id="c1260-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-410">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-411">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-412">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-413"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="c1260-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="c1260-414"><strong>Windows Vista:</strong>   1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-415">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-416">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-417">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-418">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-419">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-420">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-421">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-422">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-423">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-424">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-425">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-426">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-427">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-428">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-429">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-430">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="c1260-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="c1260-432">29</span><span class="sxs-lookup"><span data-stu-id="c1260-432">29</span></span>  

<span data-ttu-id="c1260-433">Этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c1260-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="c1260-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="c1260-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="c1260-435">31</span><span class="sxs-lookup"><span data-stu-id="c1260-435">31</span></span>  

<span data-ttu-id="c1260-436">Этот параметр определяет, когда кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="c1260-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="c1260-437">Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов.</span><span class="sxs-lookup"><span data-stu-id="c1260-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="c1260-438">Это пороговое значение всегда относительно максимального размера кэша, установленного **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="c1260-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="c1260-439">Это пороговое значение также должно быть меньше порога окончания, установленного **JET_paramStopFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="c1260-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="c1260-440">Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их.</span><span class="sxs-lookup"><span data-stu-id="c1260-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="c1260-441">При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование.</span><span class="sxs-lookup"><span data-stu-id="c1260-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="c1260-442">Однако при высоком пороговом значении для параметра «Порог» появляется более высокий порог, что уменьшает эффективный размер кэша страниц базы данных для измененных страниц (Windows 2000) или для всех страниц (Windows XP и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="c1260-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-443">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-444"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="c1260-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="c1260-445"><strong>Windows Vista:</strong>  20000000 (1%)</span><span class="sxs-lookup"><span data-stu-id="c1260-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-446">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-447">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-448">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-449"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="c1260-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="c1260-450"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="c1260-451"><strong>Windows Vista:</strong>  Все значения</span><span class="sxs-lookup"><span data-stu-id="c1260-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-452">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-453">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-454">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-455">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-456">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-457">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-458">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-459">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-460">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-461">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-462">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-463">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-464">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-465">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-466">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-467">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1260-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="c1260-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="c1260-469">32</span><span class="sxs-lookup"><span data-stu-id="c1260-469">32</span></span>  

<span data-ttu-id="c1260-470">Этот параметр управляет тем, когда кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="c1260-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="c1260-471">Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается.</span><span class="sxs-lookup"><span data-stu-id="c1260-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="c1260-472">Это пороговое значение всегда относительно максимального размера кэша, установленного **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="c1260-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="c1260-473">Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное **JET_paramStartFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="c1260-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="c1260-474">Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом.</span><span class="sxs-lookup"><span data-stu-id="c1260-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="c1260-475">Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="c1260-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="c1260-476">Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных для измененных страниц (Windows 2000) или для всех страниц (Windows XP и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="c1260-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-477">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c1260-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c1260-478"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="c1260-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="c1260-479"><strong>Windows Vista:</strong>  40000000 (2%)</span><span class="sxs-lookup"><span data-stu-id="c1260-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-480">Тип:</span><span class="sxs-lookup"><span data-stu-id="c1260-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="c1260-481">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="c1260-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-482">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="c1260-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c1260-483"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="c1260-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="c1260-484"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1260-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="c1260-485"><strong>Windows Vista:</strong>  Все значения</span><span class="sxs-lookup"><span data-stu-id="c1260-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-486">Область.</span><span class="sxs-lookup"><span data-stu-id="c1260-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c1260-487">Глобальный</span><span class="sxs-lookup"><span data-stu-id="c1260-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-488">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-489">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-490">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="c1260-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c1260-491">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-492">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="c1260-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c1260-493">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-494">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="c1260-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-495">Нет</span><span class="sxs-lookup"><span data-stu-id="c1260-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-496">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="c1260-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c1260-497">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-498">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="c1260-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c1260-499">Да</span><span class="sxs-lookup"><span data-stu-id="c1260-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-500">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="c1260-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c1260-501">Все</span><span class="sxs-lookup"><span data-stu-id="c1260-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c1260-502">Требования</span><span class="sxs-lookup"><span data-stu-id="c1260-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1260-503"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c1260-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c1260-504">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c1260-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1260-505"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c1260-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c1260-506">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c1260-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1260-507"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c1260-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c1260-508">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c1260-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c1260-509">См. также:</span><span class="sxs-lookup"><span data-stu-id="c1260-509">See Also</span></span>

[<span data-ttu-id="c1260-510">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="c1260-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c1260-511">жетинит</span><span class="sxs-lookup"><span data-stu-id="c1260-511">JetInit</span></span>](./jetinit-function.md)
