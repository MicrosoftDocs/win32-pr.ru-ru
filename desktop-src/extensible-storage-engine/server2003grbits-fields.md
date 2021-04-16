---
description: 'Дополнительные сведения о: Server2003Grbits Fields'
title: Поля Server2003Grbits (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564011"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="1f6a1-103">Поля Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="1f6a1-103">Server2003Grbits fields</span></span>

<span data-ttu-id="1f6a1-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="1f6a1-104">Include protected members</span></span>  
<span data-ttu-id="1f6a1-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="1f6a1-105">Include inherited members</span></span>  

<span data-ttu-id="1f6a1-106">Тип [Server2003Grbits](./server2003grbits-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="1f6a1-107">Поля</span><span class="sxs-lookup"><span data-stu-id="1f6a1-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1f6a1-108">name</span><span class="sxs-lookup"><span data-stu-id="1f6a1-108">Name</span></span></th>
<th><span data-ttu-id="1f6a1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1f6a1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="1f6a1-112"><a href="dn351203(v=exchg.10).md">енумератеигнореусердефинеддефаулт</a></span><span class="sxs-lookup"><span data-stu-id="1f6a1-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="1f6a1-113">Если данный столбец отсутствует в записи и имеет определенное пользователем значение по умолчанию, значение столбца не будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="1f6a1-114">Этот параметр предотвратит вызов функции обратного вызова, которая будет вычислять определенное пользователем значение по умолчанию для столбца, при перечислении значений для этого столбца.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="1f6a1-117"><a href="dn351284(v=exchg.10).md">форвардонли</a></span><span class="sxs-lookup"><span data-stu-id="1f6a1-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="1f6a1-118">Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="1f6a1-119">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="1f6a1-120">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="1f6a1-121">Дополнительные сведения см. в разделе <a href="hh558517(v=exchg.10).md">UNIQUE</a> .</span><span class="sxs-lookup"><span data-stu-id="1f6a1-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="1f6a1-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="1f6a1-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="1f6a1-125">Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="1f6a1-126">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="1f6a1-127">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="1f6a1-128">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="1f6a1-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f6a1-129">Начало</span><span class="sxs-lookup"><span data-stu-id="1f6a1-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1f6a1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f6a1-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f6a1-131">Справочник</span><span class="sxs-lookup"><span data-stu-id="1f6a1-131">Reference</span></span>

[<span data-ttu-id="1f6a1-132">Класс Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="1f6a1-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="1f6a1-133">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="1f6a1-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
