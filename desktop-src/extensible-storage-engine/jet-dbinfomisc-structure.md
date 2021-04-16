---
description: 'Дополнительные сведения: структура JET_DBINFOMISC'
title: Структура JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540095"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="ea1a9-103">Структура JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ea1a9-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="ea1a9-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ea1a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="ea1a9-105">Структура JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ea1a9-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="ea1a9-106">Структура **JET_DBINFOMISC** содержит различные сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="ea1a9-107">Это сведения, содержащиеся в заголовке базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="ea1a9-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="ea1a9-108">Members</span></span>

<span data-ttu-id="ea1a9-109">**улверсион**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-109">**ulVersion**</span></span>

<span data-ttu-id="ea1a9-110">Собственная версия ядра СУБД, создавшая базу данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="ea1a9-111">См. раздел [жетжетверсион](./jetgetversion-function.md) to получение собственной версии для текущего ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="ea1a9-112">**улупдате**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-112">**ulUpdate**</span></span>

<span data-ttu-id="ea1a9-113">Отслеживает добавочные обновления формата базы данных с обратной совместимостью.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea1a9-114">Улверсион, Улупдате =</span><span class="sxs-lookup"><span data-stu-id="ea1a9-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="ea1a9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1a9-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="ea1a9-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-117">Исходный формат бета-версии операционной системы (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="ea1a9-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-119">Добавление столбцов в каталог для условного индексирования и старых (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="ea1a9-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-121">Добавьте флаг Флокализедтекст в IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="ea1a9-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-123">Добавьте SPLIT_BUFFER корневые страницы дерева пространства (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="ea1a9-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-125">Отмените изменения, чтобы ESE97 оставалась совместимыми с прямыми (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="ea1a9-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-127">Добавьте новые столбцы с тегами в каталог ( &quot; каллбаккдата &quot; и &quot; каллбаккдепенденЦиес &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="ea1a9-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-129">Поддержка SLV: Сигнслв, Фслвексистс в заголовке базы данных (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="ea1a9-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-131">Новое дерево пространства SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="ea1a9-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-133">Схема пространства SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="ea1a9-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-135">4-байтовый ИДКССЕГ (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="ea1a9-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-137">Новый формат столбца шаблона (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="ea1a9-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-139">Отсортированные столбцы шаблона (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="ea1a9-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-141">Новый диспетчер пространства (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea1a9-142">**сигндб**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-142">**signDb**</span></span>

<span data-ttu-id="ea1a9-143">Подпись базы данных (включая время создания).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="ea1a9-144">Эта структура составляет 28 байт.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="ea1a9-145">**дбстате**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-145">**dbstate**</span></span>

<span data-ttu-id="ea1a9-146">Это состояние базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-146">This is the database state.</span></span>

<span data-ttu-id="ea1a9-147">Для этого элемента доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea1a9-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1a9-148">Value</span></span></p></th>
<th><p><span data-ttu-id="ea1a9-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1a9-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="ea1a9-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="ea1a9-151">1</span><span class="sxs-lookup"><span data-stu-id="ea1a9-151">1</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-152">База данных была только что создана.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="ea1a9-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="ea1a9-154">2</span><span class="sxs-lookup"><span data-stu-id="ea1a9-154">2</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-155">Для использования или перемещаемой базы данных необходимо выполнить жесткое или мягкое восстановление.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="ea1a9-156">Одна из них не должна пытаться переместить базы данных в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="ea1a9-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="ea1a9-158">3</span><span class="sxs-lookup"><span data-stu-id="ea1a9-158">3</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-159">База данных находится в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-159">The database is in a clean state.</span></span> <span data-ttu-id="ea1a9-160">База данных может быть присоединена без каких бы то ни было файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="ea1a9-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="ea1a9-162">4</span><span class="sxs-lookup"><span data-stu-id="ea1a9-162">4</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-163">Выполняется обновление базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="ea1a9-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="ea1a9-165">5</span><span class="sxs-lookup"><span data-stu-id="ea1a9-165">5</span></span></p></td>
<td><p><span data-ttu-id="ea1a9-166">Внутренний.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea1a9-167">**лгпосконсистент**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-167">**lgposConsistent**</span></span>

