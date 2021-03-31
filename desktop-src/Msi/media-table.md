---
description: В таблице Media описывается набор дисков, которые составляют исходный носитель для установки.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Таблица мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351255"
---
# <a name="media-table"></a><span data-ttu-id="ccdc9-103">Таблица мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ccdc9-103">Media Table</span></span>

<span data-ttu-id="ccdc9-104">В таблице Media описывается набор дисков, которые составляют исходный носитель для установки.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="ccdc9-105">Таблица Media содержит столбцы, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="ccdc9-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="ccdc9-106">Column</span></span>       | <span data-ttu-id="ccdc9-107">Type</span><span class="sxs-lookup"><span data-stu-id="ccdc9-107">Type</span></span>                     | <span data-ttu-id="ccdc9-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="ccdc9-108">Key</span></span> | <span data-ttu-id="ccdc9-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="ccdc9-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="ccdc9-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="ccdc9-110">DiskId</span></span>       | [<span data-ttu-id="ccdc9-111">Integer</span><span class="sxs-lookup"><span data-stu-id="ccdc9-111">Integer</span></span>](integer.md)   | <span data-ttu-id="ccdc9-112">Да</span><span class="sxs-lookup"><span data-stu-id="ccdc9-112">Y</span></span>   | <span data-ttu-id="ccdc9-113">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-113">N</span></span>        |
| <span data-ttu-id="ccdc9-114">ластсекуенце</span><span class="sxs-lookup"><span data-stu-id="ccdc9-114">LastSequence</span></span> | [<span data-ttu-id="ccdc9-115">Integer</span><span class="sxs-lookup"><span data-stu-id="ccdc9-115">Integer</span></span>](integer.md)   | <span data-ttu-id="ccdc9-116">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-116">N</span></span>   | <span data-ttu-id="ccdc9-117">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-117">N</span></span>        |
| <span data-ttu-id="ccdc9-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="ccdc9-118">DiskPrompt</span></span>   | [<span data-ttu-id="ccdc9-119">Text</span><span class="sxs-lookup"><span data-stu-id="ccdc9-119">Text</span></span>](text.md)         | <span data-ttu-id="ccdc9-120">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-120">N</span></span>   | <span data-ttu-id="ccdc9-121">Да</span><span class="sxs-lookup"><span data-stu-id="ccdc9-121">Y</span></span>        |
| <span data-ttu-id="ccdc9-122">Файле</span><span class="sxs-lookup"><span data-stu-id="ccdc9-122">Cabinet</span></span>      | [<span data-ttu-id="ccdc9-123">Файле</span><span class="sxs-lookup"><span data-stu-id="ccdc9-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="ccdc9-124">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-124">N</span></span>   | <span data-ttu-id="ccdc9-125">Да</span><span class="sxs-lookup"><span data-stu-id="ccdc9-125">Y</span></span>        |
| <span data-ttu-id="ccdc9-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="ccdc9-126">VolumeLabel</span></span>  | [<span data-ttu-id="ccdc9-127">Text</span><span class="sxs-lookup"><span data-stu-id="ccdc9-127">Text</span></span>](text.md)         | <span data-ttu-id="ccdc9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-128">N</span></span>   | <span data-ttu-id="ccdc9-129">Да</span><span class="sxs-lookup"><span data-stu-id="ccdc9-129">Y</span></span>        |
| <span data-ttu-id="ccdc9-130">Источник</span><span class="sxs-lookup"><span data-stu-id="ccdc9-130">Source</span></span>       | [<span data-ttu-id="ccdc9-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="ccdc9-131">Property</span></span>](property.md) | <span data-ttu-id="ccdc9-132">Нет</span><span class="sxs-lookup"><span data-stu-id="ccdc9-132">N</span></span>   | <span data-ttu-id="ccdc9-133">Да</span><span class="sxs-lookup"><span data-stu-id="ccdc9-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ccdc9-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="ccdc9-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ccdc9-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="ccdc9-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-136">Определяет порядок сортировки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-136">Determines the sort order for the table.</span></span> <span data-ttu-id="ccdc9-137">Это число должно быть больше или равно 1.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="ccdc9-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>ластсекуенце</span><span class="sxs-lookup"><span data-stu-id="ccdc9-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-139">Порядковый номер файла для последнего файла этого носителя.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="ccdc9-140">Числа в столбце Ластсекуенце указывают, какие файлы в таблице [файлов](file-table.md) находятся на определенном исходном диске.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="ccdc9-141">Каждый исходный диск содержит все файлы с порядковыми номерами (как показано в столбце последовательности таблицы файлов), которые меньше или равны значению в столбце Ластсекуенце и больше чем значение Ластсекуенце предыдущего диска (или больше 0 для первой записи в таблице Media).</span><span class="sxs-lookup"><span data-stu-id="ccdc9-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="ccdc9-142">Это число не должно быть отрицательным. максимальный предел — 32767 файлов.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="ccdc9-143">Дополнительные сведения о создании установщик Windows пакета с большим числом файлов см. [в разделе Разработка большого пакета](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="ccdc9-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccdc9-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="ccdc9-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-145">Имя диска, которое обычно является видимым текстом, напечатанным на диске.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="ccdc9-146">Этот локализуемый текст используется для запроса пользователя, когда необходимо вставить этот диск.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="ccdc9-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Файле</span><span class="sxs-lookup"><span data-stu-id="ccdc9-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-148">Имя CAB-файла, если некоторые или все файлы, хранящиеся на носителе, сжимаются в файл CAB.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="ccdc9-149">Если ящики не используются, этот столбец должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="ccdc9-150">Имя CAB-файла должно использовать синтаксис типа данных [CAB](cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdc9-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="ccdc9-151">Установщик Windows всегда требуется допустимый источник для восстановления файлов, включенных во встроенные CAB-файлы.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="ccdc9-152">Когда установщик Windows устанавливает пакет, содержащий внедренный CAB-файл, его копия может быть сохранена системой.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="ccdc9-153">Эту копию нельзя использовать для восстановления CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="ccdc9-154">Для экономии места на диске используйте внешние CAB-файлы вместо встроенных CAB-файлов.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="ccdc9-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="ccdc9-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-156">Метка, помеченная для тома.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-156">The label attributed to the volume.</span></span> <span data-ttu-id="ccdc9-157">Это метка тома, возвращаемая функцией [**жетволумеинформатион**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="ccdc9-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="ccdc9-158">Если свойство [**SourceDir**](sourcedir.md) ссылается на съемный (гибкий или компакт-диск) том, то эта метка тома используется для проверки того, что диск находится в дисководе, прежде чем пытаться установить файлы.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="ccdc9-159">Запись в этом столбце должна соответствовать метке тома физического носителя.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="ccdc9-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Источника</span><span class="sxs-lookup"><span data-stu-id="ccdc9-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="ccdc9-161">Это поле используется только установкой исправлений. в противном случае оно остается пустым.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="ccdc9-162">Преобразование исправления может ввести здесь свойство, которое является расположением CAB-файла, содержащего файлы исправлений, или новые файлы, добавленные исправлением.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="ccdc9-163">Для этих файлов необходимо указать другой источник, поскольку источник пакета исправлений можно хранить отдельно от источника продукта.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="ccdc9-164">Если поле CAB-файла пустое, установщик игнорирует значение в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="ccdc9-165">Если это поле пустое, установщик использует значение свойства [**SourceDir**](sourcedir.md) в качестве источника CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccdc9-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccdc9-166">Remarks</span></span>

<span data-ttu-id="ccdc9-167">Если перед именем CAB-файла стоит знак решетки ( \# ), файлы, ссылающиеся на эту запись таблицы мультимедиа, упаковываются в CAB-файл, хранящийся в базе данных в виде отдельного потока.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="ccdc9-168">Дополнительные сведения о добавлении CAB в таблицы файлов и таблицы мультимедиа см. в разделе [Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="ccdc9-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="ccdc9-169">Для установщик Windows требуется, чтобы MSI-файл был на первом диске съемного носителя (CD, DVD или дискета), используемого для установки продукта.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="ccdc9-170">**Определение Саурцемоде**</span><span class="sxs-lookup"><span data-stu-id="ccdc9-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="ccdc9-171">Свойство « [**Сводка слов**](word-count-summary.md) » определяет режим источника для текущей установки.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="ccdc9-172">Если это свойство имеет значение 2 или 3, предполагается установка CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="ccdc9-173">В этом режиме предполагается, что CAB-файлы существуют в каталоге, указанном свойством [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdc9-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="ccdc9-174">Если значение типа источника равно 0 или 1, то предполагается, что все исходные файлы существуют в дереве, корневой элемент которого указывается свойством **SourceDir** .</span><span class="sxs-lookup"><span data-stu-id="ccdc9-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="ccdc9-175">Обратите внимание, что это относится только к файлам в таблице файлов, которые не содержат сжатые или несжатые биты, заданные в столбце Attributes.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="ccdc9-176">Эти биты переопределяют значение свойства " [**Сводка слов**](word-count-summary.md) " при определении того, является ли определенный файл сжатым или несжатым.</span><span class="sxs-lookup"><span data-stu-id="ccdc9-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="ccdc9-177">Проверка</span><span class="sxs-lookup"><span data-stu-id="ccdc9-177">Validation</span></span>

<dl>

[<span data-ttu-id="ccdc9-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="ccdc9-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ccdc9-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="ccdc9-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="ccdc9-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="ccdc9-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ccdc9-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="ccdc9-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="ccdc9-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="ccdc9-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="ccdc9-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="ccdc9-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="ccdc9-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="ccdc9-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
