---
description: 'Дополнительные сведения: методы Windows8Api'
title: Методы Windows8Api (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555201"
---
# <a name="windows8api-methods"></a><span data-ttu-id="5be49-103">Методы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5be49-103">Windows8Api methods</span></span>

<span data-ttu-id="5be49-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="5be49-104">Include protected members</span></span>  
<span data-ttu-id="5be49-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="5be49-105">Include inherited members</span></span>  

<span data-ttu-id="5be49-106">Тип [Windows8Api](./windows8api-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="5be49-106">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="5be49-107">Методы</span><span class="sxs-lookup"><span data-stu-id="5be49-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5be49-108">Имя</span><span class="sxs-lookup"><span data-stu-id="5be49-108">Name</span></span></th>
<th><span data-ttu-id="5be49-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5be49-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="5be49-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="5be49-113">Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="5be49-113">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="5be49-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="5be49-117">Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="5be49-117">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="5be49-118">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5be49-118">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="5be49-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="5be49-122">Создает индексы для данных в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="5be49-122">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="5be49-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="5be49-126">Создает таблицу, добавляет столбцы и индексы для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5be49-126">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="5be49-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="5be49-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-130"><a href="dn335493(v=exchg.10).md">жетжетерроринфо</a></span><span class="sxs-lookup"><span data-stu-id="5be49-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="5be49-131">Получает расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5be49-131">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="5be49-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="5be49-135">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="5be49-135">Creates a temporary table with a single index.</span></span> <span data-ttu-id="5be49-136">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="5be49-136">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="5be49-137">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="5be49-137">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="5be49-138">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="5be49-138">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="5be49-139">См. также <a href="dn292231(v=exchg.10).md">жетопентемптабле (JET_SESID, [], Int32, темптаблегрбит, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="5be49-139">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="5be49-140"><a href="dn335326(v=exchg.10).md">Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="5be49-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-143"><a href="dn335382(v=exchg.10).md">жетпререадиндексранжес</a></span><span class="sxs-lookup"><span data-stu-id="5be49-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="5be49-144">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="5be49-144">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-147"><a href="dn335496(v=exchg.10).md">жетресизедатабасе</a></span><span class="sxs-lookup"><span data-stu-id="5be49-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="5be49-148">Изменяет размер открытой в данный момент базы данных.</span><span class="sxs-lookup"><span data-stu-id="5be49-148">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-151"><a href="dn335383(v=exchg.10).md">жетсеткурсорфилтер</a></span><span class="sxs-lookup"><span data-stu-id="5be49-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="5be49-152">Задайте массив простых фильтров для <a href="dn292217(v=exchg.10).md">жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)</a>.</span><span class="sxs-lookup"><span data-stu-id="5be49-152">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-155"><a href="dn335495(v=exchg.10).md">жетсетсессионпараметер</a></span><span class="sxs-lookup"><span data-stu-id="5be49-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="5be49-156">Задает параметр для указанного состояния сеанса, используемый в течение времени существования этого сеанса или до сброса.</span><span class="sxs-lookup"><span data-stu-id="5be49-156">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="5be49-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="5be49-160">Подготавливает экземпляр к завершению.</span><span class="sxs-lookup"><span data-stu-id="5be49-160">Prepares an instance for termination.</span></span> <span data-ttu-id="5be49-161">Также можно использовать для возобновления предыдущего замораживания.</span><span class="sxs-lookup"><span data-stu-id="5be49-161">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-164"><a href="dn335386(v=exchg.10).md">жеттрипререадиндексранжес</a></span><span class="sxs-lookup"><span data-stu-id="5be49-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="5be49-165">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="5be49-165">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="5be49-168"><a href="dn335499(v=exchg.10).md">пререадкэйранжес</a></span><span class="sxs-lookup"><span data-stu-id="5be49-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="5be49-169">Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="5be49-169">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5be49-170">Начало</span><span class="sxs-lookup"><span data-stu-id="5be49-170">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5be49-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5be49-171">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5be49-172">Справочник</span><span class="sxs-lookup"><span data-stu-id="5be49-172">Reference</span></span>

[<span data-ttu-id="5be49-173">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5be49-173">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="5be49-174">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="5be49-174">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
