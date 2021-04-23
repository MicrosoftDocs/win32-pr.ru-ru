---
description: 'Дополнительные сведения: элементы транзакций'
title: 'Участники транзакции '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560889"
---
# <a name="transaction-members"></a><span data-ttu-id="3e7ea-103">Участники транзакции </span><span class="sxs-lookup"><span data-stu-id="3e7ea-103">Transaction members</span></span>

<span data-ttu-id="3e7ea-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="3e7ea-104">Include protected members</span></span>  
<span data-ttu-id="3e7ea-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="3e7ea-105">Include inherited members</span></span>  

<span data-ttu-id="3e7ea-106">Класс, инкапсулирующий транзакцию на JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="3e7ea-107">Тип [транзакции](./transaction-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3e7ea-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="3e7ea-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3e7ea-109">Имя</span><span class="sxs-lookup"><span data-stu-id="3e7ea-109">Name</span></span></th>
<th><span data-ttu-id="3e7ea-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3e7ea-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-112"><a href="dn351177(v=exchg.10).md">Транзакция</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="3e7ea-113">Инициализирует новый экземпляр класса Transaction.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="3e7ea-114">Это автоматически начнет транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-114">This automatically begins a transaction.</span></span> <span data-ttu-id="3e7ea-115">Если не зафиксировано явно, будет выполнен откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e7ea-116">Начало</span><span class="sxs-lookup"><span data-stu-id="3e7ea-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3e7ea-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e7ea-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3e7ea-118">Имя</span><span class="sxs-lookup"><span data-stu-id="3e7ea-118">Name</span></span></th>
<th><span data-ttu-id="3e7ea-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3e7ea-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Защищенное свойство" alt="Protected property" /></td>
<td><span data-ttu-id="3e7ea-121"><a href="dn350578(v=exchg.10).md">хасресаурце</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="3e7ea-122">Возвращает значение, указывающее, выделен ли базовый ресурс в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="3e7ea-123">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="3e7ea-125"><a href="dn351180(v=exchg.10).md">исинтрансактион</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="3e7ea-126">Возвращает значение, указывающее, находится ли данный объект в данный момент в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e7ea-127">Начало</span><span class="sxs-lookup"><span data-stu-id="3e7ea-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3e7ea-128">Методы</span><span class="sxs-lookup"><span data-stu-id="3e7ea-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3e7ea-129">Имя</span><span class="sxs-lookup"><span data-stu-id="3e7ea-129">Name</span></span></th>
<th><span data-ttu-id="3e7ea-130">Описание</span><span class="sxs-lookup"><span data-stu-id="3e7ea-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-132"><a href="dn351172(v=exchg.10).md">Начать</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="3e7ea-133">Начать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-133">Begin a transaction.</span></span> <span data-ttu-id="3e7ea-134">В настоящее время этот объект не должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-136"><a href="dn350541(v=exchg.10).md">чеккобжектиснотдиспосед</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="3e7ea-137">Создать исключение, если этот объект был удален.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="3e7ea-138">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-140"><a href="dn351179(v=exchg.10).md">Commit (Коммиттрансактионгрбит)</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="3e7ea-141">Фиксация транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-141">Commit a transaction.</span></span> <span data-ttu-id="3e7ea-142">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-144"><a href="dn351243(v=exchg.10).md">Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="3e7ea-145">Фиксация транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-145">Commit a transaction.</span></span> <span data-ttu-id="3e7ea-146">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-148"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="3e7ea-149">Удаляет этот объект, освобождая базовый ресурс ESENT.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="3e7ea-150">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-152"><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="3e7ea-153">Вызывается методом Dispose и методом завершения.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="3e7ea-154">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3e7ea-157">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="3e7ea-160">Завершает экземпляр класса Есентресаурце.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="3e7ea-161">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3e7ea-164">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3e7ea-167">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3e7ea-170">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-172"><a href="dn351176(v=exchg.10).md">релеасересаурце</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="3e7ea-173">Вызывается, когда транзакция удаляется в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="3e7ea-174">Эта операция должна откатить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-174">This should rollback the transaction.</span></span> <span data-ttu-id="3e7ea-175">(Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-177"><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="3e7ea-178">Вызывается подклассом при выделении ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="3e7ea-179">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3e7ea-181"><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="3e7ea-182">Вызывается подклассом при освобождении ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="3e7ea-183">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-185"><a href="dn351244(v=exchg.10).md">Откат</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="3e7ea-186">Откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-186">Rollback a transaction.</span></span> <span data-ttu-id="3e7ea-187">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3e7ea-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3e7ea-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3e7ea-190">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущую <a href="dn351174(v=exchg.10).md">транзакцию</a>.</span><span class="sxs-lookup"><span data-stu-id="3e7ea-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="3e7ea-191">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3e7ea-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e7ea-192">Начало</span><span class="sxs-lookup"><span data-stu-id="3e7ea-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3e7ea-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e7ea-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e7ea-194">Справочник</span><span class="sxs-lookup"><span data-stu-id="3e7ea-194">Reference</span></span>

[<span data-ttu-id="3e7ea-195">класс Transaction</span><span class="sxs-lookup"><span data-stu-id="3e7ea-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="3e7ea-196">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3e7ea-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
