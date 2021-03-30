---
description: 'Дополнительные сведения о: Windows8Api Members'
title: Элементы Windows8Api (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: Windows8Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_members(v=EXCHG.10)
ms:contentKeyID: 55104331
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21167b66736e5bc05ec14f32cb715226264d2757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991388"
---
# <a name="windows8api-members"></a><span data-ttu-id="0ba92-103">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="0ba92-103">Windows8Api members</span></span>

<span data-ttu-id="0ba92-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="0ba92-104">Include protected members</span></span>  
<span data-ttu-id="0ba92-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="0ba92-105">Include inherited members</span></span>  

<span data-ttu-id="0ba92-106">Вызовы API, появившиеся в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ba92-106">Api calls introduced in Windows 8.</span></span>

<span data-ttu-id="0ba92-107">Тип [Windows8Api](./windows8api-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="0ba92-107">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="0ba92-108">Методы</span><span class="sxs-lookup"><span data-stu-id="0ba92-108">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0ba92-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0ba92-109">Name</span></span></th>
<th><span data-ttu-id="0ba92-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0ba92-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="0ba92-114">Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="0ba92-114">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="0ba92-118">Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="0ba92-118">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="0ba92-119">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="0ba92-119">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="0ba92-123">Создает индексы для данных в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="0ba92-123">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="0ba92-127">Создает таблицу, добавляет столбцы и индексы для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="0ba92-127">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="0ba92-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-131"><a href="dn335493(v=exchg.10).md">жетжетерроринфо</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-131"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="0ba92-132">Получает расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0ba92-132">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="0ba92-136">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="0ba92-136">Creates a temporary table with a single index.</span></span> <span data-ttu-id="0ba92-137">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="0ba92-137">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="0ba92-138">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="0ba92-138">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="0ba92-139">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="0ba92-139">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="0ba92-140">См. также <a href="dn292231(v=exchg.10).md">жетопентемптабле (JET_SESID, [], Int32, темптаблегрбит, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="0ba92-140">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="0ba92-141"><a href="dn335326(v=exchg.10).md">Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="0ba92-141"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-144"><a href="dn335382(v=exchg.10).md">жетпререадиндексранжес</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-144"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="0ba92-145">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ba92-145">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-148"><a href="dn335496(v=exchg.10).md">жетресизедатабасе</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-148"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="0ba92-149">Изменяет размер открытой в данный момент базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ba92-149">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-152"><a href="dn335383(v=exchg.10).md">жетсеткурсорфилтер</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-152"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="0ba92-153">Задайте массив простых фильтров для <a href="dn292217(v=exchg.10).md">жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)</a>.</span><span class="sxs-lookup"><span data-stu-id="0ba92-153">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-156"><a href="dn335495(v=exchg.10).md">жетсетсессионпараметер</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-156"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="0ba92-157">Задает параметр для указанного состояния сеанса, используемый в течение времени существования этого сеанса или до сброса.</span><span class="sxs-lookup"><span data-stu-id="0ba92-157">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="0ba92-161">Подготавливает экземпляр к завершению.</span><span class="sxs-lookup"><span data-stu-id="0ba92-161">Prepares an instance for termination.</span></span> <span data-ttu-id="0ba92-162">Также можно использовать для возобновления предыдущего замораживания.</span><span class="sxs-lookup"><span data-stu-id="0ba92-162">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-165"><a href="dn335386(v=exchg.10).md">жеттрипререадиндексранжес</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-165"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="0ba92-166">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ba92-166">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="0ba92-169"><a href="dn335499(v=exchg.10).md">пререадкэйранжес</a></span><span class="sxs-lookup"><span data-stu-id="0ba92-169"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="0ba92-170">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ba92-170">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ba92-171">Начало</span><span class="sxs-lookup"><span data-stu-id="0ba92-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0ba92-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ba92-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ba92-173">Справочник</span><span class="sxs-lookup"><span data-stu-id="0ba92-173">Reference</span></span>

[<span data-ttu-id="0ba92-174">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="0ba92-174">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="0ba92-175">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="0ba92-175">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
