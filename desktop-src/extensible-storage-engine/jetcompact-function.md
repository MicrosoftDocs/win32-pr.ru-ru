---
description: Дополнительные сведения о функции Жеткомпакт
title: Функция Жеткомпакт
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712074"
---
# <a name="jetcompact-function"></a><span data-ttu-id="56020-103">Функция Жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="56020-103">JetCompact Function</span></span>


<span data-ttu-id="56020-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56020-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="56020-105">Функция Жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="56020-105">JetCompact Function</span></span>

<span data-ttu-id="56020-106">Функция **жеткомпакт** создает копию существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="56020-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="56020-107">Копия сжимается в состояние, оптимальное для использования.</span><span class="sxs-lookup"><span data-stu-id="56020-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="56020-108">Данные в скопированных данных будут упаковываться в соответствии с мерами, выбранными для индексов при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="56020-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="56020-109">Таким образом, сжатые данные могут храниться как можно более плотно.</span><span class="sxs-lookup"><span data-stu-id="56020-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="56020-110">Кроме того, сжатые данные могут резервировать пространство для последующего роста записи или вставки индекса.</span><span class="sxs-lookup"><span data-stu-id="56020-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="56020-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="56020-111">Parameters</span></span>

<span data-ttu-id="56020-112">*сесид*</span><span class="sxs-lookup"><span data-stu-id="56020-112">*sesid*</span></span>

<span data-ttu-id="56020-113">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="56020-113">The session to use for this call.</span></span>

<span data-ttu-id="56020-114">*сздатабасесрк*</span><span class="sxs-lookup"><span data-stu-id="56020-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="56020-115">База данных источника, которая будет сжата.</span><span class="sxs-lookup"><span data-stu-id="56020-115">The source database that will be compacted.</span></span>

<span data-ttu-id="56020-116">*сздатабаседест*</span><span class="sxs-lookup"><span data-stu-id="56020-116">*szDatabaseDest*</span></span>

<span data-ttu-id="56020-117">Имя, используемое для сжатой базы данных.</span><span class="sxs-lookup"><span data-stu-id="56020-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="56020-118">*пфнстатус*</span><span class="sxs-lookup"><span data-stu-id="56020-118">*pfnStatus*</span></span>

<span data-ttu-id="56020-119">Функция обратного вызова, которую можно периодически вызывать с помощью операции Database Compact для отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="56020-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="56020-120">*пконверт*</span><span class="sxs-lookup"><span data-stu-id="56020-120">*pconvert*</span></span>

<span data-ttu-id="56020-121">Указатель, используемый для обозначения альтернативной библиотеки DLL ESE, которая может использоваться для чтения базы данных-источника, а также для предоставления необязательных параметров для операции **жеткомпакт** , которая преобразует базу данных из более ранней версии в формат более поздней.</span><span class="sxs-lookup"><span data-stu-id="56020-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="56020-122">Эта функция прекращена в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56020-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="56020-123">*грбит*</span><span class="sxs-lookup"><span data-stu-id="56020-123">*grbit*</span></span>

<span data-ttu-id="56020-124">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="56020-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56020-125">Значение</span><span class="sxs-lookup"><span data-stu-id="56020-125">Value</span></span></p></th>
<th><p><span data-ttu-id="56020-126">Значение</span><span class="sxs-lookup"><span data-stu-id="56020-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56020-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="56020-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="56020-128">Используется, если база данных-источник повреждена.</span><span class="sxs-lookup"><span data-stu-id="56020-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="56020-129">Она обеспечивает целый набор новых поведений, предназначенных для восстановления максимально возможного объема данных из базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="56020-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="56020-130"><strong>Жеткомпакт</strong> с этим набором параметров может возвращать JET_errSuccess но не копировать все данные, созданные в базе данных источника.</span><span class="sxs-lookup"><span data-stu-id="56020-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="56020-131">Данные, которые находятся в поврежденных частях базы данных источника, будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="56020-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="56020-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="56020-133">Вызывает <strong>жеткомпакт</strong> для дампа статистики в базе данных-источнике в файл с именем DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="56020-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="56020-134">Статистика включает в себя имя каждой таблицы в базе данных источника, число строк в каждой таблице, общий размер в байтах всех строк в каждой таблице, общий размер в байтах всех столбцов типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> , которые достаточно велики для хранения отдельно от записи, число конечных страниц кластеризованного индекса и количество конечных страниц с длинными значениями.</span><span class="sxs-lookup"><span data-stu-id="56020-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="56020-135">Кроме того, сводные статистические данные, включая размер базы данных-источника, целевую базу данных, время, необходимое для сжатия базы данных, также сохраняются в дампе временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="56020-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="56020-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56020-136">Return Value</span></span>

