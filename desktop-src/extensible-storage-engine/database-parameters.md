---
description: 'Дополнительные сведения: параметры базы данных'
title: Параметры базы данных
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155046"
---
# <a name="database-parameters"></a><span data-ttu-id="5f425-103">Параметры базы данных</span><span class="sxs-lookup"><span data-stu-id="5f425-103">Database Parameters</span></span>


<span data-ttu-id="5f425-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f425-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="5f425-105">Параметры базы данных</span><span class="sxs-lookup"><span data-stu-id="5f425-105">Database Parameters</span></span>

<span data-ttu-id="5f425-106">Этот раздел содержит параметры, используемые для базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="5f425-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="5f425-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="5f425-108">44</span><span class="sxs-lookup"><span data-stu-id="5f425-108">44</span></span>  

<span data-ttu-id="5f425-109">Этот параметр, если он задан, приведет к тому, что [жетинит](./jetinit-function.md) будет возвращать специальную ошибку при открытии базы данных или журнала транзакций из предыдущего выпуска ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="5f425-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="5f425-110">Эти ошибки:</span><span class="sxs-lookup"><span data-stu-id="5f425-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f425-111">Ошибка</span><span class="sxs-lookup"><span data-stu-id="5f425-111">Error</span></span></p></th>
<th><p><span data-ttu-id="5f425-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5f425-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="5f425-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="5f425-114">База данных и/или файлы журнала транзакций были созданы ядром СУБД Windows NT 3,51.</span><span class="sxs-lookup"><span data-stu-id="5f425-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="5f425-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="5f425-116">База данных и (или) файлы журнала транзакций были созданы ядром СУБД в тестовом выпуске до Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="5f425-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="5f425-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="5f425-118">База данных и (или) файлы журнала транзакций были созданы ядром СУБД Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="5f425-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-119">**Windows Vista:**  В Windows Vista и более поздних версиях этот параметр устарел и не влияет на работу ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="5f425-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-120">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-121">True</span><span class="sxs-lookup"><span data-stu-id="5f425-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-122">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="5f425-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-124">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-125">False, true</span><span class="sxs-lookup"><span data-stu-id="5f425-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-126">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-127">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-128">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-129">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-130">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-131">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-132">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-133">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-134">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-135">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-136">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-137">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-138">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-139">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-140">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-141">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="5f425-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="5f425-143">64</span><span class="sxs-lookup"><span data-stu-id="5f425-143">64</span></span>  

<span data-ttu-id="5f425-144">Этот параметр настраивает размер страницы для базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="5f425-145">Размер страницы — это наименьшая единица выделения пространства для файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="5f425-146">Размер страницы базы данных также очень важен, так как он задает верхний предел размера отдельной записи в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="5f425-147">**Примечание** . В настоящее время для каждого процесса поддерживается только один размер страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="5f425-148">Это означает, что если вы используете один процесс, который содержит различные приложения, использующие ядро СУБД, то все они должны согласовать размер страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-149">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-150">4096</span><span class="sxs-lookup"><span data-stu-id="5f425-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-151">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-152">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-153">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="5f425-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-155">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-156">Глобальный</span><span class="sxs-lookup"><span data-stu-id="5f425-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-157">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-158">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-159">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-160">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-161">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-162">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-163">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-164">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-165">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-166">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-167">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-168">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-169">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-170">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="5f425-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="5f425-172">18</span><span class="sxs-lookup"><span data-stu-id="5f425-172">18</span></span>  

<span data-ttu-id="5f425-173">Этот параметр управляет объемом пространства, добавляемого в файл базы данных каждый раз, когда его необходимо увеличивать, чтобы разместить больше данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="5f425-174">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-175">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-176">256</span><span class="sxs-lookup"><span data-stu-id="5f425-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-177">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-178">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-179">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-180">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="5f425-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-181">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-182">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-183">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-184">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-185">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-186">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-186">No</span></span></p>
<p><span data-ttu-id="5f425-187"><strong>Windows Vista:</strong>  Для Windows Vista и более поздних версий: Да</span><span class="sxs-lookup"><span data-stu-id="5f425-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-188">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-189">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-190">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-191">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-192">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-193">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-194">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-195">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-196">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-197">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="5f425-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="5f425-199">45</span><span class="sxs-lookup"><span data-stu-id="5f425-199">45</span></span>  

