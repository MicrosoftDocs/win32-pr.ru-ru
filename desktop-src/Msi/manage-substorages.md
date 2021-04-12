---
description: Файл WiSubStg.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Управление подхранилищами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348975"
---
# <a name="manage-substorages"></a><span data-ttu-id="6b75b-103">Управление подхранилищами</span><span class="sxs-lookup"><span data-stu-id="6b75b-103">Manage Substorages</span></span>

<span data-ttu-id="6b75b-104">Файл WiSubStg.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6b75b-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="6b75b-105">В этом примере показано, как можно использовать скрипт для управления подхранилищами в базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="6b75b-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="6b75b-106">Преобразование можно добавить в существующую базу данных установщик Windows как подхранилище.</span><span class="sxs-lookup"><span data-stu-id="6b75b-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="6b75b-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="6b75b-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="6b75b-108">\_Таблица хранилищ</span><span class="sxs-lookup"><span data-stu-id="6b75b-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="6b75b-109">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="6b75b-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="6b75b-110">**СоздатьЗапись, метод**</span><span class="sxs-lookup"><span data-stu-id="6b75b-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="6b75b-111">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="6b75b-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="6b75b-112">**Метод OpenView**</span><span class="sxs-lookup"><span data-stu-id="6b75b-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="6b75b-113">[**Метод Commit**](database-commit.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="6b75b-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="6b75b-114">**Метод Fetch**</span><span class="sxs-lookup"><span data-stu-id="6b75b-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="6b75b-115">**Метод Modify**</span><span class="sxs-lookup"><span data-stu-id="6b75b-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="6b75b-116">[**Метод Execute**](view-execute.md) [ **объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="6b75b-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="6b75b-117">**StringData, свойство**</span><span class="sxs-lookup"><span data-stu-id="6b75b-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="6b75b-118">[**Метод сетстреам**](record-setstream.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="6b75b-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="6b75b-119">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="6b75b-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="6b75b-120">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6b75b-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="6b75b-121">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="6b75b-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="6b75b-122">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="6b75b-122">or if too few arguments are specified.</span></span> <span data-ttu-id="6b75b-123">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="6b75b-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="6b75b-124">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="6b75b-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="6b75b-125">**cscript WiSubStg.vbs \[ путь к базе данных \] \[ путь к папке \] \[ Параметры файла \] \[ имя подхранилища\]**</span><span class="sxs-lookup"><span data-stu-id="6b75b-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="6b75b-126">Укажите путь к установщик Windows базе данных для добавления или удаления вложенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b75b-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="6b75b-127">Укажите путь к преобразованию или файлу базы данных, добавляемому в качестве вложенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b75b-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="6b75b-128">Чтобы получить список вложенных хранилищ в установщик Windows базе данных, не указывайте путь к этому файлу.</span><span class="sxs-lookup"><span data-stu-id="6b75b-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="6b75b-129">Вы можете указать необязательное имя подхранилища, если оно не указано, по умолчанию используется имя файла.</span><span class="sxs-lookup"><span data-stu-id="6b75b-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="6b75b-130">Можно указать следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="6b75b-130">The following option may be specified.</span></span>



| <span data-ttu-id="6b75b-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="6b75b-131">Option</span></span>              | <span data-ttu-id="6b75b-132">Описание</span><span class="sxs-lookup"><span data-stu-id="6b75b-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b75b-133">параметр не указан</span><span class="sxs-lookup"><span data-stu-id="6b75b-133">no option specified</span></span> | <span data-ttu-id="6b75b-134">Добавьте в базу данных установщик Windows подхранилище.</span><span class="sxs-lookup"><span data-stu-id="6b75b-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="6b75b-135">/d</span><span class="sxs-lookup"><span data-stu-id="6b75b-135">/d</span></span>                  | <span data-ttu-id="6b75b-136">Удаляет подхранилище.</span><span class="sxs-lookup"><span data-stu-id="6b75b-136">Remove a substorage.</span></span> <span data-ttu-id="6b75b-137">За этим флагом параметра должно следовать имя подхранилища, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6b75b-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="6b75b-138">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6b75b-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="6b75b-139">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6b75b-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="6b75b-140">Обратите внимание, что [Пример локализации](a-localization-example.md) демонстрирует [внедрение преобразований настройки в качестве подхранилища](embedding-customization-transforms-as-substorage.md).</span><span class="sxs-lookup"><span data-stu-id="6b75b-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



