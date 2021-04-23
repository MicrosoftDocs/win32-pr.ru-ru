---
description: Файл WiExport.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Экспорт файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683096"
---
# <a name="export-files"></a><span data-ttu-id="b0fad-103">Экспорт файлов</span><span class="sxs-lookup"><span data-stu-id="b0fad-103">Export Files</span></span>

<span data-ttu-id="b0fad-104">Файл WiExport.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b0fad-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b0fad-105">В этом примере показано, как написать скрипт для экспорта таблиц в базу данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="b0fad-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="b0fad-106">Пример скрипта подключается к объекту [**установщика**](installer-object.md) , открывает базу данных и экспортирует таблицы в архивные файлы.</span><span class="sxs-lookup"><span data-stu-id="b0fad-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="b0fad-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="b0fad-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="b0fad-108">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="b0fad-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="b0fad-109">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b0fad-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="b0fad-110">**Метод экспорта**</span><span class="sxs-lookup"><span data-stu-id="b0fad-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="b0fad-111">[**Метод OpenView**](database-openview.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="b0fad-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="b0fad-112">[**Метод Fetch**](view-fetch.md) [ **объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="b0fad-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="b0fad-113">[**Свойство StringData**](record-stringdata.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="b0fad-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="b0fad-114">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="b0fad-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="b0fad-115">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="b0fad-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="b0fad-116">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="b0fad-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="b0fad-117">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="b0fad-117">or if too few arguments are specified.</span></span> <span data-ttu-id="b0fad-118">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="b0fad-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="b0fad-119">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="b0fad-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="b0fad-120">**cscript WiExport.vbs \[ путь к базе данных \] \[ путь к папке \] \[ Параметры \] \[ списка имя таблицы\]**</span><span class="sxs-lookup"><span data-stu-id="b0fad-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="b0fad-121">Укажите путь к базе данных установщика, из которой экспортируются таблицы.</span><span class="sxs-lookup"><span data-stu-id="b0fad-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="b0fad-122">Укажите путь к папке, в которую будут скопированы экспортированные архивные файлы.</span><span class="sxs-lookup"><span data-stu-id="b0fad-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="b0fad-123">Список имен экспортируемых [таблиц базы данных](database-tables.md) с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="b0fad-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="b0fad-124">Укажите " \* ", чтобы экспортировать все таблицы, включая \_ SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="b0fad-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="b0fad-125">Следующие параметры могут быть заданы в любом месте командной строки перед списком имен таблиц.</span><span class="sxs-lookup"><span data-stu-id="b0fad-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="b0fad-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="b0fad-126">Option</span></span>              | <span data-ttu-id="b0fad-127">Описание</span><span class="sxs-lookup"><span data-stu-id="b0fad-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="b0fad-128">параметр не указан</span><span class="sxs-lookup"><span data-stu-id="b0fad-128">no option specified</span></span> | <span data-ttu-id="b0fad-129">Экспортированные архивные файлы могут иметь длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="b0fad-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="b0fad-130">/s</span><span class="sxs-lookup"><span data-stu-id="b0fad-130">/s</span></span>                  | <span data-ttu-id="b0fad-131">Принудительно экспортировать архивные файлы, чтобы иметь короткие имена файлов.</span><span class="sxs-lookup"><span data-stu-id="b0fad-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="b0fad-132">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b0fad-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="b0fad-133">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b0fad-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



