---
description: Эта таблица содержит файлы значков. Каждый значок из таблицы копируется в файл как часть объявления продукта, который будет использоваться для объявленных сочетаний клавиш и OLE-серверов. См. раздел ограничения OLE для потоков.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Таблица значков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264180"
---
# <a name="icon-table"></a><span data-ttu-id="3c770-105">Таблица значков</span><span class="sxs-lookup"><span data-stu-id="3c770-105">Icon Table</span></span>

<span data-ttu-id="3c770-106">Эта таблица содержит файлы значков.</span><span class="sxs-lookup"><span data-stu-id="3c770-106">This table contains the icon files.</span></span> <span data-ttu-id="3c770-107">Каждый значок из таблицы копируется в файл как часть объявления продукта, который будет использоваться для объявленных сочетаний клавиш и OLE-серверов.</span><span class="sxs-lookup"><span data-stu-id="3c770-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="3c770-108">См. раздел [ограничения OLE для потоков](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3c770-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="3c770-109">Таблица значков содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="3c770-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="3c770-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="3c770-110">Column</span></span> | <span data-ttu-id="3c770-111">Type</span><span class="sxs-lookup"><span data-stu-id="3c770-111">Type</span></span>                         | <span data-ttu-id="3c770-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="3c770-112">Key</span></span> | <span data-ttu-id="3c770-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="3c770-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="3c770-114">Имя</span><span class="sxs-lookup"><span data-stu-id="3c770-114">Name</span></span>   | [<span data-ttu-id="3c770-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3c770-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="3c770-116">Да</span><span class="sxs-lookup"><span data-stu-id="3c770-116">Y</span></span>   | <span data-ttu-id="3c770-117">Нет</span><span class="sxs-lookup"><span data-stu-id="3c770-117">N</span></span>        |
| <span data-ttu-id="3c770-118">Данные</span><span class="sxs-lookup"><span data-stu-id="3c770-118">Data</span></span>   | [<span data-ttu-id="3c770-119">Двоичный</span><span class="sxs-lookup"><span data-stu-id="3c770-119">Binary</span></span>](binary.md)         | <span data-ttu-id="3c770-120">Нет</span><span class="sxs-lookup"><span data-stu-id="3c770-120">N</span></span>   | <span data-ttu-id="3c770-121">Нет</span><span class="sxs-lookup"><span data-stu-id="3c770-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3c770-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="3c770-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3c770-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="3c770-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3c770-124">Имя файла значка.</span><span class="sxs-lookup"><span data-stu-id="3c770-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="3c770-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="3c770-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="3c770-126">Двоичные данные значка в формате PE (DLL или exe) или значке (ICO).</span><span class="sxs-lookup"><span data-stu-id="3c770-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c770-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c770-127">Remarks</span></span>

<span data-ttu-id="3c770-128">Эта таблица упоминается при выполнении [действия публишпродукт](publishproduct-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3c770-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="3c770-129">Значки сочетаний клавиш, расширений имен файлов и идентификаторов CLSID должны храниться в файлах, отделяющих от самого целевого файла.</span><span class="sxs-lookup"><span data-stu-id="3c770-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="3c770-130">Это необходимо, поскольку при объявлении ресурса установщик должен скопировать на компьютер пользователя только небольшие файлы значков.</span><span class="sxs-lookup"><span data-stu-id="3c770-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="3c770-131">Поэтому разработчику пакета установки необходимо создать отдельные файлы, содержащие только значки.</span><span class="sxs-lookup"><span data-stu-id="3c770-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="3c770-132">Эти файлы значков затем сохраняются в виде двоичных данных в таблице значков.</span><span class="sxs-lookup"><span data-stu-id="3c770-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="3c770-133">Файлы значков, связанные строго с расширениями имен файлов или CLSID, могут иметь любое расширение, например ICO.</span><span class="sxs-lookup"><span data-stu-id="3c770-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="3c770-134">Однако файлы значков, связанные с ярлыками, должны быть в двоичном формате EXE и должны называться так, чтобы их расширения совпадали с расширением целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c770-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="3c770-135">Ярлык не будет работать, если это правило не соблюдается.</span><span class="sxs-lookup"><span data-stu-id="3c770-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="3c770-136">Например, если ярлык указывает на ресурс с файлом ключа Red.bar, то файл значка также должен иметь расширение. Bar.</span><span class="sxs-lookup"><span data-stu-id="3c770-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="3c770-137">В один файл значка можно составить несколько значков, если все целевые файлы имеют одинаковое расширение.</span><span class="sxs-lookup"><span data-stu-id="3c770-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="3c770-138">Проверка</span><span class="sxs-lookup"><span data-stu-id="3c770-138">Validation</span></span>

<dl>

[<span data-ttu-id="3c770-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="3c770-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3c770-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="3c770-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3c770-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="3c770-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="3c770-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="3c770-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3c770-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="3c770-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="3c770-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="3c770-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



