---
description: В таблице Patch указан файл, который должен принимать определенное исправление, и физическое расположение файлов исправлений на образах носителей.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Таблица исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818560"
---
# <a name="patch-table"></a><span data-ttu-id="e5fbf-103">Таблица исправлений</span><span class="sxs-lookup"><span data-stu-id="e5fbf-103">Patch Table</span></span>

<span data-ttu-id="e5fbf-104">В таблице Patch указан файл, который должен принимать определенное исправление, и физическое расположение файлов исправлений на образах носителей.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="e5fbf-105">Таблица исправлений содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="e5fbf-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="e5fbf-106">Column</span></span>      | <span data-ttu-id="e5fbf-107">Type</span><span class="sxs-lookup"><span data-stu-id="e5fbf-107">Type</span></span>                               | <span data-ttu-id="e5fbf-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="e5fbf-108">Key</span></span> | <span data-ttu-id="e5fbf-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="e5fbf-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="e5fbf-110">Файл\_</span><span class="sxs-lookup"><span data-stu-id="e5fbf-110">File\_</span></span>      | [<span data-ttu-id="e5fbf-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e5fbf-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="e5fbf-112">Да</span><span class="sxs-lookup"><span data-stu-id="e5fbf-112">Y</span></span>   | <span data-ttu-id="e5fbf-113">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-113">N</span></span>        |
| <span data-ttu-id="e5fbf-114">Последовательность</span><span class="sxs-lookup"><span data-stu-id="e5fbf-114">Sequence</span></span>    | [<span data-ttu-id="e5fbf-115">Integer</span><span class="sxs-lookup"><span data-stu-id="e5fbf-115">Integer</span></span>](integer.md)             | <span data-ttu-id="e5fbf-116">Да</span><span class="sxs-lookup"><span data-stu-id="e5fbf-116">Y</span></span>   | <span data-ttu-id="e5fbf-117">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-117">N</span></span>        |
| <span data-ttu-id="e5fbf-118">патчсизе</span><span class="sxs-lookup"><span data-stu-id="e5fbf-118">PatchSize</span></span>   | [<span data-ttu-id="e5fbf-119">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="e5fbf-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="e5fbf-120">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-120">N</span></span>   | <span data-ttu-id="e5fbf-121">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-121">N</span></span>        |
| <span data-ttu-id="e5fbf-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5fbf-122">Attributes</span></span>  | [<span data-ttu-id="e5fbf-123">Integer</span><span class="sxs-lookup"><span data-stu-id="e5fbf-123">Integer</span></span>](integer.md)             | <span data-ttu-id="e5fbf-124">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-124">N</span></span>   | <span data-ttu-id="e5fbf-125">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-125">N</span></span>        |
| <span data-ttu-id="e5fbf-126">Header</span><span class="sxs-lookup"><span data-stu-id="e5fbf-126">Header</span></span>      | [<span data-ttu-id="e5fbf-127">Двоичный</span><span class="sxs-lookup"><span data-stu-id="e5fbf-127">Binary</span></span>](binary.md)               | <span data-ttu-id="e5fbf-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-128">N</span></span>   | <span data-ttu-id="e5fbf-129">Да</span><span class="sxs-lookup"><span data-stu-id="e5fbf-129">Y</span></span>        |
| <span data-ttu-id="e5fbf-130">стреамреф\_</span><span class="sxs-lookup"><span data-stu-id="e5fbf-130">StreamRef\_</span></span> | [<span data-ttu-id="e5fbf-131">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e5fbf-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="e5fbf-132">Нет</span><span class="sxs-lookup"><span data-stu-id="e5fbf-132">N</span></span>   | <span data-ttu-id="e5fbf-133">Да</span><span class="sxs-lookup"><span data-stu-id="e5fbf-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e5fbf-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="e5fbf-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e5fbf-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="e5fbf-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-136">Исправление применяется к файлу, заданному идентификатором в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="e5fbf-137">Это первичный ключ таблицы, который является внешним ключом для [таблицы файлов](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fbf-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Виртуализирован</span><span class="sxs-lookup"><span data-stu-id="e5fbf-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-139">Это расположение файла исправления в порядке последовательности файлов на изображениях мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="e5fbf-140">Порядок последовательности должен соответствовать порядку файлов в CAB-файле пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="e5fbf-141">Это первичный ключ для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-141">This is a primary key for this table.</span></span> <span data-ttu-id="e5fbf-142">Максимальный предел — 32767 файлов, чтобы создать пакет установщик Windows с большим числом файлов, см. раздел [Разработка большого пакета](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fbf-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>патчсизе</span><span class="sxs-lookup"><span data-stu-id="e5fbf-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-144">Этот столбец задает размер исправления в байтах, записанных в виде длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="e5fbf-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута</span><span class="sxs-lookup"><span data-stu-id="e5fbf-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-146">Целочисленное значение, содержащее битовые флаги, представляющие атрибуты исправления.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="e5fbf-147">Вставьте значение 1 в этот столбец, чтобы указать, что сбой применения данного исправления не является неустранимой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="e5fbf-148">Константа</span><span class="sxs-lookup"><span data-stu-id="e5fbf-148">Constant</span></span>                         | <span data-ttu-id="e5fbf-149">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="e5fbf-149">Hexadecimal</span></span> | <span data-ttu-id="e5fbf-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="e5fbf-150">Decimal</span></span> | <span data-ttu-id="e5fbf-151">Описание</span><span class="sxs-lookup"><span data-stu-id="e5fbf-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="e5fbf-152">(нет)</span><span class="sxs-lookup"><span data-stu-id="e5fbf-152">(none)</span></span>                           | <span data-ttu-id="e5fbf-153">0x000</span><span class="sxs-lookup"><span data-stu-id="e5fbf-153">0x000</span></span>       | <span data-ttu-id="e5fbf-154">0</span><span class="sxs-lookup"><span data-stu-id="e5fbf-154">0</span></span>       | <span data-ttu-id="e5fbf-155">Сбой установки этого исправления является неустранимой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="e5fbf-156">**мсидбпатчаттрибутеснонвитал**</span><span class="sxs-lookup"><span data-stu-id="e5fbf-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="e5fbf-157">0x001</span><span class="sxs-lookup"><span data-stu-id="e5fbf-157">0x001</span></span>       | <span data-ttu-id="e5fbf-158">1</span><span class="sxs-lookup"><span data-stu-id="e5fbf-158">1</span></span>       | <span data-ttu-id="e5fbf-159">Указывает, что сбой применения этого исправления не является неустранимой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e5fbf-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5fbf-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-161">Этот столбец является заголовком двоичного обновления потока, используемого для проверки исправлений.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="e5fbf-162">Если столбец Стреамреф не равен null, этот столбец должен иметь значение NULL \_ .</span><span class="sxs-lookup"><span data-stu-id="e5fbf-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="e5fbf-163">В этом случае поток заголовков исправлений хранится в [таблице мсипатчхеадерс](msipatchheaders-table.md) , чтобы преодолеть ограничения имен потоков, описанные в разделе [ограничения по OLE для потоков](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fbf-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>стреамреф\_</span><span class="sxs-lookup"><span data-stu-id="e5fbf-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="e5fbf-165">Внешний ключ в таблицу Мсипатчхеадерс, указывающий строку, содержащую поток заголовков исправлений.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5fbf-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5fbf-166">Remarks</span></span>

<span data-ttu-id="e5fbf-167">Эта таблица обрабатывается [действием патчфилес](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="e5fbf-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="e5fbf-168">Обычно он добавляется в пакет установки путем преобразования из пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="e5fbf-169">Обычно он не создается непосредственно в установочном пакете.</span><span class="sxs-lookup"><span data-stu-id="e5fbf-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="e5fbf-170">Проверка</span><span class="sxs-lookup"><span data-stu-id="e5fbf-170">Validation</span></span>

<dl>

[<span data-ttu-id="e5fbf-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="e5fbf-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e5fbf-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="e5fbf-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e5fbf-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="e5fbf-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="e5fbf-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="e5fbf-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



