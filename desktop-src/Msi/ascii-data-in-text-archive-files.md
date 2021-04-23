---
description: Если в текстовый файл архива экспортируется таблица, содержащая только символы ASCII, файл IDT соответствует базовому формату архивного файла.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Данные ASCII в текстовых архивных файлах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909083"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="e9d6e-103">Данные ASCII в текстовых архивных файлах</span><span class="sxs-lookup"><span data-stu-id="e9d6e-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="e9d6e-104">Если в [текстовый файл архива](text-archive-files.md)экспортируется таблица, содержащая только символы ASCII, файл IDT соответствует базовому [формату архивного файла](archive-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="e9d6e-105">Если в таблице содержатся данные, отличные от ASCII, формат файла архива расширяется для включения сведений о кодовой странице.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="e9d6e-106">Текстовые архивные файлы, содержащие только символы ASCII</span><span class="sxs-lookup"><span data-stu-id="e9d6e-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="e9d6e-107">Если таблица, содержащая только символы ASCII, экспортируется в файл архива, то файл IDT находится в базовом [формате файла архива](archive-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="e9d6e-108">Каждый поток в таблице экспортируется как файл с расширением имени файла ИБД.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="e9d6e-109">ИБД-файлы хранятся в папке с тем же именем, что и таблица.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="e9d6e-110">Например, рассмотрим экспорт следующей [двоичной](binary-table.md) таблицы.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="e9d6e-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e9d6e-111">Name</span></span>  | <span data-ttu-id="e9d6e-112">Данные</span><span class="sxs-lookup"><span data-stu-id="e9d6e-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="e9d6e-113">Книги</span><span class="sxs-lookup"><span data-stu-id="e9d6e-113">Books</span></span> | <span data-ttu-id="e9d6e-114">Books. ИБД</span><span class="sxs-lookup"><span data-stu-id="e9d6e-114">Books.ibd</span></span> |
| <span data-ttu-id="e9d6e-115">Автомобили</span><span class="sxs-lookup"><span data-stu-id="e9d6e-115">Cars</span></span>  | <span data-ttu-id="e9d6e-116">Автомобили. ИБД</span><span class="sxs-lookup"><span data-stu-id="e9d6e-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="e9d6e-117">Структура каталогов после экспорта этой таблицы выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="e9d6e-118">Сведения в таблице базы данных экспортируются в файл binary. IDT.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="e9d6e-119">Два потока двоичных данных экспортируются в Book. ИБД и автомобили. ИБД, сохраненные в папке с именем binary.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="e9d6e-120">Файл архива binary. IDT находится в базовом [формате файла архива](archive-file-format.md) и будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="e9d6e-121">Текстовые архивные файлы, содержащие символы, не входящие в набор ASCII</span><span class="sxs-lookup"><span data-stu-id="e9d6e-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="e9d6e-122">Если файл содержит данные, не входящие в набор ASCII, то базовый [Формат файла архива](archive-file-format.md) IDT расширяется для включения сведений кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="e9d6e-123">Третья строка в таблице IDT — это числовая кодовая страница, за которой следуют имя таблицы и имена первичных ключевых столбцов, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="e9d6e-124">Файл IDT, содержащий сведения, не относящиеся к ASCII, должен сохраняться в формате ASCII.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="e9d6e-125">Например, текстовый файл архива может содержать имена столбцов и таблиц в кодировке UTF-8, но сам файл архива должен быть ASCII.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="e9d6e-126">Следующая таблица Актионтекст, локализованная на французский язык, будет содержать сведения, отличные от ASCII.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="e9d6e-127">Числовая кодовая страница, используемая для строк на французском языке, — 1252.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="e9d6e-128">Действие</span><span class="sxs-lookup"><span data-stu-id="e9d6e-128">Action</span></span>    | <span data-ttu-id="e9d6e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="e9d6e-129">Description</span></span>                                  | <span data-ttu-id="e9d6e-130">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e9d6e-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="e9d6e-131">ОБЪЯВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9d6e-131">ADVERTISE</span></span> | <span data-ttu-id="e9d6e-132">Публикация д'информатионс Sur л'аппликатион</span><span class="sxs-lookup"><span data-stu-id="e9d6e-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="e9d6e-133">Экспортированный файл архива Актионтекст. IDT будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="e9d6e-134">Если текстовый файл архива содержит данные, не входящие в набор ASCII, файл архива содержит сведения о кодовой странице.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="e9d6e-135">Архивные файлы со сведениями кодовой страницы можно импортировать обратно в базу данных с этой точной кодовой страницей или в базу данных, не зависящую от языка.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="e9d6e-136">В случае независимого от языка базы данных кодовая страница задается как кодовая страница файла архива.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="e9d6e-137">Дополнительные сведения о том, как установщик Windows обрабатывает кодовые страницы, см. в разделе [Обработка кодовых страниц (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



