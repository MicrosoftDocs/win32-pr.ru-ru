---
description: Дополнительные сведения о параметрах ввода-вывода
title: Параметры ввода-вывода
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811639"
---
# <a name="io-parameters"></a><span data-ttu-id="289f7-103">Параметры ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="289f7-103">I/O Parameters</span></span>


<span data-ttu-id="289f7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="289f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="289f7-105">Параметры ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="289f7-105">I/O Parameters</span></span>

<span data-ttu-id="289f7-106">Этот раздел содержит параметры, используемые для ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="289f7-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="289f7-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="289f7-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="289f7-108">53</span><span class="sxs-lookup"><span data-stu-id="289f7-108">53</span></span>  

<span data-ttu-id="289f7-109">**Windows XP и более поздние версии:**  Этот параметр задает длительность времени (в миллисекундах), в течение которого ядро СУБД будет обращаться к файлу, заблокированному до сбоя JET_errFileAccessDenied.</span><span class="sxs-lookup"><span data-stu-id="289f7-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="289f7-110">Эта временная задержка предназначена для работы с антивирусным программным обеспечением, которое может содержать некоторые файлы ядра СУБД, открытые после их закрытия.</span><span class="sxs-lookup"><span data-stu-id="289f7-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="289f7-111">**Примечание**  .  В результате выполнения описанной выше логики повторных попыток присоединения к базе данных или использования файла журнала, который уже используется ядром СУБД, произойдет задержка этого размера, прежде чем вызов API вернет несанкционированный сбой.</span><span class="sxs-lookup"><span data-stu-id="289f7-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="289f7-112">Этот параметр можно использовать для отключения задержки в случае, если это распространенный сценарий.</span><span class="sxs-lookup"><span data-stu-id="289f7-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-113">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-114">10000</span><span class="sxs-lookup"><span data-stu-id="289f7-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-115">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-116">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-117">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-118">0 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="289f7-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-119">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-120">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-121">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-122">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-123">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-124">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-125">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-126">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-127">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-128">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-129">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-130">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-131">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-132">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-133">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-134">Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="289f7-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="289f7-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="289f7-136">100</span><span class="sxs-lookup"><span data-stu-id="289f7-136">100</span></span>  

<span data-ttu-id="289f7-137">Если этот параметр имеет значение true, любая папка, отсутствующая в пути файловой системы, используемой ядром СУБД, будет создана автоматически.</span><span class="sxs-lookup"><span data-stu-id="289f7-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="289f7-138">В противном случае операция, использующая отсутствующий путь файловой системы, завершится с JET_errInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="289f7-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-139">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="289f7-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-141">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-142">Логическое</span><span class="sxs-lookup"><span data-stu-id="289f7-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-143">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-144">False, true</span><span class="sxs-lookup"><span data-stu-id="289f7-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-145">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-146">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="289f7-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-147">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-148">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-149">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-150">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-151">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-152">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-153">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-154">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-155">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-156">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-157">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-158">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-159">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-160">Все</span><span class="sxs-lookup"><span data-stu-id="289f7-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="289f7-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="289f7-162">126</span><span class="sxs-lookup"><span data-stu-id="289f7-162">126</span></span>  

<span data-ttu-id="289f7-163">Если этот параметр имеет **значение true**, ядро СУБД будет использовать файловый кэш Windows в качестве кэша чтения для всех его различных файлов.</span><span class="sxs-lookup"><span data-stu-id="289f7-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="289f7-164">Он также будет использовать его как кэш записи для временной базы данных или для баз данных, открываемых с отключенным восстановлением.</span><span class="sxs-lookup"><span data-stu-id="289f7-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="289f7-165">Ядро СУБД должно отключить кэширование записи для обычных баз данных, файлов журналов транзакций и файлов контрольных точек для защиты транзакционной целостности баз данных.</span><span class="sxs-lookup"><span data-stu-id="289f7-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="289f7-166">Важно отметить, что использование кэша файлов Windows приведет к добавлению второго уровня кэширования для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="289f7-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="289f7-167">Кэш базы данных по-прежнему будет использовать собственную память для кэширования файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="289f7-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="289f7-168">Цель этого режима — позволить приложению настроить ядро СУБД с помощью небольшого выделенного кэша и позволить Windows подносить запасную память для дальнейшего улучшения кэширования данных базы данных.</span><span class="sxs-lookup"><span data-stu-id="289f7-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-169">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="289f7-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-171">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-172">Логическое</span><span class="sxs-lookup"><span data-stu-id="289f7-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-173">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-174">False, true</span><span class="sxs-lookup"><span data-stu-id="289f7-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-175">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-176">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-177">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-178">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-179">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-180">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-181">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-182">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-183">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-184">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-185">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-186">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-187">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-188">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-189">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-190">Windows Vista и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="289f7-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="289f7-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="289f7-192">152</span><span class="sxs-lookup"><span data-stu-id="289f7-192">152</span></span>  

