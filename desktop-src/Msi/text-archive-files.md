---
description: Таблицы установщик Windows базы данных можно экспортировать в текстовые файлы ASCII с помощью Мсидатабасикспорт или метода Export объекта Database.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Файлы архивов текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910363"
---
# <a name="text-archive-files"></a><span data-ttu-id="93be3-103">Файлы архивов текста</span><span class="sxs-lookup"><span data-stu-id="93be3-103">Text Archive Files</span></span>

<span data-ttu-id="93be3-104">Таблицы установщик Windows базы данных можно экспортировать в текстовые файлы ASCII с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) или метода [**Export**](database-export.md) объекта [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="93be3-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="93be3-105">Сведения в этих файлах текстовых архивов затем можно импортировать обратно в базу данных установщик Windows с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) или метода [Import](database-import.md) объекта **Database** .</span><span class="sxs-lookup"><span data-stu-id="93be3-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="93be3-106">Такие средства, как [msidb.exe](msidb-exe.md) , способны экспортировать и импортировать текстовые архивные файлы.</span><span class="sxs-lookup"><span data-stu-id="93be3-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="93be3-107">[Примеры сценариев установщик Windows](windows-installer-scripting-examples.md) , в которых можно экспортировать и импортировать текстовые архивные файлы из базы данных, см. в разделе [Экспорт файлов](export-files.md) и [Импорт файлов](import-files.md) .</span><span class="sxs-lookup"><span data-stu-id="93be3-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="93be3-108">Файлы текстовых архивов не предназначены для изменения базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="93be3-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="93be3-109">Для создания и изменения пакета установки следует использовать средство редактирования таблиц установщик Windows, например [Orca](orca-exe.md) или сторонний инструмент.</span><span class="sxs-lookup"><span data-stu-id="93be3-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="93be3-110">Файлы архивов текста можно использовать в следующих целях.</span><span class="sxs-lookup"><span data-stu-id="93be3-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="93be3-111">Файлы архивов текста можно использовать с системами управления версиями.</span><span class="sxs-lookup"><span data-stu-id="93be3-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="93be3-112">Чтобы удалить неиспользуемое дисковое пространство и сократить окончательный размер MSI-файлов.</span><span class="sxs-lookup"><span data-stu-id="93be3-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="93be3-113">См. раздел [уменьшение размера MSI файла](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="93be3-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="93be3-114">Для добавления сведений о локализации в базу данных установки.</span><span class="sxs-lookup"><span data-stu-id="93be3-114">To add localization information to an installation database.</span></span> <span data-ttu-id="93be3-115">Дополнительные сведения см. в разделе [Обработка кодовых страниц импортированных и экспортированных таблиц](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="93be3-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="93be3-116">Для определения кодовой страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="93be3-116">To determine the code page of a database.</span></span> <span data-ttu-id="93be3-117">См. раздел [Определение кодовой страницы базы данных установки](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="93be3-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="93be3-118">Для задания кодовой страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="93be3-118">To set the code page of a database.</span></span> <span data-ttu-id="93be3-119">См. раздел [Настройка кодовой страницы базы данных](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="93be3-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="93be3-120">Для увеличения предельного значения столбца базы данных.</span><span class="sxs-lookup"><span data-stu-id="93be3-120">To increase the limit of a database column.</span></span> <span data-ttu-id="93be3-121">Экспортируйте таблицу с помощью [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), измените экспортированный файл IDT, а затем импортируйте таблицу с помощью [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="93be3-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="93be3-122">Авторы не могут изменять типы данных столбцов, допустимость значений NULL или атрибуты локализации любых столбцов в стандартных таблицах.</span><span class="sxs-lookup"><span data-stu-id="93be3-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="93be3-123">См. также [Создание большого пакета](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="93be3-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="93be3-124">На следующих страницах описываются текстовые архивные страницы и их форматы.</span><span class="sxs-lookup"><span data-stu-id="93be3-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="93be3-125">Формат файла архива</span><span class="sxs-lookup"><span data-stu-id="93be3-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="93be3-126">Данные ASCII в текстовых архивных файлах</span><span class="sxs-lookup"><span data-stu-id="93be3-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="93be3-127">\_форцекодепаже</span><span class="sxs-lookup"><span data-stu-id="93be3-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="93be3-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="93be3-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



