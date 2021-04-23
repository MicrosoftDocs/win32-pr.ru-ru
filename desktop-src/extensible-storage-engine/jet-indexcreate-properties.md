---
description: 'Дополнительные сведения о: JET_INDEXCREATE свойствах'
title: Свойства JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999355"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="4a949-103">Свойства JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="4a949-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="4a949-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="4a949-104">Include protected members</span></span>  
<span data-ttu-id="4a949-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="4a949-105">Include inherited members</span></span>  

<span data-ttu-id="4a949-106">Тип [JET_INDEXCREATE](./jet-indexcreate-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="4a949-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="4a949-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="4a949-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4a949-108">Имя</span><span class="sxs-lookup"><span data-stu-id="4a949-108">Name</span></span></th>
<th><span data-ttu-id="4a949-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4a949-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="4a949-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="4a949-112">Возвращает или задает длину (в символах) Сзкэй, включая два завершающих значения NULL.</span><span class="sxs-lookup"><span data-stu-id="4a949-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-114"><a href="dn335156(v=exchg.10).md">кбкэймост</a></span><span class="sxs-lookup"><span data-stu-id="4a949-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="4a949-115">Возвращает или задает максимально допустимый размер (в байтах) для ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="4a949-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="4a949-116">Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="4a949-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="4a949-117">Максимальный размер ключа зависит от размера страницы базы данных <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="4a949-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="4a949-118">Максимальный размер ключа можно получить с помощью <a href="dn351156(v=exchg.10).md">кэймост</a>.</span><span class="sxs-lookup"><span data-stu-id="4a949-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="4a949-119">Этот параметр не учитывается в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4a949-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4a949-120">В отличие от неуправляемого API, <strong>индекскэймост ()</strong> (JET_bitIndexKeyMost) не требуется, он будет добавлен автоматически.</span><span class="sxs-lookup"><span data-stu-id="4a949-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-122"><a href="dn335158(v=exchg.10).md">кбварсегмак</a></span><span class="sxs-lookup"><span data-stu-id="4a949-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="4a949-123">Возвращает или задает максимальную длину (в байтах) каждого столбца для хранения в индексе.</span><span class="sxs-lookup"><span data-stu-id="4a949-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-125"><a href="dn335118(v=exchg.10).md">ккондитионалколумн</a></span><span class="sxs-lookup"><span data-stu-id="4a949-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="4a949-126">Возвращает или задает количество условных столбцов.</span><span class="sxs-lookup"><span data-stu-id="4a949-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-128"><a href="dn335157(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="4a949-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="4a949-129">Возвращает или задает код ошибки из создания этого индекса.</span><span class="sxs-lookup"><span data-stu-id="4a949-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-131"><a href="dn335119(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="4a949-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="4a949-132">Возвращает или задает параметры создания индекса.</span><span class="sxs-lookup"><span data-stu-id="4a949-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-134"><a href="dn335159(v=exchg.10).md">пидксуникоде</a></span><span class="sxs-lookup"><span data-stu-id="4a949-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="4a949-135">Возвращает или задает необязательные параметры сравнения Юникода.</span><span class="sxs-lookup"><span data-stu-id="4a949-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-137"><a href="dn335120(v=exchg.10).md">пспацехинтс</a></span><span class="sxs-lookup"><span data-stu-id="4a949-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="4a949-138">Возвращает или задает размещение, Обслуживание и указания по использованию пространства.</span><span class="sxs-lookup"><span data-stu-id="4a949-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-140"><a href="dn335160(v=exchg.10).md">ргкондитионалколумн</a></span><span class="sxs-lookup"><span data-stu-id="4a949-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="4a949-141">Возвращает или задает необязательные условные столбцы.</span><span class="sxs-lookup"><span data-stu-id="4a949-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-143"><a href="dn335121(v=exchg.10).md">сзиндекснаме</a></span><span class="sxs-lookup"><span data-stu-id="4a949-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="4a949-144">Возвращает или задает имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="4a949-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-146"><a href="dn335161(v=exchg.10).md">сзкэй</a></span><span class="sxs-lookup"><span data-stu-id="4a949-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="4a949-147">Возвращает или задает описание ключа индекса.</span><span class="sxs-lookup"><span data-stu-id="4a949-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="4a949-148">Это строка токенов с разделителями null, заканчивающаяся символом двойной точности null.</span><span class="sxs-lookup"><span data-stu-id="4a949-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="4a949-149">Каждый маркер имеет форму [Direction-name], где параметр Direction-Specification имеет значение &quot; + &quot; или &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="4a949-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="4a949-150">Например, Сзкэй &quot; + abc\0-def\0 + ghi\0 &quot; будет индексировать три столбца &quot; ABC &quot; (в порядке возрастания), &quot; DEF &quot; (в убывающем порядке) и &quot; GHI &quot; (в порядке возрастания).</span><span class="sxs-lookup"><span data-stu-id="4a949-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="4a949-152"><a href="dn335162(v=exchg.10).md">улденсити</a></span><span class="sxs-lookup"><span data-stu-id="4a949-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="4a949-153">Возвращает или задает плотность индекса.</span><span class="sxs-lookup"><span data-stu-id="4a949-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a949-154">Начало</span><span class="sxs-lookup"><span data-stu-id="4a949-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="4a949-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a949-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a949-156">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a949-156">Reference</span></span>

[<span data-ttu-id="4a949-157">Класс JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="4a949-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="4a949-158">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a949-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
