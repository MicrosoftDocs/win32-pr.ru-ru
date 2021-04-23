---
description: 'Дополнительные сведения: временные параметры базы данных'
title: Параметры временной базы данных
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272112"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="f2a67-103">Параметры временной базы данных</span><span class="sxs-lookup"><span data-stu-id="f2a67-103">Temporary Database Parameters</span></span>


<span data-ttu-id="f2a67-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2a67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="f2a67-105">Параметры временной базы данных</span><span class="sxs-lookup"><span data-stu-id="f2a67-105">Temporary Database Parameters</span></span>

<span data-ttu-id="f2a67-106">Этот раздел содержит параметры, используемые для временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2a67-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="f2a67-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="f2a67-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="f2a67-108">46</span><span class="sxs-lookup"><span data-stu-id="f2a67-108">46</span></span>  

<span data-ttu-id="f2a67-109">Этот параметр управляет использованием транзакций во временных таблицах.</span><span class="sxs-lookup"><span data-stu-id="f2a67-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="f2a67-110">Если этот параметр имеет значение false, временные таблицы будут работать быстрее, но откат всех обновлений, внесенных в транзакцию, будет невозможен.</span><span class="sxs-lookup"><span data-stu-id="f2a67-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-111">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="f2a67-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-112">True</span><span class="sxs-lookup"><span data-stu-id="f2a67-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="f2a67-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-114">Логическое</span><span class="sxs-lookup"><span data-stu-id="f2a67-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-115">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="f2a67-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-116">False, true</span><span class="sxs-lookup"><span data-stu-id="f2a67-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-117">Область.</span><span class="sxs-lookup"><span data-stu-id="f2a67-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-118">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="f2a67-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-119">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-120">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-121">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-122">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-123">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="f2a67-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-124">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-125">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-126">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-127">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-128">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-129">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="f2a67-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-130">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-131">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="f2a67-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-132">Все</span><span class="sxs-lookup"><span data-stu-id="f2a67-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2a67-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="f2a67-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="f2a67-134">19</span><span class="sxs-lookup"><span data-stu-id="f2a67-134">19</span></span>  

<span data-ttu-id="f2a67-135">Этот параметр определяет начальный размер временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2a67-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="f2a67-136">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2a67-136">The size is in database pages.</span></span> <span data-ttu-id="f2a67-137">Нулевой размер означает, что следует использовать стандартный размер обычной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2a67-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="f2a67-138">Часто нежелательно, чтобы небольшие приложения настроили временную базу данных как можно меньше.</span><span class="sxs-lookup"><span data-stu-id="f2a67-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="f2a67-139">Если задать для этого параметра значение 14, будет достигнута наименьшая временная база данных.</span><span class="sxs-lookup"><span data-stu-id="f2a67-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="f2a67-140">Обратите внимание, что можно также полностью устранить временную базу данных, установив значение **JET_paramMaxTemporaryTables** равным нулю.</span><span class="sxs-lookup"><span data-stu-id="f2a67-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-141">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="f2a67-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-142">0</span><span class="sxs-lookup"><span data-stu-id="f2a67-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-143">Тип:</span><span class="sxs-lookup"><span data-stu-id="f2a67-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-144">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="f2a67-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-145">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="f2a67-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-146">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f2a67-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-147">Область.</span><span class="sxs-lookup"><span data-stu-id="f2a67-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-148">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="f2a67-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-149">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-150">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-151">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-152">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-153">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="f2a67-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-154">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-155">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-156">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-157">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-158">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-159">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="f2a67-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-160">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-161">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="f2a67-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-162">Все</span><span class="sxs-lookup"><span data-stu-id="f2a67-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2a67-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="f2a67-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="f2a67-164">1</span><span class="sxs-lookup"><span data-stu-id="f2a67-164">1</span></span>  

<span data-ttu-id="f2a67-165">Этот параметр указывает относительный или абсолютный путь файловой системы к папке или файлу, который будет содержать временную базу данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f2a67-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="f2a67-166">Если путь к папке, в которой будет находиться временная база данных, должен быть завершен символом обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="f2a67-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="f2a67-167">Временная база данных используется для хранения временных данных, создаваемых в процессе обработки вызовов сведений API ESE, создания индексов или хранения содержимого временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2a67-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="f2a67-168">**Примечание**  .  Если указан относительный путь, он будет относиться к текущему рабочему каталогу процесса, в котором размещается приложение, использующее ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="f2a67-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-169">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="f2a67-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-170">&quot;TMP. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="f2a67-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-171">Тип:</span><span class="sxs-lookup"><span data-stu-id="f2a67-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-172">Path (строка)</span><span class="sxs-lookup"><span data-stu-id="f2a67-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-173">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="f2a67-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-174">0 – 247 символов</span><span class="sxs-lookup"><span data-stu-id="f2a67-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-175">Область.</span><span class="sxs-lookup"><span data-stu-id="f2a67-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-176">Экземпляр</span><span class="sxs-lookup"><span data-stu-id="f2a67-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-177">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-178">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-179">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="f2a67-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-180">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-181">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="f2a67-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-182">Да</span><span class="sxs-lookup"><span data-stu-id="f2a67-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-183">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-184">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-185">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="f2a67-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-186">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-187">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="f2a67-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-188">Нет</span><span class="sxs-lookup"><span data-stu-id="f2a67-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-189">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="f2a67-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f2a67-190">Все</span><span class="sxs-lookup"><span data-stu-id="f2a67-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f2a67-191">Требования</span><span class="sxs-lookup"><span data-stu-id="f2a67-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-192"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f2a67-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2a67-193">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f2a67-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2a67-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f2a67-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2a67-195">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f2a67-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2a67-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f2a67-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2a67-197">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f2a67-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f2a67-198">См. также:</span><span class="sxs-lookup"><span data-stu-id="f2a67-198">See Also</span></span>

[<span data-ttu-id="f2a67-199">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="f2a67-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="f2a67-200">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="f2a67-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f2a67-201">жетинит</span><span class="sxs-lookup"><span data-stu-id="f2a67-201">JetInit</span></span>](./jetinit-function.md)
