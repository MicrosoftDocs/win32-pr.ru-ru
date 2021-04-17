---
description: 'Дополнительные сведения: коды ошибок расширенного подсистемы хранилища'
title: Коды ошибок расширенного подсистемы хранилища
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712739"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="d0304-103">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d0304-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="d0304-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d0304-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="d0304-105">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d0304-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="d0304-106">Следующие коды ошибок (flags) используются функциями в API-интерфейсе расширяемого механизма хранилища.</span><span class="sxs-lookup"><span data-stu-id="d0304-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="d0304-107">Значение [JET_ERR](./jet-err.md) , равное нулю, должно интерпретироваться как Success.</span><span class="sxs-lookup"><span data-stu-id="d0304-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0304-108">Успешно</span><span class="sxs-lookup"><span data-stu-id="d0304-108">Success</span></span></p></th>
<th><p><span data-ttu-id="d0304-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d0304-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0304-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="d0304-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="d0304-111">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d0304-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0304-112">Значение [JET_ERR](./jet-err.md) , большее нуля, должно интерпретироваться как предупреждение.</span><span class="sxs-lookup"><span data-stu-id="d0304-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0304-113">Предупреждения</span><span class="sxs-lookup"><span data-stu-id="d0304-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="d0304-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d0304-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0304-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="d0304-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="d0304-116">321</span><span class="sxs-lookup"><span data-stu-id="d0304-116">321</span></span></p></td>
<td><p><span data-ttu-id="d0304-117">Хранилище версий все еще активно.</span><span class="sxs-lookup"><span data-stu-id="d0304-117">The version store is still active.</span></span> <span data-ttu-id="d0304-118">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d0304-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="d0304-120">345</span><span class="sxs-lookup"><span data-stu-id="d0304-120">345</span></span></p></td>
<td><p><span data-ttu-id="d0304-121">Поиск в неуникальном индексе подает уникальный ключ.</span><span class="sxs-lookup"><span data-stu-id="d0304-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="d0304-122">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="d0304-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="d0304-124">406</span><span class="sxs-lookup"><span data-stu-id="d0304-124">406</span></span></p></td>
<td><p><span data-ttu-id="d0304-125">Столбец базы данных имеет разделенное длинное значение.</span><span class="sxs-lookup"><span data-stu-id="d0304-125">A database column is a separated long value.</span></span> <span data-ttu-id="d0304-126">Эта ошибка возвращается диспетчером записей.</span><span class="sxs-lookup"><span data-stu-id="d0304-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="d0304-128">558</span><span class="sxs-lookup"><span data-stu-id="d0304-128">558</span></span></p></td>
<td><p><span data-ttu-id="d0304-129">Существующий файл журнала имеет неправильную подпись.</span><span class="sxs-lookup"><span data-stu-id="d0304-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="d0304-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="d0304-131">559</span><span class="sxs-lookup"><span data-stu-id="d0304-131">559</span></span></p></td>
<td><p><span data-ttu-id="d0304-132">Существующий файл журнала не является смежным.</span><span class="sxs-lookup"><span data-stu-id="d0304-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="d0304-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="d0304-134">564</span><span class="sxs-lookup"><span data-stu-id="d0304-134">564</span></span></p></td>
<td><p><span data-ttu-id="d0304-135">Эта ошибка относится только к внутреннему использованию.</span><span class="sxs-lookup"><span data-stu-id="d0304-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="d0304-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="d0304-137">578</span><span class="sxs-lookup"><span data-stu-id="d0304-137">578</span></span></p></td>
<td><p><span data-ttu-id="d0304-138">TargetInstance, указанный для восстановления, работает.</span><span class="sxs-lookup"><span data-stu-id="d0304-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="d0304-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="d0304-140">595</span><span class="sxs-lookup"><span data-stu-id="d0304-140">595</span></span></p></td>
<td><p><span data-ttu-id="d0304-141">Повреждение базы данных восстановлено.</span><span class="sxs-lookup"><span data-stu-id="d0304-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="d0304-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="d0304-143">1004</span><span class="sxs-lookup"><span data-stu-id="d0304-143">1004</span></span></p></td>
<td><p><span data-ttu-id="d0304-144">Столбец имеет значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="d0304-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="d0304-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="d0304-146">1006</span><span class="sxs-lookup"><span data-stu-id="d0304-146">1006</span></span></p></td>
<td><p><span data-ttu-id="d0304-147">Буфер слишком мал для данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="d0304-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="d0304-149">1007</span><span class="sxs-lookup"><span data-stu-id="d0304-149">1007</span></span></p></td>
<td><p><span data-ttu-id="d0304-150">База данных уже присоединена.</span><span class="sxs-lookup"><span data-stu-id="d0304-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="d0304-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="d0304-152">1009</span><span class="sxs-lookup"><span data-stu-id="d0304-152">1009</span></span></p></td>
<td><p><span data-ttu-id="d0304-153">Для выполнения сортировки не хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="d0304-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="d0304-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="d0304-155">1039</span><span class="sxs-lookup"><span data-stu-id="d0304-155">1039</span></span></p></td>
<td><p><span data-ttu-id="d0304-156">Точное совпадение не найдено во время поиска.</span><span class="sxs-lookup"><span data-stu-id="d0304-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="d0304-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="d0304-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="d0304-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="d0304-159">Точное совпадение не найдено во время поиска.</span><span class="sxs-lookup"><span data-stu-id="d0304-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="d0304-160">Эта ошибка возвращается диспетчером записей.</span><span class="sxs-lookup"><span data-stu-id="d0304-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="d0304-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="d0304-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="d0304-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="d0304-163">Точное совпадение не найдено во время поиска.</span><span class="sxs-lookup"><span data-stu-id="d0304-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="d0304-164">Эта ошибка возвращается диспетчером записей.</span><span class="sxs-lookup"><span data-stu-id="d0304-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d0304-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="d0304-166">1055</span><span class="sxs-lookup"><span data-stu-id="d0304-166">1055</span></span></p></td>
<td><p><span data-ttu-id="d0304-167">Расширенные сведения об ошибках отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d0304-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="d0304-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="d0304-169">1058</span><span class="sxs-lookup"><span data-stu-id="d0304-169">1058</span></span></p></td>
<td><p><span data-ttu-id="d0304-170">Неактивное действие не выполнено.</span><span class="sxs-lookup"><span data-stu-id="d0304-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="d0304-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="d0304-172">1067.</span><span class="sxs-lookup"><span data-stu-id="d0304-172">1067</span></span></p></td>
<td><p><span data-ttu-id="d0304-173">Отсутствует блокировка записи на уровне транзакций 0.</span><span class="sxs-lookup"><span data-stu-id="d0304-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="d0304-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="d0304-175">1068</span><span class="sxs-lookup"><span data-stu-id="d0304-175">1068</span></span></p></td>
<td><p><span data-ttu-id="d0304-176">Для столбца задается значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="d0304-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="d0304-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="d0304-178">1301</span><span class="sxs-lookup"><span data-stu-id="d0304-178">1301</span></span></p></td>
<td><p><span data-ttu-id="d0304-179">Была открыта пустая таблица.</span><span class="sxs-lookup"><span data-stu-id="d0304-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="d0304-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="d0304-181">1327</span><span class="sxs-lookup"><span data-stu-id="d0304-181">1327</span></span></p></td>
<td><p><span data-ttu-id="d0304-182">Для очистки системы в таблице открыт курсор.</span><span class="sxs-lookup"><span data-stu-id="d0304-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="d0304-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="d0304-184">1415</span><span class="sxs-lookup"><span data-stu-id="d0304-184">1415</span></span></p></td>
<td><p><span data-ttu-id="d0304-185">Неактуальный индекс должен быть удален.</span><span class="sxs-lookup"><span data-stu-id="d0304-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="d0304-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="d0304-187">1512</span><span class="sxs-lookup"><span data-stu-id="d0304-187">1512</span></span></p></td>
<td><p><span data-ttu-id="d0304-188">Максимальная длина слишком велика и была усечена.</span><span class="sxs-lookup"><span data-stu-id="d0304-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="d0304-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="d0304-190">1520</span><span class="sxs-lookup"><span data-stu-id="d0304-190">1520</span></span></p></td>
<td><p><span data-ttu-id="d0304-191">Значение большого двоичного объекта было перемещено из записи в отдельное хранилище больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d0304-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="d0304-192"><strong>Примечание</strong> . Эта ошибка относится только к внутреннему использованию.</span><span class="sxs-lookup"><span data-stu-id="d0304-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="d0304-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="d0304-194">1531</span><span class="sxs-lookup"><span data-stu-id="d0304-194">1531</span></span></p></td>
<td><p><span data-ttu-id="d0304-195">Значения столбца не были возвращены, так как соответствующий идентификатор столбца или элемент <em>итагсекуенце</em> из структуры <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> , запрошенной для перечисления, имел значение null.</span><span class="sxs-lookup"><span data-stu-id="d0304-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="d0304-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="d0304-197">1532</span><span class="sxs-lookup"><span data-stu-id="d0304-197">1532</span></span></p></td>
<td><p><span data-ttu-id="d0304-198">Значения столбца не были возвращены, так как их не удалось перестроить из существующих данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="d0304-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="d0304-200">1533</span><span class="sxs-lookup"><span data-stu-id="d0304-200">1533</span></span></p></td>
<td><p><span data-ttu-id="d0304-201">Существующие значения столбца не были запрошены для перечисления.</span><span class="sxs-lookup"><span data-stu-id="d0304-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="d0304-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="d0304-203">1534</span><span class="sxs-lookup"><span data-stu-id="d0304-203">1534</span></span></p></td>
<td><p><span data-ttu-id="d0304-204">Значение столбца было усечено по запрошенному пределу размера во время перечисления.</span><span class="sxs-lookup"><span data-stu-id="d0304-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="d0304-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="d0304-206">1535</span><span class="sxs-lookup"><span data-stu-id="d0304-206">1535</span></span></p></td>
<td><p><span data-ttu-id="d0304-207">Значения столбца существуют, но не возвращены запросом.</span><span class="sxs-lookup"><span data-stu-id="d0304-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="d0304-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="d0304-209">1536</span><span class="sxs-lookup"><span data-stu-id="d0304-209">1536</span></span></p></td>
<td><p><span data-ttu-id="d0304-210">Значение столбца было возвращено в JET_COLUMNENUM в результате задания JET_bitEnumerateCompressOutput.</span><span class="sxs-lookup"><span data-stu-id="d0304-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="d0304-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="d0304-212">1537</span><span class="sxs-lookup"><span data-stu-id="d0304-212">1537</span></span></p></td>
<td><p><span data-ttu-id="d0304-213">Значение столбца устанавливается в значение по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="d0304-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="d0304-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="d0304-215">1610</span><span class="sxs-lookup"><span data-stu-id="d0304-215">1610</span></span></p></td>
<td><p><span data-ttu-id="d0304-216">Данные были изменены.</span><span class="sxs-lookup"><span data-stu-id="d0304-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="d0304-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="d0304-218">1618</span><span class="sxs-lookup"><span data-stu-id="d0304-218">1618</span></span></p></td>
<td><p><span data-ttu-id="d0304-219">Используется новый ключ.</span><span class="sxs-lookup"><span data-stu-id="d0304-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="d0304-221">1813</span><span class="sxs-lookup"><span data-stu-id="d0304-221">1813</span></span></p></td>
<td><p><span data-ttu-id="d0304-222">Файл базы данных доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d0304-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="d0304-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="d0304-224">1908</span><span class="sxs-lookup"><span data-stu-id="d0304-224">1908</span></span></p></td>
<td><p><span data-ttu-id="d0304-225">Неактивный реестр заполнен.</span><span class="sxs-lookup"><span data-stu-id="d0304-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="d0304-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="d0304-227">2000</span><span class="sxs-lookup"><span data-stu-id="d0304-227">2000</span></span></p></td>
<td><p><span data-ttu-id="d0304-228">В указанной базе данных уже запущена оперативная дефрагментация.</span><span class="sxs-lookup"><span data-stu-id="d0304-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="d0304-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="d0304-230">2001</span><span class="sxs-lookup"><span data-stu-id="d0304-230">2001</span></span></p></td>
<td><p><span data-ttu-id="d0304-231">В указанной базе данных не запущена оперативная дефрагментация.</span><span class="sxs-lookup"><span data-stu-id="d0304-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="d0304-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="d0304-233">2100</span><span class="sxs-lookup"><span data-stu-id="d0304-233">2100</span></span></p></td>
<td><p><span data-ttu-id="d0304-234">Регистрация несуществующей функции обратного вызова отменена.</span><span class="sxs-lookup"><span data-stu-id="d0304-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0304-235">Значение [JET_ERR](./jet-err.md) , меньшее нуля, должно интерпретироваться как ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0304-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0304-236">ошибки</span><span class="sxs-lookup"><span data-stu-id="d0304-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="d0304-237">Описание</span><span class="sxs-lookup"><span data-stu-id="d0304-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0304-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="d0304-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="d0304-239">-1</span><span class="sxs-lookup"><span data-stu-id="d0304-239">-1</span></span></p></td>
<td><p><span data-ttu-id="d0304-240">Функция еще не реализована.</span><span class="sxs-lookup"><span data-stu-id="d0304-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="d0304-242">–100</span><span class="sxs-lookup"><span data-stu-id="d0304-242">-100</span></span></p></td>
<td><p><span data-ttu-id="d0304-243">Не удалось выполнить симулятор сбоя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0304-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="d0304-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="d0304-245">–101</span><span class="sxs-lookup"><span data-stu-id="d0304-245">-101</span></span></p></td>
<td><p><span data-ttu-id="d0304-246">Симулятор сбоя ресурса не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="d0304-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="d0304-247">JET_errFileClose</span></span><br />
<span data-ttu-id="d0304-248">–102</span><span class="sxs-lookup"><span data-stu-id="d0304-248">-102</span></span></p></td>
<td><p><span data-ttu-id="d0304-249">Не удалось закрыть файл.</span><span class="sxs-lookup"><span data-stu-id="d0304-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="d0304-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="d0304-251">-103</span><span class="sxs-lookup"><span data-stu-id="d0304-251">-103</span></span></p></td>
<td><p><span data-ttu-id="d0304-252">Не удалось запустить поток.</span><span class="sxs-lookup"><span data-stu-id="d0304-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="d0304-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="d0304-254">-105</span><span class="sxs-lookup"><span data-stu-id="d0304-254">-105</span></span></p></td>
<td><p><span data-ttu-id="d0304-255">Система занята из-за слишком большого количества IOs.</span><span class="sxs-lookup"><span data-stu-id="d0304-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="d0304-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="d0304-257">-106</span><span class="sxs-lookup"><span data-stu-id="d0304-257">-106</span></span></p></td>
<td><p><span data-ttu-id="d0304-258">Не удалось выполнить запрошенную асинхронную задачу.</span><span class="sxs-lookup"><span data-stu-id="d0304-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="d0304-259">JET_errInternalError</span></span><br />
<span data-ttu-id="d0304-260">-107</span><span class="sxs-lookup"><span data-stu-id="d0304-260">-107</span></span></p></td>
<td><p><span data-ttu-id="d0304-261">Произошла неустранимая внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0304-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="d0304-263">— 255</span><span class="sxs-lookup"><span data-stu-id="d0304-263">-255</span></span></p></td>
<td><p><span data-ttu-id="d0304-264">Неправильно заданы зависимости буфера, и произошла ошибка восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="d0304-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="d0304-266">— 322</span><span class="sxs-lookup"><span data-stu-id="d0304-266">-322</span></span></p></td>
<td><p><span data-ttu-id="d0304-267">Версия уже существовала, и произошла ошибка восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="d0304-268">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="d0304-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="d0304-270">— 323</span><span class="sxs-lookup"><span data-stu-id="d0304-270">-323</span></span></p></td>
<td><p><span data-ttu-id="d0304-271">Достигнута граница страницы.</span><span class="sxs-lookup"><span data-stu-id="d0304-271">The page boundary has been reached.</span></span> <span data-ttu-id="d0304-272">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="d0304-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="d0304-274">— 324</span><span class="sxs-lookup"><span data-stu-id="d0304-274">-324</span></span></p></td>
<td><p><span data-ttu-id="d0304-275">Достигнута граница ключа.</span><span class="sxs-lookup"><span data-stu-id="d0304-275">The key boundary has been reached.</span></span> <span data-ttu-id="d0304-276">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="d0304-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="d0304-278">— 327</span><span class="sxs-lookup"><span data-stu-id="d0304-278">-327</span></span></p></td>
<td><p><span data-ttu-id="d0304-279">База данных повреждена.</span><span class="sxs-lookup"><span data-stu-id="d0304-279">The database is corrupt.</span></span> <span data-ttu-id="d0304-280">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="d0304-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="d0304-282">— 328</span><span class="sxs-lookup"><span data-stu-id="d0304-282">-328</span></span></p></td>
<td><p><span data-ttu-id="d0304-283">Закладка не имеет соответствующего адреса в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="d0304-284">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="d0304-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="d0304-286">— 334</span><span class="sxs-lookup"><span data-stu-id="d0304-286">-334</span></span></p></td>
<td><p><span data-ttu-id="d0304-287">Сбой вызова операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d0304-287">The call to the operating system failed.</span></span> <span data-ttu-id="d0304-288">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="d0304-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="d0304-290">— 338</span><span class="sxs-lookup"><span data-stu-id="d0304-290">-338</span></span></p></td>
<td><p><span data-ttu-id="d0304-291">Родительская база данных повреждена.</span><span class="sxs-lookup"><span data-stu-id="d0304-291">A parent database is corrupt.</span></span> <span data-ttu-id="d0304-292">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="d0304-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="d0304-294">— 340</span><span class="sxs-lookup"><span data-stu-id="d0304-294">-340</span></span></p></td>
<td><p><span data-ttu-id="d0304-295">Кэш Аваилекст не соответствует дереву B +.</span><span class="sxs-lookup"><span data-stu-id="d0304-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="d0304-296">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="d0304-298">— 341</span><span class="sxs-lookup"><span data-stu-id="d0304-298">-341</span></span></p></td>
<td><p><span data-ttu-id="d0304-299">Дерево пространства Аллаваилекст повреждено.</span><span class="sxs-lookup"><span data-stu-id="d0304-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="d0304-300">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="d0304-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="d0304-302">— 342</span><span class="sxs-lookup"><span data-stu-id="d0304-302">-342</span></span></p></td>
<td><p><span data-ttu-id="d0304-303">Произошла ошибка нехватки памяти при выделении узла кэша Аваилекст.</span><span class="sxs-lookup"><span data-stu-id="d0304-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="d0304-304">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="d0304-306">— 343</span><span class="sxs-lookup"><span data-stu-id="d0304-306">-343</span></span></p></td>
<td><p><span data-ttu-id="d0304-307">Дерево пространства Овнекст повреждено.</span><span class="sxs-lookup"><span data-stu-id="d0304-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="d0304-308">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="d0304-310">— 344</span><span class="sxs-lookup"><span data-stu-id="d0304-310">-344</span></span></p></td>
<td><p><span data-ttu-id="d0304-311">Дбтиме на текущей странице больше, чем глобальная база данных дбтиме.</span><span class="sxs-lookup"><span data-stu-id="d0304-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="d0304-312">Эта ошибка возвращается диспетчером каталогов.</span><span class="sxs-lookup"><span data-stu-id="d0304-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="d0304-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="d0304-314">— 346</span><span class="sxs-lookup"><span data-stu-id="d0304-314">-346</span></span></p></td>
<td><p><span data-ttu-id="d0304-315">Попытка создать ключ для элемента индекса завершилась неудачей, так как ключ был усечен, а определение индекса не разрешает усечение ключа.</span><span class="sxs-lookup"><span data-stu-id="d0304-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="d0304-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="d0304-317">— 408</span><span class="sxs-lookup"><span data-stu-id="d0304-317">-408</span></span></p></td>
<td><p><span data-ttu-id="d0304-318">Слишком большой ключ.</span><span class="sxs-lookup"><span data-stu-id="d0304-318">The key is too large.</span></span> <span data-ttu-id="d0304-319">Эта ошибка возвращается диспетчером записей.</span><span class="sxs-lookup"><span data-stu-id="d0304-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="d0304-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="d0304-321">-500</span><span class="sxs-lookup"><span data-stu-id="d0304-321">-500</span></span></p></td>
<td><p><span data-ttu-id="d0304-322">Не удается выполнить запротоколированную операцию.</span><span class="sxs-lookup"><span data-stu-id="d0304-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="d0304-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="d0304-324">— 501</span><span class="sxs-lookup"><span data-stu-id="d0304-324">-501</span></span></p></td>
<td><p><span data-ttu-id="d0304-325">Файл журнала поврежден.</span><span class="sxs-lookup"><span data-stu-id="d0304-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="d0304-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="d0304-327">— 503</span><span class="sxs-lookup"><span data-stu-id="d0304-327">-503</span></span></p></td>
<td><p><span data-ttu-id="d0304-328">Не указан каталог резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d0304-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="d0304-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="d0304-330">— 504</span><span class="sxs-lookup"><span data-stu-id="d0304-330">-504</span></span></p></td>
<td><p><span data-ttu-id="d0304-331">Каталог резервного копирования не пуст.</span><span class="sxs-lookup"><span data-stu-id="d0304-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="d0304-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="d0304-333">— 505</span><span class="sxs-lookup"><span data-stu-id="d0304-333">-505</span></span></p></td>
<td><p><span data-ttu-id="d0304-334">Резервная копия уже активна.</span><span class="sxs-lookup"><span data-stu-id="d0304-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d0304-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="d0304-336">— 506</span><span class="sxs-lookup"><span data-stu-id="d0304-336">-506</span></span></p></td>
<td><p><span data-ttu-id="d0304-337">Выполняется восстановление.</span><span class="sxs-lookup"><span data-stu-id="d0304-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="d0304-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="d0304-339">— 509</span><span class="sxs-lookup"><span data-stu-id="d0304-339">-509</span></span></p></td>
<td><p><span data-ttu-id="d0304-340">Отсутствует файл журнала для контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="d0304-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="d0304-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="d0304-342">— 510</span><span class="sxs-lookup"><span data-stu-id="d0304-342">-510</span></span></p></td>
<td><p><span data-ttu-id="d0304-343">Ошибка записи в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="d0304-345">— 511</span><span class="sxs-lookup"><span data-stu-id="d0304-345">-511</span></span></p></td>
<td><p><span data-ttu-id="d0304-346">Попытка записи в журнал после сбоя восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="d0304-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="d0304-348">— 512</span><span class="sxs-lookup"><span data-stu-id="d0304-348">-512</span></span></p></td>
<td><p><span data-ttu-id="d0304-349">Попытка записи в журнал во время повтора восстановления завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="d0304-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="d0304-351">— 513</span><span class="sxs-lookup"><span data-stu-id="d0304-351">-513</span></span></p></td>
<td><p><span data-ttu-id="d0304-352">Имя файла журнала не соответствует номеру внутреннего поколения.</span><span class="sxs-lookup"><span data-stu-id="d0304-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="d0304-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="d0304-354">— 514</span><span class="sxs-lookup"><span data-stu-id="d0304-354">-514</span></span></p></td>
<td><p><span data-ttu-id="d0304-355">Версия файла журнала несовместима с версией ESE.</span><span class="sxs-lookup"><span data-stu-id="d0304-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="d0304-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="d0304-357">— 515</span><span class="sxs-lookup"><span data-stu-id="d0304-357">-515</span></span></p></td>
<td><p><span data-ttu-id="d0304-358">Метка времени в следующем журнале не соответствует ожидаемой метке времени.</span><span class="sxs-lookup"><span data-stu-id="d0304-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="d0304-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="d0304-360">— 516</span><span class="sxs-lookup"><span data-stu-id="d0304-360">-516</span></span></p></td>
<td><p><span data-ttu-id="d0304-361">Журнал неактивен.</span><span class="sxs-lookup"><span data-stu-id="d0304-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d0304-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="d0304-363">— 517</span><span class="sxs-lookup"><span data-stu-id="d0304-363">-517</span></span></p></td>
<td><p><span data-ttu-id="d0304-364">Буфер журнала слишком мал для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="d0304-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="d0304-366">— 519</span><span class="sxs-lookup"><span data-stu-id="d0304-366">-519</span></span></p></td>
<td><p><span data-ttu-id="d0304-367">Превышен максимальный номер файла журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="d0304-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="d0304-369">— 520</span><span class="sxs-lookup"><span data-stu-id="d0304-369">-520</span></span></p></td>
<td><p><span data-ttu-id="d0304-370">Резервное копирование не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0304-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="d0304-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="d0304-372">— 521</span><span class="sxs-lookup"><span data-stu-id="d0304-372">-521</span></span></p></td>
<td><p><span data-ttu-id="d0304-373">Вызов резервного копирования не является последовательным.</span><span class="sxs-lookup"><span data-stu-id="d0304-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="d0304-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="d0304-375">— 523</span><span class="sxs-lookup"><span data-stu-id="d0304-375">-523</span></span></p></td>
<td><p><span data-ttu-id="d0304-376">В настоящее время невозможно выполнить резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="d0304-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="d0304-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="d0304-378">— 524</span><span class="sxs-lookup"><span data-stu-id="d0304-378">-524</span></span></p></td>
<td><p><span data-ttu-id="d0304-379">Не удалось удалить файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d0304-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="d0304-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="d0304-381">— 525</span><span class="sxs-lookup"><span data-stu-id="d0304-381">-525</span></span></p></td>
<td><p><span data-ttu-id="d0304-382">Не удалось создать временный каталог резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d0304-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="d0304-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="d0304-384">— 526</span><span class="sxs-lookup"><span data-stu-id="d0304-384">-526</span></span></p></td>
<td><p><span data-ttu-id="d0304-385">Циклическое ведение журнала включено; невозможно выполнить добавочное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="d0304-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="d0304-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="d0304-387">— 527</span><span class="sxs-lookup"><span data-stu-id="d0304-387">-527</span></span></p></td>
<td><p><span data-ttu-id="d0304-388">Данные были восстановлены с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d0304-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="d0304-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="d0304-390">— 528</span><span class="sxs-lookup"><span data-stu-id="d0304-390">-528</span></span></p></td>
<td><p><span data-ttu-id="d0304-391">Текущий файл журнала отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d0304-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="d0304-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="d0304-393">— 529</span><span class="sxs-lookup"><span data-stu-id="d0304-393">-529</span></span></p></td>
<td><p><span data-ttu-id="d0304-394">Диск журнала заполнен.</span><span class="sxs-lookup"><span data-stu-id="d0304-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="d0304-396">— 530</span><span class="sxs-lookup"><span data-stu-id="d0304-396">-530</span></span></p></td>
<td><p><span data-ttu-id="d0304-397">Неверная подпись для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="d0304-399">— 531</span><span class="sxs-lookup"><span data-stu-id="d0304-399">-531</span></span></p></td>
<td><p><span data-ttu-id="d0304-400">Неверная подпись для файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="d0304-402">— 532</span><span class="sxs-lookup"><span data-stu-id="d0304-402">-532</span></span></p></td>
<td><p><span data-ttu-id="d0304-403">Неверное описание файла контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="d0304-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="d0304-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="d0304-405">— 533</span><span class="sxs-lookup"><span data-stu-id="d0304-405">-533</span></span></p></td>
<td><p><span data-ttu-id="d0304-406">Файл контрольных точек не найден или поврежден.</span><span class="sxs-lookup"><span data-stu-id="d0304-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="d0304-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="d0304-408">— 534</span><span class="sxs-lookup"><span data-stu-id="d0304-408">-534</span></span></p></td>
<td><p><span data-ttu-id="d0304-409">Страница файла исправления базы данных не найдена во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="d0304-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="d0304-411">— 535</span><span class="sxs-lookup"><span data-stu-id="d0304-411">-535</span></span></p></td>
<td><p><span data-ttu-id="d0304-412">Недопустимая страница файла исправления базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="d0304-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="d0304-414">— 536</span><span class="sxs-lookup"><span data-stu-id="d0304-414">-536</span></span></p></td>
<td><p><span data-ttu-id="d0304-415">Непредвиденное завершение операции повтора из-за внезапного сбоя при чтении журналов из файла журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="d0304-417">— 537</span><span class="sxs-lookup"><span data-stu-id="d0304-417">-537</span></span></p></td>
<td><p><span data-ttu-id="d0304-418">Этот флаг зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="d0304-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="d0304-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="d0304-420">— 538</span><span class="sxs-lookup"><span data-stu-id="d0304-420">-538</span></span></p></td>
<td><p><span data-ttu-id="d0304-421">При сложном восстановлении обнаружено, что в резервном наборе данных отсутствует файл исправления.</span><span class="sxs-lookup"><span data-stu-id="d0304-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="d0304-423">— 539</span><span class="sxs-lookup"><span data-stu-id="d0304-423">-539</span></span></p></td>
<td><p><span data-ttu-id="d0304-424">База данных не принадлежит текущему набору файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="d0304-426">— 540</span><span class="sxs-lookup"><span data-stu-id="d0304-426">-540</span></span></p></td>
<td><p><span data-ttu-id="d0304-427">Этот флаг зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="d0304-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="d0304-429">— 541</span><span class="sxs-lookup"><span data-stu-id="d0304-429">-541</span></span></p></td>
<td><p><span data-ttu-id="d0304-430">Фактический размер файла журнала не совпадает с <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="d0304-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="d0304-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="d0304-432">— 542</span><span class="sxs-lookup"><span data-stu-id="d0304-432">-542</span></span></p></td>
<td><p><span data-ttu-id="d0304-433">Не удалось найти файл контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="d0304-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="d0304-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="d0304-435">— 543</span><span class="sxs-lookup"><span data-stu-id="d0304-435">-543</span></span></p></td>
<td><p><span data-ttu-id="d0304-436">Отсутствуют необходимые файлы журнала для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="d0304-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="d0304-438">— 544</span><span class="sxs-lookup"><span data-stu-id="d0304-438">-544</span></span></p></td>
<td><p><span data-ttu-id="d0304-439">Мягкое восстановление будет использоваться в базе данных резервного копирования, когда вместо этого следует использовать восстановление.</span><span class="sxs-lookup"><span data-stu-id="d0304-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="d0304-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="d0304-441">— 545</span><span class="sxs-lookup"><span data-stu-id="d0304-441">-545</span></span></p></td>
<td><p><span data-ttu-id="d0304-442">Базы данных восстановлены, но размер файла журнала, используемый во время восстановления, не соответствует <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="d0304-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="d0304-444">— 546</span><span class="sxs-lookup"><span data-stu-id="d0304-444">-546</span></span></p></td>
<td><p><span data-ttu-id="d0304-445">Размер сектора файла журнала не совпадает с размером сектора текущего тома.</span><span class="sxs-lookup"><span data-stu-id="d0304-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="d0304-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="d0304-447">— 547</span><span class="sxs-lookup"><span data-stu-id="d0304-447">-547</span></span></p></td>
<td><p><span data-ttu-id="d0304-448">Базы данных восстановлены, но размер сектора файла журнала (используемый во время восстановления) не совпадает с размером сектора текущего тома.</span><span class="sxs-lookup"><span data-stu-id="d0304-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="d0304-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="d0304-450">— 548</span><span class="sxs-lookup"><span data-stu-id="d0304-450">-548</span></span></p></td>
<td><p><span data-ttu-id="d0304-451">Базы данных восстановлены, но использовались все возможные поколения журналов в текущей последовательности.</span><span class="sxs-lookup"><span data-stu-id="d0304-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="d0304-452">Перед продолжением необходимо удалить все файлы журналов и файл контрольных точек, а также создать резервные копии баз данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="d0304-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="d0304-454">— 549</span><span class="sxs-lookup"><span data-stu-id="d0304-454">-549</span></span></p></td>
<td><p><span data-ttu-id="d0304-455">Недопустимая попытка воспроизвести операцию потокового файла, в которой данные не были занесены в журнал.</span><span class="sxs-lookup"><span data-stu-id="d0304-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="d0304-456">Возможно, это вызвано попыткой Накату с включением циклического ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="d0304-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="d0304-458">— 550</span><span class="sxs-lookup"><span data-stu-id="d0304-458">-550</span></span></p></td>
<td><p><span data-ttu-id="d0304-459">Работа базы данных не была завершена аккуратно.</span><span class="sxs-lookup"><span data-stu-id="d0304-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="d0304-460">Сначала необходимо выполнить восстановление, чтобы правильно завершить операции с базой данных для предыдущего завершения работы.</span><span class="sxs-lookup"><span data-stu-id="d0304-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="d0304-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="d0304-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="d0304-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="d0304-463">Эта ошибка устарела и была заменена JET_errDatabaseDirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="d0304-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="d0304-465">— 551</span><span class="sxs-lookup"><span data-stu-id="d0304-465">-551</span></span></p></td>
<td><p><span data-ttu-id="d0304-466">Последнее согласованное время для базы данных не сопоставлено.</span><span class="sxs-lookup"><span data-stu-id="d0304-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="d0304-468">— 552</span><span class="sxs-lookup"><span data-stu-id="d0304-468">-552</span></span></p></td>
<td><p><span data-ttu-id="d0304-469">Файл исправления базы данных не создается из этой резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d0304-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="d0304-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="d0304-471">— 553</span><span class="sxs-lookup"><span data-stu-id="d0304-471">-553</span></span></p></td>
<td><p><span data-ttu-id="d0304-472">Начальный номер журнала слишком мал для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="d0304-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="d0304-474">— 554</span><span class="sxs-lookup"><span data-stu-id="d0304-474">-554</span></span></p></td>
<td><p><span data-ttu-id="d0304-475">Начальный номер журнала слишком велик для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="d0304-477">— 555</span><span class="sxs-lookup"><span data-stu-id="d0304-477">-555</span></span></p></td>
<td><p><span data-ttu-id="d0304-478">Файл журнала восстановления имеет неправильную подпись.</span><span class="sxs-lookup"><span data-stu-id="d0304-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="d0304-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="d0304-480">— 556</span><span class="sxs-lookup"><span data-stu-id="d0304-480">-556</span></span></p></td>
<td><p><span data-ttu-id="d0304-481">Файл журнала восстановления не является смежным.</span><span class="sxs-lookup"><span data-stu-id="d0304-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="d0304-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="d0304-483">— 557</span><span class="sxs-lookup"><span data-stu-id="d0304-483">-557</span></span></p></td>
<td><p><span data-ttu-id="d0304-484">Отсутствуют некоторые файлы журнала восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="d0304-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="d0304-486">— 560</span><span class="sxs-lookup"><span data-stu-id="d0304-486">-560</span></span></p></td>
<td><p><span data-ttu-id="d0304-487">Перед попыткой выполнить добавочное резервное копирование база данных пропустила предыдущую полную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="d0304-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="d0304-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="d0304-489">— 561</span><span class="sxs-lookup"><span data-stu-id="d0304-489">-561</span></span></p></td>
<td><p><span data-ttu-id="d0304-490">Размер базы данных резервного копирования не кратен размеру страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="d0304-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="d0304-492">— 562</span><span class="sxs-lookup"><span data-stu-id="d0304-492">-562</span></span></p></td>
<td><p><span data-ttu-id="d0304-493">Текущая попытка обновить базу данных остановлена, так как база данных уже является текущей.</span><span class="sxs-lookup"><span data-stu-id="d0304-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="d0304-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="d0304-495">— 563</span><span class="sxs-lookup"><span data-stu-id="d0304-495">-563</span></span></p></td>
<td><p><span data-ttu-id="d0304-496">База данных была частично преобразована в текущий формат.</span><span class="sxs-lookup"><span data-stu-id="d0304-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="d0304-497">База данных должна быть восстановлена из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d0304-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="d0304-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="d0304-499">— 565</span><span class="sxs-lookup"><span data-stu-id="d0304-499">-565</span></span></p></td>
<td><p><span data-ttu-id="d0304-500">Некоторые текущие файлы журнала отсутствуют для непрерывного восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0304-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="d0304-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="d0304-502">— 566</span><span class="sxs-lookup"><span data-stu-id="d0304-502">-566</span></span></p></td>
<td><p><span data-ttu-id="d0304-503">Дбтиме на странице меньше, чем Дбтимебефоре в записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="d0304-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="d0304-505">— 567</span><span class="sxs-lookup"><span data-stu-id="d0304-505">-567</span></span></p></td>
<td><p><span data-ttu-id="d0304-506">Дбтиме на странице предварительно находится в Дбтимебефоре, который находится в записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="d0304-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="d0304-508">— 569</span><span class="sxs-lookup"><span data-stu-id="d0304-508">-569</span></span></p></td>
<td><p><span data-ttu-id="d0304-509">Некоторые файлы журнала или исправления базы данных отсутствовали во время резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d0304-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="d0304-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="d0304-511">— 570</span><span class="sxs-lookup"><span data-stu-id="d0304-511">-570</span></span></p></td>
<td><p><span data-ttu-id="d0304-512">В резервной копии, заданной во время жесткого восстановления, обнаружена разорванная запись.</span><span class="sxs-lookup"><span data-stu-id="d0304-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="d0304-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="d0304-514">— 571</span><span class="sxs-lookup"><span data-stu-id="d0304-514">-571</span></span></p></td>
<td><p><span data-ttu-id="d0304-515">Обнаружена разорванная запись во время жесткого восстановления (журнал не был частью резервного набора данных).</span><span class="sxs-lookup"><span data-stu-id="d0304-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="d0304-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="d0304-517">— 573</span><span class="sxs-lookup"><span data-stu-id="d0304-517">-573</span></span></p></td>
<td><p><span data-ttu-id="d0304-518">Во время жесткого восстановления обнаружено повреждение в резервном наборе данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="d0304-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="d0304-520">— 574</span><span class="sxs-lookup"><span data-stu-id="d0304-520">-574</span></span></p></td>
<td><p><span data-ttu-id="d0304-521">Во время жесткого восстановления обнаружено повреждение (журнал не был частью резервного набора данных).</span><span class="sxs-lookup"><span data-stu-id="d0304-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="d0304-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="d0304-523">— 575</span><span class="sxs-lookup"><span data-stu-id="d0304-523">-575</span></span></p></td>
<td><p><span data-ttu-id="d0304-524">Ведение журнала невозможно включить при попытке обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="d0304-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="d0304-526">— 577</span><span class="sxs-lookup"><span data-stu-id="d0304-526">-577</span></span></p></td>
<td><p><span data-ttu-id="d0304-527">Либо TargetInstance, который был указан для восстановления, не найден, либо файлы журнала не совпадают.</span><span class="sxs-lookup"><span data-stu-id="d0304-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="d0304-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="d0304-529">— 579</span><span class="sxs-lookup"><span data-stu-id="d0304-529">-579</span></span></p></td>
<td><p><span data-ttu-id="d0304-530">Ядро СУБД успешно воспроизводило все операции в журнале транзакций, чтобы выполнить восстановление после сбоя, но вызывающий объект, выбранный для отмены восстановления без отката незафиксированных обновлений.</span><span class="sxs-lookup"><span data-stu-id="d0304-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="d0304-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="d0304-532">— 580</span><span class="sxs-lookup"><span data-stu-id="d0304-532">-580</span></span></p></td>
<td><p><span data-ttu-id="d0304-533">Восстанавливаемые базы данных не относятся к одной резервной копии теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="d0304-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="d0304-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="d0304-535">— 581</span><span class="sxs-lookup"><span data-stu-id="d0304-535">-581</span></span></p></td>
<td><p><span data-ttu-id="d0304-536">Существует мягкое восстановление базы данных из резервного набора данных теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="d0304-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d0304-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="d0304-538">— 601</span><span class="sxs-lookup"><span data-stu-id="d0304-538">-601</span></span></p></td>
<td><p><span data-ttu-id="d0304-539">Буфер преобразования Юникода слишком мал.</span><span class="sxs-lookup"><span data-stu-id="d0304-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="d0304-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="d0304-541">— 602</span><span class="sxs-lookup"><span data-stu-id="d0304-541">-602</span></span></p></td>
<td><p><span data-ttu-id="d0304-542">Сбой нормализации Юникода.</span><span class="sxs-lookup"><span data-stu-id="d0304-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="d0304-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="d0304-544">— 603</span><span class="sxs-lookup"><span data-stu-id="d0304-544">-603</span></span></p></td>
<td><p><span data-ttu-id="d0304-545">Операционная система не поддерживает нормализацию Юникода, и обратный вызов нормализации не был указан.</span><span class="sxs-lookup"><span data-stu-id="d0304-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="d0304-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="d0304-547">— 610</span><span class="sxs-lookup"><span data-stu-id="d0304-547">-610</span></span></p></td>
<td><p><span data-ttu-id="d0304-548">Существующий файл журнала имеет неправильную подпись.</span><span class="sxs-lookup"><span data-stu-id="d0304-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="d0304-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="d0304-550">— 611</span><span class="sxs-lookup"><span data-stu-id="d0304-550">-611</span></span></p></td>
<td><p><span data-ttu-id="d0304-551">Существующий файл журнала не является смежным.</span><span class="sxs-lookup"><span data-stu-id="d0304-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="d0304-553">— 612</span><span class="sxs-lookup"><span data-stu-id="d0304-553">-612</span></span></p></td>
<td><p><span data-ttu-id="d0304-554">В файле журнала во время резервного копирования обнаружена ошибка контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="d0304-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="d0304-556">— 613</span><span class="sxs-lookup"><span data-stu-id="d0304-556">-613</span></span></p></td>
<td><p><span data-ttu-id="d0304-557">Этот флаг зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="d0304-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="d0304-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="d0304-559">— 614</span><span class="sxs-lookup"><span data-stu-id="d0304-559">-614</span></span></p></td>
<td><p><span data-ttu-id="d0304-560">Существует слишком много невыполненных поколений между контрольной точкой и текущим поколением.</span><span class="sxs-lookup"><span data-stu-id="d0304-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="d0304-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="d0304-562">— 615</span><span class="sxs-lookup"><span data-stu-id="d0304-562">-615</span></span></p></td>
<td><p><span data-ttu-id="d0304-563">Предпринята попытка принудительного восстановления базы данных, которая не является резервной базой данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="d0304-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="d0304-565">— 900</span><span class="sxs-lookup"><span data-stu-id="d0304-565">-900</span></span></p></td>
<td><p><span data-ttu-id="d0304-566">Недопустимый параметр грбит.</span><span class="sxs-lookup"><span data-stu-id="d0304-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d0304-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="d0304-568">–1000</span><span class="sxs-lookup"><span data-stu-id="d0304-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="d0304-569">Выполняется завершение.</span><span class="sxs-lookup"><span data-stu-id="d0304-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="d0304-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="d0304-571">— 1001</span><span class="sxs-lookup"><span data-stu-id="d0304-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="d0304-572">Этот элемент API не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d0304-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="d0304-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="d0304-574">— 1002</span><span class="sxs-lookup"><span data-stu-id="d0304-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="d0304-575">Используется недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="d0304-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d0304-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="d0304-577">— 1003</span><span class="sxs-lookup"><span data-stu-id="d0304-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="d0304-578">Используется недопустимый параметр API.</span><span class="sxs-lookup"><span data-stu-id="d0304-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="d0304-580">— 1008</span><span class="sxs-lookup"><span data-stu-id="d0304-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="d0304-581">Попытка присоединиться к файлу базы данных, доступному только для чтения, для операций чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d0304-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="d0304-583">— 1010</span><span class="sxs-lookup"><span data-stu-id="d0304-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="d0304-584">Недопустимый идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="d0304-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="d0304-586">— 1011</span><span class="sxs-lookup"><span data-stu-id="d0304-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="d0304-587">Системе не хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="d0304-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="d0304-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="d0304-589">— 1012</span><span class="sxs-lookup"><span data-stu-id="d0304-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="d0304-590">Достигнут максимальный размер базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="d0304-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="d0304-592">— 1013</span><span class="sxs-lookup"><span data-stu-id="d0304-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="d0304-593">Таблица находится за пределами курсоров.</span><span class="sxs-lookup"><span data-stu-id="d0304-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="d0304-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="d0304-595">— 1014</span><span class="sxs-lookup"><span data-stu-id="d0304-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="d0304-596">В базе данных недостаточно буферов страниц.</span><span class="sxs-lookup"><span data-stu-id="d0304-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="d0304-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="d0304-598">— 1015</span><span class="sxs-lookup"><span data-stu-id="d0304-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="d0304-599">Слишком много индексов.</span><span class="sxs-lookup"><span data-stu-id="d0304-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="d0304-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="d0304-601">— 1016</span><span class="sxs-lookup"><span data-stu-id="d0304-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="d0304-602">Слишком много столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="d0304-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="d0304-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="d0304-604">— 1017</span><span class="sxs-lookup"><span data-stu-id="d0304-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="d0304-605">Запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="d0304-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="d0304-607">— 1018</span><span class="sxs-lookup"><span data-stu-id="d0304-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="d0304-608">Ошибка контрольной суммы на странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d0304-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="d0304-610">— 1019</span><span class="sxs-lookup"><span data-stu-id="d0304-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="d0304-611">Пустая страница базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="d0304-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="d0304-613">— 1020</span><span class="sxs-lookup"><span data-stu-id="d0304-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="d0304-614">Дескрипторы файлов отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d0304-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="d0304-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="d0304-616">— 1022</span><span class="sxs-lookup"><span data-stu-id="d0304-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="d0304-617">Ошибка ввода-вывода на диск.</span><span class="sxs-lookup"><span data-stu-id="d0304-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="d0304-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="d0304-619">— 1023</span><span class="sxs-lookup"><span data-stu-id="d0304-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="d0304-620">Недопустимый путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="d0304-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="d0304-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="d0304-622">— 1024</span><span class="sxs-lookup"><span data-stu-id="d0304-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="d0304-623">Недопустимый системный путь.</span><span class="sxs-lookup"><span data-stu-id="d0304-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="d0304-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="d0304-625">— 1025</span><span class="sxs-lookup"><span data-stu-id="d0304-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="d0304-626">Недопустимый каталог журнала.</span><span class="sxs-lookup"><span data-stu-id="d0304-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="d0304-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="d0304-628">— 1026</span><span class="sxs-lookup"><span data-stu-id="d0304-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="d0304-629">Запись больше, чем максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="d0304-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="d0304-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="d0304-631">— 1027</span><span class="sxs-lookup"><span data-stu-id="d0304-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="d0304-632">Слишком много открытых баз данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="d0304-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="d0304-634">— 1028</span><span class="sxs-lookup"><span data-stu-id="d0304-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="d0304-635">Это не файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d0304-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="d0304-637">— 1029</span><span class="sxs-lookup"><span data-stu-id="d0304-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="d0304-638">Ядро СУБД не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="d0304-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="d0304-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="d0304-640">— 1030</span><span class="sxs-lookup"><span data-stu-id="d0304-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="d0304-641">Ядро СУБД уже инициализировано.</span><span class="sxs-lookup"><span data-stu-id="d0304-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="d0304-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="d0304-643">— 1031</span><span class="sxs-lookup"><span data-stu-id="d0304-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="d0304-644">Инициализируется ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="d0304-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="d0304-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="d0304-646">— 1032</span><span class="sxs-lookup"><span data-stu-id="d0304-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="d0304-647">Не удается получить доступ к файлу, так как файл заблокирован или используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d0304-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="d0304-649">— 1038</span><span class="sxs-lookup"><span data-stu-id="d0304-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="d0304-650">Буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="d0304-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="d0304-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="d0304-652">— 1040</span><span class="sxs-lookup"><span data-stu-id="d0304-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="d0304-653">Определено слишком много столбцов.</span><span class="sxs-lookup"><span data-stu-id="d0304-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="d0304-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="d0304-655">— 1043</span><span class="sxs-lookup"><span data-stu-id="d0304-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="d0304-656">Контейнер не пуст.</span><span class="sxs-lookup"><span data-stu-id="d0304-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="d0304-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="d0304-658">— 1044</span><span class="sxs-lookup"><span data-stu-id="d0304-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="d0304-659">Недопустимое имя файла.</span><span class="sxs-lookup"><span data-stu-id="d0304-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="d0304-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="d0304-661">— 1045</span><span class="sxs-lookup"><span data-stu-id="d0304-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="d0304-662">Недопустимая закладка.</span><span class="sxs-lookup"><span data-stu-id="d0304-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="d0304-664">— 1046</span><span class="sxs-lookup"><span data-stu-id="d0304-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="d0304-665">Используемый столбец находится в индексе.</span><span class="sxs-lookup"><span data-stu-id="d0304-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="d0304-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="d0304-667">— 1047</span><span class="sxs-lookup"><span data-stu-id="d0304-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="d0304-668">Буфер данных не соответствует размеру столбца.</span><span class="sxs-lookup"><span data-stu-id="d0304-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="d0304-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="d0304-670">— 1048</span><span class="sxs-lookup"><span data-stu-id="d0304-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="d0304-671">Не удается задать значение столбца.</span><span class="sxs-lookup"><span data-stu-id="d0304-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="d0304-673">— 1051</span><span class="sxs-lookup"><span data-stu-id="d0304-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="d0304-674">Индекс используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="d0304-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="d0304-676">— 1052</span><span class="sxs-lookup"><span data-stu-id="d0304-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="d0304-677">Ссылка недоступна.</span><span class="sxs-lookup"><span data-stu-id="d0304-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="d0304-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="d0304-679">— 1053</span><span class="sxs-lookup"><span data-stu-id="d0304-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="d0304-680">Ключи NULL не допускаются в индексе.</span><span class="sxs-lookup"><span data-stu-id="d0304-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="d0304-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="d0304-682">— 1054</span><span class="sxs-lookup"><span data-stu-id="d0304-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="d0304-683">Операция должна выполняться в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0304-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="d0304-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="d0304-685">— 1059</span><span class="sxs-lookup"><span data-stu-id="d0304-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="d0304-686">Слишком много активных пользователей базы данных</span><span class="sxs-lookup"><span data-stu-id="d0304-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="d0304-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="d0304-688">— 1061</span><span class="sxs-lookup"><span data-stu-id="d0304-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="d0304-689">Недопустимый или неизвестный код страны.</span><span class="sxs-lookup"><span data-stu-id="d0304-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="d0304-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="d0304-691">— 1062</span><span class="sxs-lookup"><span data-stu-id="d0304-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="d0304-692">Недопустимый или Неизвестный идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="d0304-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="d0304-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="d0304-694">— 1063</span><span class="sxs-lookup"><span data-stu-id="d0304-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="d0304-695">Недопустимая или неизвестная кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="d0304-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="d0304-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="d0304-697">— 1064</span><span class="sxs-lookup"><span data-stu-id="d0304-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="d0304-698">Для <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString завершилось ошибкой</a>используются недопустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="d0304-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="d0304-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="d0304-700">— 1065</span><span class="sxs-lookup"><span data-stu-id="d0304-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="d0304-701">Попытка создать запись в хранилище версий (RCE), которая была больше, чем у контейнера версий.</span><span class="sxs-lookup"><span data-stu-id="d0304-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="d0304-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="d0304-703">— 1066</span><span class="sxs-lookup"><span data-stu-id="d0304-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="d0304-704">В хранилище версий недостаточно памяти, попытка очистки завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="d0304-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="d0304-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="d0304-706">— 1069</span><span class="sxs-lookup"><span data-stu-id="d0304-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="d0304-707">В хранилище версий недостаточно памяти, и уже была предпринята попытка очистки.</span><span class="sxs-lookup"><span data-stu-id="d0304-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="d0304-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="d0304-709">— 1071</span><span class="sxs-lookup"><span data-stu-id="d0304-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="d0304-710">Столбцы депонирования и SLV не могут быть проиндексированы.</span><span class="sxs-lookup"><span data-stu-id="d0304-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="d0304-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="d0304-712">— 1072</span><span class="sxs-lookup"><span data-stu-id="d0304-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="d0304-713">Запись не была удалена.</span><span class="sxs-lookup"><span data-stu-id="d0304-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="d0304-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="d0304-715">— 1073</span><span class="sxs-lookup"><span data-stu-id="d0304-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="d0304-716">Запрошено слишком много записей мемпул.</span><span class="sxs-lookup"><span data-stu-id="d0304-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="d0304-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="d0304-718">— 1074</span><span class="sxs-lookup"><span data-stu-id="d0304-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="d0304-719">База данных находится за пределами объектов ObjectID дерева B +, поэтому для освобождения или неиспользуемых идентификаторов ObjectId необходимо выполнить автономную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="d0304-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="d0304-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="d0304-721">— 1075</span><span class="sxs-lookup"><span data-stu-id="d0304-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="d0304-722">Счетчик с ИДЕНТИФИКАТОРом длинных значений достиг максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d0304-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="d0304-723">Для освобождения бесплатной или неиспользуемой Лонгвалуеидс необходимо выполнить автономную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="d0304-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="d0304-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="d0304-725">— 1076</span><span class="sxs-lookup"><span data-stu-id="d0304-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="d0304-726">Счетчик автоматического приращения достиг максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d0304-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="d0304-727">Автономная дефрагментация не сможет освободить свободные или неиспользуемые значения автоинкремента.</span><span class="sxs-lookup"><span data-stu-id="d0304-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="d0304-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="d0304-729">— 1077</span><span class="sxs-lookup"><span data-stu-id="d0304-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="d0304-730">Счетчик Дбтиме достиг максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d0304-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="d0304-731">Для освобождения бесплатных или неиспользуемых значений Дбтиме необходимо выполнить автономную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="d0304-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="d0304-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="d0304-733">— 1078</span><span class="sxs-lookup"><span data-stu-id="d0304-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="d0304-734">Достигнуто максимальное значение счетчика последовательных индексов.</span><span class="sxs-lookup"><span data-stu-id="d0304-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="d0304-735">Для освобождения бесплатных или неиспользуемых значений Секуентиалиндекс необходимо выполнить автономную дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="d0304-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="d0304-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="d0304-737">— 1080</span><span class="sxs-lookup"><span data-stu-id="d0304-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="d0304-738">В этом вызове с несколькими экземплярами включен режим с одним экземпляром.</span><span class="sxs-lookup"><span data-stu-id="d0304-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="d0304-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="d0304-740">— 1081</span><span class="sxs-lookup"><span data-stu-id="d0304-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="d0304-741">В этом вызове одного экземпляра включен режим с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="d0304-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="d0304-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="d0304-743">— 1082</span><span class="sxs-lookup"><span data-stu-id="d0304-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="d0304-744">Глобальные системные параметры уже заданы.</span><span class="sxs-lookup"><span data-stu-id="d0304-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="d0304-746">— 1083</span><span class="sxs-lookup"><span data-stu-id="d0304-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="d0304-747">Системный путь уже используется другим экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="d0304-749">— 1084</span><span class="sxs-lookup"><span data-stu-id="d0304-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="d0304-750">Путь к файлу журнала уже используется другим экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="d0304-752">— 1085</span><span class="sxs-lookup"><span data-stu-id="d0304-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="d0304-753">Путь к временной базе данных уже используется другим экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="d0304-755">— 1086</span><span class="sxs-lookup"><span data-stu-id="d0304-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="d0304-756">Имя экземпляра уже используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d0304-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="d0304-758">— 1090</span><span class="sxs-lookup"><span data-stu-id="d0304-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="d0304-759">Этот экземпляр нельзя использовать, так как в нем возникла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0304-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="d0304-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="d0304-761">— 1091</span><span class="sxs-lookup"><span data-stu-id="d0304-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="d0304-762">Эту базу данных невозможно использовать, так как произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0304-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="d0304-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="d0304-764">— 1092</span><span class="sxs-lookup"><span data-stu-id="d0304-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="d0304-765">Этот экземпляр не может быть использован, так как при выполнении операции (например, откат транзакции), которая не допускает ошибок, произошла ошибка переполнения журнала диска.</span><span class="sxs-lookup"><span data-stu-id="d0304-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="d0304-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="d0304-767">— 1101</span><span class="sxs-lookup"><span data-stu-id="d0304-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="d0304-768">В базе данных недостаточно сеансов.</span><span class="sxs-lookup"><span data-stu-id="d0304-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="d0304-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="d0304-770">— 1102</span><span class="sxs-lookup"><span data-stu-id="d0304-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="d0304-771">Сбой блокировки записи из-за существования ожидающей блокировки записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="d0304-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="d0304-773">— 1103</span><span class="sxs-lookup"><span data-stu-id="d0304-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="d0304-774">Слишком глубокая вложенность транзакций.</span><span class="sxs-lookup"><span data-stu-id="d0304-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="d0304-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="d0304-776">— 1104</span><span class="sxs-lookup"><span data-stu-id="d0304-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="d0304-777">Недопустимый обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="d0304-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="d0304-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="d0304-779">— 1105</span><span class="sxs-lookup"><span data-stu-id="d0304-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="d0304-780">Попытка обновления для незафиксированного первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="d0304-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="d0304-782">— 1108</span><span class="sxs-lookup"><span data-stu-id="d0304-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="d0304-783">Операция не разрешена в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0304-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="d0304-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="d0304-785">— 1109</span><span class="sxs-lookup"><span data-stu-id="d0304-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="d0304-786">Должна быть произведена откат текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0304-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="d0304-787">Она не может быть зафиксирована, и не может быть запущена новая.</span><span class="sxs-lookup"><span data-stu-id="d0304-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="d0304-789">— 1110</span><span class="sxs-lookup"><span data-stu-id="d0304-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="d0304-790">Транзакция, доступная только для чтения, попыталась изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="d0304-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="d0304-792">— 1111</span><span class="sxs-lookup"><span data-stu-id="d0304-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="d0304-793">Предпринята попытка заменить одну и ту же запись двумя разными курсорами в одном сеансе.</span><span class="sxs-lookup"><span data-stu-id="d0304-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="d0304-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="d0304-795">— 1112</span><span class="sxs-lookup"><span data-stu-id="d0304-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="d0304-796">Запись будет слишком большой, если она представлена в формате базы данных из предыдущей версии Jet.</span><span class="sxs-lookup"><span data-stu-id="d0304-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="d0304-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="d0304-798">— 1113</span><span class="sxs-lookup"><span data-stu-id="d0304-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="d0304-799">Не удалось создать временную таблицу из-за параметров, конфликтующих с JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="d0304-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="d0304-801">— 1114</span><span class="sxs-lookup"><span data-stu-id="d0304-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="d0304-802">Невозможно использовать этот обработчик сеанса с идентификатором таблицы, так как он не использовался для его создания.</span><span class="sxs-lookup"><span data-stu-id="d0304-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="d0304-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="d0304-804">— 1115</span><span class="sxs-lookup"><span data-stu-id="d0304-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="d0304-805">Недопустимый указатель экземпляра или ссылка на экземпляр, который был закрыт.</span><span class="sxs-lookup"><span data-stu-id="d0304-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d0304-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="d0304-807">— 1119</span><span class="sxs-lookup"><span data-stu-id="d0304-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="d0304-808">На странице базы данных, считанной с диска, была записана Предыдущая запись, не представленная на странице.</span><span class="sxs-lookup"><span data-stu-id="d0304-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="d0304-809">Доступно в Windows 8 и более поздних версиях для Client, Windows Server 2012 и более поздних версий для сервера.</span><span class="sxs-lookup"><span data-stu-id="d0304-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="d0304-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="d0304-811">— 1201</span><span class="sxs-lookup"><span data-stu-id="d0304-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="d0304-812">База данных уже существует.</span><span class="sxs-lookup"><span data-stu-id="d0304-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="d0304-814">— 1202</span><span class="sxs-lookup"><span data-stu-id="d0304-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="d0304-815">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="d0304-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="d0304-817">— 1203</span><span class="sxs-lookup"><span data-stu-id="d0304-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="d0304-818">Такая база данных отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d0304-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="d0304-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="d0304-820">— 1204</span><span class="sxs-lookup"><span data-stu-id="d0304-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="d0304-821">Недопустимое имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="d0304-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="d0304-823">— 1205</span><span class="sxs-lookup"><span data-stu-id="d0304-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="d0304-824">Недопустимое число страниц.</span><span class="sxs-lookup"><span data-stu-id="d0304-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="d0304-826">— 1206</span><span class="sxs-lookup"><span data-stu-id="d0304-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="d0304-827">Отсутствует файл, отличный от базы данных, или повреждена база данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="d0304-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="d0304-829">— 1207</span><span class="sxs-lookup"><span data-stu-id="d0304-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="d0304-830">База данных заблокирована в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="d0304-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="d0304-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="d0304-832">— 1208</span><span class="sxs-lookup"><span data-stu-id="d0304-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="d0304-833">Не удается отключить управление версиями для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="d0304-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="d0304-835">— 1209</span><span class="sxs-lookup"><span data-stu-id="d0304-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="d0304-836">Ядро СУБД несовместимо с базой данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="d0304-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="d0304-838">— 1210</span><span class="sxs-lookup"><span data-stu-id="d0304-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="d0304-839">База данных имеет более старый формат (200).</span><span class="sxs-lookup"><span data-stu-id="d0304-839">The database is in an older (200) format.</span></span> <span data-ttu-id="d0304-840">Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="d0304-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="d0304-841">Только клиент Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d0304-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="d0304-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="d0304-843">— 1211</span><span class="sxs-lookup"><span data-stu-id="d0304-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="d0304-844">База данных имеет более старый формат (400).</span><span class="sxs-lookup"><span data-stu-id="d0304-844">The database is in an older (400) format.</span></span> <span data-ttu-id="d0304-845">Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="d0304-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="d0304-846">Только клиент Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d0304-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="d0304-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="d0304-848">— 1212</span><span class="sxs-lookup"><span data-stu-id="d0304-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="d0304-849">База данных имеет более старый формат (500).</span><span class="sxs-lookup"><span data-stu-id="d0304-849">The database is in an older (500) format.</span></span> <span data-ttu-id="d0304-850">Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="d0304-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="d0304-851">Только клиент Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d0304-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="d0304-853">— 1213</span><span class="sxs-lookup"><span data-stu-id="d0304-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="d0304-854">Размер страницы базы данных не соответствует подсистеме.</span><span class="sxs-lookup"><span data-stu-id="d0304-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="d0304-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="d0304-856">— 1214</span><span class="sxs-lookup"><span data-stu-id="d0304-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="d0304-857">Больше нельзя запускать экземпляры базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d0304-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="d0304-859">— 1215</span><span class="sxs-lookup"><span data-stu-id="d0304-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="d0304-860">База данных используется другим экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="d0304-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="d0304-862">— 1216</span><span class="sxs-lookup"><span data-stu-id="d0304-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="d0304-863">Необработанное вложение базы данных обнаружено в начале или в конце восстановления, но база данных отсутствует или не соответствует сведениям о вложении.</span><span class="sxs-lookup"><span data-stu-id="d0304-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="d0304-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="d0304-865">— 1217</span><span class="sxs-lookup"><span data-stu-id="d0304-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="d0304-866">Указан недопустимый путь к файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="d0304-868">— 1218</span><span class="sxs-lookup"><span data-stu-id="d0304-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="d0304-869">Базе данных назначается идентификатор, который уже используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="d0304-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="d0304-871">— 1219</span><span class="sxs-lookup"><span data-stu-id="d0304-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="d0304-872">Принудительная отсоединение разрешена только после того, как нормальная отсоединение была остановлена из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="d0304-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="d0304-874">— 1220</span><span class="sxs-lookup"><span data-stu-id="d0304-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="d0304-875">В каталоге обнаружено повреждение.</span><span class="sxs-lookup"><span data-stu-id="d0304-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="d0304-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="d0304-877">— 1221</span><span class="sxs-lookup"><span data-stu-id="d0304-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="d0304-878">База данных присоединена только частично, а операция присоединения не может быть завершена.</span><span class="sxs-lookup"><span data-stu-id="d0304-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="d0304-880">— 1222</span><span class="sxs-lookup"><span data-stu-id="d0304-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="d0304-881">База данных с такой же подписью уже используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="d0304-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="d0304-883">— 1224</span><span class="sxs-lookup"><span data-stu-id="d0304-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="d0304-884">База данных повреждена, но восстановление не разрешено.</span><span class="sxs-lookup"><span data-stu-id="d0304-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="d0304-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="d0304-886">— 1225</span><span class="sxs-lookup"><span data-stu-id="d0304-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="d0304-887">Ядро СУБД попыталось воспроизвести операцию создания базы данных из журнала транзакций, но не удалось выполнить из-за несовместимой версии этой операции.</span><span class="sxs-lookup"><span data-stu-id="d0304-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="d0304-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="d0304-889">— 1302</span><span class="sxs-lookup"><span data-stu-id="d0304-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="d0304-890">Таблица монопольно заблокирована.</span><span class="sxs-lookup"><span data-stu-id="d0304-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="d0304-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="d0304-892">— 1303</span><span class="sxs-lookup"><span data-stu-id="d0304-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="d0304-893">Таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="d0304-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="d0304-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="d0304-895">— 1304</span><span class="sxs-lookup"><span data-stu-id="d0304-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="d0304-896">Таблица используется и не может быть заблокирована.</span><span class="sxs-lookup"><span data-stu-id="d0304-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="d0304-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="d0304-898">— 1305</span><span class="sxs-lookup"><span data-stu-id="d0304-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="d0304-899">Такой таблицы или объекта нет.</span><span class="sxs-lookup"><span data-stu-id="d0304-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="d0304-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="d0304-901">— 1307</span><span class="sxs-lookup"><span data-stu-id="d0304-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="d0304-902">Недопустимая плотность файла или индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="d0304-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="d0304-904">— 1308</span><span class="sxs-lookup"><span data-stu-id="d0304-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="d0304-905">Таблица не пуста.</span><span class="sxs-lookup"><span data-stu-id="d0304-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="d0304-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="d0304-907">— 1310</span><span class="sxs-lookup"><span data-stu-id="d0304-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="d0304-908">Недопустимый идентификатор таблицы.</span><span class="sxs-lookup"><span data-stu-id="d0304-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="d0304-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="d0304-910">— 1311</span><span class="sxs-lookup"><span data-stu-id="d0304-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="d0304-911">Невозможно открыть больше таблиц даже после выполнения внутренней задачи очистки.</span><span class="sxs-lookup"><span data-stu-id="d0304-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="d0304-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="d0304-913">— 1312</span><span class="sxs-lookup"><span data-stu-id="d0304-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="d0304-914">Операция не поддерживается для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d0304-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="d0304-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="d0304-916">— 1313</span><span class="sxs-lookup"><span data-stu-id="d0304-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="d0304-917">Не удается открыть больше таблиц, так как не удалось завершить попытку очистки.</span><span class="sxs-lookup"><span data-stu-id="d0304-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="d0304-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="d0304-919">— 1314</span><span class="sxs-lookup"><span data-stu-id="d0304-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="d0304-920">Имя таблицы или объекта используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="d0304-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="d0304-922">— 1316</span><span class="sxs-lookup"><span data-stu-id="d0304-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="d0304-923">Объект недопустим для операции.</span><span class="sxs-lookup"><span data-stu-id="d0304-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="d0304-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="d0304-925">— 1317</span><span class="sxs-lookup"><span data-stu-id="d0304-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="d0304-926">Для удаления временной таблицы необходимо использовать <a href="gg294087(v=exchg.10).md">жетклосетабле</a> вместо <a href="gg294128(v=exchg.10).md">жетделететабле</a> .</span><span class="sxs-lookup"><span data-stu-id="d0304-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="d0304-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="d0304-928">— 1318</span><span class="sxs-lookup"><span data-stu-id="d0304-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="d0304-929">Недопустимая попытка удалить системную таблицу.</span><span class="sxs-lookup"><span data-stu-id="d0304-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="d0304-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="d0304-931">— 1319</span><span class="sxs-lookup"><span data-stu-id="d0304-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="d0304-932">Недопустимая попытка удалить таблицу шаблонов.</span><span class="sxs-lookup"><span data-stu-id="d0304-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="d0304-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="d0304-934">— 1322</span><span class="sxs-lookup"><span data-stu-id="d0304-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="d0304-935">Должна быть монопольная блокировка таблицы.</span><span class="sxs-lookup"><span data-stu-id="d0304-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="d0304-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="d0304-937">— 1323</span><span class="sxs-lookup"><span data-stu-id="d0304-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="d0304-938">В этой таблице запрещены операции DDL.</span><span class="sxs-lookup"><span data-stu-id="d0304-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="d0304-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="d0304-940">— 1324</span><span class="sxs-lookup"><span data-stu-id="d0304-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="d0304-941">В производной таблице операции DDL запрещены в наследуемой части DDL.</span><span class="sxs-lookup"><span data-stu-id="d0304-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="d0304-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="d0304-943">— 1325</span><span class="sxs-lookup"><span data-stu-id="d0304-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="d0304-944">Вложенные иерархические DDL в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d0304-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="d0304-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="d0304-946">— 1326</span><span class="sxs-lookup"><span data-stu-id="d0304-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="d0304-947">Предпринята попытка наследования DDL из таблицы, которая не помечена как таблица шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0304-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="d0304-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="d0304-949">— 1328</span><span class="sxs-lookup"><span data-stu-id="d0304-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="d0304-950">Системные параметры заданы неправильно.</span><span class="sxs-lookup"><span data-stu-id="d0304-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d0304-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="d0304-952">— 1329</span><span class="sxs-lookup"><span data-stu-id="d0304-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="d0304-953">Клиент запросил остановку службы.</span><span class="sxs-lookup"><span data-stu-id="d0304-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="d0304-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="d0304-955">— 1330</span><span class="sxs-lookup"><span data-stu-id="d0304-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="d0304-956">Таблица шаблона была создана с установленным флагом Нофикседварколумнсиндериведтаблес.</span><span class="sxs-lookup"><span data-stu-id="d0304-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="d0304-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="d0304-958">— 1401</span><span class="sxs-lookup"><span data-stu-id="d0304-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="d0304-959">Не удалось выполнить сборку индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="d0304-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="d0304-961">— 1402</span><span class="sxs-lookup"><span data-stu-id="d0304-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="d0304-962">Первичный индекс уже определен.</span><span class="sxs-lookup"><span data-stu-id="d0304-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="d0304-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="d0304-964">— 1403</span><span class="sxs-lookup"><span data-stu-id="d0304-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="d0304-965">Индекс уже определен.</span><span class="sxs-lookup"><span data-stu-id="d0304-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="d0304-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="d0304-967">— 1404</span><span class="sxs-lookup"><span data-stu-id="d0304-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="d0304-968">Такого индекса нет.</span><span class="sxs-lookup"><span data-stu-id="d0304-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="d0304-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="d0304-970">— 1405</span><span class="sxs-lookup"><span data-stu-id="d0304-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="d0304-971">Невозможно удалить кластеризованный индекс.</span><span class="sxs-lookup"><span data-stu-id="d0304-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="d0304-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="d0304-973">— 1406</span><span class="sxs-lookup"><span data-stu-id="d0304-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="d0304-974">Недопустимое определение индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d0304-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="d0304-976">— 1409</span><span class="sxs-lookup"><span data-stu-id="d0304-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="d0304-977">Недопустимое создание описания индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="d0304-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="d0304-979">— 1410</span><span class="sxs-lookup"><span data-stu-id="d0304-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="d0304-980">База данных выходит за пределы блоков описания индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="d0304-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="d0304-982">— 1411</span><span class="sxs-lookup"><span data-stu-id="d0304-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="d0304-983">Для многозначного индекса были созданы неуникальные ключи индексов между записями.</span><span class="sxs-lookup"><span data-stu-id="d0304-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="d0304-985">— 1412</span><span class="sxs-lookup"><span data-stu-id="d0304-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="d0304-986">Вторичный индекс, который правильно отражает первичный индекс, не удалось построить.</span><span class="sxs-lookup"><span data-stu-id="d0304-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="d0304-988">— 1413</span><span class="sxs-lookup"><span data-stu-id="d0304-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="d0304-989">Первичный индекс поврежден, и база данных должна быть дефрагментирована.</span><span class="sxs-lookup"><span data-stu-id="d0304-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="d0304-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="d0304-991">— 1414</span><span class="sxs-lookup"><span data-stu-id="d0304-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="d0304-992">Вторичный индекс поврежден, и база данных должна быть дефрагментирована.</span><span class="sxs-lookup"><span data-stu-id="d0304-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="d0304-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="d0304-994">— 1416</span><span class="sxs-lookup"><span data-stu-id="d0304-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="d0304-995">Недопустимый идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="d0304-997">— 1430</span><span class="sxs-lookup"><span data-stu-id="d0304-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="d0304-998">Индекс кортежа можно задать только для вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="d0304-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="d0304-1000">— 1431</span><span class="sxs-lookup"><span data-stu-id="d0304-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="d0304-1001">Определение индекса для индекса кортежа содержит дополнительные ключевые столбцы, которые может поддерживать ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="d0304-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="d0304-1002"><strong>Примечание  </strong> . JET_errIndexTuplesOneColumnOnlyная ошибка устарела и заменена JET_errIndexTuplesTooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="d0304-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="d0304-1004">— 1432</span><span class="sxs-lookup"><span data-stu-id="d0304-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="d0304-1005">Индекс кортежа должен быть неуникальным индексом.</span><span class="sxs-lookup"><span data-stu-id="d0304-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="d0304-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="d0304-1007">— 1433</span><span class="sxs-lookup"><span data-stu-id="d0304-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="d0304-1008">Определение индекса кортежа может содержать только ключевые столбцы с типами столбцов text или binary.</span><span class="sxs-lookup"><span data-stu-id="d0304-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="d0304-1009"><strong>Примечание  </strong> . JET_errIndexTuplesTextColumnsOnlyная ошибка устарела и заменена JET_errIndexTuplesTextBinaryColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="d0304-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="d0304-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="d0304-1011">— 1434</span><span class="sxs-lookup"><span data-stu-id="d0304-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="d0304-1012">Индекс кортежа не допускает настройки Кбварсегмак.</span><span class="sxs-lookup"><span data-stu-id="d0304-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="d0304-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="d0304-1014">— 1435</span><span class="sxs-lookup"><span data-stu-id="d0304-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="d0304-1015">Минимальная или максимальная длина кортежа или максимальное число символов, указанных для индекса, недопустимы.</span><span class="sxs-lookup"><span data-stu-id="d0304-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d0304-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="d0304-1017">— 1436</span><span class="sxs-lookup"><span data-stu-id="d0304-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="d0304-1018"><a href="gg269198(v=exchg.10).md">Жетретриевеколумн</a> не может быть вызван с установленным флагом JET_bitRetrieveFromIndex при извлечении столбца в индексе кортежа.</span><span class="sxs-lookup"><span data-stu-id="d0304-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="d0304-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="d0304-1020">— 1437</span><span class="sxs-lookup"><span data-stu-id="d0304-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="d0304-1021">Указанный ключ не соответствует минимальной длине кортежа.</span><span class="sxs-lookup"><span data-stu-id="d0304-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="d0304-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="d0304-1023">— 1501</span><span class="sxs-lookup"><span data-stu-id="d0304-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="d0304-1024">Значение столбца является длинным.</span><span class="sxs-lookup"><span data-stu-id="d0304-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="d0304-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="d0304-1026">— 1502</span><span class="sxs-lookup"><span data-stu-id="d0304-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="d0304-1027">Такой фрагмент не существует в длинном значении.</span><span class="sxs-lookup"><span data-stu-id="d0304-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="d0304-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="d0304-1029">— 1503</span><span class="sxs-lookup"><span data-stu-id="d0304-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="d0304-1030">Поле не будет помещаться в записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="d0304-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="d0304-1032">— 1504</span><span class="sxs-lookup"><span data-stu-id="d0304-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="d0304-1033">Недопустимое значение null.</span><span class="sxs-lookup"><span data-stu-id="d0304-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="d0304-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="d0304-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="d0304-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="d0304-1036">Недопустимое значение null.</span><span class="sxs-lookup"><span data-stu-id="d0304-1036">Null is not valid.</span></span> <span data-ttu-id="d0304-1037">Эта ошибка возвращается диспетчером записей.</span><span class="sxs-lookup"><span data-stu-id="d0304-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="d0304-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="d0304-1039">Столбец индексируется и не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="d0304-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="d0304-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="d0304-1041">Длина поля превышает максимально допустимую длину.</span><span class="sxs-lookup"><span data-stu-id="d0304-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="d0304-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="d0304-1043">Такого столбца нет.</span><span class="sxs-lookup"><span data-stu-id="d0304-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="d0304-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="d0304-1045">Это поле уже определено.</span><span class="sxs-lookup"><span data-stu-id="d0304-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="d0304-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="d0304-1047">Предпринята попытка создать столбец с несколькими значениями, но столбец не был помечен.</span><span class="sxs-lookup"><span data-stu-id="d0304-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="d0304-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="d0304-1049">Второй столбец с автоматическим приращением или версией.</span><span class="sxs-lookup"><span data-stu-id="d0304-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="d0304-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="d0304-1051">Недопустимый тип данных столбца.</span><span class="sxs-lookup"><span data-stu-id="d0304-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="d0304-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="d0304-1053">Нет помеченных столбцов, относящихся к NULL.</span><span class="sxs-lookup"><span data-stu-id="d0304-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="d0304-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="d0304-1055">База данных недопустима, так как она не содержит текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="d0304-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="d0304-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="d0304-1057">Ключ полностью создан.</span><span class="sxs-lookup"><span data-stu-id="d0304-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="d0304-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="d0304-1059">Неправильный идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="d0304-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="d0304-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="d0304-1061">Некорректный Итагсекуенце для столбца с тегами.</span><span class="sxs-lookup"><span data-stu-id="d0304-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="d0304-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="d0304-1063">Невозможно удалить столбец, так как он является частью связи.</span><span class="sxs-lookup"><span data-stu-id="d0304-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="d0304-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="d0304-1065">Автоматическое увеличение и версия не могут быть помечены.</span><span class="sxs-lookup"><span data-stu-id="d0304-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="d0304-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="d0304-1067">Значение по умолчанию превышает максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="d0304-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="d0304-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="d0304-1069">В уникальном столбце с несколькими значениями обнаружено повторяющееся значение.</span><span class="sxs-lookup"><span data-stu-id="d0304-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="d0304-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="d0304-1071">Обнаружено повреждение в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="d0304-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="d0304-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="d0304-1073">Обнаружено повторяющееся значение в уникальном столбце с несколькими значениями после нормализации данных, и нормализация усекает данные перед сравнением.</span><span class="sxs-lookup"><span data-stu-id="d0304-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="d0304-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="d0304-1075">Недопустимый столбец в производной таблице.</span><span class="sxs-lookup"><span data-stu-id="d0304-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="d0304-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="d0304-1077">Предпринята попытка преобразовать столбец в заполнитель первичного индекса, но этот столбец не соответствует необходимым критериям.</span><span class="sxs-lookup"><span data-stu-id="d0304-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="d0304-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="d0304-1079">Ключ не найден.</span><span class="sxs-lookup"><span data-stu-id="d0304-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="d0304-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="d0304-1081">Нет рабочего буфера.</span><span class="sxs-lookup"><span data-stu-id="d0304-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="d0304-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="d0304-1083">Отсутствует текущая запись.</span><span class="sxs-lookup"><span data-stu-id="d0304-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="d0304-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="d0304-1085">Первичный ключ может не измениться.</span><span class="sxs-lookup"><span data-stu-id="d0304-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="d0304-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="d0304-1087">Недопустимый дублирующийся ключ.</span><span class="sxs-lookup"><span data-stu-id="d0304-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="d0304-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="d0304-1089">Предпринята попытка обновить запись, пока уже выполняется обновление записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="d0304-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="d0304-1091">Вызов не был сделан в <a href="gg269329(v=exchg.10).md">жетмакекэй</a>.</span><span class="sxs-lookup"><span data-stu-id="d0304-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="d0304-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="d0304-1093">Вызов не был сделан в <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>.</span><span class="sxs-lookup"><span data-stu-id="d0304-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="d0304-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="d0304-1095">Данные были изменены, операция прервана.</span><span class="sxs-lookup"><span data-stu-id="d0304-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="d0304-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="d0304-1097">Эта установка Windows не поддерживает выбранный язык.</span><span class="sxs-lookup"><span data-stu-id="d0304-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="d0304-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="d0304-1099">Слишком много процессов сортировки.</span><span class="sxs-lookup"><span data-stu-id="d0304-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="d0304-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="d0304-1101">Во время сортировки произошла Недопустимая операция.</span><span class="sxs-lookup"><span data-stu-id="d0304-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="d0304-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="d0304-1103">Не удалось открыть временный файл.</span><span class="sxs-lookup"><span data-stu-id="d0304-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="d0304-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="d0304-1105">Открыто слишком много баз данных.</span><span class="sxs-lookup"><span data-stu-id="d0304-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="d0304-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="d0304-1107">На диске не осталось места.</span><span class="sxs-lookup"><span data-stu-id="d0304-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="d0304-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="d0304-1109">Отказано в разрешении.</span><span class="sxs-lookup"><span data-stu-id="d0304-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="d0304-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="d0304-1111">Файл не найден.</span><span class="sxs-lookup"><span data-stu-id="d0304-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="d0304-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="d0304-1113">Недопустимый тип файла.</span><span class="sxs-lookup"><span data-stu-id="d0304-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="d0304-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="d0304-1115">Невозможно запустить восстановление после инициализации.</span><span class="sxs-lookup"><span data-stu-id="d0304-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="d0304-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="d0304-1117">Не удалось интерпретировать журналы.</span><span class="sxs-lookup"><span data-stu-id="d0304-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="d0304-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="d0304-1119">Недопустимая операция.</span><span class="sxs-lookup"><span data-stu-id="d0304-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="d0304-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="d0304-1121">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="d0304-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="d0304-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="d0304-1123">Бесконечное разбиение.</span><span class="sxs-lookup"><span data-stu-id="d0304-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="d0304-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="d0304-1125">Несколько потоков используют один сеанс.</span><span class="sxs-lookup"><span data-stu-id="d0304-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="d0304-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="d0304-1127">Не удалось найти точку входа в требуемой библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d0304-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="d0304-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="d0304-1129">Для указанного сеанса уже задан контекст сеанса.</span><span class="sxs-lookup"><span data-stu-id="d0304-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="d0304-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="d0304-1131">Предпринята попытка сбросить контекст сеанса, но текущий поток не был исходным, который задает контекст сеанса.</span><span class="sxs-lookup"><span data-stu-id="d0304-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="d0304-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="d0304-1133">Предпринята попытка завершить сеанс, который сейчас используется.</span><span class="sxs-lookup"><span data-stu-id="d0304-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="d0304-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="d0304-1135">Произошла внутренняя ошибка при преобразовании формата динамической записи.</span><span class="sxs-lookup"><span data-stu-id="d0304-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="d0304-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="d0304-1137">Допускается только одна открытая пользовательская база данных на сеанс (как указано установкой флага <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> во время создания базы данных).</span><span class="sxs-lookup"><span data-stu-id="d0304-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="d0304-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="d0304-1139">Произошла ошибка во время отката.</span><span class="sxs-lookup"><span data-stu-id="d0304-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="d0304-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="d0304-1141">Не удалось вызвать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d0304-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="d0304-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="d0304-1143">Не удалось найти функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d0304-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="d0304-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="d0304-1145">API теневого копирования операционной системы использован в недопустимой последовательности.</span><span class="sxs-lookup"><span data-stu-id="d0304-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="d0304-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="d0304-1147">Теневое копирование операционной системы завершилось с превышением времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="d0304-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="d0304-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="d0304-1149">Теневое копирование операционной системы запрещено, так как выполняется резервное копирование или восстановление.</span><span class="sxs-lookup"><span data-stu-id="d0304-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="d0304-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="d0304-1151">Не удалось выполнить операцию, так как указан недопустимый маркер теневого копирования операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d0304-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="d0304-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="d0304-1153">Предпринята попытка использовать локальное хранилище без указания функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d0304-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="d0304-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="d0304-1155">Была предпринята попытка задать локальное хранилище для объекта, который уже был задан.</span><span class="sxs-lookup"><span data-stu-id="d0304-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="d0304-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="d0304-1157">Предпринята попытка получить локальное хранилище из объекта, в котором он не был задан.</span><span class="sxs-lookup"><span data-stu-id="d0304-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="d0304-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="d0304-1159">Не удалось выполнить операцию ввода-вывода, так как она была предпринята для нераспределенной области файла.</span><span class="sxs-lookup"><span data-stu-id="d0304-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="d0304-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="d0304-1161">Операция чтения была выдана в расположение после конца файла (операции записи разворачивают файл).</span><span class="sxs-lookup"><span data-stu-id="d0304-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="d0304-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="d0304-1163">Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту прервать указанный ввод-вывод.</span><span class="sxs-lookup"><span data-stu-id="d0304-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="d0304-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="d0304-1165">Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту повторить указанный ввод-вывод.</span><span class="sxs-lookup"><span data-stu-id="d0304-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="d0304-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="d0304-1167">Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту завершиться ошибкой указанного ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="d0304-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="d0304-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="d0304-1169">Доступ для чтения и записи не поддерживается для сжатых файлов.</span><span class="sxs-lookup"><span data-stu-id="d0304-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="d0304-1170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0304-1170">Remarks</span></span>

<span data-ttu-id="d0304-1171">В общем случае значение, большее нуля, должно интерпретироваться как предупреждение, нулевое значение должно интерпретироваться как успешно, а значение меньше нуля должно интерпретироваться как ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0304-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="d0304-1172">Никакие другие шаблоны в этих значениях, например диапазоны значений, должны быть полагаться на приложения.</span><span class="sxs-lookup"><span data-stu-id="d0304-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="d0304-1173">Требования</span><span class="sxs-lookup"><span data-stu-id="d0304-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1174"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d0304-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d0304-1175">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d0304-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0304-1176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d0304-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d0304-1177">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d0304-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0304-1178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d0304-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d0304-1179">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d0304-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d0304-1180">См. также:</span><span class="sxs-lookup"><span data-stu-id="d0304-1180">See Also</span></span>

[<span data-ttu-id="d0304-1181">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="d0304-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="d0304-1182">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d0304-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="d0304-1183">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d0304-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
