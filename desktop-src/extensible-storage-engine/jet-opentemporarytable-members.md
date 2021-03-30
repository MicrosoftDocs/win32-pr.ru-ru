---
description: 'Дополнительные сведения о: JET_OPENTEMPORARYTABLE Members'
title: Элементы JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552296"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="ea344-103">Элементы JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="ea344-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="ea344-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="ea344-104">Include protected members</span></span>  
<span data-ttu-id="ea344-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="ea344-105">Include inherited members</span></span>  

<span data-ttu-id="ea344-106">Коллекция параметров для метода Жетопентемпораритабле.</span><span class="sxs-lookup"><span data-stu-id="ea344-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="ea344-107">Тип [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="ea344-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ea344-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="ea344-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ea344-109">Имя</span><span class="sxs-lookup"><span data-stu-id="ea344-109">Name</span></span></th>
<th><span data-ttu-id="ea344-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ea344-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="ea344-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="ea344-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea344-113">Начало</span><span class="sxs-lookup"><span data-stu-id="ea344-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ea344-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea344-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ea344-115">Имя</span><span class="sxs-lookup"><span data-stu-id="ea344-115">Name</span></span></th>
<th><span data-ttu-id="ea344-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ea344-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-118"><a href="dn335290(v=exchg.10).md">кбкэймост</a></span><span class="sxs-lookup"><span data-stu-id="ea344-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="ea344-119">Возвращает или задает максимальный размер ключа, представляющего заданную строку.</span><span class="sxs-lookup"><span data-stu-id="ea344-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="ea344-120">Для управления способом усечения ключей можно задать максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="ea344-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="ea344-121">Усечение ключа важно, так как это может повлиять на то, что строки считаются разными.</span><span class="sxs-lookup"><span data-stu-id="ea344-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="ea344-122">Если этот параметр имеет значение 0 или 255, то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ea344-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="ea344-123">Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="ea344-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="ea344-124">Дополнительные сведения см. в разделе <a href="dn335292(v=exchg.10).md">кэймост</a> .</span><span class="sxs-lookup"><span data-stu-id="ea344-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-126"><a href="dn351219(v=exchg.10).md">кбварсегмак</a></span><span class="sxs-lookup"><span data-stu-id="ea344-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="ea344-127">Возвращает или задает максимальный объем данных, который будет использоваться из любой переменной ленгсколумн для создания ключа для данной строки.</span><span class="sxs-lookup"><span data-stu-id="ea344-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="ea344-128">Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом.</span><span class="sxs-lookup"><span data-stu-id="ea344-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="ea344-129">Это ограничение указано в байтах.</span><span class="sxs-lookup"><span data-stu-id="ea344-129">This limit is in bytes.</span></span> <span data-ttu-id="ea344-130">Если этот параметр равен нулю или имеет то же значение, что и свойство <a href="dn335290(v=exchg.10).md">кбкэймост</a> , ограничение не действует.</span><span class="sxs-lookup"><span data-stu-id="ea344-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-132"><a href="dn335287(v=exchg.10).md">кколумн</a></span><span class="sxs-lookup"><span data-stu-id="ea344-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="ea344-133">Возвращает или задает количество столбцов в <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</span><span class="sxs-lookup"><span data-stu-id="ea344-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-135"><a href="dn351232(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="ea344-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="ea344-136">Возвращает или задает параметры для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="ea344-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-138"><a href="dn335288(v=exchg.10).md">пидксуникоде</a></span><span class="sxs-lookup"><span data-stu-id="ea344-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="ea344-139">Возвращает или задает код локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="ea344-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="ea344-140">Если этот параметр имеет значение null, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea344-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="ea344-141">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="ea344-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="ea344-142">Если этот параметр имеет значение null, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea344-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="ea344-143">Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="ea344-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-145"><a href="dn351228(v=exchg.10).md">пргколумндеф</a></span><span class="sxs-lookup"><span data-stu-id="ea344-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="ea344-146">Возвращает или задает определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="ea344-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-148"><a href="dn351233(v=exchg.10).md">пргколумнид</a></span><span class="sxs-lookup"><span data-stu-id="ea344-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="ea344-149">Возвращает или задает выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="ea344-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="ea344-150">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="ea344-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="ea344-151">В результате размер этого буфера должен соответствовать размеру <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</span><span class="sxs-lookup"><span data-stu-id="ea344-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ea344-153"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="ea344-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="ea344-154">Возвращает маркер таблицы для временной таблицы, созданной в результате успешного вызова Жетопентемпораритабле.</span><span class="sxs-lookup"><span data-stu-id="ea344-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea344-155">Начало</span><span class="sxs-lookup"><span data-stu-id="ea344-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ea344-156">Методы</span><span class="sxs-lookup"><span data-stu-id="ea344-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ea344-157">Имя</span><span class="sxs-lookup"><span data-stu-id="ea344-157">Name</span></span></th>
<th><span data-ttu-id="ea344-158">Описание</span><span class="sxs-lookup"><span data-stu-id="ea344-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="ea344-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="ea344-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ea344-161">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="ea344-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="ea344-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ea344-164">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="ea344-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ea344-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ea344-167">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="ea344-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ea344-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ea344-170">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="ea344-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="ea344-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ea344-173">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="ea344-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ea344-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ea344-176">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span><span class="sxs-lookup"><span data-stu-id="ea344-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="ea344-177">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ea344-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea344-178">Начало</span><span class="sxs-lookup"><span data-stu-id="ea344-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ea344-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea344-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ea344-180">Справочник</span><span class="sxs-lookup"><span data-stu-id="ea344-180">Reference</span></span>

[<span data-ttu-id="ea344-181">Класс JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="ea344-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="ea344-182">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="ea344-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