<span data-ttu-id="56020-137">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="56020-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56020-138">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56020-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56020-139">Код возврата</span><span class="sxs-lookup"><span data-stu-id="56020-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="56020-140">Описание</span><span class="sxs-lookup"><span data-stu-id="56020-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56020-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56020-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56020-142">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56020-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="56020-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="56020-144">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="56020-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="56020-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="56020-146">Указан непустой указатель <em>пконверт</em> , но используемая версия ESE не поддерживает функцию CONVERT.</span><span class="sxs-lookup"><span data-stu-id="56020-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="56020-147">Эта функция была удалена в версии ESE для Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56020-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="56020-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="56020-149">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="56020-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="56020-150">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="56020-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="56020-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="56020-152">Вызывающий сеанс находится в пределах транзакции.</span><span class="sxs-lookup"><span data-stu-id="56020-152">The calling session is within a transaction.</span></span> <span data-ttu-id="56020-153"><strong>Жеткомпакт</strong> должен вызываться сеансом за пределами какой-либо транзакции.</span><span class="sxs-lookup"><span data-stu-id="56020-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="56020-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="56020-155">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="56020-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="56020-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="56020-157">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="56020-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="56020-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="56020-159">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="56020-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="56020-160">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="56020-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="56020-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="56020-162">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="56020-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56020-163">При успешном выполнении база данных-источник копируется в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="56020-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="56020-164">Целевая база данных находится в оптимальном состоянии, например все индексы таблиц находятся в смежном пространстве логического диска.</span><span class="sxs-lookup"><span data-stu-id="56020-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="56020-165">Каждая страница индекса дополняется объемом, настроенным при первоначальном создании индексов в базе данных-источнике.</span><span class="sxs-lookup"><span data-stu-id="56020-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="56020-166">Все параметры данных и метаданных копируются с полной точностью, если не указан параметр восстановления.</span><span class="sxs-lookup"><span data-stu-id="56020-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="56020-167">Если указан параметр восстановления, некоторые данные из базы данных источника могут быть не скопированы.</span><span class="sxs-lookup"><span data-stu-id="56020-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="56020-168">В случае сбоя Целевая база данных может существовать, но не является полной копией базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="56020-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56020-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56020-169">Remarks</span></span>

<span data-ttu-id="56020-170">Сжатие базы данных также используется для обновления базы данных в формате более ранней версии до более современной версии.</span><span class="sxs-lookup"><span data-stu-id="56020-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="56020-171">Необязательный параметр — *пконверт*, который содержит структуру, которая может содержать описание для библиотеки DLL более ранней версии, используемой для чтения формата базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="56020-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="56020-172">Эта функция прекращена в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56020-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="56020-173">После Windows Server 2003 новые версии ESE всегда могут читать старые версии формата базы данных, поэтому эта функция не требуется.</span><span class="sxs-lookup"><span data-stu-id="56020-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="56020-174">Требуемая плотность данных после операции сжатия указывается при создании таблиц и индексов.</span><span class="sxs-lookup"><span data-stu-id="56020-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="56020-175">Плотность должна составлять от 20% до 100%.</span><span class="sxs-lookup"><span data-stu-id="56020-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="56020-176">Если база данных в основном считывается и не обновляется, то для уменьшения числа операций ввода-вывода во время обработки запроса приложения будут устанавливать плотность равным 100%.</span><span class="sxs-lookup"><span data-stu-id="56020-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="56020-177">Однако если данные часто обновляются с операциями, увеличивающими размер данных, хранящихся вместе с записью, или часто вставляются новые данные, то приложение выбирает меньшую плотность, чтобы обновления чаще нашли необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="56020-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="56020-178">Операция сжатия базы данных приводит к тому, что база данных лучше располагаться в соответствии с заполнением, выбранной приложением.</span><span class="sxs-lookup"><span data-stu-id="56020-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="56020-179">Сжатие базы данных — это автономная операция.</span><span class="sxs-lookup"><span data-stu-id="56020-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="56020-180">Она не может быть выполнена, пока используется база данных.</span><span class="sxs-lookup"><span data-stu-id="56020-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="56020-181">В результате он обычно выполняется как часть процесса сборки приложения, который доставляет набор данных как часть самого себя.</span><span class="sxs-lookup"><span data-stu-id="56020-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="56020-182">Автономное сжатие базы данных касается каждого бита данных в базе данных и может использоваться как средство проверки согласованности базы данных.</span><span class="sxs-lookup"><span data-stu-id="56020-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="56020-183">Если база данных сомнительна, ее можно сжать.</span><span class="sxs-lookup"><span data-stu-id="56020-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="56020-184">Если в сжатии не обнаружена ошибка, то будет известно, что база данных находится в допустимом состоянии для ESE.</span><span class="sxs-lookup"><span data-stu-id="56020-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56020-185">Требования</span><span class="sxs-lookup"><span data-stu-id="56020-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56020-186"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="56020-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-187">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="56020-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="56020-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-189">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="56020-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="56020-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-191">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="56020-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-192"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="56020-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-193">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="56020-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56020-194"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="56020-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-195">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="56020-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56020-196"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="56020-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="56020-197">Реализуется как <strong>жеткомпактв</strong> (Юникод) и <strong>жеткомпакта</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="56020-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56020-198">См. также:</span><span class="sxs-lookup"><span data-stu-id="56020-198">See Also</span></span>

[<span data-ttu-id="56020-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="56020-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="56020-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56020-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56020-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="56020-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="56020-202">жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="56020-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="56020-203">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="56020-203">JetStopService</span></span>](./jetstopservice-function.md)