<span data-ttu-id="ea1a9-168">Значение null, если база данных находится в состоянии "грязный".</span><span class="sxs-lookup"><span data-stu-id="ea1a9-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="ea1a9-169">Это расположение журнала, использованное при последнем переключении базы данных в состояние чистого отключения.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="ea1a9-170">**логтимеконсистент**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-170">**logtimeConsistent**</span></span>

<span data-ttu-id="ea1a9-171">Значение null, если база данных находится в состоянии "грязный".</span><span class="sxs-lookup"><span data-stu-id="ea1a9-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="ea1a9-172">Это время последнего перевода базы данных в состояние чистого отключения.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="ea1a9-173">**логтимеаттач**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-173">**logtimeAttach**</span></span>

<span data-ttu-id="ea1a9-174">Время последнего подключения базы данных к [жетаттачдатабасе](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="ea1a9-175">**лгпосаттач**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-175">**lgposAttach**</span></span>

<span data-ttu-id="ea1a9-176">Расположение журнала, которое использовалось в последний раз при присоединении базы данных с помощью [жетаттачдатабасе](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="ea1a9-177">**логтимедетач**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-177">**logtimeDetach**</span></span>

<span data-ttu-id="ea1a9-178">Время последней отсоединения базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="ea1a9-179">**лгпосдетач**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-179">**lgposDetach**</span></span>

<span data-ttu-id="ea1a9-180">Расположение журнала, которое использовалось в последний раз при отсоединении базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="ea1a9-181">**сигнлог**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-181">**signLog**</span></span>

<span data-ttu-id="ea1a9-182">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-183">**бкинфофуллпрев**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="ea1a9-184">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-185">**бкинфоинкпрев**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="ea1a9-186">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-187">**бкинфофуллкур**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="ea1a9-188">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-189">**фшадовингдисаблед**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="ea1a9-190">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-191">**фупградедб**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-191">**fUpgradeDb**</span></span>

<span data-ttu-id="ea1a9-192">Поддерживает инфраструктуру ESE и не может использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="ea1a9-193">**двмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-193">**dwMajorVersion**</span></span>

<span data-ttu-id="ea1a9-194">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ea1a9-195">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-195">Used for updating indexes.</span></span>

<span data-ttu-id="ea1a9-196">**двминорверсион**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-196">**dwMinorVersion**</span></span>

<span data-ttu-id="ea1a9-197">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ea1a9-198">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-198">Used for updating indexes.</span></span>

<span data-ttu-id="ea1a9-199">**двбуилднумбер**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-199">**dwBuildNumber**</span></span>

<span data-ttu-id="ea1a9-200">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ea1a9-201">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-201">Used for updating indexes.</span></span>

<span data-ttu-id="ea1a9-202">**лспнумбер**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-202">**lSPNumber**</span></span>

<span data-ttu-id="ea1a9-203">Представляет номера версий Windows NT при обновлении индексов баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="ea1a9-204">Используется для обновления индексов.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-204">Used for updating indexes.</span></span>

<span data-ttu-id="ea1a9-205">**кбпажесизе**</span><span class="sxs-lookup"><span data-stu-id="ea1a9-205">**cbPageSize**</span></span>

<span data-ttu-id="ea1a9-206">Размер страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-206">Database page size.</span></span> <span data-ttu-id="ea1a9-207">0 означает, что размер страницы равен 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="ea1a9-208">Это значение извлекается, только если JET_DbInfoMisc передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ea1a9-209">Требования</span><span class="sxs-lookup"><span data-stu-id="ea1a9-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-210"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="ea1a9-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ea1a9-211">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea1a9-212"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ea1a9-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ea1a9-213">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea1a9-214"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ea1a9-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ea1a9-215">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ea1a9-216">См. также:</span><span class="sxs-lookup"><span data-stu-id="ea1a9-216">See Also</span></span>

[<span data-ttu-id="ea1a9-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="ea1a9-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="ea1a9-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="ea1a9-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="ea1a9-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="ea1a9-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="ea1a9-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="ea1a9-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="ea1a9-221">жетжетдатабасеинфо</span><span class="sxs-lookup"><span data-stu-id="ea1a9-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="ea1a9-222">жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="ea1a9-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
