---
description: Дополнительные сведения о перечислении Сетколумнгрбит
title: Перечисление Сетколумнгрбит
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497673"
---
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="d15dd-103">Перечисление Сетколумнгрбит</span><span class="sxs-lookup"><span data-stu-id="d15dd-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="d15dd-104">Параметры для Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="d15dd-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="d15dd-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="d15dd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d15dd-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d15dd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d15dd-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d15dd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d15dd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d15dd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a><span data-ttu-id="d15dd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d15dd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d15dd-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="d15dd-110">Member name</span></span></th>
<th><span data-ttu-id="d15dd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d15dd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d15dd-112">Нет</span><span class="sxs-lookup"><span data-stu-id="d15dd-112">None</span></span></td>
<td><span data-ttu-id="d15dd-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d15dd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d15dd-114">аппендлв</span><span class="sxs-lookup"><span data-stu-id="d15dd-114">AppendLV</span></span></td>
<td><span data-ttu-id="d15dd-115">Этот параметр используется для добавления данных в столбец типа JET_coltypLongText или JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="d15dd-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="d15dd-116">Аналогичное поведение можно добиться, определив размер существующего длинного значения и указав Иблонгвалуе в псетинфо.</span><span class="sxs-lookup"><span data-stu-id="d15dd-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="d15dd-117">Однако проще использовать этот грбит, так как знание размера существующего значения столбца не требуется.</span><span class="sxs-lookup"><span data-stu-id="d15dd-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d15dd-118">оверврителв</span><span class="sxs-lookup"><span data-stu-id="d15dd-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="d15dd-119">Этот параметр используется для замены существующего длинного значения новыми предоставленными данными.</span><span class="sxs-lookup"><span data-stu-id="d15dd-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="d15dd-120">При использовании этого параметра, как будто существующее длинное значение было установлено равным 0 (нулю), перед установкой новых данных.</span><span class="sxs-lookup"><span data-stu-id="d15dd-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d15dd-121">реверттодефаултвалуе</span><span class="sxs-lookup"><span data-stu-id="d15dd-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="d15dd-122">Этот параметр применим только к столбцам с тегами, разреженным или многозначным.</span><span class="sxs-lookup"><span data-stu-id="d15dd-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="d15dd-123">Это приводит к тому, что столбец возвращает значение столбца по умолчанию при последующих операциях получения столбца.</span><span class="sxs-lookup"><span data-stu-id="d15dd-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="d15dd-124">Все существующие значения столбцов удаляются.</span><span class="sxs-lookup"><span data-stu-id="d15dd-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d15dd-125">сепарателв</span><span class="sxs-lookup"><span data-stu-id="d15dd-125">SeparateLV</span></span></td>
<td><span data-ttu-id="d15dd-126">Этот параметр используется для принудительного задания длинного значения, столбцов типа JET_coltyp. LongText или JET_coltyp. Лонгбинари, который будет храниться отдельно от оставшейся части данных записи.</span><span class="sxs-lookup"><span data-stu-id="d15dd-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="d15dd-127">Обычно это происходит, когда размер длинного значения предотвращает сохранение его с помощью оставшихся данных записи.</span><span class="sxs-lookup"><span data-stu-id="d15dd-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="d15dd-128">Однако этот параметр можно использовать для принудительного сохранения длинного значения.</span><span class="sxs-lookup"><span data-stu-id="d15dd-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="d15dd-129">Обратите внимание, что значения long размером четыре байта меньше не могут быть разными.</span><span class="sxs-lookup"><span data-stu-id="d15dd-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="d15dd-130">В таких случаях параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d15dd-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d15dd-131">сизелв</span><span class="sxs-lookup"><span data-stu-id="d15dd-131">SizeLV</span></span></td>
<td><span data-ttu-id="d15dd-132">Этот параметр используется для интерпретации входного буфера в виде целого числа байтов, устанавливаемого в качестве длины длинного значения, описываемого значением columnid, и если оно предоставлено, порядковый номер в псетинфо- &gt; итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="d15dd-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d15dd-133">Если указанный размер больше значения существующего столбца, столбец будет расширен с помощью нулей.</span><span class="sxs-lookup"><span data-stu-id="d15dd-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="d15dd-134">Если размер меньше значения существующего столбца, то значение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="d15dd-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d15dd-135">уникуемултивалуес</span><span class="sxs-lookup"><span data-stu-id="d15dd-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="d15dd-136">Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="d15dd-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="d15dd-137">Этот параметр сравнивает данные исходного столбца без преобразований с другими существующими значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d15dd-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="d15dd-138">Если этот параметр задан, также нельзя указывать Аппендлв, Оверврителв и Сизелв.</span><span class="sxs-lookup"><span data-stu-id="d15dd-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d15dd-139">уникуенормализедмултивалуес</span><span class="sxs-lookup"><span data-stu-id="d15dd-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="d15dd-140">Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="d15dd-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="d15dd-141">Этот параметр сравнивает ключевое нормализованное преобразование данных столбца с другими аналогично преобразованными значениями столбцов, и при обнаружении дубликата возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d15dd-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="d15dd-142">Если этот параметр задан, также нельзя указывать Аппендлв, Оверврителв и Сизелв.</span><span class="sxs-lookup"><span data-stu-id="d15dd-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d15dd-143">зероленгс</span><span class="sxs-lookup"><span data-stu-id="d15dd-143">ZeroLength</span></span></td>
<td><span data-ttu-id="d15dd-144">Этот параметр используется для задания значения нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="d15dd-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="d15dd-145">Как правило, значение столбца устанавливается равным NULL путем передачи Кбмакс 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="d15dd-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="d15dd-146">Однако для некоторых типов, например JET_coltyp. Текст, значение столбца может быть равно 0 (нулевой) длине, а не NULL, и этот параметр используется для различения длины, равной NULL, и 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="d15dd-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d15dd-147">интринсиклв</span><span class="sxs-lookup"><span data-stu-id="d15dd-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="d15dd-148">Попробуйте сохранить в записи столбцы длинных значений, даже если они превышают размер разделения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d15dd-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d15dd-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d15dd-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d15dd-150">Справочник</span><span class="sxs-lookup"><span data-stu-id="d15dd-150">Reference</span></span>

[<span data-ttu-id="d15dd-151">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d15dd-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="d15dd-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="d15dd-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="d15dd-153">Без сжатия</span><span class="sxs-lookup"><span data-stu-id="d15dd-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
