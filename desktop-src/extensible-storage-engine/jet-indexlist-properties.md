---
description: 'Дополнительные сведения о: JET_INDEXLIST свойствах'
title: Свойства JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566371"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="077c5-103">Свойства JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="077c5-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="077c5-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="077c5-104">Include protected members</span></span>  
<span data-ttu-id="077c5-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="077c5-105">Include inherited members</span></span>  

<span data-ttu-id="077c5-106">Тип [JET_INDEXLIST](./jet-indexlist-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="077c5-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="077c5-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="077c5-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="077c5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="077c5-108">Name</span></span></th>
<th><span data-ttu-id="077c5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="077c5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-111"><a href="dn335125(v=exchg.10).md">колумнидкколумн</a></span><span class="sxs-lookup"><span data-stu-id="077c5-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="077c5-112">Возвращает значение columnid столбца во временной таблице, в котором хранится количество столбцов в ключе индекса.</span><span class="sxs-lookup"><span data-stu-id="077c5-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="077c5-113">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-115"><a href="dn335126(v=exchg.10).md">колумнидцентри</a></span><span class="sxs-lookup"><span data-stu-id="077c5-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="077c5-116">Возвращает значение columnid столбца во временной таблице, в котором хранится количество записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="077c5-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="077c5-117">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="077c5-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="077c5-118">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-120"><a href="dn335127(v=exchg.10).md">колумнидккэй</a></span><span class="sxs-lookup"><span data-stu-id="077c5-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="077c5-121">Возвращает значение columnid столбца во временной таблице, в котором хранится количество уникальных ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="077c5-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="077c5-122">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="077c5-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="077c5-123">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-125"><a href="dn335129(v=exchg.10).md">колумнидколтип</a></span><span class="sxs-lookup"><span data-stu-id="077c5-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="077c5-126">Возвращает значение columnid столбца во временной таблице, в котором хранится тип столбца индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="077c5-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="077c5-127">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-129"><a href="dn335130(v=exchg.10).md">колумнидколумнид</a></span><span class="sxs-lookup"><span data-stu-id="077c5-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="077c5-130">Возвращает значение columnid столбца во временной таблице, в котором хранится значение columnid индексируемого столбца.</span><span class="sxs-lookup"><span data-stu-id="077c5-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="077c5-131">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-133"><a href="dn335167(v=exchg.10).md">колумнидколумннаме</a></span><span class="sxs-lookup"><span data-stu-id="077c5-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="077c5-134">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="077c5-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="077c5-135">См. <a href="hh579266(v=exchg.10).md">индекскэйгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="077c5-136">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-138"><a href="dn335168(v=exchg.10).md">колумнидкп</a></span><span class="sxs-lookup"><span data-stu-id="077c5-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="077c5-139">Возвращает значение columnid столбца во временной таблице, в котором хранится кодовая страница индексированного столбца.</span><span class="sxs-lookup"><span data-stu-id="077c5-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="077c5-140">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-142"><a href="dn335136(v=exchg.10).md">колумнидкпаже</a></span><span class="sxs-lookup"><span data-stu-id="077c5-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="077c5-143">Возвращает значение columnid столбца во временной таблице, в котором хранится количество страниц в индексе.</span><span class="sxs-lookup"><span data-stu-id="077c5-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="077c5-144">Это значение не является текущим и обновляется только &quot; API. жеткомпутестатс &quot; .</span><span class="sxs-lookup"><span data-stu-id="077c5-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="077c5-145">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-147"><a href="dn335169(v=exchg.10).md">колумнидгрбитколумн</a></span><span class="sxs-lookup"><span data-stu-id="077c5-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="077c5-148">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="077c5-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="077c5-149">См. <a href="hh579266(v=exchg.10).md">индекскэйгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="077c5-150">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-152"><a href="dn335134(v=exchg.10).md">колумнидгрбитиндекс</a></span><span class="sxs-lookup"><span data-stu-id="077c5-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="077c5-153">Возвращает значение columnid столбца во временной таблице, в котором хранится грбитс, используемый в индексе.</span><span class="sxs-lookup"><span data-stu-id="077c5-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="077c5-154">См. <a href="hh578433(v=exchg.10).md">креатеиндексгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="077c5-155">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-157"><a href="dn335170(v=exchg.10).md">колумнидиколумн</a></span><span class="sxs-lookup"><span data-stu-id="077c5-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="077c5-158">Возвращает значение columnid столбца во временной таблице, в котором хранится индекс этого столбца в ключе индекса.</span><span class="sxs-lookup"><span data-stu-id="077c5-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="077c5-159">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-161"><a href="dn335138(v=exchg.10).md">колумнидиндекснаме</a></span><span class="sxs-lookup"><span data-stu-id="077c5-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="077c5-162">Возвращает значение columnid столбца во временной таблице, в котором хранится имя индекса.</span><span class="sxs-lookup"><span data-stu-id="077c5-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="077c5-163">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-165"><a href="dn335171(v=exchg.10).md">колумнидлангид</a></span><span class="sxs-lookup"><span data-stu-id="077c5-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="077c5-166">Возвращает значение columnid столбца во временной таблице, в котором хранится идентификатор языка (LCID) индекса.</span><span class="sxs-lookup"><span data-stu-id="077c5-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="077c5-167">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-169"><a href="dn335172(v=exchg.10).md">колумнидлкмапфлагс</a></span><span class="sxs-lookup"><span data-stu-id="077c5-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="077c5-170">Возвращает значение columnid столбца во временной таблице, в котором хранятся флаги нормализации Юникода для индекса.</span><span class="sxs-lookup"><span data-stu-id="077c5-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="077c5-171">Столбец имеет тип <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="077c5-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-173"><a href="dn335173(v=exchg.10).md">крекорд</a></span><span class="sxs-lookup"><span data-stu-id="077c5-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="077c5-174">Возвращает количество записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="077c5-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="077c5-176"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="077c5-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="077c5-177">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="077c5-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="077c5-178">Этот параметр должен быть закрыт, если таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="077c5-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="077c5-179">Начало</span><span class="sxs-lookup"><span data-stu-id="077c5-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="077c5-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="077c5-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="077c5-181">Справочник</span><span class="sxs-lookup"><span data-stu-id="077c5-181">Reference</span></span>

[<span data-ttu-id="077c5-182">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="077c5-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="077c5-183">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="077c5-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
