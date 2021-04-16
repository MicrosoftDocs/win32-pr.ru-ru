---
description: Таблица Дрлокатор содержит сведения, необходимые для поиска файла или каталога путем поиска по дереву каталогов.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Таблица Дрлокатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650580"
---
# <a name="drlocator-table"></a><span data-ttu-id="ef6f2-103">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="ef6f2-103">DrLocator Table</span></span>

<span data-ttu-id="ef6f2-104">Таблица Дрлокатор содержит сведения, необходимые для поиска файла или каталога путем поиска по дереву каталогов.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="ef6f2-105">Таблица Дрлокатор содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="ef6f2-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="ef6f2-106">Column</span></span>      | <span data-ttu-id="ef6f2-107">Type</span><span class="sxs-lookup"><span data-stu-id="ef6f2-107">Type</span></span>                         | <span data-ttu-id="ef6f2-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="ef6f2-108">Key</span></span> | <span data-ttu-id="ef6f2-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="ef6f2-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ef6f2-110">Образец\_</span><span class="sxs-lookup"><span data-stu-id="ef6f2-110">Signature\_</span></span> | [<span data-ttu-id="ef6f2-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ef6f2-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ef6f2-112">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-112">Y</span></span>   | <span data-ttu-id="ef6f2-113">Нет</span><span class="sxs-lookup"><span data-stu-id="ef6f2-113">N</span></span>        |
| <span data-ttu-id="ef6f2-114">Parent</span><span class="sxs-lookup"><span data-stu-id="ef6f2-114">Parent</span></span>      | [<span data-ttu-id="ef6f2-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ef6f2-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ef6f2-116">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-116">Y</span></span>   | <span data-ttu-id="ef6f2-117">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-117">Y</span></span>        |
| <span data-ttu-id="ef6f2-118">Путь</span><span class="sxs-lookup"><span data-stu-id="ef6f2-118">Path</span></span>        | [<span data-ttu-id="ef6f2-119">анипас</span><span class="sxs-lookup"><span data-stu-id="ef6f2-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="ef6f2-120">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-120">Y</span></span>   | <span data-ttu-id="ef6f2-121">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-121">Y</span></span>        |
| <span data-ttu-id="ef6f2-122">Глубина</span><span class="sxs-lookup"><span data-stu-id="ef6f2-122">Depth</span></span>       | [<span data-ttu-id="ef6f2-123">Integer</span><span class="sxs-lookup"><span data-stu-id="ef6f2-123">Integer</span></span>](integer.md)       | <span data-ttu-id="ef6f2-124">Нет</span><span class="sxs-lookup"><span data-stu-id="ef6f2-124">N</span></span>   | <span data-ttu-id="ef6f2-125">Да</span><span class="sxs-lookup"><span data-stu-id="ef6f2-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ef6f2-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="ef6f2-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ef6f2-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_</span><span class="sxs-lookup"><span data-stu-id="ef6f2-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="ef6f2-128">Столбец сигнатуры \_ является внешним ключом к первому столбцу [таблицы сигнатур](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef6f2-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="ef6f2-129">Это поле может представлять уникальную подпись файла, указанную в таблице сигнатур.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="ef6f2-130">Если значение в этом столбце отсутствует в таблице сигнатур, то предполагается, что поиск выполняется для каталога, на который указывает таблица Дрлокатор.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="ef6f2-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Источника</span><span class="sxs-lookup"><span data-stu-id="ef6f2-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="ef6f2-132">Этот столбец является сигнатурой родительского каталога файла или каталога в столбце сигнатуры \_ .</span><span class="sxs-lookup"><span data-stu-id="ef6f2-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="ef6f2-133">Если это поле имеет значение null, а столбец Path не разворачивается до полного пути, то поиск выполняется по всем фиксированным дискам системы пользователя с помощью пути.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="ef6f2-134">Это поле является ключом к одной из следующих таблиц: [реглокатор](reglocator-table.md), [инилокатор](inilocator-table.md), [комплокатор](complocator-table.md)или дрлокатор Tables.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="ef6f2-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Путь</span><span class="sxs-lookup"><span data-stu-id="ef6f2-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="ef6f2-136">Столбец path содержит путь в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="ef6f2-137">Это либо полный путь, либо относительный вложенный путь, расположенный под каталогом, заданным в родительском столбце.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="ef6f2-138">См. ограничения на тип данных [анипас](anypath.md) .</span><span class="sxs-lookup"><span data-stu-id="ef6f2-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="ef6f2-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Длина</span><span class="sxs-lookup"><span data-stu-id="ef6f2-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="ef6f2-140">Глубина ниже пути, который установщик ищет для файла или каталога, указанных в столбце сигнатуры \_ .</span><span class="sxs-lookup"><span data-stu-id="ef6f2-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="ef6f2-141">Значение, используемое в поле Depth, основано на нулевом значении.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="ef6f2-142">Например, если поле пути имеет значение c:/Program Files/bin, то столбцу Depth должно быть присвоено значение 0 или больше, чтобы обнаружить файл, расположенный в bin папки.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="ef6f2-143">Если поле глубины пусто, то глубина будет равна нулю.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef6f2-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef6f2-144">Remarks</span></span>

<span data-ttu-id="ef6f2-145">Эта таблица используется с [таблицей аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef6f2-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="ef6f2-146">Столбцы этой таблицы, как правило, не локализованы.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="ef6f2-147">Если автор решает выполнить поиск продуктов на нескольких языках, для каждого языка должна быть включена отдельная запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="ef6f2-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="ef6f2-148">См. раздел [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="ef6f2-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ef6f2-149">Проверка</span><span class="sxs-lookup"><span data-stu-id="ef6f2-149">Validation</span></span>

<dl>

[<span data-ttu-id="ef6f2-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="ef6f2-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ef6f2-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="ef6f2-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ef6f2-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="ef6f2-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



