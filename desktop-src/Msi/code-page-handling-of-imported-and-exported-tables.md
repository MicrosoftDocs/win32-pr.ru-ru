---
description: Вы можете добавить сведения о локализации в базу данных установки, импортировав и экспортировав текстовые архивные файлы ASCII с помощью Мсидатабасикспорт и Мсидатабасеимпорт.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Обработка кодовой страницы импортированных и экспортированных таблиц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662592"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a><span data-ttu-id="aa74b-103">Обработка кодовой страницы импортированных и экспортированных таблиц</span><span class="sxs-lookup"><span data-stu-id="aa74b-103">Code Page Handling of Imported and Exported Tables</span></span>

<span data-ttu-id="aa74b-104">Вы можете добавить сведения о локализации в базу данных установки, импортировав и экспортировав текстовые архивные файлы ASCII с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) и [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="aa74b-104">You can add localization information to an installation database by importing and exporting ASCII text archive files using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) and [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="aa74b-105">Поскольку пул строк базы данных использует кодовую страницу ANSI, то как база данных, так и экспортированные [текстовые архивные файлы](text-archive-files.md) содержат кодовые страницы.</span><span class="sxs-lookup"><span data-stu-id="aa74b-105">Because the database string pool uses an ANSI code page, both the database and exported [Text Archive Files](text-archive-files.md) have code pages.</span></span>

<span data-ttu-id="aa74b-106">При экспорте [файла текстового архива](text-archive-files.md) из базы данных кодовая страница файла архива совпадает с родительской базой данных.</span><span class="sxs-lookup"><span data-stu-id="aa74b-106">When a [Text Archive File](text-archive-files.md) is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="aa74b-107">Список страниц с числовыми кодовыми номерами см. в разделе [Локализация таблиц ошибок и актионтекст](localizing-the-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="aa74b-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

> [!Note]  
> <span data-ttu-id="aa74b-108">При экспорте таблицы в текстовый файл архива преобразуются управляющие символы, чтобы избежать конфликтов с разделителями файлов.</span><span class="sxs-lookup"><span data-stu-id="aa74b-108">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span>

 

## <a name="ascii-text-archive-files"></a><span data-ttu-id="aa74b-109">Текстовые архивные файлы ASCII</span><span class="sxs-lookup"><span data-stu-id="aa74b-109">ASCII Text Archive Files</span></span>

<span data-ttu-id="aa74b-110">[Текстовые архивные файлы](text-archive-files.md) ASCII, экспортированные с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) , объясняются в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="aa74b-110">The ASCII [Text Archive Files](text-archive-files.md) exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) are explained in the following format:</span></span>

-   <span data-ttu-id="aa74b-111">Имена столбцов таблицы записываются в первой строке.</span><span class="sxs-lookup"><span data-stu-id="aa74b-111">The names of the table columns are written on the first line.</span></span>
-   <span data-ttu-id="aa74b-112">Форматы столбцов записываются во второй строке.</span><span class="sxs-lookup"><span data-stu-id="aa74b-112">The column formats are written on the second line.</span></span>
-   <span data-ttu-id="aa74b-113">Если таблица содержит только данные ASCII, третья строка текстового файла представляет собой имя таблицы, за которым следует список первичных ключей.</span><span class="sxs-lookup"><span data-stu-id="aa74b-113">If the table contains only ASCII data, the third line of the text file is the table name followed by a list of the primary keys.</span></span>
-   <span data-ttu-id="aa74b-114">Если таблица содержит данные, не входящие в набор ASCII, а база данных помечена цифровой кодовой страницей, номер кодовой страницы отображается в начале третьей строки.</span><span class="sxs-lookup"><span data-stu-id="aa74b-114">If the table contains non-ASCII data and the database is stamped with a numeric code page, the code page number appears at the beginning of the third line.</span></span>
-   <span data-ttu-id="aa74b-115">Если база данных содержит данные, не входящие в набор ASCII, но база данных не помечена цифровой кодовой страницей, номер текущей системной кодовой страницы записывается в начале третьей строки.</span><span class="sxs-lookup"><span data-stu-id="aa74b-115">If the database contains non-ASCII data, but the database is not stamped with the numeric code page, the current system code page number is written at the beginning of the third line.</span></span>
-   <span data-ttu-id="aa74b-116">Остальные строки текстового файла — это данные в указанной кодовой странице.</span><span class="sxs-lookup"><span data-stu-id="aa74b-116">The remaining lines of the text file are the data in the specified code page.</span></span>
-   <span data-ttu-id="aa74b-117">Если таблица содержит потоки, [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) экспортирует каждый поток в таблице в отдельный файл.</span><span class="sxs-lookup"><span data-stu-id="aa74b-117">If a table contains streams, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exports each stream in the table to a separate file.</span></span>

