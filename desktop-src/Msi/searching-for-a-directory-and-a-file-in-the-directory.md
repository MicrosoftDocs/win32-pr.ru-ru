---
description: Во время установки установщик Windows установщик может выполнить поиск каталога и файла в этом каталоге.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Поиск каталога и файла в каталоге
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663571"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="a65c6-103">Поиск каталога и файла в каталоге</span><span class="sxs-lookup"><span data-stu-id="a65c6-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="a65c6-104">**Поиск каталога и файла в этом каталоге**</span><span class="sxs-lookup"><span data-stu-id="a65c6-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="a65c6-105">Сначала найдите каталог.</span><span class="sxs-lookup"><span data-stu-id="a65c6-105">First search for the directory.</span></span>

    <span data-ttu-id="a65c6-106">AppDir должен быть определен как действительная подпись каталога.</span><span class="sxs-lookup"><span data-stu-id="a65c6-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="a65c6-107">Если AppDir не определен как действительная сигнатура, Аппсеарч не имеет места для поиска файла, например, если поиск выполняется в c: \\ MyDir \\MyApp.exe, AppDir должен быть определен как c: \\ MyDir.</span><span class="sxs-lookup"><span data-stu-id="a65c6-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="a65c6-108">AppDir может быть определен путем включения записи в [таблицу дрлокатор](drlocator-table.md)или другим методом.</span><span class="sxs-lookup"><span data-stu-id="a65c6-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="a65c6-109">Ни одна запись не включена в [таблицу сигнатур](signature-table.md) для поиска в каталоге.</span><span class="sxs-lookup"><span data-stu-id="a65c6-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="a65c6-110">Для поиска файлов перечислите подпись файла и имя в таблице сигнатур.</span><span class="sxs-lookup"><span data-stu-id="a65c6-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="a65c6-111">Оставшиеся поля в этой записи могут иметь значение NULL для поиска любой версии MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="a65c6-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="a65c6-112">[Таблица сигнатур](signature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a65c6-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="a65c6-113">Подпись</span><span class="sxs-lookup"><span data-stu-id="a65c6-113">Signature</span></span>          | <span data-ttu-id="a65c6-114">Имя файла</span><span class="sxs-lookup"><span data-stu-id="a65c6-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="a65c6-115">аппфиле</span><span class="sxs-lookup"><span data-stu-id="a65c6-115">AppFile</span></span><br/> | <span data-ttu-id="a65c6-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="a65c6-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="a65c6-117">Используйте [таблицу аппсеарч](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="a65c6-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="a65c6-118">Введите свойство, устанавливаемое установщиком при установке каталога с подписью AppDir.</span><span class="sxs-lookup"><span data-stu-id="a65c6-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="a65c6-119">Если установщик обнаруживает, что этот каталог установлен, он задает для MYDIR путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="a65c6-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="a65c6-120">Введите свойство, устанавливаемое установщиком, если MyApp.exe установлен.</span><span class="sxs-lookup"><span data-stu-id="a65c6-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="a65c6-121">[Таблица аппсеарч](appsearch-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a65c6-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="a65c6-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="a65c6-122">Property</span></span>         | <span data-ttu-id="a65c6-123">Подпись</span><span class="sxs-lookup"><span data-stu-id="a65c6-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="a65c6-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="a65c6-124">MYDIR</span></span><br/> | <span data-ttu-id="a65c6-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="a65c6-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="a65c6-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="a65c6-126">MYAPP</span></span><br/> | <span data-ttu-id="a65c6-127">аппфиле</span><span class="sxs-lookup"><span data-stu-id="a65c6-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="a65c6-128">Используйте [таблицу дрлокатор](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="a65c6-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="a65c6-129">Введите в родительском столбце сигнатуру AppDir, которая определена как путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="a65c6-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="a65c6-130">Укажите в столбце Depth число уровней подкаталогов для поиска в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="a65c6-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="a65c6-131">AppDir должен быть определен как подпись каталога.</span><span class="sxs-lookup"><span data-stu-id="a65c6-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="a65c6-132">AppDir можно определить, включив запись, как показано ниже, или с помощью другого метода.</span><span class="sxs-lookup"><span data-stu-id="a65c6-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="a65c6-133">Таблица Дрлокатор</span><span class="sxs-lookup"><span data-stu-id="a65c6-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="a65c6-134">Подпись</span><span class="sxs-lookup"><span data-stu-id="a65c6-134">Signature</span></span> | <span data-ttu-id="a65c6-135">Parent</span><span class="sxs-lookup"><span data-stu-id="a65c6-135">Parent</span></span> | <span data-ttu-id="a65c6-136">Путь</span><span class="sxs-lookup"><span data-stu-id="a65c6-136">Path</span></span>      | <span data-ttu-id="a65c6-137">Глубина</span><span class="sxs-lookup"><span data-stu-id="a65c6-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="a65c6-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="a65c6-138">AppDir</span></span>    |        | <span data-ttu-id="a65c6-139">C: \\ MyDir</span><span class="sxs-lookup"><span data-stu-id="a65c6-139">C:\\MyDir</span></span> | <span data-ttu-id="a65c6-140">0</span><span class="sxs-lookup"><span data-stu-id="a65c6-140">0</span></span>     |
    | <span data-ttu-id="a65c6-141">аппфиле</span><span class="sxs-lookup"><span data-stu-id="a65c6-141">AppFile</span></span>   | <span data-ttu-id="a65c6-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="a65c6-142">AppDir</span></span> |           | <span data-ttu-id="a65c6-143">0</span><span class="sxs-lookup"><span data-stu-id="a65c6-143">0</span></span>     |

    

     

4.  <span data-ttu-id="a65c6-144">Включите действие Аппсеарч в последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="a65c6-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="a65c6-145">Если MyApp.exe найдена для установки в AppDir, установщик задает для свойства MYAPP расположение файла.</span><span class="sxs-lookup"><span data-stu-id="a65c6-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a65c6-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a65c6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a65c6-147">Поиск существующих приложений, файлов, записей реестра или INI-файлов</span><span class="sxs-lookup"><span data-stu-id="a65c6-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




