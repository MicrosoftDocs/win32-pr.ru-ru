---
description: 'Дополнительные сведения о: Вистагрбитс Members'
title: Элементы Вистагрбитс (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559777"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="61272-103">Элементы Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="61272-103">VistaGrbits members</span></span>

<span data-ttu-id="61272-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="61272-104">Include protected members</span></span>  
<span data-ttu-id="61272-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="61272-105">Include inherited members</span></span>  

<span data-ttu-id="61272-106">Грбитс, которые были добавлены в версию ESENT для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61272-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="61272-107">Тип [вистагрбитс](./vistagrbits-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="61272-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="61272-108">Поля</span><span class="sxs-lookup"><span data-stu-id="61272-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="61272-109">name</span><span class="sxs-lookup"><span data-stu-id="61272-109">Name</span></span></th>
<th><span data-ttu-id="61272-110">Описание</span><span class="sxs-lookup"><span data-stu-id="61272-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-113"><a href="dn351283(v=exchg.10).md">континуеафтерсав</a></span><span class="sxs-lookup"><span data-stu-id="61272-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="61272-114">Сеанс моментального снимка продолжится после Жетосснапшотсав и потребуется вызов функции Жетосснапшотенд.</span><span class="sxs-lookup"><span data-stu-id="61272-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-117"><a href="dn335364(v=exchg.10).md">индекскросспродукт</a></span><span class="sxs-lookup"><span data-stu-id="61272-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="61272-118">Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах.</span><span class="sxs-lookup"><span data-stu-id="61272-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="61272-119">В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первое Многозначное значение из любых других ключевых столбцов, которые являются многозначными столбцами.</span><span class="sxs-lookup"><span data-stu-id="61272-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="61272-120">Например, если вы указали этот флаг для индекса по столбцу A, который имеет значения &quot; Red &quot; и &quot; Blue, &quot; а столбец B имеет значения &quot; 1 и 2, то будут &quot; &quot; &quot; созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; красный &quot; , &quot; 2 &quot; ; &quot; синий &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="61272-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="61272-121">В противном случае будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="61272-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-124"><a href="dn335368(v=exchg.10).md">индексдисалловтрункатион</a></span><span class="sxs-lookup"><span data-stu-id="61272-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="61272-125">При указании этого флага любое обновление индекса приведет к сбою усечения ключа с <a href="hh564840(v=exchg.10).md">кэйтрункатед</a>.</span><span class="sxs-lookup"><span data-stu-id="61272-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="61272-126">В противном случае ключи будут обрезаны без уведомления.</span><span class="sxs-lookup"><span data-stu-id="61272-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-129"><a href="dn351285(v=exchg.10).md">индекснестедтабле</a></span><span class="sxs-lookup"><span data-stu-id="61272-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="61272-130">Индексировать несколько столбцов с несколькими значениями, но только со значениями одного Итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="61272-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-133"><a href="dn335282(v=exchg.10).md">логстреаммустексист</a></span><span class="sxs-lookup"><span data-stu-id="61272-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="61272-134">Журналы транзакций должны находиться в каталоге файла журнала (т. е. не может автоматически запустить новый поток).</span><span class="sxs-lookup"><span data-stu-id="61272-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-137"><a href="dn335367(v=exchg.10).md">рековеривисаутундо</a></span><span class="sxs-lookup"><span data-stu-id="61272-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="61272-138">Выполните восстановление, но остановите на этапе отката.</span><span class="sxs-lookup"><span data-stu-id="61272-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="61272-139">Позволяет воспроизводить все журналы, а позднее можно копировать и воспроизводить дополнительные журналы.</span><span class="sxs-lookup"><span data-stu-id="61272-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-142"><a href="dn335375(v=exchg.10).md">реплаймиссингмапентридб</a></span><span class="sxs-lookup"><span data-stu-id="61272-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="61272-143">Отсутствует запись схемы базы данных по умолчанию в то же расположение.</span><span class="sxs-lookup"><span data-stu-id="61272-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-146"><a href="dn335283(v=exchg.10).md">трункатедоне</a></span><span class="sxs-lookup"><span data-stu-id="61272-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="61272-147">Подсистема может пометить заголовки базы данных соответствующим образом (например, завершить полное резервное копирование), даже если вызов truncate не был завершен.</span><span class="sxs-lookup"><span data-stu-id="61272-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="61272-150"><a href="dn335371(v=exchg.10).md">трункателогсафтеррековери</a></span><span class="sxs-lookup"><span data-stu-id="61272-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="61272-151">При успешном обратимом восстановлении усечение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="61272-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61272-152">Начало</span><span class="sxs-lookup"><span data-stu-id="61272-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="61272-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61272-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61272-154">Справочник</span><span class="sxs-lookup"><span data-stu-id="61272-154">Reference</span></span>

[<span data-ttu-id="61272-155">Класс Вистагрбитс</span><span class="sxs-lookup"><span data-stu-id="61272-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="61272-156">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="61272-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
