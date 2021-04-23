---
description: Дополнительные сведения о методах сеансов
title: 'Методы сеанса '
TOCTitle: Session methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Session
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session_methods(v=EXCHG.10)
ms:contentKeyID: 55104007
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 11f8b31d8c74e3074788b60f62677e9e81135ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811051"
---
# <a name="session-methods"></a><span data-ttu-id="e0b8a-103">Методы сеанса </span><span class="sxs-lookup"><span data-stu-id="e0b8a-103">Session methods</span></span>

<span data-ttu-id="e0b8a-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="e0b8a-104">Include protected members</span></span>  
<span data-ttu-id="e0b8a-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="e0b8a-105">Include inherited members</span></span>  

<span data-ttu-id="e0b8a-106">Тип [сеанса](./session-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-106">The [Session](./session-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="e0b8a-107">Методы</span><span class="sxs-lookup"><span data-stu-id="e0b8a-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e0b8a-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e0b8a-108">Name</span></span></th>
<th><span data-ttu-id="e0b8a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e0b8a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-111"><a href="dn350541(v=exchg.10).md">чеккобжектиснотдиспосед</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="e0b8a-112">Создать исключение, если этот объект был удален.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-112">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="e0b8a-113">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-113">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-115"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-115"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="e0b8a-116">Удаляет этот объект, освобождая базовый ресурс ESENT.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-116">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="e0b8a-117">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-119"><a href="dn350543(v=exchg.10).md">Dispose (логическое значение)</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-119"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="e0b8a-120">Вызывается методом Dispose и методом завершения.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-120">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="e0b8a-121">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-121">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-123"><a href="dn351128(v=exchg.10).md">END</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-123"><a href="dn351128(v=exchg.10).md">End</a></span></span></td>
<td><span data-ttu-id="e0b8a-124">Завершите сеанс.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-124">Terminate the session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e0b8a-127">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-127">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-129"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-129"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="e0b8a-130">Завершает экземпляр класса Есентресаурце.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-130">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="e0b8a-131">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-131">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e0b8a-134">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e0b8a-137">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e0b8a-140">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-142"><a href="dn351165(v=exchg.10).md">релеасересаурце</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-142"><a href="dn351165(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="e0b8a-143">Освободите базовую JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-143">Free the underlying JET_SESID.</span></span> <span data-ttu-id="e0b8a-144">(Переопределяет <a href="dn350545(v=exchg.10).md">есентресаурце. релеасересаурце ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-144">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-146"><a href="dn350576(v=exchg.10).md">ресаурцевасаллокатед</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="e0b8a-147">Вызывается подклассом при выделении ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-147">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="e0b8a-148">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-148">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="e0b8a-150"><a href="dn350577(v=exchg.10).md">ресаурцевасрелеасед</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="e0b8a-151">Вызывается подклассом при освобождении ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-151">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="e0b8a-152">(Наследуется от <a href="dn319890(v=exchg.10).md">есентресаурце</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-152">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="e0b8a-154"><a href="dn351129(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e0b8a-154"><a href="dn351129(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e0b8a-155">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351164(v=exchg.10).md">сеанс</a>.</span><span class="sxs-lookup"><span data-stu-id="e0b8a-155">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351164(v=exchg.10).md">Session</a>.</span></span> <span data-ttu-id="e0b8a-156">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e0b8a-156">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0b8a-157">Начало</span><span class="sxs-lookup"><span data-stu-id="e0b8a-157">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e0b8a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0b8a-158">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0b8a-159">Справочник</span><span class="sxs-lookup"><span data-stu-id="e0b8a-159">Reference</span></span>

[<span data-ttu-id="e0b8a-160">Session class</span><span class="sxs-lookup"><span data-stu-id="e0b8a-160">Session class</span></span>](./session-class.md)

[<span data-ttu-id="e0b8a-161">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e0b8a-161">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
