---
description: 'Дополнительные сведения: структура JET_SPACEHINTS'
title: Структура JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719286"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="886e7-103">Структура JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="886e7-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="886e7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="886e7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="886e7-105">Структура JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="886e7-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="886e7-106">Структура **JET_SPACEHINTS** содержит сведения о шаблонах выделения пространства, когда сбалансированное дерево растет через разбиение или хотпоинт.</span><span class="sxs-lookup"><span data-stu-id="886e7-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="886e7-107">Разбиение на страницы происходит, когда записи добавляются в конец сбалансированного дерева, а разбиение хотпоинт происходит, когда несколько записей добавляются в одну и ту же виртуальную точку вставки (например, при добавлении "Марие", "Mark", "Мартин'", "Mary" в середину сбалансированного дерева, отсортированного в алфавитном порядке).</span><span class="sxs-lookup"><span data-stu-id="886e7-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="886e7-108">**Windows 7:** Структура **JET_SPACEHINTS** появилась в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="886e7-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="886e7-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="886e7-109">Members</span></span>

<span data-ttu-id="886e7-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="886e7-110">**cbStruct**</span></span>

<span data-ttu-id="886e7-111">Размер данной структуры (в байтах).</span><span class="sxs-lookup"><span data-stu-id="886e7-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="886e7-112">Присвойте этому элементу значение sizeof (JET_SPACEHINTS).</span><span class="sxs-lookup"><span data-stu-id="886e7-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="886e7-113">**улинитиалденсити**</span><span class="sxs-lookup"><span data-stu-id="886e7-113">**ulInitialDensity**</span></span>

<span data-ttu-id="886e7-114">Схема плотности в (добавление).</span><span class="sxs-lookup"><span data-stu-id="886e7-114">The density at (append) layout.</span></span>

<span data-ttu-id="886e7-115">**кбинитиал**</span><span class="sxs-lookup"><span data-stu-id="886e7-115">**cbInitial**</span></span>

<span data-ttu-id="886e7-116">Начальный размер создаваемого объекта (в байтах).</span><span class="sxs-lookup"><span data-stu-id="886e7-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="886e7-117">Это должен быть кратный размер страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="886e7-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="886e7-118">**грбит**</span><span class="sxs-lookup"><span data-stu-id="886e7-118">**grbit**</span></span>

<span data-ttu-id="886e7-119">Группа битов, содержащая параметры, которые должны использоваться для этой структуры, включая ноль или более следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="886e7-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="886e7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="886e7-120">Value</span></span></p></th>
<th><p><span data-ttu-id="886e7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="886e7-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="886e7-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="886e7-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="886e7-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="886e7-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="886e7-124">Изменяет внутреннюю политику выделения для получения хеирарчикалли пространства от непосредственного родителя сбалансированного дерева.</span><span class="sxs-lookup"><span data-stu-id="886e7-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886e7-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="886e7-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="886e7-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="886e7-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="886e7-127">Включает поведение раздельного разбиения для увеличения в соответствии с Dynamics of таблицы (задается Кбминекстент, Улгровс, Кбмаксекстент).</span><span class="sxs-lookup"><span data-stu-id="886e7-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886e7-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="886e7-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="886e7-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="886e7-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="886e7-130">Обеспечивает увеличение поведения хотпоинт Split в соответствии с Dynamics of в таблице (устанавливается параметрами Кбминекстент, Улгровс, Кбмаксекстент).</span><span class="sxs-lookup"><span data-stu-id="886e7-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886e7-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="886e7-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="886e7-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="886e7-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="886e7-133">Если этот параметр задан, клиент указывает, что в качестве основного шаблона использования этой таблицы используется прямая последовательная проверка.</span><span class="sxs-lookup"><span data-stu-id="886e7-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886e7-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="886e7-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="886e7-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="886e7-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="886e7-136">Если задано значение, клиент указывает, что для этой таблицы используется обратная последовательная проверка.</span><span class="sxs-lookup"><span data-stu-id="886e7-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886e7-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="886e7-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="886e7-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="886e7-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="886e7-139">Если задано, приложение ждет, что эта таблица будет очищена в последовательном порядке, от наименьшего ключа к наибольшему.</span><span class="sxs-lookup"><span data-stu-id="886e7-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="886e7-140">**улмаинтденсити**</span><span class="sxs-lookup"><span data-stu-id="886e7-140">**ulMaintDensity**</span></span>

