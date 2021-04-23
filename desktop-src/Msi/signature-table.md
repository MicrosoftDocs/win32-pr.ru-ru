---
description: Таблица сигнатур содержит сведения, которые однозначно идентифицируют подпись файла. Дополнительные сведения о сигнатурах см. в статье цифровые подписи и установщик Windows.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Таблица сигнатур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673975"
---
# <a name="signature-table"></a><span data-ttu-id="44f46-104">Таблица сигнатур</span><span class="sxs-lookup"><span data-stu-id="44f46-104">Signature Table</span></span>

<span data-ttu-id="44f46-105">Таблица сигнатур содержит сведения, которые однозначно идентифицируют подпись файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="44f46-106">Дополнительные сведения о сигнатурах см. в статье [цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="44f46-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="44f46-107">Таблица сигнатур содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="44f46-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="44f46-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="44f46-108">Column</span></span>     | <span data-ttu-id="44f46-109">Type</span><span class="sxs-lookup"><span data-stu-id="44f46-109">Type</span></span>                               | <span data-ttu-id="44f46-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="44f46-110">Key</span></span> | <span data-ttu-id="44f46-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="44f46-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="44f46-112">Подпись</span><span class="sxs-lookup"><span data-stu-id="44f46-112">Signature</span></span>  | [<span data-ttu-id="44f46-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="44f46-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="44f46-114">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-114">Y</span></span>   | <span data-ttu-id="44f46-115">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-115">N</span></span>        |
| <span data-ttu-id="44f46-116">FileName</span><span class="sxs-lookup"><span data-stu-id="44f46-116">FileName</span></span>   | [<span data-ttu-id="44f46-117">Text</span><span class="sxs-lookup"><span data-stu-id="44f46-117">Text</span></span>](text.md)                   | <span data-ttu-id="44f46-118">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-118">N</span></span>   | <span data-ttu-id="44f46-119">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-119">N</span></span>        |
| <span data-ttu-id="44f46-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-120">MinVersion</span></span> | [<span data-ttu-id="44f46-121">Text</span><span class="sxs-lookup"><span data-stu-id="44f46-121">Text</span></span>](text.md)                   | <span data-ttu-id="44f46-122">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-122">N</span></span>   | <span data-ttu-id="44f46-123">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-123">Y</span></span>        |
| <span data-ttu-id="44f46-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-124">MaxVersion</span></span> | [<span data-ttu-id="44f46-125">Text</span><span class="sxs-lookup"><span data-stu-id="44f46-125">Text</span></span>](text.md)                   | <span data-ttu-id="44f46-126">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-126">N</span></span>   | <span data-ttu-id="44f46-127">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-127">Y</span></span>        |
| <span data-ttu-id="44f46-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="44f46-128">MinSize</span></span>    | [<span data-ttu-id="44f46-129">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="44f46-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="44f46-130">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-130">N</span></span>   | <span data-ttu-id="44f46-131">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-131">Y</span></span>        |
| <span data-ttu-id="44f46-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="44f46-132">MaxSize</span></span>    | [<span data-ttu-id="44f46-133">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="44f46-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="44f46-134">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-134">N</span></span>   | <span data-ttu-id="44f46-135">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-135">Y</span></span>        |
| <span data-ttu-id="44f46-136">MinDate</span><span class="sxs-lookup"><span data-stu-id="44f46-136">MinDate</span></span>    | [<span data-ttu-id="44f46-137">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="44f46-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="44f46-138">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-138">N</span></span>   | <span data-ttu-id="44f46-139">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-139">Y</span></span>        |
| <span data-ttu-id="44f46-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="44f46-140">MaxDate</span></span>    | [<span data-ttu-id="44f46-141">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="44f46-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="44f46-142">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-142">N</span></span>   | <span data-ttu-id="44f46-143">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-143">Y</span></span>        |
| <span data-ttu-id="44f46-144">Языки</span><span class="sxs-lookup"><span data-stu-id="44f46-144">Languages</span></span>  | [<span data-ttu-id="44f46-145">Text</span><span class="sxs-lookup"><span data-stu-id="44f46-145">Text</span></span>](text.md)                   | <span data-ttu-id="44f46-146">Нет</span><span class="sxs-lookup"><span data-stu-id="44f46-146">N</span></span>   | <span data-ttu-id="44f46-147">Да</span><span class="sxs-lookup"><span data-stu-id="44f46-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="44f46-148">Столбцы</span><span class="sxs-lookup"><span data-stu-id="44f46-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="44f46-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Образец</span><span class="sxs-lookup"><span data-stu-id="44f46-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="44f46-150">Столбец сигнатуры является уникальной сигнатурой файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов</span><span class="sxs-lookup"><span data-stu-id="44f46-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="44f46-152">Имя файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="44f46-154">Минимальная версия файла с сравнением языков.</span><span class="sxs-lookup"><span data-stu-id="44f46-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="44f46-155">Если это поле указано, то файл должен иметь версию, которая по крайней мере равна MinVersion.</span><span class="sxs-lookup"><span data-stu-id="44f46-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="44f46-156">Если файл имеет равную версию для значения поля MinVersion, но язык, указанный в столбце Languages, отличается, он не удовлетворяет условиям фильтра подписи.</span><span class="sxs-lookup"><span data-stu-id="44f46-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="44f46-157">Язык, указанный в столбце Languages, используется в сравнении и не позволяет пропускать язык.</span><span class="sxs-lookup"><span data-stu-id="44f46-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="44f46-158">Если требуется, чтобы файл соответствовал требованиям к полю MinVersion независимо от языка, необходимо ввести значение в поле MinVersion, которое меньше фактического значения.</span><span class="sxs-lookup"><span data-stu-id="44f46-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="44f46-159">Например, если минимальная версия фильтра — 2.0.2600.1183, используйте 2.0.2600.1182 для поиска файла без соответствующей информации о языке.</span><span class="sxs-lookup"><span data-stu-id="44f46-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="44f46-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="44f46-161">Максимальная версия файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-161">The maximum version of the file.</span></span> <span data-ttu-id="44f46-162">Если это поле указано, то файл должен иметь версию, не превышающую MaxVersion.</span><span class="sxs-lookup"><span data-stu-id="44f46-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="44f46-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="44f46-164">Минимальный размер файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-164">The minimum size of the file.</span></span> <span data-ttu-id="44f46-165">Если это поле указано, то файл проверки должен иметь размер не менее MinSize.</span><span class="sxs-lookup"><span data-stu-id="44f46-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="44f46-166">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="44f46-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="44f46-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="44f46-168">Максимальный размер файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-168">The maximum size of the file.</span></span> <span data-ttu-id="44f46-169">Если это поле указано, то размер файла проверки должен быть не более MaxSize.</span><span class="sxs-lookup"><span data-stu-id="44f46-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="44f46-170">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="44f46-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span><span class="sxs-lookup"><span data-stu-id="44f46-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="44f46-172">Минимальная дата и время изменения файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="44f46-173">Если это поле указано, то файл проверки должен иметь дату и время изменения, которые по крайней мере равны MinDate.</span><span class="sxs-lookup"><span data-stu-id="44f46-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="44f46-174">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="44f46-174">This must be a non-negative number.</span></span> <span data-ttu-id="44f46-175">Формат этого поля — два упакованных 16-разрядных значения типа **слово**.</span><span class="sxs-lookup"><span data-stu-id="44f46-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="44f46-176">Значение **слова** с высоким порядковым значением указывает дату в формате даты MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="44f46-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="44f46-177">Значение **слова** нижнего порядка указывает время в формате времени MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="44f46-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="44f46-178">Значение 0 означает, что значение времени представляет полночь.</span><span class="sxs-lookup"><span data-stu-id="44f46-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="44f46-179">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="44f46-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="44f46-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="44f46-181">Максимальная дата создания файла.</span><span class="sxs-lookup"><span data-stu-id="44f46-181">The maximum creation date of the file.</span></span> <span data-ttu-id="44f46-182">Если это поле указано, то в ходе проверки файл должен иметь дату создания, превышающую значение MaxDate.</span><span class="sxs-lookup"><span data-stu-id="44f46-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="44f46-183">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="44f46-183">This must be a non-negative number.</span></span> <span data-ttu-id="44f46-184">Формат этого поля — два упакованных 16-разрядных значения типа **слово**.</span><span class="sxs-lookup"><span data-stu-id="44f46-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="44f46-185">Значение **слова** с высоким порядковым значением указывает дату в формате даты MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="44f46-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="44f46-186">Значение **слова** нижнего порядка указывает время в формате времени MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="44f46-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="44f46-187">Значение 0 для значения времени представляет полночь.</span><span class="sxs-lookup"><span data-stu-id="44f46-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="44f46-188">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="44f46-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="44f46-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Языки</span><span class="sxs-lookup"><span data-stu-id="44f46-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="44f46-190">Языки, поддерживаемые файлом.</span><span class="sxs-lookup"><span data-stu-id="44f46-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44f46-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44f46-191">Remarks</span></span>

<span data-ttu-id="44f46-192">Эта таблица используется с [таблицей аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="44f46-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="44f46-193">Поиск в сигнатуре осуществляется с помощью [таблицы реглокатор](reglocator-table.md), [таблицы Инилокатор](inilocator-table.md), [таблицы комплокатор](complocator-table.md)и [таблицы дрлокатор](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="44f46-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="44f46-194">Столбцы этой таблицы, как правило, не локализованы.</span><span class="sxs-lookup"><span data-stu-id="44f46-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="44f46-195">Если автор решает выполнить поиск продуктов на нескольких языках, в таблице для каждого языка может присутствовать отдельная запись.</span><span class="sxs-lookup"><span data-stu-id="44f46-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="44f46-196">Таблица сигнатур обычно соответствует [правилам управления версиями файлов](file-versioning-rules.md)установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="44f46-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="44f46-197">Языки, указанные в столбце Languages таблицы Signature, не оцениваются, если только версии файлов не эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="44f46-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="44f46-198">Столбец языки обеспечит наличие файла на определенном языке, если он является запрошенной версией.</span><span class="sxs-lookup"><span data-stu-id="44f46-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="44f46-199">Нет доступных методов для пропуска столбца Languages.</span><span class="sxs-lookup"><span data-stu-id="44f46-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="44f46-200">Значение NULL, указанное в столбце Languages, обрабатывается как файл без языка и не соответствует сигнатуре файла с языком, отображаемым в таблице сигнатур.</span><span class="sxs-lookup"><span data-stu-id="44f46-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="44f46-201">В следующем примере выполняется поиск конкретной версии MSI.DLL.</span><span class="sxs-lookup"><span data-stu-id="44f46-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="44f46-202">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="44f46-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="44f46-203">Образец\_</span><span class="sxs-lookup"><span data-stu-id="44f46-203">Signature\_</span></span> | <span data-ttu-id="44f46-204">Parent</span><span class="sxs-lookup"><span data-stu-id="44f46-204">Parent</span></span> | <span data-ttu-id="44f46-205">Путь</span><span class="sxs-lookup"><span data-stu-id="44f46-205">Path</span></span>                  | <span data-ttu-id="44f46-206">Глубина</span><span class="sxs-lookup"><span data-stu-id="44f46-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="44f46-207">Версию msidll</span><span class="sxs-lookup"><span data-stu-id="44f46-207">MsiDll</span></span>      | <span data-ttu-id="44f46-208">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-208">{null}</span></span> | <span data-ttu-id="44f46-209">c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="44f46-209">c:\\windows\\system32</span></span> | <span data-ttu-id="44f46-210">0</span><span class="sxs-lookup"><span data-stu-id="44f46-210">0</span></span>     |



 

[<span data-ttu-id="44f46-211">Таблица Аппсеарч</span><span class="sxs-lookup"><span data-stu-id="44f46-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="44f46-212">Свойство</span><span class="sxs-lookup"><span data-stu-id="44f46-212">Property</span></span> | <span data-ttu-id="44f46-213">Образец\_</span><span class="sxs-lookup"><span data-stu-id="44f46-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="44f46-214">ВЕРСИЮ MSIDLL</span><span class="sxs-lookup"><span data-stu-id="44f46-214">MSIDLL</span></span>   | <span data-ttu-id="44f46-215">Версию msidll</span><span class="sxs-lookup"><span data-stu-id="44f46-215">MsiDll</span></span>      |



 

<span data-ttu-id="44f46-216">Таблица сигнатур</span><span class="sxs-lookup"><span data-stu-id="44f46-216">Signature table</span></span>



| <span data-ttu-id="44f46-217">Подпись</span><span class="sxs-lookup"><span data-stu-id="44f46-217">Signature</span></span> | <span data-ttu-id="44f46-218">FileName</span><span class="sxs-lookup"><span data-stu-id="44f46-218">FileName</span></span> | <span data-ttu-id="44f46-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-219">MinVersion</span></span>    | <span data-ttu-id="44f46-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="44f46-220">MaxVersion</span></span> | <span data-ttu-id="44f46-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="44f46-221">MinSize</span></span> | <span data-ttu-id="44f46-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="44f46-222">MaxSize</span></span> | <span data-ttu-id="44f46-223">MinDate</span><span class="sxs-lookup"><span data-stu-id="44f46-223">MinDate</span></span> | <span data-ttu-id="44f46-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="44f46-224">MaxDate</span></span> | <span data-ttu-id="44f46-225">Языки</span><span class="sxs-lookup"><span data-stu-id="44f46-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="44f46-226">Версию msidll</span><span class="sxs-lookup"><span data-stu-id="44f46-226">MsiDll</span></span>    | <span data-ttu-id="44f46-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="44f46-227">msi.dll</span></span>  | <span data-ttu-id="44f46-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="44f46-228">2.0.2600.1106</span></span> | <span data-ttu-id="44f46-229">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-229">{null}</span></span>     | <span data-ttu-id="44f46-230">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-230">{null}</span></span>  | <span data-ttu-id="44f46-231">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-231">{null}</span></span>  | <span data-ttu-id="44f46-232">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-232">{null}</span></span>  | <span data-ttu-id="44f46-233">заканчивающ</span><span class="sxs-lookup"><span data-stu-id="44f46-233">{null}</span></span>  | <span data-ttu-id="44f46-234">0</span><span class="sxs-lookup"><span data-stu-id="44f46-234">0</span></span>         |



 

<span data-ttu-id="44f46-235">В этом случае и в Windows XP с пакетом обновления 1 (SP1) [действие аппсеарч](appsearch-action.md) устанавливает для версию msidll значение c: \\ Windows \\ system32 \\msi.dll так как MSI.DLL является файлом, не зависящим от языка.</span><span class="sxs-lookup"><span data-stu-id="44f46-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="44f46-236">Если значение столбца Languages изменено с 0 на 1033, то действие Аппсеарч не сможет найти соответствующий msi.dll и свойство версию MSIDLL не определено.</span><span class="sxs-lookup"><span data-stu-id="44f46-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="44f46-237">Нельзя использовать таблицу сигнатур для запроса только на языках.</span><span class="sxs-lookup"><span data-stu-id="44f46-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="44f46-238">Для поиска различных языковых версий файла необходимо иметь отдельную запись в таблице сигнатур для каждой языковой версии.</span><span class="sxs-lookup"><span data-stu-id="44f46-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="44f46-239">Если в столбце Languages (языки) указано несколько языков, поиск выполняется для файла, поддерживающего все эти языки.</span><span class="sxs-lookup"><span data-stu-id="44f46-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="44f46-240">Формат столбцов MinDate и MaxDate — это два упакованных 16-разрядных значения типа **слово**.</span><span class="sxs-lookup"><span data-stu-id="44f46-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="44f46-241">Дата **слова**</span><span class="sxs-lookup"><span data-stu-id="44f46-241">Date **WORD**</span></span>



| <span data-ttu-id="44f46-242">Bits</span><span class="sxs-lookup"><span data-stu-id="44f46-242">Bits</span></span> | <span data-ttu-id="44f46-243">Содержимое</span><span class="sxs-lookup"><span data-stu-id="44f46-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="44f46-244">0 – 4</span><span class="sxs-lookup"><span data-stu-id="44f46-244">0–4</span></span>  | <span data-ttu-id="44f46-245">День месяца (1-31)</span><span class="sxs-lookup"><span data-stu-id="44f46-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="44f46-246">5-8</span><span class="sxs-lookup"><span data-stu-id="44f46-246">5-8</span></span>  | <span data-ttu-id="44f46-247">Месяц (1 = Январь, 2 = Февраль и т. д.)</span><span class="sxs-lookup"><span data-stu-id="44f46-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="44f46-248">9-15</span><span class="sxs-lookup"><span data-stu-id="44f46-248">9-15</span></span> | <span data-ttu-id="44f46-249">Смещение года от 1980 (Добавление 1980 для получения фактического года)</span><span class="sxs-lookup"><span data-stu-id="44f46-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="44f46-250">**Слово** времени</span><span class="sxs-lookup"><span data-stu-id="44f46-250">Time **WORD**</span></span>



| <span data-ttu-id="44f46-251">Bits</span><span class="sxs-lookup"><span data-stu-id="44f46-251">Bits</span></span>  | <span data-ttu-id="44f46-252">Содержимое</span><span class="sxs-lookup"><span data-stu-id="44f46-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="44f46-253">0 – 4</span><span class="sxs-lookup"><span data-stu-id="44f46-253">0–4</span></span>   | <span data-ttu-id="44f46-254">Секунды, разделенные на 2</span><span class="sxs-lookup"><span data-stu-id="44f46-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="44f46-255">5-10</span><span class="sxs-lookup"><span data-stu-id="44f46-255">5-10</span></span>  | <span data-ttu-id="44f46-256">Мин (0-59)</span><span class="sxs-lookup"><span data-stu-id="44f46-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="44f46-257">11-15</span><span class="sxs-lookup"><span data-stu-id="44f46-257">11-15</span></span> | <span data-ttu-id="44f46-258">Час (0 – 23 в 24-часовом формате)</span><span class="sxs-lookup"><span data-stu-id="44f46-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="44f46-259">Формула для вычисления значений полей MinDate и MaxDate:</span><span class="sxs-lookup"><span data-stu-id="44f46-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="44f46-260">((Year-1980) \* 512 + месяц \* 32 + день) \* 65536 + ч \* 2048 + минуты \* 32 + секунды/2</span><span class="sxs-lookup"><span data-stu-id="44f46-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="44f46-261">Проверка</span><span class="sxs-lookup"><span data-stu-id="44f46-261">Validation</span></span>

<dl>

[<span data-ttu-id="44f46-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="44f46-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="44f46-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="44f46-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



