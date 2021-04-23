---
description: Необходимо создать модули слияния на нескольких языках, преобразования языка и CAB-файлы, чтобы порядок файлов совпадал с порядком, указанным в таблице File.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Упорядочивание последовательности файлов в CAB-файле модуля слияния с несколькими языками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272793"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="3580c-103">Упорядочивание последовательности файлов в CAB-файле модуля слияния с несколькими языками</span><span class="sxs-lookup"><span data-stu-id="3580c-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="3580c-104">Необходимо создать модули слияния на нескольких языках, преобразования языка и CAB-файлы, чтобы порядок файлов в CAB-файле совпадал с порядком установки файлов, указанных в [таблице File](file-table.md), даже после применения преобразования языка.</span><span class="sxs-lookup"><span data-stu-id="3580c-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="3580c-105">Если порядок в модуле и в CAB-файле не совпадают, то модуль слияния использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3580c-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="3580c-106">Назначьте каждому файлу в модуле Уникальный порядковый номер, не зависящий от языка, а затем всегда используйте этот порядковый номер для файла.</span><span class="sxs-lookup"><span data-stu-id="3580c-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="3580c-107">Используйте ту же последовательность при создании CAB-файла и разработав преобразование языка.</span><span class="sxs-lookup"><span data-stu-id="3580c-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="3580c-108">Поскольку установщик устанавливает только файлы, перечисленные в [таблице File](file-table.md), использование глобальной последовательности файлов в CAB-файле, [таблице файлов](file-table.md)и языкового преобразования позволяет средству слияния пропустить все дополнительные файлы, хранящиеся в CAB-файле, который не указан в [таблице файлов](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3580c-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="3580c-109">Другие файлы могут существовать в CAB-файле, но они не должны быть перечислены в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3580c-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="3580c-110">Например, модуль, устанавливающий Code.dll, English. dat, немецкий. dat и французский. dat, может использовать следующий глобальный порядок последовательности файлов.</span><span class="sxs-lookup"><span data-stu-id="3580c-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="3580c-111">Файл</span><span class="sxs-lookup"><span data-stu-id="3580c-111">File</span></span>        | <span data-ttu-id="3580c-112">Последовательность</span><span class="sxs-lookup"><span data-stu-id="3580c-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="3580c-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="3580c-113">Code.Dll</span></span>    | <span data-ttu-id="3580c-114">1</span><span class="sxs-lookup"><span data-stu-id="3580c-114">1</span></span>        |
| <span data-ttu-id="3580c-115">Английский. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-115">English.Dat</span></span> | <span data-ttu-id="3580c-116">2</span><span class="sxs-lookup"><span data-stu-id="3580c-116">2</span></span>        |
| <span data-ttu-id="3580c-117">Немецкий. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-117">German.Dat</span></span>  | <span data-ttu-id="3580c-118">3</span><span class="sxs-lookup"><span data-stu-id="3580c-118">3</span></span>        |
| <span data-ttu-id="3580c-119">Французский. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-119">French.Dat</span></span>  | <span data-ttu-id="3580c-120">4</span><span class="sxs-lookup"><span data-stu-id="3580c-120">4</span></span>        |



 

<span data-ttu-id="3580c-121">Затем можно создать преобразования языка, чтобы изменить [таблицу файлов](file-table.md) модуля для английского, немецкого или французского языков.</span><span class="sxs-lookup"><span data-stu-id="3580c-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="3580c-122">[Таблица файлов](file-table.md) (частично для английского языка)</span><span class="sxs-lookup"><span data-stu-id="3580c-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="3580c-123">Файл</span><span class="sxs-lookup"><span data-stu-id="3580c-123">File</span></span>        | <span data-ttu-id="3580c-124">Последовательность</span><span class="sxs-lookup"><span data-stu-id="3580c-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="3580c-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="3580c-125">Code.Dll</span></span>    | <span data-ttu-id="3580c-126">1</span><span class="sxs-lookup"><span data-stu-id="3580c-126">1</span></span>        |
| <span data-ttu-id="3580c-127">Английский. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-127">English.Dat</span></span> | <span data-ttu-id="3580c-128">2</span><span class="sxs-lookup"><span data-stu-id="3580c-128">2</span></span>        |



 

<span data-ttu-id="3580c-129">[Файловая таблица](file-table.md) (частично для немецкого языка)</span><span class="sxs-lookup"><span data-stu-id="3580c-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="3580c-130">Файл</span><span class="sxs-lookup"><span data-stu-id="3580c-130">File</span></span>       | <span data-ttu-id="3580c-131">Последовательность</span><span class="sxs-lookup"><span data-stu-id="3580c-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="3580c-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="3580c-132">Code.Dll</span></span>   | <span data-ttu-id="3580c-133">1</span><span class="sxs-lookup"><span data-stu-id="3580c-133">1</span></span>        |
| <span data-ttu-id="3580c-134">Немецкий. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-134">German.Dat</span></span> | <span data-ttu-id="3580c-135">3</span><span class="sxs-lookup"><span data-stu-id="3580c-135">3</span></span>        |



 

<span data-ttu-id="3580c-136">[Таблица файлов](file-table.md) (частично для французского)</span><span class="sxs-lookup"><span data-stu-id="3580c-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="3580c-137">Файл</span><span class="sxs-lookup"><span data-stu-id="3580c-137">File</span></span>       | <span data-ttu-id="3580c-138">Последовательность</span><span class="sxs-lookup"><span data-stu-id="3580c-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="3580c-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="3580c-139">Code.Dll</span></span>   | <span data-ttu-id="3580c-140">1</span><span class="sxs-lookup"><span data-stu-id="3580c-140">1</span></span>        |
| <span data-ttu-id="3580c-141">Французский. dat</span><span class="sxs-lookup"><span data-stu-id="3580c-141">French.Dat</span></span> | <span data-ttu-id="3580c-142">4</span><span class="sxs-lookup"><span data-stu-id="3580c-142">4</span></span>        |



 

<span data-ttu-id="3580c-143">Дополнительные сведения см. в разделе [Создание преобразования языка для модуля слияния с несколькими языками](authoring-a-language-transform-for-a-multiple-language-merge-module.md) и [Создание таблиц файлов модулей слияния](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3580c-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



