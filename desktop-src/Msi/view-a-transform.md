---
description: Файл WiLstXfm.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Этот пример скрипта можно использовать для просмотра файла преобразования.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Просмотр преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650522"
---
# <a name="view-a-transform"></a><span data-ttu-id="2717a-104">Просмотр преобразования</span><span class="sxs-lookup"><span data-stu-id="2717a-104">View a Transform</span></span>

<span data-ttu-id="2717a-105">Файл WiLstXfm.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2717a-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="2717a-106">Этот пример скрипта можно использовать для просмотра файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="2717a-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="2717a-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="2717a-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="2717a-108">\_Таблица переformview</span><span class="sxs-lookup"><span data-stu-id="2717a-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="2717a-109">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="2717a-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="2717a-110">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="2717a-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="2717a-111">**Метод Апплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="2717a-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="2717a-112">**Метод OpenView**</span><span class="sxs-lookup"><span data-stu-id="2717a-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="2717a-113">[**Метод Commit**](database-commit.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="2717a-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="2717a-114">**Свойство IsNull**</span><span class="sxs-lookup"><span data-stu-id="2717a-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="2717a-115">[**Свойство StringData**](record-stringdata.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="2717a-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="2717a-116">Для использования этого примера требуется CScript.exe версия сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="2717a-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="2717a-117">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2717a-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="2717a-118">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="2717a-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="2717a-119">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="2717a-119">or if too few arguments are specified.</span></span> <span data-ttu-id="2717a-120">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="2717a-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="2717a-121">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="2717a-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="2717a-122">**cscript WiLstXfm.vbs** *\[ путь для ссылки на \] \[ путь к параметру базы данных \] \[ для \] просмотра преобразования*</span><span class="sxs-lookup"><span data-stu-id="2717a-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="2717a-123">Укажите путь к справочной базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="2717a-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="2717a-124">Укажите список путей для преобразования просматриваемых файлов.</span><span class="sxs-lookup"><span data-stu-id="2717a-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="2717a-125">Каждому пути в списке может предшествовать необязательное числовое значение.</span><span class="sxs-lookup"><span data-stu-id="2717a-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="2717a-126">Это значение указывает набор ошибочных условий, которые следует подавлять.</span><span class="sxs-lookup"><span data-stu-id="2717a-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="2717a-127">Эти значения можно добавить вместе, чтобы отключить несколько условий.</span><span class="sxs-lookup"><span data-stu-id="2717a-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="2717a-128">Если параметр Numeric не указан, все условия ошибки подавляются.</span><span class="sxs-lookup"><span data-stu-id="2717a-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="2717a-129">Аргументы в этом списке выполняются в порядке слева направо, в котором они отображаются в командной строке.</span><span class="sxs-lookup"><span data-stu-id="2717a-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="2717a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2717a-130">Value</span></span> | <span data-ttu-id="2717a-131">Условие ошибки для подавления</span><span class="sxs-lookup"><span data-stu-id="2717a-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="2717a-132">1</span><span class="sxs-lookup"><span data-stu-id="2717a-132">1</span></span>     | <span data-ttu-id="2717a-133">Добавление уже существующей строки.</span><span class="sxs-lookup"><span data-stu-id="2717a-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="2717a-134">2</span><span class="sxs-lookup"><span data-stu-id="2717a-134">2</span></span>     | <span data-ttu-id="2717a-135">Удаление несуществующей строки.</span><span class="sxs-lookup"><span data-stu-id="2717a-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="2717a-136">4</span><span class="sxs-lookup"><span data-stu-id="2717a-136">4</span></span>     | <span data-ttu-id="2717a-137">Добавление уже существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="2717a-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="2717a-138">8</span><span class="sxs-lookup"><span data-stu-id="2717a-138">8</span></span>     | <span data-ttu-id="2717a-139">Удаление несуществующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="2717a-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="2717a-140">16</span><span class="sxs-lookup"><span data-stu-id="2717a-140">16</span></span>    | <span data-ttu-id="2717a-141">Обновление несуществующей строки.</span><span class="sxs-lookup"><span data-stu-id="2717a-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="2717a-142">256</span><span class="sxs-lookup"><span data-stu-id="2717a-142">256</span></span>   | <span data-ttu-id="2717a-143">Несоответствие кодовых страниц базы данных и преобразования.</span><span class="sxs-lookup"><span data-stu-id="2717a-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="2717a-144">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2717a-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="2717a-145">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2717a-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



