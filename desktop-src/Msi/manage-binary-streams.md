---
description: Файл WiStream.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Управление двоичными потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674158"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="52068-103">Управление двоичными потоками</span><span class="sxs-lookup"><span data-stu-id="52068-103">Manage Binary Streams</span></span>

<span data-ttu-id="52068-104">Файл WiStream.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="52068-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="52068-105">В этом примере показано, как можно использовать скрипт для управления двоичными потоками в базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="52068-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="52068-106">Образец можно использовать для ввода сжатых файловых CAB-файлов в базу данных.</span><span class="sxs-lookup"><span data-stu-id="52068-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="52068-107">В этом примере демонстрируется работа [ \_ таблицы Streams](-streams-table.md) в базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="52068-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="52068-108">В примере также демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="52068-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="52068-109">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="52068-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="52068-110">**СоздатьЗапись, метод**</span><span class="sxs-lookup"><span data-stu-id="52068-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="52068-111">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="52068-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="52068-112">**Метод OpenView**</span><span class="sxs-lookup"><span data-stu-id="52068-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="52068-113">[**Метод Commit**](database-commit.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="52068-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="52068-114">**Метод Fetch**</span><span class="sxs-lookup"><span data-stu-id="52068-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="52068-115">**Метод Modify**</span><span class="sxs-lookup"><span data-stu-id="52068-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="52068-116">[**Метод Execute**](view-execute.md) [ **объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="52068-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="52068-117">**StringData, свойство**</span><span class="sxs-lookup"><span data-stu-id="52068-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="52068-118">[**Метод сетстреам**](record-setstream.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="52068-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="52068-119">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="52068-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="52068-120">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="52068-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="52068-121">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="52068-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="52068-122">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="52068-122">or if too few arguments are specified.</span></span> <span data-ttu-id="52068-123">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="52068-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="52068-124">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="52068-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="52068-125">**cscript WiStream.vbs \[ путь к базе данных \] \[ путь к файлу \] \[ Параметры файла \] \[ имя потока\]**</span><span class="sxs-lookup"><span data-stu-id="52068-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="52068-126">Укажите путь к установщик Windows базе данных, которая будет принимать поток.</span><span class="sxs-lookup"><span data-stu-id="52068-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="52068-127">Укажите путь к двоичному файлу, содержащему потоковые данные.</span><span class="sxs-lookup"><span data-stu-id="52068-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="52068-128">Чтобы вывести список потоков в базе данных установщика, опустите этот путь.</span><span class="sxs-lookup"><span data-stu-id="52068-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="52068-129">Вы можете указать необязательное имя потока, если оно не указано, по умолчанию используется имя файла.</span><span class="sxs-lookup"><span data-stu-id="52068-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="52068-130">Можно указать следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="52068-130">The following option may be specified.</span></span>



| <span data-ttu-id="52068-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="52068-131">Option</span></span>              | <span data-ttu-id="52068-132">Описание</span><span class="sxs-lookup"><span data-stu-id="52068-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52068-133">параметр не указан</span><span class="sxs-lookup"><span data-stu-id="52068-133">no option specified</span></span> | <span data-ttu-id="52068-134">Добавьте поток в базу данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="52068-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="52068-135">/d</span><span class="sxs-lookup"><span data-stu-id="52068-135">/d</span></span>                  | <span data-ttu-id="52068-136">Удалить поток.</span><span class="sxs-lookup"><span data-stu-id="52068-136">Remove a stream.</span></span> <span data-ttu-id="52068-137">За этим флагом параметра должно следовать имя удаляемого подхранилища.</span><span class="sxs-lookup"><span data-stu-id="52068-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="52068-138">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="52068-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="52068-139">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="52068-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



