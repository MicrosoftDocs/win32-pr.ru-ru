---
description: ICE60 проверяет таблицу файлов установщик Windows базы данных.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663848"
---
# <a name="ice60"></a><span data-ttu-id="e0336-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="e0336-103">ICE60</span></span>

<span data-ttu-id="e0336-104">ICE60 проверяет, что файлы в [таблице File](file-table.md) соответствуют следующему условию:</span><span class="sxs-lookup"><span data-stu-id="e0336-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="e0336-105">Если файл не является шрифтом и имеет версию, то он должен иметь язык.</span><span class="sxs-lookup"><span data-stu-id="e0336-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="e0336-106">ICE60 проверяет, что в [таблице мсифилехаш](msifilehash-table.md)не указаны файлы с версиями.</span><span class="sxs-lookup"><span data-stu-id="e0336-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="e0336-107">Ошибка исправления предупреждения, о котором сообщает ICE60, обычно приводит к ненужной повторной установке файла после завершения восстановления продукта.</span><span class="sxs-lookup"><span data-stu-id="e0336-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="e0336-108">Это происходит потому, что файл, устанавливаемый в процессе восстановления, и существующий файл на диске имеют одинаковую версию (они являются одним и тем же файлом), но разными языками.</span><span class="sxs-lookup"><span data-stu-id="e0336-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="e0336-109">В таблице File указано, что язык имеет значение null, но сам файл имеет языковой параметр в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="e0336-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="e0336-110">В зависимости от [правил управления версиями файлов](file-versioning-rules.md)установщик предпочитает установку файла, поэтому он будет повторно скопирован.</span><span class="sxs-lookup"><span data-stu-id="e0336-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="e0336-111">Результат</span><span class="sxs-lookup"><span data-stu-id="e0336-111">Result</span></span>

<span data-ttu-id="e0336-112">ICE60 отправляет предупреждение или ошибку, если файл в [таблице файлов](file-table.md) , который не является шрифтом и имеет версию, не имеет языка.</span><span class="sxs-lookup"><span data-stu-id="e0336-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="e0336-113">ICE60 отправляет следующую ошибку, если файл, указанный в таблице Мсифилехаш, имеет версию.</span><span class="sxs-lookup"><span data-stu-id="e0336-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="e0336-114">Пример</span><span class="sxs-lookup"><span data-stu-id="e0336-114">Example</span></span>

<span data-ttu-id="e0336-115">ICE60 сообщает о следующей ошибке и предупреждении для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="e0336-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="e0336-116">(Файл б является шрифтом; другие файлы — нет.)</span><span class="sxs-lookup"><span data-stu-id="e0336-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="e0336-117">Файл a имеет версию и язык; Поэтому предупреждение или ошибка не создаются.</span><span class="sxs-lookup"><span data-stu-id="e0336-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="e0336-118">Филеб имеет версию, но не имеет языка.</span><span class="sxs-lookup"><span data-stu-id="e0336-118">FileB has a version but no language.</span></span> <span data-ttu-id="e0336-119">Однако предупреждение или ошибка не создаются, так как это шрифт.</span><span class="sxs-lookup"><span data-stu-id="e0336-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="e0336-120">Филек — это сопровождающая ссылка, поэтому язык не обязательно должен быть языком.</span><span class="sxs-lookup"><span data-stu-id="e0336-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="e0336-121">Предупреждение или ошибка не создаются.</span><span class="sxs-lookup"><span data-stu-id="e0336-121">No warning or error is generated.</span></span>

<span data-ttu-id="e0336-122">В заархивированном виде нет версии, поэтому язык не требуется.</span><span class="sxs-lookup"><span data-stu-id="e0336-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="e0336-123">Предупреждение или ошибка не создаются.</span><span class="sxs-lookup"><span data-stu-id="e0336-123">No warning or error is generated.</span></span>

<span data-ttu-id="e0336-124">Файл имеет версию, но не имеет языка.</span><span class="sxs-lookup"><span data-stu-id="e0336-124">FileE has a version but no language.</span></span> <span data-ttu-id="e0336-125">Поэтому создается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="e0336-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="e0336-126">Чтобы устранить это предупреждение, добавьте язык в файл.</span><span class="sxs-lookup"><span data-stu-id="e0336-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="e0336-127">По возможности файлы должны иметь значения языка, хранящиеся в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="e0336-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="e0336-128">Если файл не зависит от языка, используйте [LangID](column-data-types.md) 0.</span><span class="sxs-lookup"><span data-stu-id="e0336-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="e0336-129">[Файловая таблица](file-table.md) (филеб — это Font; другие файлы — нет).</span><span class="sxs-lookup"><span data-stu-id="e0336-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="e0336-130">Файл</span><span class="sxs-lookup"><span data-stu-id="e0336-130">File</span></span>  | <span data-ttu-id="e0336-131">Версия</span><span class="sxs-lookup"><span data-stu-id="e0336-131">Version</span></span> | <span data-ttu-id="e0336-132">Язык</span><span class="sxs-lookup"><span data-stu-id="e0336-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="e0336-133">Файл а</span><span class="sxs-lookup"><span data-stu-id="e0336-133">FileA</span></span> | <span data-ttu-id="e0336-134">1.0</span><span class="sxs-lookup"><span data-stu-id="e0336-134">1.0</span></span>     | <span data-ttu-id="e0336-135">1033</span><span class="sxs-lookup"><span data-stu-id="e0336-135">1033</span></span>     |
| <span data-ttu-id="e0336-136">филеб</span><span class="sxs-lookup"><span data-stu-id="e0336-136">FileB</span></span> | <span data-ttu-id="e0336-137">1.0</span><span class="sxs-lookup"><span data-stu-id="e0336-137">1.0</span></span>     |          |
| <span data-ttu-id="e0336-138">филек</span><span class="sxs-lookup"><span data-stu-id="e0336-138">FileC</span></span> | <span data-ttu-id="e0336-139">Файл а</span><span class="sxs-lookup"><span data-stu-id="e0336-139">FileA</span></span>   |          |
| <span data-ttu-id="e0336-140">Подан</span><span class="sxs-lookup"><span data-stu-id="e0336-140">FileD</span></span> |         |          |
| <span data-ttu-id="e0336-141">Файл</span><span class="sxs-lookup"><span data-stu-id="e0336-141">FileE</span></span> | <span data-ttu-id="e0336-142">1.0</span><span class="sxs-lookup"><span data-stu-id="e0336-142">1.0</span></span>     |          |



 

[<span data-ttu-id="e0336-143">Таблица шрифтов</span><span class="sxs-lookup"><span data-stu-id="e0336-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="e0336-144">Файл</span><span class="sxs-lookup"><span data-stu-id="e0336-144">File</span></span>  | <span data-ttu-id="e0336-145">фонттитле</span><span class="sxs-lookup"><span data-stu-id="e0336-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="e0336-146">филеб</span><span class="sxs-lookup"><span data-stu-id="e0336-146">FileB</span></span> | <span data-ttu-id="e0336-147">Название шрифта</span><span class="sxs-lookup"><span data-stu-id="e0336-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e0336-148">См. также</span><span class="sxs-lookup"><span data-stu-id="e0336-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0336-149">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e0336-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



