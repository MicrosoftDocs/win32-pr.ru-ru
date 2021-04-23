---
description: Файл WiFilVer.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как можно использовать скрипт для создания отчетов или обновления версии файла, размера и сведений о языке.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Управление размерами и версиями файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810732"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="3231c-104">Управление размерами и версиями файлов</span><span class="sxs-lookup"><span data-stu-id="3231c-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="3231c-105">Файл WiFilVer.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="3231c-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="3231c-106">В этом примере показано, как можно использовать скрипт для создания отчетов или обновления версии файла, размера и сведений о языке.</span><span class="sxs-lookup"><span data-stu-id="3231c-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="3231c-107">В этом примере также показаны установщик Windows действия, доступ к базе данных установщик Windows и использование следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3231c-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="3231c-108">Метод [**Installer. Опендатабасе**](installer-opendatabase.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="3231c-109">Свойство [**Installer. FileAttributes**](installer-fileattributes.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="3231c-110">Метод [**Installer. FileHash**](installer-filehash.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="3231c-111">Метод [**Installer. FileVersion**](installer-fileversion.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="3231c-112">Метод [**Installer. Ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="3231c-113">[**Database. OpenView,**](database-openview.md) метод</span><span class="sxs-lookup"><span data-stu-id="3231c-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="3231c-114">Свойство [**Database. SummaryInformation**](database-summaryinformation.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="3231c-115">[**Session. DoAction,**](session-doaction.md) метод</span><span class="sxs-lookup"><span data-stu-id="3231c-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="3231c-116">**Session. Property**</span><span class="sxs-lookup"><span data-stu-id="3231c-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="3231c-117">Свойство [**Session. SourcePath**](session-sourcepath.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="3231c-118">Свойство [**Session. Mode**](session-mode.md) [ **объекта Session**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="3231c-119">Свойство [**Record. StringData**](record-stringdata.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="3231c-120">Свойство [**Record. IntegerData**](record-integerdata.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="3231c-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="3231c-121">Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="3231c-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="3231c-122">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="3231c-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="3231c-123">**cscript WiFilVer.vbs \[ путь к \] \[ необязательным исходным расположениям базы данных\]**</span><span class="sxs-lookup"><span data-stu-id="3231c-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="3231c-124">Также необходимо учитывать следующее:</span><span class="sxs-lookup"><span data-stu-id="3231c-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="3231c-125">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="3231c-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="3231c-126">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="3231c-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="3231c-127">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="3231c-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="3231c-128">Пример возвращает значение 0 (ноль) для успешного выполнения, 1 (один), если вызывается Справка, и 2 (два) в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="3231c-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="3231c-129">Укажите установщик Windows базу данных, которую необходимо обновить, которая должна находиться в корне исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3231c-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="3231c-130">Однако можно указать источники базы данных в разных расположениях.</span><span class="sxs-lookup"><span data-stu-id="3231c-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="3231c-131">Если источник сжат, все файлы открываются в корне.</span><span class="sxs-lookup"><span data-stu-id="3231c-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="3231c-132">Следующие параметры можно указать в любом расположении в командной строке.</span><span class="sxs-lookup"><span data-stu-id="3231c-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="3231c-133">Параметр</span><span class="sxs-lookup"><span data-stu-id="3231c-133">Option</span></span>                | <span data-ttu-id="3231c-134">Описание</span><span class="sxs-lookup"><span data-stu-id="3231c-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3231c-135">*параметр не указан*</span><span class="sxs-lookup"><span data-stu-id="3231c-135">*no option specified*</span></span> | <span data-ttu-id="3231c-136">Отображает сведения о файле базы данных.</span><span class="sxs-lookup"><span data-stu-id="3231c-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="3231c-137">/U</span><span class="sxs-lookup"><span data-stu-id="3231c-137">/u</span></span>                    | <span data-ttu-id="3231c-138">Обновите размер файла, версию и сведения о языке в базе данных источника.</span><span class="sxs-lookup"><span data-stu-id="3231c-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="3231c-139">Дополнительные сведения см. в статьях [примеры сценариев установщик Windows](windows-installer-scripting-examples.md) и [средства разработки установщик Windows](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3231c-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



