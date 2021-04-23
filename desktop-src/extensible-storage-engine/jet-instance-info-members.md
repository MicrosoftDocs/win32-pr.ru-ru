---
description: 'Дополнительные сведения о: JET_INSTANCE_INFO Members'
title: Элементы JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570317"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="66a22-103">Элементы JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="66a22-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="66a22-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="66a22-104">Include protected members</span></span>  
<span data-ttu-id="66a22-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="66a22-105">Include inherited members</span></span>  

<span data-ttu-id="66a22-106">Получает сведения о выполняющихся экземплярах базы данных при использовании с функциями Жетжетинстанцеинфо и Жетосснапшотфризе.</span><span class="sxs-lookup"><span data-stu-id="66a22-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="66a22-107">Тип [JET_INSTANCE_INFO](./jet-instance-info-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="66a22-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="66a22-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="66a22-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="66a22-109">Имя</span><span class="sxs-lookup"><span data-stu-id="66a22-109">Name</span></span></th>
<th><span data-ttu-id="66a22-110">Описание</span><span class="sxs-lookup"><span data-stu-id="66a22-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="66a22-112"><a href="dn335189(v=exchg.10).md">cDatabase</a></span><span class="sxs-lookup"><span data-stu-id="66a22-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="66a22-113">Возвращает число баз данных, присоединенных к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="66a22-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="66a22-115"><a href="dn335190(v=exchg.10).md">хинстанцеид</a></span><span class="sxs-lookup"><span data-stu-id="66a22-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="66a22-116">Возвращает JET_INSTANCE заданного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="66a22-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="66a22-118"><a href="dn335193(v=exchg.10).md">сздатабасефиленаме</a></span><span class="sxs-lookup"><span data-stu-id="66a22-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="66a22-119">Возвращает коллекцию строк, содержащую имя файла базы данных, присоединенной к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="66a22-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="66a22-120">Массив содержит элементы cDatabase.</span><span class="sxs-lookup"><span data-stu-id="66a22-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="66a22-122"><a href="dn335194(v=exchg.10).md">сзинстанценаме</a></span><span class="sxs-lookup"><span data-stu-id="66a22-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="66a22-123">Возвращает имя экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="66a22-123">Gets the name of the database instance.</span></span> <span data-ttu-id="66a22-124">Это значение может быть равно null, если у экземпляра нет имени.</span><span class="sxs-lookup"><span data-stu-id="66a22-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66a22-125">Начало</span><span class="sxs-lookup"><span data-stu-id="66a22-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="66a22-126">Методы</span><span class="sxs-lookup"><span data-stu-id="66a22-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="66a22-127">Имя</span><span class="sxs-lookup"><span data-stu-id="66a22-127">Name</span></span></th>
<th><span data-ttu-id="66a22-128">Описание</span><span class="sxs-lookup"><span data-stu-id="66a22-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="66a22-130"><a href="dn335184(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="66a22-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="66a22-131">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="66a22-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="66a22-132">(Переопределяет <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="66a22-134"><a href="dn335187(v=exchg.10).md">Equals (JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="66a22-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="66a22-135">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="66a22-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="66a22-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="66a22-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="66a22-138">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="66a22-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="66a22-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="66a22-141">Возвращает хэш-код данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="66a22-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="66a22-142">(Переопределяет <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="66a22-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="66a22-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="66a22-145">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="66a22-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="66a22-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="66a22-148">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="66a22-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="66a22-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="66a22-151">Создает строковое представление экземпляра.</span><span class="sxs-lookup"><span data-stu-id="66a22-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="66a22-152">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="66a22-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66a22-153">Начало</span><span class="sxs-lookup"><span data-stu-id="66a22-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="66a22-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66a22-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66a22-155">Справочник</span><span class="sxs-lookup"><span data-stu-id="66a22-155">Reference</span></span>

[<span data-ttu-id="66a22-156">Класс JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="66a22-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="66a22-157">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="66a22-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
