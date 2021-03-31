---
description: 'Дополнительные сведения о: Есентстопватч Members'
title: Элементы Есентстопватч
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815673"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="26496-103">Элементы Есентстопватч</span><span class="sxs-lookup"><span data-stu-id="26496-103">EsentStopwatch members</span></span>

<span data-ttu-id="26496-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="26496-104">Include protected members</span></span>  
<span data-ttu-id="26496-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="26496-105">Include inherited members</span></span>  

<span data-ttu-id="26496-106">Предоставляет набор методов и свойств, которые можно использовать для измерения статистики работы ESENT для потока.</span><span class="sxs-lookup"><span data-stu-id="26496-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="26496-107">Если текущая версия ESENT не поддерживает [жетжетсреадстатс (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) , все статистические данные ESENT будут иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="26496-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="26496-108">Тип [есентстопватч](./esentstopwatch-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="26496-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="26496-109">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="26496-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="26496-110">Имя</span><span class="sxs-lookup"><span data-stu-id="26496-110">Name</span></span></th>
<th><span data-ttu-id="26496-111">Описание</span><span class="sxs-lookup"><span data-stu-id="26496-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-113"><a href="dn334872(v=exchg.10).md">есентстопватч</a></span><span class="sxs-lookup"><span data-stu-id="26496-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26496-114">Начало</span><span class="sxs-lookup"><span data-stu-id="26496-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="26496-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="26496-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="26496-116">Имя</span><span class="sxs-lookup"><span data-stu-id="26496-116">Name</span></span></th>
<th><span data-ttu-id="26496-117">Описание</span><span class="sxs-lookup"><span data-stu-id="26496-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="26496-119"><a href="dn334934(v=exchg.10).md">Затраченное</a></span><span class="sxs-lookup"><span data-stu-id="26496-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="26496-120">Получает общее затраченное время, измеренное текущим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="26496-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="26496-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span><span class="sxs-lookup"><span data-stu-id="26496-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="26496-123">Возвращает значение, указывающее, работает ли таймер Есентстопватч.</span><span class="sxs-lookup"><span data-stu-id="26496-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="26496-125"><a href="dn334930(v=exchg.10).md">среадстатс</a></span><span class="sxs-lookup"><span data-stu-id="26496-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="26496-126">Возвращает суммарную статистику объема работ ESENT, измеренную текущим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="26496-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26496-127">Начало</span><span class="sxs-lookup"><span data-stu-id="26496-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="26496-128">Методы</span><span class="sxs-lookup"><span data-stu-id="26496-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="26496-129">Имя</span><span class="sxs-lookup"><span data-stu-id="26496-129">Name</span></span></th>
<th><span data-ttu-id="26496-130">Описание</span><span class="sxs-lookup"><span data-stu-id="26496-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="26496-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="26496-133">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="26496-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="26496-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="26496-136">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="26496-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="26496-139">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="26496-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="26496-142">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="26496-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="26496-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="26496-145">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-147"><a href="dn334869(v=exchg.10).md">Сброс</a></span><span class="sxs-lookup"><span data-stu-id="26496-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="26496-148">Останавливает измерение интервала времени и сбрасывает статистику потока.</span><span class="sxs-lookup"><span data-stu-id="26496-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-150"><a href="dn334931(v=exchg.10).md">Запуск</a></span><span class="sxs-lookup"><span data-stu-id="26496-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="26496-151">Начинает измерение работы ESENT.</span><span class="sxs-lookup"><span data-stu-id="26496-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="26496-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="26496-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="26496-155">Инициализирует новый экземпляр Есентстопватч и начинает измерение истекшего времени.</span><span class="sxs-lookup"><span data-stu-id="26496-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-157"><a href="dn334932(v=exchg.10).md">Остановить</a></span><span class="sxs-lookup"><span data-stu-id="26496-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="26496-158">Прекращает измерение работы в ESENT.</span><span class="sxs-lookup"><span data-stu-id="26496-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="26496-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="26496-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="26496-161">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="/dotnet/api/system.diagnostics.stopwatch">секундомер</a>.</span><span class="sxs-lookup"><span data-stu-id="26496-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="26496-162">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="26496-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26496-163">Начало</span><span class="sxs-lookup"><span data-stu-id="26496-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="26496-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26496-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26496-165">Справочник</span><span class="sxs-lookup"><span data-stu-id="26496-165">Reference</span></span>

[<span data-ttu-id="26496-166">Класс Есентстопватч</span><span class="sxs-lookup"><span data-stu-id="26496-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="26496-167">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="26496-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
