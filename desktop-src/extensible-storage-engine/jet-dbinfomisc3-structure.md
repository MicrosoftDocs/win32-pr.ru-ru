---
description: 'Дополнительные сведения: структура JET_DBINFOMISC3'
title: Структура JET_DBINFOMISC3
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
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
ms.openlocfilehash: 761afe13638d7905b5d4a639b7100108ce6ec977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263057"
---
# <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="71164-103">Структура JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="71164-103">JET_DBINFOMISC3 Structure</span></span>


<span data-ttu-id="71164-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="71164-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="71164-105">Структура JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="71164-105">JET_DBINFOMISC3 Structure</span></span>

<span data-ttu-id="71164-106">Структура **JET_DBINFOMISC3** содержит различные сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="71164-106">The **JET_DBINFOMISC3** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="71164-107">Это сведения, содержащиеся в заголовке базы данных.</span><span class="sxs-lookup"><span data-stu-id="71164-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
    } JET_DBINFOMISC3;
```

### <a name="members"></a><span data-ttu-id="71164-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="71164-108">Members</span></span>

<span data-ttu-id="71164-109">**улверсион**</span><span class="sxs-lookup"><span data-stu-id="71164-109">**ulVersion**</span></span>

<span data-ttu-id="71164-110">Собственная версия ядра СУБД, создавшая базу данных.</span><span class="sxs-lookup"><span data-stu-id="71164-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="71164-111">См. раздел [жетжетверсион](./jetgetversion-function.md) to получение собственной версии для текущего ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="71164-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="71164-112">**улупдате**</span><span class="sxs-lookup"><span data-stu-id="71164-112">**ulUpdate**</span></span>

<span data-ttu-id="71164-113">Отслеживает добавочные обновления формата базы данных с обратной совместимостью.</span><span class="sxs-lookup"><span data-stu-id="71164-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71164-114">Улверсион, Улупдате =</span><span class="sxs-lookup"><span data-stu-id="71164-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="71164-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71164-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71164-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="71164-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="71164-117">Исходный формат бета-версии операционной системы (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="71164-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="71164-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="71164-119">Добавление столбцов в каталог для условного индексирования и старых (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="71164-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="71164-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="71164-121">Добавьте флаг Флокализедтекст в IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="71164-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="71164-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="71164-123">Добавьте SPLIT_BUFFER корневые страницы дерева пространства (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="71164-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="71164-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="71164-125">Отмените изменения, чтобы ESE97 оставалась совместимыми с прямыми (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="71164-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="71164-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="71164-127">Добавьте новые столбцы с тегами в каталог ( &quot; каллбаккдата &quot; и &quot; каллбаккдепенденЦиес &quot; ).</span><span class="sxs-lookup"><span data-stu-id="71164-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="71164-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="71164-129">Поддержка SLV: Сигнслв, Фслвексистс в заголовке базы данных (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="71164-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="71164-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="71164-131">Новое дерево пространства SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="71164-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="71164-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="71164-133">Схема пространства SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="71164-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="71164-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="71164-135">4-байтовый ИДКССЕГ (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="71164-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="71164-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="71164-137">Новый формат столбца шаблона (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="71164-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="71164-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="71164-139">Отсортированные столбцы шаблона (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="71164-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-140">0x620,</span><span class="sxs-lookup"><span data-stu-id="71164-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="71164-141">Основа Объединенного кода (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="71164-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="71164-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="71164-143">Новый формат контрольной суммы (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="71164-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="71164-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="71164-145">Увеличена максимальная длина ключа до 1000/2000 байт для 4/8 КБ страниц (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="71164-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-146">0x620, г</span><span class="sxs-lookup"><span data-stu-id="71164-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="71164-147">Указания пространства каталога, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="71164-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="71164-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="71164-149">Добавьте новый формат узла или экстента в диспетчер пространства, используйте его для зарезервированных пулов пространства (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="71164-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="71164-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="71164-151">Сжатие для внутренних значений long (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="71164-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="71164-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="71164-153">Сжатие для отдельных длинных значений (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="71164-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="71164-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="71164-155">Новый размер фрагмента LV для больших страниц (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="71164-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71164-156">**сигндб**</span><span class="sxs-lookup"><span data-stu-id="71164-156">**signDb**</span></span>

<span data-ttu-id="71164-157">Подпись базы данных (включая время создания).</span><span class="sxs-lookup"><span data-stu-id="71164-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="71164-158">Эта структура составляет 28 байт.</span><span class="sxs-lookup"><span data-stu-id="71164-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="71164-159">**дбстате**</span><span class="sxs-lookup"><span data-stu-id="71164-159">**dbstate**</span></span>

<span data-ttu-id="71164-160">Это состояние базы данных.</span><span class="sxs-lookup"><span data-stu-id="71164-160">This is the database state.</span></span>

<span data-ttu-id="71164-161">Для этого элемента доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="71164-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71164-162">Значение</span><span class="sxs-lookup"><span data-stu-id="71164-162">Value</span></span></p></th>
<th><p><span data-ttu-id="71164-163">Значение</span><span class="sxs-lookup"><span data-stu-id="71164-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71164-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="71164-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="71164-165">1</span><span class="sxs-lookup"><span data-stu-id="71164-165">1</span></span></p></td>
<td><p><span data-ttu-id="71164-166">База данных была только что создана.</span><span class="sxs-lookup"><span data-stu-id="71164-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="71164-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="71164-168">2</span><span class="sxs-lookup"><span data-stu-id="71164-168">2</span></span></p></td>
<td><p><span data-ttu-id="71164-169">Для использования или перемещаемой базы данных необходимо выполнить жесткое или мягкое восстановление.</span><span class="sxs-lookup"><span data-stu-id="71164-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="71164-170">Одна из них не должна пытаться переместить базы данных в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="71164-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="71164-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="71164-172">3</span><span class="sxs-lookup"><span data-stu-id="71164-172">3</span></span></p></td>
<td><p><span data-ttu-id="71164-173">База данных находится в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="71164-173">The database is in a clean state.</span></span> <span data-ttu-id="71164-174">База данных может быть присоединена без каких бы то ни было файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="71164-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="71164-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="71164-176">4</span><span class="sxs-lookup"><span data-stu-id="71164-176">4</span></span></p></td>
<td><p><span data-ttu-id="71164-177">Выполняется обновление базы данных.</span><span class="sxs-lookup"><span data-stu-id="71164-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="71164-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="71164-179">5</span><span class="sxs-lookup"><span data-stu-id="71164-179">5</span></span></p></td>
<td><p><span data-ttu-id="71164-180">Внутренний.</span><span class="sxs-lookup"><span data-stu-id="71164-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71164-181">**лгпосконсистент**</span><span class="sxs-lookup"><span data-stu-id="71164-181">**lgposConsistent**</span></span>

<span data-ttu-id="71164-182">Значение null, если база данных находится в состоянии "грязный".</span><span class="sxs-lookup"><span data-stu-id="71164-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="71164-183">Это расположение журнала, использованное при последнем переключении базы данных в состояние чистого отключения.</span><span class="sxs-lookup"><span data-stu-id="71164-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="71164-184">**логтимеконсистент**</span><span class="sxs-lookup"><span data-stu-id="71164-184">**logtimeConsistent**</span></span>

<span data-ttu-id="71164-185">Значение null, если база данных находится в состоянии "грязный".</span><span class="sxs-lookup"><span data-stu-id="71164-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="71164-186">Это время последнего перевода базы данных в состояние чистого отключения.</span><span class="sxs-lookup"><span data-stu-id="71164-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="71164-187">**логтимеаттач**</span><span class="sxs-lookup"><span data-stu-id="71164-187">**logtimeAttach**</span></span>

<span data-ttu-id="71164-188">Время последнего подключения базы данных к [жетаттачдатабасе](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="71164-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="71164-189">**лгпосаттач**</span><span class="sxs-lookup"><span data-stu-id="71164-189">**lgposAttach**</span></span>

<span data-ttu-id="71164-190">Расположение журнала, которое использовалось в последний раз при присоединении базы данных с помощью [жетаттачдатабасе](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="71164-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="71164-191">**логтимедетач**</span><span class="sxs-lookup"><span data-stu-id="71164-191">**logtimeDetach**</span></span>

<span data-ttu-id="71164-192">Время последней отсоединения базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="71164-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="71164-193">**лгпосдетач**</span><span class="sxs-lookup"><span data-stu-id="71164-193">**lgposDetach**</span></span>

<span data-ttu-id="71164-194">Расположение журнала, которое использовалось в последний раз при отсоединении базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="71164-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="71164-195">**сигнлог**</span><span class="sxs-lookup"><span data-stu-id="71164-195">**signLog**</span></span>

<span data-ttu-id="71164-196">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-197">**бкинфофуллпрев**</span><span class="sxs-lookup"><span data-stu-id="71164-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="71164-198">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-199">**бкинфоинкпрев**</span><span class="sxs-lookup"><span data-stu-id="71164-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="71164-200">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-201">**бкинфофуллкур**</span><span class="sxs-lookup"><span data-stu-id="71164-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="71164-202">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-203">**фшадовингдисаблед**</span><span class="sxs-lookup"><span data-stu-id="71164-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="71164-204">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-205">**фупградедб**</span><span class="sxs-lookup"><span data-stu-id="71164-205">**fUpgradeDb**</span></span>

<span data-ttu-id="71164-206">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="71164-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="71164-207">**двмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="71164-207">**dwMajorVersion**</span></span>

<span data-ttu-id="71164-208">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="71164-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="71164-209">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="71164-209">Used for updating indexes.</span></span>

<span data-ttu-id="71164-210">**двминорверсион**</span><span class="sxs-lookup"><span data-stu-id="71164-210">**dwMinorVersion**</span></span>

<span data-ttu-id="71164-211">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="71164-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="71164-212">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="71164-212">Used for updating indexes.</span></span>

<span data-ttu-id="71164-213">**двбуилднумбер**</span><span class="sxs-lookup"><span data-stu-id="71164-213">**dwBuildNumber**</span></span>

<span data-ttu-id="71164-214">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="71164-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="71164-215">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="71164-215">Used for updating indexes.</span></span>

<span data-ttu-id="71164-216">**лспнумбер**</span><span class="sxs-lookup"><span data-stu-id="71164-216">**lSPNumber**</span></span>

<span data-ttu-id="71164-217">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="71164-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="71164-218">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="71164-218">Used for updating indexes.</span></span>

<span data-ttu-id="71164-219">**кбпажесизе**</span><span class="sxs-lookup"><span data-stu-id="71164-219">**cbPageSize**</span></span>

<span data-ttu-id="71164-220">Размер страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="71164-220">Database page size.</span></span> <span data-ttu-id="71164-221">0 означает, что размер страницы равен 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="71164-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="71164-222">Это значение извлекается, только если JET_DbInfoMisc передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="71164-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="71164-223">**женминрекуиред**</span><span class="sxs-lookup"><span data-stu-id="71164-223">**genMinRequired**</span></span>

<span data-ttu-id="71164-224">Представляет минимальное поколение журналов, необходимое для воспроизведения журналов.</span><span class="sxs-lookup"><span data-stu-id="71164-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="71164-225">Обычно это аналогично созданию контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="71164-225">This is typically the same as the checkpoint generation.</span></span>

<span data-ttu-id="71164-226">**женмаксрекуиред**</span><span class="sxs-lookup"><span data-stu-id="71164-226">**genMaxRequired**</span></span>

<span data-ttu-id="71164-227">Представляет максимальное создание журнала, необходимое для воспроизведения журналов.</span><span class="sxs-lookup"><span data-stu-id="71164-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="71164-228">**логтимеженмакскреате**</span><span class="sxs-lookup"><span data-stu-id="71164-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="71164-229">Представляет дату и время создания файла журнала Женмакс.</span><span class="sxs-lookup"><span data-stu-id="71164-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="71164-230">**улрепаиркаунт**</span><span class="sxs-lookup"><span data-stu-id="71164-230">**ulRepairCount**</span></span>

<span data-ttu-id="71164-231">Количество раз, когда в этой базе данных было вызвано восстановление.</span><span class="sxs-lookup"><span data-stu-id="71164-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="71164-232">**логтимерепаир**</span><span class="sxs-lookup"><span data-stu-id="71164-232">**logtimeRepair**</span></span>

<span data-ttu-id="71164-233">Представляет дату и время выполнения последнего восстановления.</span><span class="sxs-lookup"><span data-stu-id="71164-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="71164-234">**улрепаиркаунтолд**</span><span class="sxs-lookup"><span data-stu-id="71164-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="71164-235">Количество выполнений восстановления в этой базе данных до последней дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="71164-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="71164-236">**улеккфикссукцесс**</span><span class="sxs-lookup"><span data-stu-id="71164-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="71164-237">Количество случаев, когда одна разрядная ошибка была исправлена и привела к хорошей странице.</span><span class="sxs-lookup"><span data-stu-id="71164-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="71164-238">**логтимиккфикссукцесс**</span><span class="sxs-lookup"><span data-stu-id="71164-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="71164-239">Представляет дату и время исправления последней ошибки в битах, что привело к хорошей странице.</span><span class="sxs-lookup"><span data-stu-id="71164-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="71164-240">**улеккфикссукцессолд**</span><span class="sxs-lookup"><span data-stu-id="71164-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="71164-241">Представляет количество случаев, когда одна разрядная ошибка была исправлена и привела к хорошей странице до последнего восстановления.</span><span class="sxs-lookup"><span data-stu-id="71164-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="71164-242">**улеккфиксфаил**</span><span class="sxs-lookup"><span data-stu-id="71164-242">**ulECCFixFail**</span></span>

<span data-ttu-id="71164-243">Количество случаев, когда одна разрядная ошибка была исправлена и привела к поврежденной странице.</span><span class="sxs-lookup"><span data-stu-id="71164-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="71164-244">**логтимиккфиксфаил**</span><span class="sxs-lookup"><span data-stu-id="71164-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="71164-245">Представляет дату и время исправления последней битовой ошибки, которая привела к поврежденной странице.</span><span class="sxs-lookup"><span data-stu-id="71164-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="71164-246">**улеккфиксфаилолд**</span><span class="sxs-lookup"><span data-stu-id="71164-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="71164-247">Количество случаев, когда одна разрядная ошибка была исправлена и привела к поврежденной странице до последнего восстановления.</span><span class="sxs-lookup"><span data-stu-id="71164-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="71164-248">**улбадчекксум**</span><span class="sxs-lookup"><span data-stu-id="71164-248">**ulBadChecksum**</span></span>

<span data-ttu-id="71164-249">Количество случаев, когда обнаружена Неисправимая ошибка ECC/CHECKSUM.</span><span class="sxs-lookup"><span data-stu-id="71164-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="71164-250">**логтимебадчекксум**</span><span class="sxs-lookup"><span data-stu-id="71164-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="71164-251">Представляет дату и время обнаружения последней неисправимой ошибки ECC/CHECKSUM.</span><span class="sxs-lookup"><span data-stu-id="71164-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="71164-252">**улбадчекксумолд**</span><span class="sxs-lookup"><span data-stu-id="71164-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="71164-253">Количество случаев, когда ошибка неисправимой ошибки/контрольной суммы была обнаружена перед последним восстановлением.</span><span class="sxs-lookup"><span data-stu-id="71164-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="71164-254">**женкоммиттед**</span><span class="sxs-lookup"><span data-stu-id="71164-254">**genCommitted**</span></span>

<span data-ttu-id="71164-255">Текущее создание журнала.</span><span class="sxs-lookup"><span data-stu-id="71164-255">The current log generation.</span></span> <span data-ttu-id="71164-256">Это значение может быть меньше Женмаксрекуиред, если JET_paramWaypointLatency не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="71164-256">This can be less than genMaxRequired if JET_paramWaypointLatency is non-zero.</span></span>

### <a name="requirements"></a><span data-ttu-id="71164-257">Требования</span><span class="sxs-lookup"><span data-stu-id="71164-257">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71164-258"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="71164-258"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="71164-259">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="71164-259">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71164-260"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="71164-260"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="71164-261">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="71164-261">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71164-262"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="71164-262"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="71164-263">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="71164-263">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="71164-264">См. также:</span><span class="sxs-lookup"><span data-stu-id="71164-264">See Also</span></span>

[<span data-ttu-id="71164-265">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="71164-265">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="71164-266">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="71164-266">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="71164-267">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="71164-267">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="71164-268">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="71164-268">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="71164-269">жетжетдатабасеинфо</span><span class="sxs-lookup"><span data-stu-id="71164-269">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="71164-270">жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="71164-270">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