<span data-ttu-id="289f7-193">Этот параметр определяет, как ESE обрабатывает операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="289f7-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="289f7-194">Для нормальной работы можно задать значения 0 (JET_IOPriorityNormal) или 1 (JET_IOPriorityLow) для операции с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="289f7-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="289f7-195">Если для параметра Priority задано значение JET_IOPriorityLow, ESE использует новые функции приоритета ввода-вывода потока, доступные в Windows Vista, чтобы уменьшить приоритет ввода-вывода в потоке, чтобы последующие операции ввода-вывода выдавались с новым низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="289f7-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="289f7-196">**Windows Vista:**  JET_paramIOPriority введен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="289f7-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-197">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-198">0</span><span class="sxs-lookup"><span data-stu-id="289f7-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-199">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-200">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-201">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="289f7-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-203">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-204">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="289f7-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-205">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-206">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-207">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-208">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-209">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-210">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-211">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-212">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-213">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-214">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-215">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-216">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-217">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="289f7-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="289f7-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="289f7-220">30</span><span class="sxs-lookup"><span data-stu-id="289f7-220">30</span></span> 

<span data-ttu-id="289f7-221">Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть поставлено в очередь в операционной системе узла в один момент времени.</span><span class="sxs-lookup"><span data-stu-id="289f7-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="289f7-222">Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.</span><span class="sxs-lookup"><span data-stu-id="289f7-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="289f7-223">**Windows XP и Windows Server 2003:**  Этот параметр не учитывается в Windows XP и Windows Server 2003 и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="289f7-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-224">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-225"><strong>Windows 2000: </strong>  64</span><span class="sxs-lookup"><span data-stu-id="289f7-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="289f7-226"><strong>Windows Vista:</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="289f7-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-227">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-228">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-229">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-230"><strong>Windows 2000:</strong>  8 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="289f7-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="289f7-231"><strong>Windows Vista:</strong>  0 – 65536</span><span class="sxs-lookup"><span data-stu-id="289f7-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-232">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-233">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-234">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-235">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-236">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-237">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-238">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-239">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-240">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-241">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-242">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-243">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-244">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-245">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-246">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-247">Все</span><span class="sxs-lookup"><span data-stu-id="289f7-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="289f7-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="289f7-249">164</span><span class="sxs-lookup"><span data-stu-id="289f7-249">164</span></span>  

<span data-ttu-id="289f7-250">Максимальное число байтов, которые могут быть сгруппированы для совместной операции чтения.</span><span class="sxs-lookup"><span data-stu-id="289f7-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-251">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-252">262144</span><span class="sxs-lookup"><span data-stu-id="289f7-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-253">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-254">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-255">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="289f7-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-257">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-258">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-259">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-260">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-261">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-262">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-263">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-264">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-265">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-266">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-267">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-268">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-269">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-270">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-271">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="289f7-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="289f7-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="289f7-274">165</span><span class="sxs-lookup"><span data-stu-id="289f7-274">165</span></span>  

<span data-ttu-id="289f7-275">Максимальное число байтов, которые могут быть сгруппированы для совместной операции записи.</span><span class="sxs-lookup"><span data-stu-id="289f7-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-276">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-277">393216</span><span class="sxs-lookup"><span data-stu-id="289f7-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-278">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-279">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-280">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="289f7-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-282">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-283">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-284">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-285">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-286">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-287">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-288">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-289">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-290">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-291">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-292">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-293">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-294">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-295">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-296">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="289f7-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="289f7-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="289f7-299">166</span><span class="sxs-lookup"><span data-stu-id="289f7-299">166</span></span>  

<span data-ttu-id="289f7-300">Максимальное число байтов, которое может быть гаппед для операции совместного ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="289f7-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-301">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-302">262144</span><span class="sxs-lookup"><span data-stu-id="289f7-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-303">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-304">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-305">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="289f7-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-307">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-308">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-309">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-310">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-311">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-312">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-313">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-314">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-315">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-316">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-317">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-318">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-319">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-320">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-321">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="289f7-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="289f7-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="289f7-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="289f7-324">167</span><span class="sxs-lookup"><span data-stu-id="289f7-324">167</span></span>  

<span data-ttu-id="289f7-325">Максимальное число байтов, которое может быть гаппед для совместной операции чтения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="289f7-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-326">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="289f7-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="289f7-327">393216</span><span class="sxs-lookup"><span data-stu-id="289f7-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-328">Тип:</span><span class="sxs-lookup"><span data-stu-id="289f7-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="289f7-329">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="289f7-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-330">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="289f7-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="289f7-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="289f7-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-332">Область.</span><span class="sxs-lookup"><span data-stu-id="289f7-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="289f7-333">Глобальный</span><span class="sxs-lookup"><span data-stu-id="289f7-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-334">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-335">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-336">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="289f7-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="289f7-337">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-338">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="289f7-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="289f7-339">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-340">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="289f7-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-341">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-342">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="289f7-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="289f7-343">Да</span><span class="sxs-lookup"><span data-stu-id="289f7-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-344">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="289f7-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="289f7-345">Нет</span><span class="sxs-lookup"><span data-stu-id="289f7-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-346">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="289f7-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="289f7-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="289f7-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="289f7-348">Требования</span><span class="sxs-lookup"><span data-stu-id="289f7-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289f7-349"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="289f7-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="289f7-350">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="289f7-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289f7-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="289f7-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="289f7-352">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="289f7-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289f7-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="289f7-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="289f7-354">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="289f7-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="289f7-355">См. также:</span><span class="sxs-lookup"><span data-stu-id="289f7-355">See Also</span></span>

[<span data-ttu-id="289f7-356">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="289f7-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="289f7-357">жетинит</span><span class="sxs-lookup"><span data-stu-id="289f7-357">JetInit</span></span>](./jetinit-function.md)
