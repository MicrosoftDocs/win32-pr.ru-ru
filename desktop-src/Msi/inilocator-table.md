---
description: Таблица Инилокатор содержит сведения, необходимые для поиска файла или каталога с помощью ini-файла, или для поиска конкретной записи ini. INI-файл должен присутствовать в каталоге Microsoft Windows по умолчанию.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Таблица Инилокатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650684"
---
# <a name="inilocator-table"></a><span data-ttu-id="7b6dc-104">Таблица Инилокатор</span><span class="sxs-lookup"><span data-stu-id="7b6dc-104">IniLocator Table</span></span>

<span data-ttu-id="7b6dc-105">Таблица Инилокатор содержит сведения, необходимые для поиска файла или каталога с помощью ini-файла, или для поиска конкретной записи ini.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="7b6dc-106">INI-файл должен присутствовать в каталоге Microsoft Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="7b6dc-107">Таблица Инилокатор содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="7b6dc-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="7b6dc-108">Column</span></span>      | <span data-ttu-id="7b6dc-109">Type</span><span class="sxs-lookup"><span data-stu-id="7b6dc-109">Type</span></span>                         | <span data-ttu-id="7b6dc-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="7b6dc-110">Key</span></span> | <span data-ttu-id="7b6dc-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="7b6dc-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7b6dc-112">Образец\_</span><span class="sxs-lookup"><span data-stu-id="7b6dc-112">Signature\_</span></span> | [<span data-ttu-id="7b6dc-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7b6dc-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7b6dc-114">Да</span><span class="sxs-lookup"><span data-stu-id="7b6dc-114">Y</span></span>   | <span data-ttu-id="7b6dc-115">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-115">N</span></span>        |
| <span data-ttu-id="7b6dc-116">FileName</span><span class="sxs-lookup"><span data-stu-id="7b6dc-116">FileName</span></span>    | [<span data-ttu-id="7b6dc-117">FileName</span><span class="sxs-lookup"><span data-stu-id="7b6dc-117">FileName</span></span>](text.md)         | <span data-ttu-id="7b6dc-118">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-118">N</span></span>   | <span data-ttu-id="7b6dc-119">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-119">N</span></span>        |
| <span data-ttu-id="7b6dc-120">Section</span><span class="sxs-lookup"><span data-stu-id="7b6dc-120">Section</span></span>     | [<span data-ttu-id="7b6dc-121">Text</span><span class="sxs-lookup"><span data-stu-id="7b6dc-121">Text</span></span>](text.md)             | <span data-ttu-id="7b6dc-122">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-122">N</span></span>   | <span data-ttu-id="7b6dc-123">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-123">N</span></span>        |
| <span data-ttu-id="7b6dc-124">Ключ</span><span class="sxs-lookup"><span data-stu-id="7b6dc-124">Key</span></span>         | [<span data-ttu-id="7b6dc-125">Text</span><span class="sxs-lookup"><span data-stu-id="7b6dc-125">Text</span></span>](text.md)             | <span data-ttu-id="7b6dc-126">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-126">N</span></span>   | <span data-ttu-id="7b6dc-127">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-127">N</span></span>        |
| <span data-ttu-id="7b6dc-128">Поле</span><span class="sxs-lookup"><span data-stu-id="7b6dc-128">Field</span></span>       | [<span data-ttu-id="7b6dc-129">Integer</span><span class="sxs-lookup"><span data-stu-id="7b6dc-129">Integer</span></span>](integer.md)       | <span data-ttu-id="7b6dc-130">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-130">N</span></span>   | <span data-ttu-id="7b6dc-131">Да</span><span class="sxs-lookup"><span data-stu-id="7b6dc-131">Y</span></span>        |
| <span data-ttu-id="7b6dc-132">Тип</span><span class="sxs-lookup"><span data-stu-id="7b6dc-132">Type</span></span>        | [<span data-ttu-id="7b6dc-133">Integer</span><span class="sxs-lookup"><span data-stu-id="7b6dc-133">Integer</span></span>](integer.md)       | <span data-ttu-id="7b6dc-134">Нет</span><span class="sxs-lookup"><span data-stu-id="7b6dc-134">N</span></span>   | <span data-ttu-id="7b6dc-135">Да</span><span class="sxs-lookup"><span data-stu-id="7b6dc-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7b6dc-136">Столбцы</span><span class="sxs-lookup"><span data-stu-id="7b6dc-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7b6dc-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="7b6dc-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-138">Внешний ключ в первом столбце [таблицы сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dc-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="7b6dc-139">Сигнатура \_ представляет собой уникальную подпись, а также внешний ключ в столбец одной из таблиц сигнатур.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="7b6dc-140">Если эта подпись содержится в таблице сигнатур, то поиск выполняется для файла.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="7b6dc-141">Если этот ключ отсутствует в таблице сигнатур, а значение столбца Type — **мсидблокатортипераввалуе**, поиск производится для записи ini, заданной в таблице инилокатор.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="7b6dc-142">В противном случае поиск осуществляется для каталога, указанного в таблице Инилокатор.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dc-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов</span><span class="sxs-lookup"><span data-stu-id="7b6dc-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-144">Имя ini-файла.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dc-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела</span><span class="sxs-lookup"><span data-stu-id="7b6dc-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-146">Имя раздела в ini-файле.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dc-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел</span><span class="sxs-lookup"><span data-stu-id="7b6dc-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-148">Значение ключа в разделе.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dc-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Полями</span><span class="sxs-lookup"><span data-stu-id="7b6dc-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-150">Поле в ini-строке.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-150">The field in the .ini line.</span></span> <span data-ttu-id="7b6dc-151">Если поле field имеет значение null или равно 0, считывается вся строка.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="7b6dc-152">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dc-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Тип</span><span class="sxs-lookup"><span data-stu-id="7b6dc-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="7b6dc-154">Значение, определяющее, является ли ini-файл расположением файла, расположением каталога или необработанным значением. ini.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="7b6dc-155">В следующей таблице перечислены допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-155">The following table lists valid values.</span></span> <span data-ttu-id="7b6dc-156">Если он отсутствует, для параметра Type задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="7b6dc-157">Константа</span><span class="sxs-lookup"><span data-stu-id="7b6dc-157">Constant</span></span>                      | <span data-ttu-id="7b6dc-158">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="7b6dc-158">Hexadecimal</span></span> | <span data-ttu-id="7b6dc-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="7b6dc-159">Decimal</span></span> | <span data-ttu-id="7b6dc-160">Описание</span><span class="sxs-lookup"><span data-stu-id="7b6dc-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="7b6dc-161">**мсидблокатортипедиректори**</span><span class="sxs-lookup"><span data-stu-id="7b6dc-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="7b6dc-162">0x000</span><span class="sxs-lookup"><span data-stu-id="7b6dc-162">0x000</span></span>       | <span data-ttu-id="7b6dc-163">0</span><span class="sxs-lookup"><span data-stu-id="7b6dc-163">0</span></span>       | <span data-ttu-id="7b6dc-164">Расположение каталога.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-164">A directory location.</span></span> |
| <span data-ttu-id="7b6dc-165">**мсидблокатортипефиленаме**</span><span class="sxs-lookup"><span data-stu-id="7b6dc-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="7b6dc-166">0x001</span><span class="sxs-lookup"><span data-stu-id="7b6dc-166">0x001</span></span>       | <span data-ttu-id="7b6dc-167">1</span><span class="sxs-lookup"><span data-stu-id="7b6dc-167">1</span></span>       | <span data-ttu-id="7b6dc-168">Расположение файла.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-168">A file location.</span></span>      |
| <span data-ttu-id="7b6dc-169">**мсидблокатортипераввалуе**</span><span class="sxs-lookup"><span data-stu-id="7b6dc-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="7b6dc-170">0x002</span><span class="sxs-lookup"><span data-stu-id="7b6dc-170">0x002</span></span>       | <span data-ttu-id="7b6dc-171">2</span><span class="sxs-lookup"><span data-stu-id="7b6dc-171">2</span></span>       | <span data-ttu-id="7b6dc-172">Значение RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b6dc-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b6dc-173">Remarks</span></span>

<span data-ttu-id="7b6dc-174">Эта таблица используется с [таблицей аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dc-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="7b6dc-175">Столбцы этой таблицы, как правило, не локализованы.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="7b6dc-176">Если автор решает выполнить поиск продуктов на нескольких языках, в таблице для каждого языка может присутствовать отдельная запись.</span><span class="sxs-lookup"><span data-stu-id="7b6dc-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="7b6dc-177">Связанный локализованный текст для просмотра хода выполнения или ведения журнала указывается в [таблице актионтекст](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dc-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="7b6dc-178">См. раздел [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dc-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7b6dc-179">Проверка</span><span class="sxs-lookup"><span data-stu-id="7b6dc-179">Validation</span></span>

<dl>

[<span data-ttu-id="7b6dc-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="7b6dc-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7b6dc-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="7b6dc-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



