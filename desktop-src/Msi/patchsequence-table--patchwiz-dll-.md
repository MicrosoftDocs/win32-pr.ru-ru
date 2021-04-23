---
description: Таблица Патчсекуенце используется для создания таблицы Мсипатчсекуенце в исправлении. Для таблицы требуется версия PATCHWIZ.DLL, доступная в установщик Windows&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Таблица Патчсекуенце (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913464"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="04c90-104">Таблица Патчсекуенце (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="04c90-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="04c90-105">Таблица Патчсекуенце используется для создания [таблицы мсипатчсекуенце](msipatchsequence-table.md) в исправлении.</span><span class="sxs-lookup"><span data-stu-id="04c90-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="04c90-106">Для таблицы требуется версия [PATCHWIZ.DLL](patchwiz-dll.md) , доступная в установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="04c90-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="04c90-107">В следующей таблице указаны столбцы таблицы Патчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="04c90-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="04c90-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="04c90-108">Column</span></span>      | <span data-ttu-id="04c90-109">Type</span><span class="sxs-lookup"><span data-stu-id="04c90-109">Type</span></span>       | <span data-ttu-id="04c90-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="04c90-110">Key</span></span> | <span data-ttu-id="04c90-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="04c90-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="04c90-112">патчфамили</span><span class="sxs-lookup"><span data-stu-id="04c90-112">PatchFamily</span></span> | <span data-ttu-id="04c90-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="04c90-113">Identifier</span></span> | <span data-ttu-id="04c90-114">Да</span><span class="sxs-lookup"><span data-stu-id="04c90-114">Y</span></span>   | <span data-ttu-id="04c90-115">Нет</span><span class="sxs-lookup"><span data-stu-id="04c90-115">N</span></span>        |
| <span data-ttu-id="04c90-116">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="04c90-116">Target</span></span>      | <span data-ttu-id="04c90-117">Текст</span><span class="sxs-lookup"><span data-stu-id="04c90-117">Text</span></span>       | <span data-ttu-id="04c90-118">Да</span><span class="sxs-lookup"><span data-stu-id="04c90-118">Y</span></span>   | <span data-ttu-id="04c90-119">Да</span><span class="sxs-lookup"><span data-stu-id="04c90-119">Y</span></span>        |
| <span data-ttu-id="04c90-120">Последовательность</span><span class="sxs-lookup"><span data-stu-id="04c90-120">Sequence</span></span>    | <span data-ttu-id="04c90-121">Версия</span><span class="sxs-lookup"><span data-stu-id="04c90-121">Version</span></span>    |     | <span data-ttu-id="04c90-122">Да</span><span class="sxs-lookup"><span data-stu-id="04c90-122">Y</span></span>        |
| <span data-ttu-id="04c90-123">Замена</span><span class="sxs-lookup"><span data-stu-id="04c90-123">Supersede</span></span>   | <span data-ttu-id="04c90-124">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="04c90-124">Integer</span></span>    |     | <span data-ttu-id="04c90-125">Да</span><span class="sxs-lookup"><span data-stu-id="04c90-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="04c90-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="04c90-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="04c90-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>патчфамили</span><span class="sxs-lookup"><span data-stu-id="04c90-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="04c90-128">Идентификатор, указывающий семейства последовательностей, к которым относится данное исправление.</span><span class="sxs-lookup"><span data-stu-id="04c90-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="04c90-129">Значения в столбцах Target и Патчфамили вместе определяют первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="04c90-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="04c90-130">Исправление, которое относится к нескольким семействам последовательностей или имеет разные последовательности в зависимости от кода продукта целевого объекта, может иметь по одной строке для каждой пары.</span><span class="sxs-lookup"><span data-stu-id="04c90-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="04c90-131">Это значение используется для заполнения столбца Патчфамили [таблицы мсипатчсекуенце](msipatchsequence-table.md) , которая принадлежит к исправлению.</span><span class="sxs-lookup"><span data-stu-id="04c90-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="04c90-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Мишень</span><span class="sxs-lookup"><span data-stu-id="04c90-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="04c90-133">Целевой столбец используется для фильтрации Патчфамили по коду продукта.</span><span class="sxs-lookup"><span data-stu-id="04c90-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="04c90-134">Значение NULL в этом столбце указывает, что эта Патчфамили применяется ко всем целевым объектам исправления.</span><span class="sxs-lookup"><span data-stu-id="04c90-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="04c90-135">Если этот столбец содержит внешний ключ для [таблицы таржетимажес](targetimages-table-patchwiz-dll-.md), код продукта указанного изображения извлекается и используется для заполнения значения кода продукта в строке нового исправления [таблицы мсипатчсекуенце](msipatchsequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="04c90-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="04c90-136">Если этот столбец содержит идентификатор GUID, идентификатор GUID используется для заполнения значения кода продукта строки в таблице Мсипатчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="04c90-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="04c90-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="04c90-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="04c90-138">Значение в столбце Sequence используется для заполнения столбца Sequence [таблицы мсипатчсекуенце](msipatchsequence-table.md) нового файла исправления.</span><span class="sxs-lookup"><span data-stu-id="04c90-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="04c90-139">Если значение равно NULL, порядковый номер создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="04c90-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="04c90-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Замена</span><span class="sxs-lookup"><span data-stu-id="04c90-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="04c90-141">Значение **мсидбпатчсекуенцесуперседиарлиер** или 1 в этом поле указывает на то, что это исправление заменяет более ранние [небольшие обновления](small-updates.md) в семействах последовательностей, к которым относится данное исправление.</span><span class="sxs-lookup"><span data-stu-id="04c90-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="04c90-142">Значение в этом столбце используется для задания столбца Attributes строки нового исправления в [таблице мсипатчсекуенце](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="04c90-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="04c90-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04c90-143">Remarks</span></span>

<span data-ttu-id="04c90-144">Доступно начиная с установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="04c90-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



