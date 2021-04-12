---
description: 'Дополнительные сведения о: JET_INDEXCREATE Members'
title: Элементы JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272125"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="dbe5e-103">Элементы JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="dbe5e-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="dbe5e-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="dbe5e-104">Include protected members</span></span>  
<span data-ttu-id="dbe5e-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="dbe5e-105">Include inherited members</span></span>  

<span data-ttu-id="dbe5e-106">Содержит сведения, необходимые для создания индекса по данным в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="dbe5e-107">Содержит сведения, необходимые для создания индекса по данным в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="dbe5e-108">Тип [JET_INDEXCREATE](./jet-indexcreate-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="dbe5e-109">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="dbe5e-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dbe5e-110">Имя</span><span class="sxs-lookup"><span data-stu-id="dbe5e-110">Name</span></span></th>
<th><span data-ttu-id="dbe5e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="dbe5e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbe5e-114">Начало</span><span class="sxs-lookup"><span data-stu-id="dbe5e-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="dbe5e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbe5e-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dbe5e-116">Имя</span><span class="sxs-lookup"><span data-stu-id="dbe5e-116">Name</span></span></th>
<th><span data-ttu-id="dbe5e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dbe5e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="dbe5e-120">Возвращает или задает длину (в символах) Сзкэй, включая два завершающих значения NULL.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-122"><a href="dn335156(v=exchg.10).md">кбкэймост</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="dbe5e-123">Возвращает или задает максимально допустимый размер (в байтах) для ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="dbe5e-124">Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="dbe5e-125">Максимальный размер ключа зависит от размера страницы базы данных <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="dbe5e-126">Максимальный размер ключа можно получить с помощью <a href="dn351156(v=exchg.10).md">кэймост</a>.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="dbe5e-127">Этот параметр не учитывается в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="dbe5e-128">В отличие от неуправляемого API, <strong>индекскэймост ()</strong> (JET_bitIndexKeyMost) не требуется, он будет добавлен автоматически.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-130"><a href="dn335158(v=exchg.10).md">кбварсегмак</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="dbe5e-131">Возвращает или задает максимальную длину (в байтах) каждого столбца для хранения в индексе.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-133"><a href="dn335118(v=exchg.10).md">ккондитионалколумн</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="dbe5e-134">Возвращает или задает количество условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-136"><a href="dn335157(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="dbe5e-137">Возвращает или задает код ошибки из создания этого индекса.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-139"><a href="dn335119(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="dbe5e-140">Возвращает или задает параметры создания индекса.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-142"><a href="dn335159(v=exchg.10).md">пидксуникоде</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="dbe5e-143">Возвращает или задает необязательные параметры сравнения Юникода.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-145"><a href="dn335120(v=exchg.10).md">пспацехинтс</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="dbe5e-146">Возвращает или задает размещение, Обслуживание и указания по использованию пространства.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-148"><a href="dn335160(v=exchg.10).md">ргкондитионалколумн</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="dbe5e-149">Возвращает или задает необязательные условные столбцы.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-151"><a href="dn335121(v=exchg.10).md">сзиндекснаме</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="dbe5e-152">Возвращает или задает имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-154"><a href="dn335161(v=exchg.10).md">сзкэй</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="dbe5e-155">Возвращает или задает описание ключа индекса.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="dbe5e-156">Это строка токенов с разделителями null, заканчивающаяся символом двойной точности null.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="dbe5e-157">Каждый маркер имеет форму [Direction-name], где параметр Direction-Specification имеет значение &quot; + &quot; или &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="dbe5e-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="dbe5e-158">Например, Сзкэй &quot; + abc\0-def\0 + ghi\0 &quot; будет индексировать три столбца &quot; ABC &quot; (в порядке возрастания), &quot; DEF &quot; (в убывающем порядке) и &quot; GHI &quot; (в порядке возрастания).</span><span class="sxs-lookup"><span data-stu-id="dbe5e-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="dbe5e-160"><a href="dn335162(v=exchg.10).md">улденсити</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="dbe5e-161">Возвращает или задает плотность индекса.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbe5e-162">Начало</span><span class="sxs-lookup"><span data-stu-id="dbe5e-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="dbe5e-163">Методы</span><span class="sxs-lookup"><span data-stu-id="dbe5e-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dbe5e-164">Имя</span><span class="sxs-lookup"><span data-stu-id="dbe5e-164">Name</span></span></th>
<th><span data-ttu-id="dbe5e-165">Описание</span><span class="sxs-lookup"><span data-stu-id="dbe5e-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-167"><a href="dn335116(v=exchg.10).md">контентекуалс</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="dbe5e-168">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-170"><a href="dn335153(v=exchg.10).md">дипклоне</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="dbe5e-171">Возвращает глубокую копию объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="dbe5e-174">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="dbe5e-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="dbe5e-177">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="dbe5e-180">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="dbe5e-183">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="dbe5e-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="dbe5e-186">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="dbe5e-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="dbe5e-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="dbe5e-189">Создает строковое представление экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dbe5e-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="dbe5e-190">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="dbe5e-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbe5e-191">Начало</span><span class="sxs-lookup"><span data-stu-id="dbe5e-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe5e-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbe5e-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dbe5e-193">Справочник</span><span class="sxs-lookup"><span data-stu-id="dbe5e-193">Reference</span></span>

[<span data-ttu-id="dbe5e-194">Класс JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="dbe5e-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="dbe5e-195">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dbe5e-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