### <a name="neutral-and-non-neutral-code-pages"></a><span data-ttu-id="aa74b-118">Нейтральные и ненейтральные кодовые страницы</span><span class="sxs-lookup"><span data-stu-id="aa74b-118">Neutral and Non-Neutral Code Pages</span></span>

<span data-ttu-id="aa74b-119">Локализацию можно упростить, начав с базы данных со нейтральной кодовой страницей:</span><span class="sxs-lookup"><span data-stu-id="aa74b-119">You can facilitate localization by starting with a database that has a neutral code page:</span></span>

-   <span data-ttu-id="aa74b-120">Пустая база данных имеет нейтральную кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="aa74b-120">A blank database has a neutral code page.</span></span>
-   <span data-ttu-id="aa74b-121">База данных, которая не содержит расширенные символы, требующие представления кодовой страницы в коде ASCII, имеет нейтральную кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="aa74b-121">A database that does not contain extended characters that require a code page to be represented in ASCII has a neutral code page.</span></span>

<span data-ttu-id="aa74b-122">Дополнительные сведения см. в разделе [Создание базы данных с нейтральной кодовой страницей](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="aa74b-122">For more information, see [Creating a Database with a Neutral Code Page](creating-a-database-with-a-neutral-code-page.md).</span></span>

<span data-ttu-id="aa74b-123">Нейтральные и ненейтральные кодовые страницы имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="aa74b-123">Neutral and non-neutral code pages have the following characteristics:</span></span>

-   <span data-ttu-id="aa74b-124">Если [файл текстового архива](text-archive-files.md) с ненейтральной кодовой страницей импортируется в базу данных с другой ненейтральной кодовой страницей, то установщик возвращает ошибку при вызове [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .</span><span class="sxs-lookup"><span data-stu-id="aa74b-124">If a [Text Archive File](text-archive-files.md) with a non-neutral code page is imported into a database that has a different non-neutral code page, the Installer returns an error when [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) is called.</span></span>
-   <span data-ttu-id="aa74b-125">[Файл текстового архива](text-archive-files.md) с нейтральной кодовой страницей можно импортировать в базу данных с любой кодовой страницей.</span><span class="sxs-lookup"><span data-stu-id="aa74b-125">A [Text Archive File](text-archive-files.md) that has a neutral code page can be imported into a database that has any code page.</span></span>
-   <span data-ttu-id="aa74b-126">[Файл текстового архива](text-archive-files.md) с любой кодовой страницей можно импортировать в базу данных с нейтральной кодовой страницей.</span><span class="sxs-lookup"><span data-stu-id="aa74b-126">A [Text Archive File](text-archive-files.md) that has any code page can be imported into a database that has a neutral code page.</span></span>
-   <span data-ttu-id="aa74b-127">При импорте [текстового файла архива](text-archive-files.md) в базу данных с нейтральной кодовой страницей кодовая страница базы данных задается кодовой страницей файла архива.</span><span class="sxs-lookup"><span data-stu-id="aa74b-127">Importing a [Text Archive File](text-archive-files.md) into a database with a neutral code page sets the code page of the database to the archive file code page.</span></span> <span data-ttu-id="aa74b-128">Все архивные файлы, которые впоследствии импортируются в базу данных, должны иметь ту же кодовую страницу, что и первый файл.</span><span class="sxs-lookup"><span data-stu-id="aa74b-128">All archive files subsequently imported into the database must have the same code page as the first file.</span></span>

<span data-ttu-id="aa74b-129">Дополнительные сведения см. в разделе [Определение кодовой страницы базы данных установки](determining-an-installation-database-s-code-page.md) и [Установка кодовой страницы базы данных](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="aa74b-129">For more information, see [Determining an Installation Database Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

<span data-ttu-id="aa74b-130">[Файлы архивов](text-archive-files.md) , экспортированные [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) , можно использовать с системами управления версиями.</span><span class="sxs-lookup"><span data-stu-id="aa74b-130">The [Text Archive Files](text-archive-files.md) that are exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) can be used with version control systems.</span></span> <span data-ttu-id="aa74b-131">Для изменения базы данных используйте [функции базы данных](database-functions.md) или редактор таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="aa74b-131">Use the [Database Functions](database-functions.md) or a database table editor to edit the database.</span></span>

<span data-ttu-id="aa74b-132">Сведения о локализации можно добавить в базу данных установки с помощью редактора таблиц базы данных или API установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="aa74b-132">You can add localization information to an installation database by using a database table editor or the Windows Installer API.</span></span> <span data-ttu-id="aa74b-133">Дополнительные сведения см. в разделе [Обработка кодовых страниц строк параметров](code-page-handling-of-parameter-strings.md).</span><span class="sxs-lookup"><span data-stu-id="aa74b-133">For more information, see [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span></span>

 

 



