---
description: 'Дополнительные сведения: методы транзакций'
title: 'Методы транзакции '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570391"
---
# <a name="transaction-methods"></a><span data-ttu-id="3c8bd-103">Методы транзакции </span><span class="sxs-lookup"><span data-stu-id="3c8bd-103">Transaction methods</span></span>

<span data-ttu-id="3c8bd-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="3c8bd-104">Include protected members</span></span>  
<span data-ttu-id="3c8bd-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="3c8bd-105">Include inherited members</span></span>  

<span data-ttu-id="3c8bd-106">Тип [транзакции](./transaction-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="3c8bd-107">Методы</span><span class="sxs-lookup"><span data-stu-id="3c8bd-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3c8bd-108">Имя</span><span class="sxs-lookup"><span data-stu-id="3c8bd-108">Name</span></span></th>
<th><span data-ttu-id="3c8bd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3c8bd-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-111"><a href="dn351172(v=exchg.10).md">Начать</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="3c8bd-112">Начать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-112">Begin a transaction.</span></span> <span data-ttu-id="3c8bd-113">В настоящее время этот объект не должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-115"><a href="dn350541(v=exchg.10).md">чеккобжектиснотдиспосед</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="3c8bd-116">Создать исключение, если этот объект был удален.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="3c8bd-117">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-119"><a href="dn351179(v=exchg.10).md">Commit (Коммиттрансактионгрбит)</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="3c8bd-120">Фиксация транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-120">Commit a transaction.</span></span> <span data-ttu-id="3c8bd-121">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-123"><a href="dn351243(v=exchg.10).md">Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="3c8bd-124">Фиксация транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-124">Commit a transaction.</span></span> <span data-ttu-id="3c8bd-125">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-127"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="3c8bd-128">Удаляет этот объект, освобождая базовый ресурс ESENT.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="3c8bd-129">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-131"><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="3c8bd-132">Вызывается методом Dispose и методом завершения.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="3c8bd-133">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3c8bd-136">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="3c8bd-139">Завершает экземпляр класса Есентресаурце.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="3c8bd-140">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3c8bd-143">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3c8bd-146">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3c8bd-149">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-151"><a href="dn351176(v=exchg.10).md">релеасересаурце</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="3c8bd-152">Вызывается, когда транзакция удаляется в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="3c8bd-153">Эта операция должна откатить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-153">This should rollback the transaction.</span></span> <span data-ttu-id="3c8bd-154">(Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-156"><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="3c8bd-157">Вызывается подклассом при выделении ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="3c8bd-158">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="3c8bd-160"><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="3c8bd-161">Вызывается подклассом при освобождении ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="3c8bd-162">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-164"><a href="dn351244(v=exchg.10).md">Откат</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="3c8bd-165">Откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-165">Rollback a transaction.</span></span> <span data-ttu-id="3c8bd-166">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="3c8bd-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3c8bd-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3c8bd-169">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущую <a href="dn351174(v=exchg.10).md">транзакцию</a>.</span><span class="sxs-lookup"><span data-stu-id="3c8bd-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="3c8bd-170">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3c8bd-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c8bd-171">Начало</span><span class="sxs-lookup"><span data-stu-id="3c8bd-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3c8bd-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c8bd-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3c8bd-173">Справочник</span><span class="sxs-lookup"><span data-stu-id="3c8bd-173">Reference</span></span>

[<span data-ttu-id="3c8bd-174">класс Transaction</span><span class="sxs-lookup"><span data-stu-id="3c8bd-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="3c8bd-175">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3c8bd-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
