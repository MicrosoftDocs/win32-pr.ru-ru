---
description: Дополнительные сведения о параметрах ресурсов
title: Параметры ресурсов
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683582"
---
# <a name="resource-parameters"></a><span data-ttu-id="4deb1-103">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="4deb1-103">Resource Parameters</span></span>


<span data-ttu-id="4deb1-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4deb1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="4deb1-105">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="4deb1-105">Resource Parameters</span></span>

<span data-ttu-id="4deb1-106">Этот раздел содержит параметры, используемые для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4deb1-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="4deb1-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="4deb1-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="4deb1-108">125</span><span class="sxs-lookup"><span data-stu-id="4deb1-108">125</span></span>  

<span data-ttu-id="4deb1-109">Этот параметр определяет количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="4deb1-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="4deb1-110">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="4deb1-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="4deb1-111">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="4deb1-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-112">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-113">64</span><span class="sxs-lookup"><span data-stu-id="4deb1-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-114">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-115">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-116">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-117">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-118">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-119">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-120">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-121">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-122">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-124">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-125">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-126">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-127">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-128">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-129">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-130">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-131">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-132">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-133">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="4deb1-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="4deb1-135">107</span><span class="sxs-lookup"><span data-stu-id="4deb1-135">107</span></span>  

<span data-ttu-id="4deb1-136">Этот параметр можно использовать, чтобы предотвратить публикацию данных о производительности ядром СУБД в Windows.</span><span class="sxs-lookup"><span data-stu-id="4deb1-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="4deb1-137">Это можно сделать, чтобы уменьшить активность потока обслуживания ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="4deb1-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-138">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="4deb1-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-140">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-141">Логическое</span><span class="sxs-lookup"><span data-stu-id="4deb1-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-142">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-143">False, true</span><span class="sxs-lookup"><span data-stu-id="4deb1-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-144">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-145">Глобальный</span><span class="sxs-lookup"><span data-stu-id="4deb1-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-146">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-147">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-148">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-149">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-150">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-151">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-152">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-153">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-154">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-155">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-156">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-157">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-158">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-159">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="4deb1-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="4deb1-161">81</span><span class="sxs-lookup"><span data-stu-id="4deb1-161">81</span></span>  

