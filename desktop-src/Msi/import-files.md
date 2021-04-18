---
description: Файл WiImport.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как написать скрипт для импорта таблиц в базу данных установщик Windows.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Импорт файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650621"
---
# <a name="import-files"></a><span data-ttu-id="75a16-104">Импорт файлов</span><span class="sxs-lookup"><span data-stu-id="75a16-104">Import Files</span></span>

<span data-ttu-id="75a16-105">Файл WiImport.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="75a16-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="75a16-106">В этом примере показано, как написать скрипт для импорта таблиц в базу данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="75a16-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="75a16-107">Сценарий подключается к объекту [**установщика**](installer-object.md) , открывает базу данных, обрабатывает список файлов и фиксирует изменения перед закрытием базы данных.</span><span class="sxs-lookup"><span data-stu-id="75a16-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="75a16-108">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="75a16-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="75a16-109">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="75a16-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="75a16-110">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="75a16-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="75a16-111">**Метод Import**</span><span class="sxs-lookup"><span data-stu-id="75a16-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="75a16-112">[**Метод Commit**](database-commit.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="75a16-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="75a16-113">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="75a16-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="75a16-114">Чтобы использовать CScript.exe для запуска этого образца, используйте в командной строке следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="75a16-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="75a16-115">**cscript WiImport.vbs \[ путь к базе данных \] \[ путь к папке \] \[ Параметры папки \] \[ архивный список файлов**\]</span><span class="sxs-lookup"><span data-stu-id="75a16-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="75a16-116">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="75a16-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="75a16-117">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="75a16-117">or if too few arguments are specified.</span></span> <span data-ttu-id="75a16-118">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ путь к файлу \] . Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="75a16-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="75a16-119">Укажите путь к базе данных установщика Windows, которая должна быть создана, или для получения импортированных таблиц.</span><span class="sxs-lookup"><span data-stu-id="75a16-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="75a16-120">Укажите путь к папке, содержащей архивные файлы импортируемых таблиц.</span><span class="sxs-lookup"><span data-stu-id="75a16-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="75a16-121">Перечислите имена импортируемых файлов архива.</span><span class="sxs-lookup"><span data-stu-id="75a16-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="75a16-122">Имена файлов с подстановочными знаками, например \* IDT, можно использовать для импорта нескольких файлов.</span><span class="sxs-lookup"><span data-stu-id="75a16-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="75a16-123">Следующие параметры могут быть указаны в командной строке перед списком файлов.</span><span class="sxs-lookup"><span data-stu-id="75a16-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="75a16-124">Параметр</span><span class="sxs-lookup"><span data-stu-id="75a16-124">Option</span></span>              | <span data-ttu-id="75a16-125">Описание</span><span class="sxs-lookup"><span data-stu-id="75a16-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a16-126">параметр не указан</span><span class="sxs-lookup"><span data-stu-id="75a16-126">no option specified</span></span> | <span data-ttu-id="75a16-127">Импортируйте список файлов архива таблицы из указанной папки в базу данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="75a16-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="75a16-128">/C</span><span class="sxs-lookup"><span data-stu-id="75a16-128">/c</span></span>                  | <span data-ttu-id="75a16-129">Создайте базу данных установщик Windows, а затем импортируйте список архивных файлов таблицы из указанной папки в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="75a16-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="75a16-130">Дополнительные сведения см. в статье [установщик Windows примеры сценариев](windows-installer-scripting-examples.md) для дополнительных примеров сценариев.</span><span class="sxs-lookup"><span data-stu-id="75a16-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="75a16-131">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="75a16-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="75a16-132">Обратите внимание, что [в примере локализации](a-localization-example.md) также демонстрируется [Импорт локализованных таблиц ошибок и актионтекст](importing-localized-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="75a16-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



