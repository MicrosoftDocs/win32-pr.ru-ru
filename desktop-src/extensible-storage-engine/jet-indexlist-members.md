---
description: 'Дополнительные сведения о: JET_INDEXLIST Members'
title: Элементы JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081344"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="a7227-103">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="a7227-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="a7227-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="a7227-104">Include protected members</span></span>  
<span data-ttu-id="a7227-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="a7227-105">Include inherited members</span></span>  

<span data-ttu-id="a7227-106">Сведения о временной таблице, содержащей сведения обо всех индексах для данной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7227-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="a7227-107">Тип [JET_INDEXLIST](./jet-indexlist-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="a7227-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="a7227-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="a7227-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7227-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a7227-109">Name</span></span></th>
<th><span data-ttu-id="a7227-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a7227-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="a7227-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="a7227-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7227-113">Начало</span><span class="sxs-lookup"><span data-stu-id="a7227-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="a7227-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7227-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7227-115">Имя</span><span class="sxs-lookup"><span data-stu-id="a7227-115">Name</span></span></th>
<th><span data-ttu-id="a7227-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a7227-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-118"><a href="dn335125(v=exchg.10).md">колумнидкколумн</a></span><span class="sxs-lookup"><span data-stu-id="a7227-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="a7227-119">Возвращает значение columnid столбца во временной таблице, в котором хранится количество столбцов в ключе индекса.</span><span class="sxs-lookup"><span data-stu-id="a7227-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="a7227-120">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-122"><a href="dn335126(v=exchg.10).md">колумнидцентри</a></span><span class="sxs-lookup"><span data-stu-id="a7227-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="a7227-123">Возвращает значение columnid столбца во временной таблице, в котором хранится количество записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="a7227-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="a7227-124">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="a7227-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a7227-125">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-127"><a href="dn335127(v=exchg.10).md">колумнидккэй</a></span><span class="sxs-lookup"><span data-stu-id="a7227-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="a7227-128">Возвращает значение columnid столбца во временной таблице, в котором хранится количество уникальных ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="a7227-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="a7227-129">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="a7227-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a7227-130">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-132"><a href="dn335129(v=exchg.10).md">колумнидколтип</a></span><span class="sxs-lookup"><span data-stu-id="a7227-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="a7227-133">Возвращает значение columnid столбца во временной таблице, в котором хранится тип столбца индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="a7227-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="a7227-134">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-136"><a href="dn335130(v=exchg.10).md">колумнидколумнид</a></span><span class="sxs-lookup"><span data-stu-id="a7227-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="a7227-137">Возвращает значение columnid столбца во временной таблице, в котором хранится значение columnid индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="a7227-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="a7227-138">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-140"><a href="dn335167(v=exchg.10).md">колумнидколумннаме</a></span><span class="sxs-lookup"><span data-stu-id="a7227-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="a7227-141">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a7227-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a7227-142">См. <a href="hh579266(v=exchg.10).md">индекскэйгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a7227-143">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-145"><a href="dn335168(v=exchg.10).md">колумнидкп</a></span><span class="sxs-lookup"><span data-stu-id="a7227-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="a7227-146">Возвращает значение columnid столбца во временной таблице, в котором хранится кодовая страница индексированного столбца.</span><span class="sxs-lookup"><span data-stu-id="a7227-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="a7227-147">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-149"><a href="dn335136(v=exchg.10).md">колумнидкпаже</a></span><span class="sxs-lookup"><span data-stu-id="a7227-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="a7227-150">Возвращает значение columnid столбца во временной таблице, в котором хранится количество страниц в индексе.</span><span class="sxs-lookup"><span data-stu-id="a7227-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="a7227-151">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="a7227-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a7227-152">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-154"><a href="dn335169(v=exchg.10).md">колумнидгрбитколумн</a></span><span class="sxs-lookup"><span data-stu-id="a7227-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="a7227-155">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="a7227-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a7227-156">См. <a href="hh579266(v=exchg.10).md">индекскэйгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a7227-157">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-159"><a href="dn335134(v=exchg.10).md">колумнидгрбитиндекс</a></span><span class="sxs-lookup"><span data-stu-id="a7227-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="a7227-160">Возвращает значение columnid столбца во временной таблице, в котором хранится грбитс, используемый в индексе.</span><span class="sxs-lookup"><span data-stu-id="a7227-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="a7227-161">См. <a href="hh578433(v=exchg.10).md">креатеиндексгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="a7227-162">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-164"><a href="dn335170(v=exchg.10).md">колумнидиколумн</a></span><span class="sxs-lookup"><span data-stu-id="a7227-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="a7227-165">Возвращает значение columnid столбца во временной таблице, в котором хранится индекс этого столбца в ключе индекса.</span><span class="sxs-lookup"><span data-stu-id="a7227-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="a7227-166">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-168"><a href="dn335138(v=exchg.10).md">колумнидиндекснаме</a></span><span class="sxs-lookup"><span data-stu-id="a7227-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="a7227-169">Возвращает значение columnid столбца во временной таблице, в котором хранится имя индекса.</span><span class="sxs-lookup"><span data-stu-id="a7227-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="a7227-170">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-172"><a href="dn335171(v=exchg.10).md">колумнидлангид</a></span><span class="sxs-lookup"><span data-stu-id="a7227-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="a7227-173">Возвращает значение columnid столбца во временной таблице, в котором хранится идентификатор языка (LCID) индекса.</span><span class="sxs-lookup"><span data-stu-id="a7227-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="a7227-174">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-176"><a href="dn335172(v=exchg.10).md">колумнидлкмапфлагс</a></span><span class="sxs-lookup"><span data-stu-id="a7227-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="a7227-177">Возвращает значение columnid столбца во временной таблице, в котором хранятся флаги нормализации Юникода для индекса.</span><span class="sxs-lookup"><span data-stu-id="a7227-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="a7227-178">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-180"><a href="dn335173(v=exchg.10).md">крекорд</a></span><span class="sxs-lookup"><span data-stu-id="a7227-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="a7227-181">Возвращает количество записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a7227-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="a7227-183"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="a7227-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="a7227-184">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="a7227-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="a7227-185">Этот параметр должен быть закрыт, если таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="a7227-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7227-186">Начало</span><span class="sxs-lookup"><span data-stu-id="a7227-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="a7227-187">Методы</span><span class="sxs-lookup"><span data-stu-id="a7227-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7227-188">Имя</span><span class="sxs-lookup"><span data-stu-id="a7227-188">Name</span></span></th>
<th><span data-ttu-id="a7227-189">Описание</span><span class="sxs-lookup"><span data-stu-id="a7227-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="a7227-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Равно</a></span><span class="sxs-lookup"><span data-stu-id="a7227-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="a7227-192">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="a7227-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="a7227-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="a7227-195">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="a7227-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="a7227-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="a7227-198">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="a7227-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="a7227-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="a7227-201">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Защищенный метод" alt="Protected method" /></td>
<td><span data-ttu-id="a7227-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">мембервисеклоне</a></span><span class="sxs-lookup"><span data-stu-id="a7227-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="a7227-204">(Наследуется от <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Открытый метод" alt="Public method" /></td>
<td><span data-ttu-id="a7227-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="a7227-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="a7227-207">Возвращает <a href="/dotnet/api/system.string">строку</a> , представляющую текущий <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="a7227-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="a7227-208">(Переопределяет <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7227-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7227-209">Начало</span><span class="sxs-lookup"><span data-stu-id="a7227-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a7227-210">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7227-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7227-211">Справочник</span><span class="sxs-lookup"><span data-stu-id="a7227-211">Reference</span></span>

[<span data-ttu-id="a7227-212">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="a7227-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="a7227-213">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a7227-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
