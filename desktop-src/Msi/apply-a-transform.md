---
description: Файл WiUseXfm.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как можно использовать скрипт для применения преобразования к установщик Windows базе данных.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Применение преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909104"
---
# <a name="apply-a-transform"></a><span data-ttu-id="bdeb7-104">Применение преобразования</span><span class="sxs-lookup"><span data-stu-id="bdeb7-104">Apply a Transform</span></span>

<span data-ttu-id="bdeb7-105">Файл WiUseXfm.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="bdeb7-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="bdeb7-106">В этом примере показано, как можно использовать скрипт для применения преобразования к установщик Windows базе данных.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="bdeb7-107">В примере демонстрируется использование</span><span class="sxs-lookup"><span data-stu-id="bdeb7-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="bdeb7-108">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="bdeb7-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="bdeb7-109">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="bdeb7-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="bdeb7-110">**Метод Апплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="bdeb7-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="bdeb7-111">[**Метод Commit**](database-commit.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="bdeb7-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="bdeb7-112">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="bdeb7-113">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="bdeb7-114">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="bdeb7-115">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-115">or if too few arguments are specified.</span></span> <span data-ttu-id="bdeb7-116">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="bdeb7-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="bdeb7-117">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="bdeb7-118">**cscript WiUseXfm.vbs \[ путь к исходному пути базы данных \] \[ к \] \[ параметрам преобразования файла\]**</span><span class="sxs-lookup"><span data-stu-id="bdeb7-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="bdeb7-119">Укажите путь к базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="bdeb7-120">Укажите путь к файлу преобразования.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-120">Specify the path to the transform file.</span></span> <span data-ttu-id="bdeb7-121">Если путь к файлу преобразования опущен, то сравниваются только две базы данных.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="bdeb7-122">Третьим аргументом является необязательное числовое значение, указывающее набор условий ошибки, которые следует подавлять.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="bdeb7-123">Добавьте эти значения вместе, чтобы отключить несколько условий.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="bdeb7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bdeb7-124">Value</span></span> | <span data-ttu-id="bdeb7-125">Условие ошибки для подавления</span><span class="sxs-lookup"><span data-stu-id="bdeb7-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="bdeb7-126">1</span><span class="sxs-lookup"><span data-stu-id="bdeb7-126">1</span></span>     | <span data-ttu-id="bdeb7-127">Добавление уже существующей строки.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="bdeb7-128">2</span><span class="sxs-lookup"><span data-stu-id="bdeb7-128">2</span></span>     | <span data-ttu-id="bdeb7-129">Удаление несуществующей строки.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="bdeb7-130">4</span><span class="sxs-lookup"><span data-stu-id="bdeb7-130">4</span></span>     | <span data-ttu-id="bdeb7-131">Добавление уже существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="bdeb7-132">8</span><span class="sxs-lookup"><span data-stu-id="bdeb7-132">8</span></span>     | <span data-ttu-id="bdeb7-133">Удаление несуществующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="bdeb7-134">16</span><span class="sxs-lookup"><span data-stu-id="bdeb7-134">16</span></span>    | <span data-ttu-id="bdeb7-135">Обновление несуществующей строки.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="bdeb7-136">256</span><span class="sxs-lookup"><span data-stu-id="bdeb7-136">256</span></span>   | <span data-ttu-id="bdeb7-137">Несоответствие кодовых страниц базы данных и преобразования.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="bdeb7-138">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="bdeb7-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="bdeb7-139">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bdeb7-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