<span data-ttu-id="4deb1-162">Этот параметр позволяет приложениям, работающим в режиме с несколькими экземплярами, предварительно распределять память для страниц версий в глобальном пуле, чтобы эмулировать старое поведение.</span><span class="sxs-lookup"><span data-stu-id="4deb1-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="4deb1-163">Это полезно в том случае, если приложение должно гарантировать, что транзакции определенного размера могут быть выполнены позже, даже если память становится нехватке.</span><span class="sxs-lookup"><span data-stu-id="4deb1-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="4deb1-164">**Windows 2000:**  Достаточно памяти для резервного копирования всех страниц версий всегда резервируется во время [жетинит](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4deb1-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="4deb1-165">**Windows XP:**  Начиная с Windows XP, это по-прежнему выполняется в режиме одиночного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4deb1-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="4deb1-166">Однако память страницы версии динамически выделяется в режиме с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="4deb1-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-167">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-168">64</span><span class="sxs-lookup"><span data-stu-id="4deb1-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-169">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-170">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-171">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-172">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-173">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-174">Глобальный</span><span class="sxs-lookup"><span data-stu-id="4deb1-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-175">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-176">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-177">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-178">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-179">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-180">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-181">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-182">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-183">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-184">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-185">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-186">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-187">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-188">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="4deb1-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="4deb1-190">8</span><span class="sxs-lookup"><span data-stu-id="4deb1-190">8</span></span>  

<span data-ttu-id="4deb1-191">Этот параметр резервирует запрошенное количество ресурсов курсора для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4deb1-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="4deb1-192">Ресурс курсора непосредственно соответствует [JET_TABLEID](./jet-tableid.md) типу данных.</span><span class="sxs-lookup"><span data-stu-id="4deb1-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="4deb1-193">Этот параметр влияет на количество курсоров, которые могут использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="4deb1-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="4deb1-194">Ресурс курсора не может совместно использоваться разными сеансами, поэтому для этого параметра необходимо задать достаточно большое значение, чтобы каждый сеанс мог использовать столько курсоров, сколько требуется.</span><span class="sxs-lookup"><span data-stu-id="4deb1-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="4deb1-195">Windows **2000, Windows XP и Windows Server 2003:**  Большие значения для этого параметра потребуют использования адресного пространства и могут увеличить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="4deb1-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-196">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-197">1024</span><span class="sxs-lookup"><span data-stu-id="4deb1-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-198">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-199">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-200">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-201">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-202">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-203">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-204">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-205">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-206">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-207">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-208">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-209">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-210">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-211">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-212">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-213">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-214">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-215">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-216">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-217">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="4deb1-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="4deb1-219">104</span><span class="sxs-lookup"><span data-stu-id="4deb1-219">104</span></span>  

<span data-ttu-id="4deb1-220">Этот параметр определяет максимальное количество экземпляров, которые могут быть созданы в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="4deb1-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-221">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-222">16</span><span class="sxs-lookup"><span data-stu-id="4deb1-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-223">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-224">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-225">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-226">От 1 до 1024</span><span class="sxs-lookup"><span data-stu-id="4deb1-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-227">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-228">Глобальный</span><span class="sxs-lookup"><span data-stu-id="4deb1-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-229">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-230">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-231">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-232">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-233">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-234">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-235">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-236">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-237">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-238">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-239">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-240">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-241">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-242">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="4deb1-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="4deb1-244">6</span><span class="sxs-lookup"><span data-stu-id="4deb1-244">6</span></span>  

<span data-ttu-id="4deb1-245">Этот параметр резервирует запрошенное число ресурсов дерева B + для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4deb1-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="4deb1-246">Этот параметр влияет на количество таблиц, которые могут использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="4deb1-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="4deb1-247">Этот параметр необходимо задать относительно физической схемы баз данных, используемых ядром СУБД, поэтому этот параметр не так прост, как может быть.</span><span class="sxs-lookup"><span data-stu-id="4deb1-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="4deb1-248">В общем случае вам потребуется два ресурса и один ресурс на каждый вторичный индекс в одной таблице в параллельном использовании приложением.</span><span class="sxs-lookup"><span data-stu-id="4deb1-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="4deb1-249">Windows **2000, Windows XP и Windows Server 2003:**  Большие значения для этого параметра потребуют использования адресного пространства и могут увеличить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="4deb1-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-250">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-251">300</span><span class="sxs-lookup"><span data-stu-id="4deb1-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-252">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-253">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-254">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-255">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-256">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-257">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-258">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-259">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-260">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-261">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-262">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-263">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-264">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-265">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-266">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-267">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-268">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-269">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-270">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-271">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="4deb1-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="4deb1-273">5</span><span class="sxs-lookup"><span data-stu-id="4deb1-273">5</span></span>  

<span data-ttu-id="4deb1-274">Этот параметр резервирует запрошенное число ресурсов сеанса для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4deb1-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="4deb1-275">Ресурс сеанса непосредственно соответствует [JET_SESID](./jet-sesid.md) типу данных.</span><span class="sxs-lookup"><span data-stu-id="4deb1-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="4deb1-276">Этот параметр влияет на то, сколько сеансов можно использовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="4deb1-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="4deb1-277">Windows **2000, Windows XP и Windows Server 2003:**  Большие значения для этого параметра потребуют использования адресного пространства и могут увеличить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="4deb1-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-278">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-279">16</span><span class="sxs-lookup"><span data-stu-id="4deb1-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-280">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-281">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-282">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-283">0 – 30000</span><span class="sxs-lookup"><span data-stu-id="4deb1-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-284">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-285">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-286">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-287">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-288">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-289">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-290">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-291">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-292">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-293">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-294">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-295">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-296">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-297">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-298">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-299">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="4deb1-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="4deb1-301">10</span><span class="sxs-lookup"><span data-stu-id="4deb1-301">10</span></span>  

<span data-ttu-id="4deb1-302">Этот параметр резервирует запрошенное количество временных ресурсов таблицы для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4deb1-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="4deb1-303">Этот параметр влияет на количество временных таблиц, которые можно использовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="4deb1-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="4deb1-304">Windows **2000, Windows XP и Windows Server 2003:**  Большие значения для этого параметра потребуют использования адресного пространства и могут увеличить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="4deb1-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="4deb1-305">**Windows XP и более поздние версии:**  Если этот системный параметр имеет значение 0, то временная база данных не будет создана и любое действие, требующее использования временной базы данных, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4deb1-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="4deb1-306">Этот параметр может быть полезен, чтобы избежать операций ввода-вывода, необходимых для создания временной базы данных, если известно, что она не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="4deb1-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="4deb1-307">**Примечание**  .  Для использования временной таблицы также требуется ресурс курсора.</span><span class="sxs-lookup"><span data-stu-id="4deb1-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-308">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-309">20</span><span class="sxs-lookup"><span data-stu-id="4deb1-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-310">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-311">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-312">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-313">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-314">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-315">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-316">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-317">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-318">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-319">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-320">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-321">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-322">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-323">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-324">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-325">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-326">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-327">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-328">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-329">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="4deb1-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="4deb1-331">9</span><span class="sxs-lookup"><span data-stu-id="4deb1-331">9</span></span>  

<span data-ttu-id="4deb1-332">Этот параметр резервирует запрошенное число страниц хранилища версий для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4deb1-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="4deb1-333">Хранилище версий содержит активную запись всех различных версий каждой записи или записи индекса в базе данных, которые могут быть видны всем активным транзакциям.</span><span class="sxs-lookup"><span data-stu-id="4deb1-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="4deb1-334">Эти версии используются для поддержки управления параллелизмом с несколькими версиями, используемого ядром СУБД для поддержки транзакций с использованием изоляции моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="4deb1-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="4deb1-335">Этот параметр влияет на количество обновлений, которые могут храниться в памяти за один раз.</span><span class="sxs-lookup"><span data-stu-id="4deb1-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="4deb1-336">Это, в свою очередь, влияет на максимальное количество обновлений, которые может выполнить одна транзакция, максимальную продолжительность длительности, в течение которого транзакция может оставаться открытой, максимальную одновременную нагрузку на обновление транзакций в системе или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="4deb1-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="4deb1-337">Каждая страница хранилища версий, настроенная этим параметром, имеет размер 16 КБ на 32-разрядных компьютерах и 32 КБ на 64-разрядных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="4deb1-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="4deb1-338">**Windows Vista и более поздние версии:**  Размер страницы хранилища версий можно считывать и изменять с помощью JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="4deb1-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="4deb1-339">Windows **2000, Windows XP и Windows Server 2003:**  Большие значения для этого параметра потребуют использования адресного пространства и могут увеличить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="4deb1-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="4deb1-340">**Примечание**  .  Это далеко не самый распространенный ресурс, который будет исчерпан ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="4deb1-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="4deb1-341">Необходимо уделять особое внимание параметру System и транзакционной нагрузке приложения, чтобы избежать исчерпания ресурса при нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="4deb1-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="4deb1-342">При исчерпании этого ресурса обновления базы данных будут отклонены с JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="4deb1-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="4deb1-343">Чтобы освободить некоторые из этих ресурсов, необходимо прервать самую старую невыполненную транзакцию.</span><span class="sxs-lookup"><span data-stu-id="4deb1-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-344">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-345">64</span><span class="sxs-lookup"><span data-stu-id="4deb1-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-346">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-347">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-348">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-349">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-350">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-351">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-352">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-353">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-354">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-355">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-356">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-357">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-358">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-359">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-360">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-361">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-362">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-363">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-364">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-365">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="4deb1-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="4deb1-367">101</span><span class="sxs-lookup"><span data-stu-id="4deb1-367">101</span></span>  

<span data-ttu-id="4deb1-368">Этот параметр определяет размер специального кэша, используемого для ускорения поиска указателей дочерней страницы дерева B + в кэше страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="4deb1-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="4deb1-369">Размер кэша в байтах.</span><span class="sxs-lookup"><span data-stu-id="4deb1-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-370">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-371">262144</span><span class="sxs-lookup"><span data-stu-id="4deb1-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-372">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-373">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-374">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-375">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-376">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-377">Глобальный</span><span class="sxs-lookup"><span data-stu-id="4deb1-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-378">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-379">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-380">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-381">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-382">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-383">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-384">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-385">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-386">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-387">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-388">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-389">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-390">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-391">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="4deb1-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="4deb1-393">7</span><span class="sxs-lookup"><span data-stu-id="4deb1-393">7</span></span>  

<span data-ttu-id="4deb1-394">Этот параметр пытается установить число используемых ресурсов дерева B + ниже указанного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4deb1-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="4deb1-395">Если этот параметр имеет значение 0, по умолчанию будет 100% **JET_paramMaxOpenTables**.</span><span class="sxs-lookup"><span data-stu-id="4deb1-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="4deb1-396">**Windows Vista и более поздние версии:**  Этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="4deb1-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="4deb1-397">Вместо этого приложения должны использовать JET_paramMaxCachedClosedTables.</span><span class="sxs-lookup"><span data-stu-id="4deb1-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-398">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-399">0 (100% от <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="4deb1-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-400">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-401">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-402">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-403">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-404">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-405">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-406">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-407">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-408">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-409">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-410">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-411">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-412">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-413">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-414">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-415">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-416">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-417">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-418">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-419">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="4deb1-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="4deb1-421">63</span><span class="sxs-lookup"><span data-stu-id="4deb1-421">63</span></span>  

<span data-ttu-id="4deb1-422">Этот параметр представляет пороговое значение относительно **JET_paramMaxVerPages** , которое управляет избирательным использованием страниц версий ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="4deb1-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="4deb1-423">Если размер хранилища версий превышает это пороговое значение, то любая информация, которая используется только для необязательных фоновых задач, таких как освобождение места на удаленном диске в базе данных, задается для сохранения сведений о транзакциях.</span><span class="sxs-lookup"><span data-stu-id="4deb1-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="4deb1-424">Windows **2000, Windows XP и Windows Server 2003:**  Если установить для этого параметра значение 0, то пороговое значения будет 90% от **JET_paramMaxVerPages**.</span><span class="sxs-lookup"><span data-stu-id="4deb1-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="4deb1-425">**Windows Vista и более поздние версии:**  Это больше не поддерживается, и значение этого параметра по умолчанию изменилось, чтобы уточнить его поведение.</span><span class="sxs-lookup"><span data-stu-id="4deb1-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="4deb1-426">Каждая страница хранилища версий, настроенная этим параметром, имеет размер 16 КБ на 32-разрядных компьютерах и 32 КБ на 64-разрядных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="4deb1-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="4deb1-427">**Windows Vista и более поздние версии:**  Размер страницы хранилища версий можно считывать и изменять с помощью JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="4deb1-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="4deb1-428">**Примечание**  .  Если ядро СУБД работает слишком часто, это пороговое значение может снизить производительность базы данных.</span><span class="sxs-lookup"><span data-stu-id="4deb1-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="4deb1-429">Это происходит потому, что фоновые процессы, выполняющие очистку базы данных, не могут работать без дополнительных сведений, вызываемых в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="4deb1-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="4deb1-430">Оперативная или автономная дефрагментация отменяет этот результат.</span><span class="sxs-lookup"><span data-stu-id="4deb1-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-431">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-432"><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  0 (90% JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="4deb1-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="4deb1-433"><strong>Windows Vista:</strong>  58</span><span class="sxs-lookup"><span data-stu-id="4deb1-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-434">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-435">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-436">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-437">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="4deb1-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-438">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-439">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-440">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-441">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-442">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-443">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-444">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-445">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-446">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-447">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-448">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-449">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-450">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-451">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-452">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-453">Все</span><span class="sxs-lookup"><span data-stu-id="4deb1-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="4deb1-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="4deb1-455">128</span><span class="sxs-lookup"><span data-stu-id="4deb1-455">128</span></span>  

<span data-ttu-id="4deb1-456">Этот параметр определяет размер страниц хранилища версий, используемых ядром СУБД для хранения транзакционных данных.</span><span class="sxs-lookup"><span data-stu-id="4deb1-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="4deb1-457">Значение этого параметра — это размер единицы для всех других системных параметров, которые находятся в терминах страниц версий (например, JET_paramMaxVerPages).</span><span class="sxs-lookup"><span data-stu-id="4deb1-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="4deb1-458">Ядро СУБД может использовать размер страницы хранилища более крупной версии по сравнению с запрошенным.</span><span class="sxs-lookup"><span data-stu-id="4deb1-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-459">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-460">16384</span><span class="sxs-lookup"><span data-stu-id="4deb1-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-461">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-462">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-463">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="4deb1-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-465">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-466">Глобальный</span><span class="sxs-lookup"><span data-stu-id="4deb1-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-467">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-468">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-469">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-470">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-471">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-472">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-473">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-474">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-475">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-476">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-477">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-478">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-479">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-480">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4deb1-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="4deb1-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="4deb1-482">105</span><span class="sxs-lookup"><span data-stu-id="4deb1-482">105</span></span>  

<span data-ttu-id="4deb1-483">Этот параметр управляет количеством рабочих элементов фоновой очистки, которые могут быть поставлены в очередь в пул потоков ядра СУБД в любое время.</span><span class="sxs-lookup"><span data-stu-id="4deb1-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-484">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4deb1-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-485">32</span><span class="sxs-lookup"><span data-stu-id="4deb1-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-486">Тип:</span><span class="sxs-lookup"><span data-stu-id="4deb1-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-487">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="4deb1-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-488">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="4deb1-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-489"><strong>Windows XP и Windows Server 2003:  </strong>  1 – 63</span><span class="sxs-lookup"><span data-stu-id="4deb1-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="4deb1-490"><strong>Windows Vista:</strong>  1 – 127</span><span class="sxs-lookup"><span data-stu-id="4deb1-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-491">Область.</span><span class="sxs-lookup"><span data-stu-id="4deb1-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-492">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="4deb1-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-493">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-494">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-495">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="4deb1-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-496"><strong>Windows XP и Windows Server 2003:  </strong>  Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="4deb1-497"><strong>Windows Vista:</strong>  Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-498">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="4deb1-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-499">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-500">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-501">Нет</span><span class="sxs-lookup"><span data-stu-id="4deb1-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-502">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="4deb1-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-503">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-504">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="4deb1-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-505">Да</span><span class="sxs-lookup"><span data-stu-id="4deb1-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-506">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="4deb1-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4deb1-507">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="4deb1-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="4deb1-508">Требования</span><span class="sxs-lookup"><span data-stu-id="4deb1-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-509"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4deb1-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb1-510">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4deb1-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4deb1-511"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4deb1-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb1-512">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4deb1-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4deb1-513"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4deb1-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4deb1-514">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4deb1-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4deb1-515">См. также:</span><span class="sxs-lookup"><span data-stu-id="4deb1-515">See Also</span></span>

[<span data-ttu-id="4deb1-516">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="4deb1-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4deb1-517">жетинит</span><span class="sxs-lookup"><span data-stu-id="4deb1-517">JetInit</span></span>](./jetinit-function.md)
