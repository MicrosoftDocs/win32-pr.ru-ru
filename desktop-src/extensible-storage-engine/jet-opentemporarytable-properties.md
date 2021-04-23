---
description: 'Дополнительные сведения о: JET_OPENTEMPORARYTABLE свойствах'
title: Свойства JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569972"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="ab02b-103">Свойства JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="ab02b-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="ab02b-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="ab02b-104">Include protected members</span></span>  
<span data-ttu-id="ab02b-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="ab02b-105">Include inherited members</span></span>  

<span data-ttu-id="ab02b-106">Тип [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="ab02b-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ab02b-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab02b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ab02b-108">Имя</span><span class="sxs-lookup"><span data-stu-id="ab02b-108">Name</span></span></th>
<th><span data-ttu-id="ab02b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ab02b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-111"><a href="dn335290(v=exchg.10).md">кбкэймост</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="ab02b-112">Возвращает или задает максимальный размер ключа, представляющего заданную строку.</span><span class="sxs-lookup"><span data-stu-id="ab02b-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="ab02b-113">Для управления способом усечения ключей можно задать максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="ab02b-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="ab02b-114">Усечение ключа важно, так как это может повлиять на то, что строки считаются разными.</span><span class="sxs-lookup"><span data-stu-id="ab02b-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="ab02b-115">Если этот параметр имеет значение 0 или 255, то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ab02b-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="ab02b-116">Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>.</span><span class="sxs-lookup"><span data-stu-id="ab02b-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="ab02b-117">Дополнительные сведения см. в разделе <a href="dn335292(v=exchg.10).md">кэймост</a> .</span><span class="sxs-lookup"><span data-stu-id="ab02b-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-119"><a href="dn351219(v=exchg.10).md">кбварсегмак</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="ab02b-120">Возвращает или задает максимальный объем данных, который будет использоваться из любой переменной ленгсколумн для создания ключа для данной строки.</span><span class="sxs-lookup"><span data-stu-id="ab02b-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="ab02b-121">Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом.</span><span class="sxs-lookup"><span data-stu-id="ab02b-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="ab02b-122">Это ограничение указано в байтах.</span><span class="sxs-lookup"><span data-stu-id="ab02b-122">This limit is in bytes.</span></span> <span data-ttu-id="ab02b-123">Если этот параметр равен нулю или имеет то же значение, что и свойство <a href="dn335290(v=exchg.10).md">кбкэймост</a> , ограничение не действует.</span><span class="sxs-lookup"><span data-stu-id="ab02b-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-125"><a href="dn335287(v=exchg.10).md">кколумн</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="ab02b-126">Возвращает или задает количество столбцов в <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</span><span class="sxs-lookup"><span data-stu-id="ab02b-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-128"><a href="dn351232(v=exchg.10).md">грбит</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="ab02b-129">Возвращает или задает параметры для временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="ab02b-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-131"><a href="dn335288(v=exchg.10).md">пидксуникоде</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="ab02b-132">Возвращает или задает код локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="ab02b-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="ab02b-133">Если этот параметр имеет значение null, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab02b-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="ab02b-134">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="ab02b-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="ab02b-135">Если этот параметр имеет значение null, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab02b-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="ab02b-136">Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="ab02b-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-138"><a href="dn351228(v=exchg.10).md">пргколумндеф</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="ab02b-139">Возвращает или задает определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="ab02b-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-141"><a href="dn351233(v=exchg.10).md">пргколумнид</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="ab02b-142">Возвращает или задает выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="ab02b-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="ab02b-143">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="ab02b-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="ab02b-144">В результате размер этого буфера должен соответствовать размеру <a href="dn351228(v=exchg.10).md">пргколумндеф</a>.</span><span class="sxs-lookup"><span data-stu-id="ab02b-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="ab02b-146"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="ab02b-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="ab02b-147">Возвращает маркер таблицы для временной таблицы, созданной в результате успешного вызова Жетопентемпораритабле.</span><span class="sxs-lookup"><span data-stu-id="ab02b-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab02b-148">Начало</span><span class="sxs-lookup"><span data-stu-id="ab02b-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ab02b-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab02b-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab02b-150">Справочник</span><span class="sxs-lookup"><span data-stu-id="ab02b-150">Reference</span></span>

[<span data-ttu-id="ab02b-151">Класс JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="ab02b-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="ab02b-152">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="ab02b-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
