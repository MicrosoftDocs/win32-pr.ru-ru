---
description: Дополнительные сведения о перечислении Енумератеколумнсгрбит
title: Перечисление Енумератеколумнсгрбит
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713003"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="892d6-103">Перечисление Енумератеколумнсгрбит</span><span class="sxs-lookup"><span data-stu-id="892d6-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="892d6-104">Параметры для Жетенумератеколумнс.</span><span class="sxs-lookup"><span data-stu-id="892d6-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="892d6-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="892d6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="892d6-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="892d6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="892d6-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="892d6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="892d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="892d6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a><span data-ttu-id="892d6-109">Члены</span><span class="sxs-lookup"><span data-stu-id="892d6-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="892d6-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="892d6-110">Member name</span></span></th>
<th><span data-ttu-id="892d6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="892d6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="892d6-112">Нет</span><span class="sxs-lookup"><span data-stu-id="892d6-112">None</span></span></td>
<td><span data-ttu-id="892d6-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="892d6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="892d6-114">енумератекомпрессаутпут</span><span class="sxs-lookup"><span data-stu-id="892d6-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="892d6-115">При перечислении значений столбцов все столбцы, для которых мы получаем все значения и которые имеют только одно значение столбца, отличного от NULL, могут быть возвращены в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="892d6-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="892d6-116">Для таких столбцов будет задано значение <a href="hh557250(v=exchg.10).md">колумнсинглевалуе</a> , а размер значения столбца и объем памяти, содержащий значение столбца, будут возвращаться непосредственно в структуре <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="892d6-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="892d6-117">Не гарантируется, что все подходящие столбцы сжимаются таким образом.</span><span class="sxs-lookup"><span data-stu-id="892d6-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="892d6-118">Дополнительные сведения см. в разделе <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="892d6-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="892d6-119">енумератекопи</span><span class="sxs-lookup"><span data-stu-id="892d6-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="892d6-120">Этот параметр указывает, что необходимо перечислить измененные значения столбца записи, а не исходные значения столбца.</span><span class="sxs-lookup"><span data-stu-id="892d6-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="892d6-121">Если значение столбца не было изменено, исходное значение столбца перечисляется.</span><span class="sxs-lookup"><span data-stu-id="892d6-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="892d6-122">Таким образом, значение столбца, которое еще не было вставлено или Обновлено, может быть перечислено при вставке или обновлении записи.</span><span class="sxs-lookup"><span data-stu-id="892d6-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="892d6-123">Этот параметр идентичен <a href="hh578120(v=exchg.10).md">ретриевекопи</a>.</span><span class="sxs-lookup"><span data-stu-id="892d6-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="892d6-124">енумератеигноредефаулт</span><span class="sxs-lookup"><span data-stu-id="892d6-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="892d6-125">Если данный столбец отсутствует в записи, значение столбца не будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="892d6-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="892d6-126">Обычно в этом случае возвращается значение по умолчанию для столбца, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="892d6-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="892d6-127">Гарантируется, что если в столбце задано значение, отличное от значения по умолчанию, то будет возвращено другое значение (т. е. Если для столбца со значением по умолчанию явно задано значение NULL, то в качестве значения для этого столбца будет возвращено значение NULL).</span><span class="sxs-lookup"><span data-stu-id="892d6-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="892d6-128">Даже при запросе этого параметра по-прежнему можно увидеть значение столбца, которое должно быть равно значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="892d6-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="892d6-129">Для удаления значений столбцов, соответствующих значениям по умолчанию, никаких усилий не предпринимается.</span><span class="sxs-lookup"><span data-stu-id="892d6-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="892d6-130">Важно помнить, что этот параметр влияет на выходные данные <a href="dn292148(v=exchg.10).md">жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)</a> при использовании с Енумератепресенцеонли или енумератетагжедонли.</span><span class="sxs-lookup"><span data-stu-id="892d6-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="892d6-131">енумератепресенцеонли</span><span class="sxs-lookup"><span data-stu-id="892d6-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="892d6-132">Если для запрошенного столбца или значения столбца существует значение, отличное от NULL, связанные данные не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="892d6-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="892d6-133">Вместо этого для этого столбца или значения столбца будет задано значение <a href="hh557250(v=exchg.10).md">колумнпресент</a>.</span><span class="sxs-lookup"><span data-stu-id="892d6-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="892d6-134">Если значение столбца или столбца равно NULL, <a href="hh557250(v=exchg.10).md">колумннулл</a> будет возвращен как обычно.</span><span class="sxs-lookup"><span data-stu-id="892d6-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="892d6-135">енумератетагжедонли</span><span class="sxs-lookup"><span data-stu-id="892d6-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="892d6-136">При перечислении всех значений столбцов в записи (например, если Нумколумнидс равен нулю) будут возвращены только значения столбцов с тегами.</span><span class="sxs-lookup"><span data-stu-id="892d6-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="892d6-137">Этот параметр не допускается при перечислении определенного массива идентификаторов столбцов.</span><span class="sxs-lookup"><span data-stu-id="892d6-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="892d6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="892d6-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="892d6-139">Справочник</span><span class="sxs-lookup"><span data-stu-id="892d6-139">Reference</span></span>

[<span data-ttu-id="892d6-140">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="892d6-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="892d6-141">енумератеигнореусердефинеддефаулт</span><span class="sxs-lookup"><span data-stu-id="892d6-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="892d6-142">енумератеинрекордонли</span><span class="sxs-lookup"><span data-stu-id="892d6-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