<span data-ttu-id="886e7-141">плотность к Мулмаинтденсити</span><span class="sxs-lookup"><span data-stu-id="886e7-141">density to mulMaintDensity</span></span>

<span data-ttu-id="886e7-142">Плотность для обслуживания в.</span><span class="sxs-lookup"><span data-stu-id="886e7-142">Density to maintain at.</span></span> <span data-ttu-id="886e7-143">Если в указаниях по пространству указано JET_bitRetrieveHintTableScanForward или JET_bitRetrieveHintTableScanBackward, Дефрагментация таблицы будет срабатывать, когда используемое место в таблице станет меньше этого порогового значения.</span><span class="sxs-lookup"><span data-stu-id="886e7-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="886e7-144">Дефрагментацию таблицы можно отключить, установив для этого члена значение 0.</span><span class="sxs-lookup"><span data-stu-id="886e7-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="886e7-145">Если установить этот элемент в значение 100, Дефрагментация таблицы будет выполняться сразу после высвобождения страницы.</span><span class="sxs-lookup"><span data-stu-id="886e7-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="886e7-146">**улгровс**</span><span class="sxs-lookup"><span data-stu-id="886e7-146">**ulGrowth**</span></span>

<span data-ttu-id="886e7-147">Процент роста с последнего роста или исходного размера, округленный до ближайшего размера выделения для собственного модуля JET.</span><span class="sxs-lookup"><span data-stu-id="886e7-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="886e7-148">**Кбминекстент слишком мал**</span><span class="sxs-lookup"><span data-stu-id="886e7-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="886e7-149">Это переопределяет Улгровс, если слишком мал.</span><span class="sxs-lookup"><span data-stu-id="886e7-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="886e7-150">**кбмаксекстент**</span><span class="sxs-lookup"><span data-stu-id="886e7-150">**cbMaxExtent**</span></span>

<span data-ttu-id="886e7-151">Максимальное значение для увеличения в байтах.</span><span class="sxs-lookup"><span data-stu-id="886e7-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="886e7-152">Эти политики Улгровс.</span><span class="sxs-lookup"><span data-stu-id="886e7-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="886e7-153">При увеличении сбалансированного дерева с помощью операций Append или хотпоинт (в отличие от вставки случайных записей) объем пространства, на который будет расти таблица, вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="886e7-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="886e7-154">При создании мы дадим сбалансированное дерево Кбинитиал, всегда.</span><span class="sxs-lookup"><span data-stu-id="886e7-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="886e7-155">При первом выделении данной области мы выделим: Кбинитиал \* улгровс/100 (округленный до размера страницы базы данных) или кбминекстент, если больше.</span><span class="sxs-lookup"><span data-stu-id="886e7-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="886e7-156">При следующем выделении Кбласталлок \* улгровс/100 (округленный до размера страницы базы данных) или кбминекстент, если больше.</span><span class="sxs-lookup"><span data-stu-id="886e7-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="886e7-157">При выделении (которое может быть первым выделением) Вычисленный размер будет превысить Кбмаксекстент, а это будет размер роста.</span><span class="sxs-lookup"><span data-stu-id="886e7-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="886e7-158">Требования</span><span class="sxs-lookup"><span data-stu-id="886e7-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="886e7-159"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="886e7-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="886e7-160">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="886e7-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886e7-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="886e7-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="886e7-162">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="886e7-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886e7-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="886e7-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="886e7-164">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="886e7-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="886e7-165">См. также:</span><span class="sxs-lookup"><span data-stu-id="886e7-165">See Also</span></span>

[<span data-ttu-id="886e7-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="886e7-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="886e7-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="886e7-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