<span data-ttu-id="5f425-200">Если этот параметр имеет значение true, каждая база данных проверяется во время [жетаттачдатабасе](./jetattachdatabase-function.md) для индексов по ключевым столбцам Юникода, созданным с помощью более старой версии библиотеки NLS в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="5f425-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="5f425-201">Это необходимо сделать, так как ядро СУБД сохраняет ключи сортировки, созданные [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa) , а значения этих ключей сортировки изменяются с выпуска на выпуск.</span><span class="sxs-lookup"><span data-stu-id="5f425-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="5f425-202">Если в этом состоянии обнаруживается первичный индекс, то [жетаттачдатабасе](./jetattachdatabase-function.md) всегда завершается с JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="5f425-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="5f425-203">Если в этом состоянии обнаружены какие-либо вторичные индексы, возможны два результата.</span><span class="sxs-lookup"><span data-stu-id="5f425-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="5f425-204">Если JET_bitDbDeleteCorruptIndexes был передан в [жетаттачдатабасе](./jetattachdatabase-function.md) , эти индексы будут удалены, а JET_wrnCorruptIndexDeleted будут возвращены из [жетаттачдатабасе](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5f425-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="5f425-205">Эти индексы потребуется создать повторно в приложении.</span><span class="sxs-lookup"><span data-stu-id="5f425-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="5f425-206">Если JET_bitDbDeleteCorruptIndexes не был передан в [жетаттачдатабасе](./jetattachdatabase-function.md) , вызов завершится с JET_errSecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="5f425-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="5f425-207">**Примечание** . Настоятельно рекомендуется, чтобы для этого параметра было задано значение true для приложения.</span><span class="sxs-lookup"><span data-stu-id="5f425-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="5f425-208">**Примечание** . Настоятельно рекомендуется, чтобы приложения не использовали ключевые столбцы Юникода в индексах первичного ключа (кластеризованных).</span><span class="sxs-lookup"><span data-stu-id="5f425-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-209">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f425-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-211">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-212">Логическое</span><span class="sxs-lookup"><span data-stu-id="5f425-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-213">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-214">False, true</span><span class="sxs-lookup"><span data-stu-id="5f425-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-215">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-216">Глобальный</span><span class="sxs-lookup"><span data-stu-id="5f425-216">Global</span></span></p>
<p><span data-ttu-id="5f425-217"><strong>Windows Vista:</strong>  Для Windows Vista и более поздних версий: экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-218">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-219">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-220">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-221">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-222">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-223">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-224">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-225">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-226">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-227">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-228">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-229">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-230">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-231">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="5f425-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="5f425-233">54</span><span class="sxs-lookup"><span data-stu-id="5f425-233">54</span></span>  

<span data-ttu-id="5f425-234">Если этот параметр имеет значение true, то ядро СУБД может автоматически очищать индексы по ключевым столбцам Юникода во время [жетинит](./jetinit-function.md) , чтобы избежать изменений в формате базы данных, вызванных изменениями в библиотеке NLS в Windows.</span><span class="sxs-lookup"><span data-stu-id="5f425-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="5f425-235">Такие изменения вносятся в библиотеку NLS для добавления поддержки новых языков, добавления недостающих символов к языку, добавления порядка сортировки к языку или исправления ошибок в порядке следования языка.</span><span class="sxs-lookup"><span data-stu-id="5f425-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="5f425-236">Эти изменения влияют на ключи сортировки, созданные [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa) , которые сохраняются ядром СУБД в качестве компонентов ключей индекса.</span><span class="sxs-lookup"><span data-stu-id="5f425-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="5f425-237">Важно понимать, что изменения в индексе могут быть настолько замечательными, что добавочная очистка невозможна.</span><span class="sxs-lookup"><span data-stu-id="5f425-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="5f425-238">В этом случае индекс будет обрабатываться, как предписано **JET_paramEnableIndexChecking**.</span><span class="sxs-lookup"><span data-stu-id="5f425-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="5f425-239">**Примечание** . Настоятельно рекомендуется, чтобы этот параметр и **JET_paramEnableIndexChecking** были установлены в **значение true** приложением.</span><span class="sxs-lookup"><span data-stu-id="5f425-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-240">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-241">True</span><span class="sxs-lookup"><span data-stu-id="5f425-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-242">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-243">Логическое</span><span class="sxs-lookup"><span data-stu-id="5f425-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-244">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-245">False, true</span><span class="sxs-lookup"><span data-stu-id="5f425-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-246">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-247">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-248">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-249">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-250">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-251">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-251">No</span></span></p>
<p><span data-ttu-id="5f425-252"><strong>Windows Vista:</strong>  Для Windows Vista и более поздних версий: Да</span><span class="sxs-lookup"><span data-stu-id="5f425-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-253">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-254">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-255">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-256">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-257">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-258">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-259">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-260">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-261">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-262">Windows Server 2003 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5f425-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="5f425-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="5f425-264">102</span><span class="sxs-lookup"><span data-stu-id="5f425-264">102</span></span>  

<span data-ttu-id="5f425-265">Если этот параметр имеет значение true, то разрешается открывать только одну базу данных с помощью [жетопендатабасе](./jetopendatabase-function.md) в заданном сеансе одновременно.</span><span class="sxs-lookup"><span data-stu-id="5f425-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="5f425-266">Временная база данных исключается из этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="5f425-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="5f425-267">**Windows XP и Windows Server 2003:**  Этот параметр доступен только для записи в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f425-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="5f425-268">**Windows Vista:**  Этот параметр обычно работает в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5f425-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="5f425-269">**Примечание**  .  Этот параметр доступен только для записи.</span><span class="sxs-lookup"><span data-stu-id="5f425-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-270">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f425-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-272">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-273">Логическое</span><span class="sxs-lookup"><span data-stu-id="5f425-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-274">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-275">False, true</span><span class="sxs-lookup"><span data-stu-id="5f425-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-276">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-277">Глобальный</span><span class="sxs-lookup"><span data-stu-id="5f425-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-278">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-279">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-279">No</span></span></p>
<p><span data-ttu-id="5f425-280"><strong>Windows Vista:</strong>  Для Windows Vista и более поздних версий: Да</span><span class="sxs-lookup"><span data-stu-id="5f425-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-281">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-282">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-283">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-284">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-285">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-286">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-287">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-288">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-289">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-290">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-291">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-292">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5f425-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="5f425-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="5f425-294">35</span><span class="sxs-lookup"><span data-stu-id="5f425-294">35</span></span>  

<span data-ttu-id="5f425-295">Этот параметр управляет поведением оперативной дефрагментации при запуске с помощью [жетдефрагмент](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="5f425-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="5f425-296">Дополнительные сведения см. в разделе [жетдефрагмент](./jetdefragment-function.md) .</span><span class="sxs-lookup"><span data-stu-id="5f425-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="5f425-297">Windows 2000: в Windows 2000 этот параметр был простым логическим, который будет выполнять дефрагментацию в оперативном режиме при запуске [жетдефрагмент](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="5f425-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="5f425-298">Если задано **значение true**, оперативная дефрагментация будет выполняться для записей каждой таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="5f425-299">**Windows XP:**  В Windows XP и более поздних версиях для этого параметра можно задать один или несколько следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="5f425-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f425-300">Параметр</span><span class="sxs-lookup"><span data-stu-id="5f425-300">Option</span></span></p></th>
<th><p><span data-ttu-id="5f425-301">Описание</span><span class="sxs-lookup"><span data-stu-id="5f425-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="5f425-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="5f425-303">Не выполнять оперативную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="5f425-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="5f425-304">Это двоичный эквивалент параметра Windows 2000, который имеет значение false для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5f425-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="5f425-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="5f425-306">Выполнить полную оперативную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="5f425-306">Perform full online defragmentation.</span></span> <span data-ttu-id="5f425-307">Это двоичное значение, эквивалентное значению параметра Windows 2000 true для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5f425-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="5f425-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="5f425-309">Выполняет оперативную дефрагментацию записей каждой таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="5f425-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="5f425-311">Выполняет оперативную дефрагментацию деревьев пространства каждой таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="5f425-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="5f425-313">Этот параметр используется для поддержки инфраструктуры Microsoft Exchange и не предназначен для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="5f425-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="5f425-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="5f425-315">Выполнить полную оперативную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="5f425-315">Perform full online defragmentation.</span></span> <span data-ttu-id="5f425-316">Это концептуальный эквивалент параметра Windows 2000 true для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5f425-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-317">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-318"><strong>Windows 2000:</strong>  Условия</span><span class="sxs-lookup"><span data-stu-id="5f425-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="5f425-319"><strong>Windows XP: для Windows XP и более поздних версий:</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="5f425-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-320">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-321"><strong>Windows 2000:</strong>  Логическая</span><span class="sxs-lookup"><span data-stu-id="5f425-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="5f425-322"><strong>Windows XP и более поздние версии:</strong>  JET_GRBIT (целое число)</span><span class="sxs-lookup"><span data-stu-id="5f425-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-323">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-324"><strong>Windows 2000:</strong>  False, true</span><span class="sxs-lookup"><span data-stu-id="5f425-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="5f425-325"><strong>Windows XP и более поздние версии:</strong>  0 — JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="5f425-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-326">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-327">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-328">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-329">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-330">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-331">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-332">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-333">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-334">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-335">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-336">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-337">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-338">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-339">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-340">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-341">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="5f425-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="5f425-343">20</span><span class="sxs-lookup"><span data-stu-id="5f425-343">20</span></span>  

<span data-ttu-id="5f425-344">Этот параметр является пороговое значение, которое ядро СУБД использует для управления фрагментацией свободного пространства.</span><span class="sxs-lookup"><span data-stu-id="5f425-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="5f425-345">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-346">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-347">8</span><span class="sxs-lookup"><span data-stu-id="5f425-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-348">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-349">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-350">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-351">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="5f425-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-352">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-353">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-354">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-355">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-356">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-357">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-358">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-359">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-360">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-361">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-362">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-363">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-364">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-365">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-366">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-367">Все</span><span class="sxs-lookup"><span data-stu-id="5f425-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="5f425-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="5f425-369">78</span><span class="sxs-lookup"><span data-stu-id="5f425-369">78</span></span>

<span data-ttu-id="5f425-370">Этот параметр определяет, как агрессивно диспетчер кэша страниц базы данных будет записывать страницу базы данных, преобразованную в формат "на месте".</span><span class="sxs-lookup"><span data-stu-id="5f425-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="5f425-371">Эти преобразования формата происходят на лету, когда страницы загружаются из базы данных, созданной с помощью ядра СУБД Windows 2000, но используемой в Windows XP или более поздней версии ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="5f425-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-372">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-373">1</span><span class="sxs-lookup"><span data-stu-id="5f425-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-374">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-375">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-376">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-377">0-3</span><span class="sxs-lookup"><span data-stu-id="5f425-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-378">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-379">Глобальный</span><span class="sxs-lookup"><span data-stu-id="5f425-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-380">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-381">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-382">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-383">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-384">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-385">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-386">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-387">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-388">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-389">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-390">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-391">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-392">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-393">Windows XP и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5f425-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="5f425-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="5f425-395">153</span><span class="sxs-lookup"><span data-stu-id="5f425-395">153</span></span>  

<span data-ttu-id="5f425-396">Задержка (в журналах) в журнале TIP/COMMITTED, зафиксированной для задержки очистки страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f425-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="5f425-397">Включение этой задержки может привести к восстановлению базы данных в случае катастрофической потери самого последнего файла журнала.</span><span class="sxs-lookup"><span data-stu-id="5f425-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="5f425-398">См. JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="5f425-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-399">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-400">0</span><span class="sxs-lookup"><span data-stu-id="5f425-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-401">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-402">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-403">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="5f425-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-405">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-406">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-407">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-408">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-409">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-410">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-411">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-412">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-413">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-414">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-415">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-416">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-417">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-418">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-419">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f425-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="5f425-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="5f425-422">160</span><span class="sxs-lookup"><span data-stu-id="5f425-422">160</span></span>  

<span data-ttu-id="5f425-423">Включить/отключить автоматическое последовательное дефрагментацию в сбалансированном дереве.</span><span class="sxs-lookup"><span data-stu-id="5f425-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-424">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-425">1</span><span class="sxs-lookup"><span data-stu-id="5f425-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-426">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-427">Логическое</span><span class="sxs-lookup"><span data-stu-id="5f425-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-428">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-429">0—1</span><span class="sxs-lookup"><span data-stu-id="5f425-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-430">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-431">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-432">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-433">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-434">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-435">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-436">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-437">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-438">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-439">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-440">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-441">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-442">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-443">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-444">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f425-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="5f425-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="5f425-447">161</span><span class="sxs-lookup"><span data-stu-id="5f425-447">161</span></span>  

<span data-ttu-id="5f425-448">Определяет частоту проверки плотности сбалансированного дерева.</span><span class="sxs-lookup"><span data-stu-id="5f425-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-449">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-450">10</span><span class="sxs-lookup"><span data-stu-id="5f425-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-451">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-452">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-453">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-454">0 — максимальное целое число</span><span class="sxs-lookup"><span data-stu-id="5f425-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-455">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-456">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="5f425-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-457">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-458">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-459">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-460">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-461">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-462">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-463">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-464">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-465">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-466">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-467">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-468">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-469">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f425-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f425-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="5f425-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="5f425-472">162</span><span class="sxs-lookup"><span data-stu-id="5f425-472">162</span></span>  

<span data-ttu-id="5f425-473">Максимальное время в миллисекундах, в течение которого механизм регулирования ввода-вывода предоставляет задачу для выполнения, чтобы считаться "завершенным".</span><span class="sxs-lookup"><span data-stu-id="5f425-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-474">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5f425-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="5f425-475">125</span><span class="sxs-lookup"><span data-stu-id="5f425-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-476">Тип:</span><span class="sxs-lookup"><span data-stu-id="5f425-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="5f425-477">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5f425-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-478">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="5f425-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="5f425-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="5f425-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-480">Область.</span><span class="sxs-lookup"><span data-stu-id="5f425-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="5f425-481">Глобальный</span><span class="sxs-lookup"><span data-stu-id="5f425-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-482">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-483">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-484">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="5f425-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="5f425-485">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-486">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="5f425-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="5f425-487">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-488">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="5f425-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-489">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-490">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="5f425-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="5f425-491">Да</span><span class="sxs-lookup"><span data-stu-id="5f425-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-492">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="5f425-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="5f425-493">Нет</span><span class="sxs-lookup"><span data-stu-id="5f425-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-494">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="5f425-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="5f425-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f425-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="5f425-496">Требования</span><span class="sxs-lookup"><span data-stu-id="5f425-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f425-497"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="5f425-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f425-498">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5f425-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f425-499"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5f425-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f425-500">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5f425-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f425-501"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5f425-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f425-502">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5f425-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5f425-503">См. также:</span><span class="sxs-lookup"><span data-stu-id="5f425-503">See Also</span></span>

[<span data-ttu-id="5f425-504">жетаттачдатабасе</span><span class="sxs-lookup"><span data-stu-id="5f425-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="5f425-505">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="5f425-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="5f425-506">жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="5f425-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="5f425-507">жетинит</span><span class="sxs-lookup"><span data-stu-id="5f425-507">JetInit</span></span>](./jetinit-function.md)
