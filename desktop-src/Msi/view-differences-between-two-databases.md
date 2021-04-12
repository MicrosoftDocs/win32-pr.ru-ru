---
description: Файл WiDiffDb.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Этот пример скрипта создает временный файл преобразования между двумя установщик Windowsными базами данных и отображает преобразование.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Просмотр различий между двумя базами данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541191"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="4858e-104">Просмотр различий между двумя базами данных</span><span class="sxs-lookup"><span data-stu-id="4858e-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="4858e-105">Файл WiDiffDb.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4858e-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="4858e-106">Этот пример скрипта создает временный файл преобразования между двумя установщик Windowsными базами данных и отображает преобразование.</span><span class="sxs-lookup"><span data-stu-id="4858e-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="4858e-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="4858e-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="4858e-108">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="4858e-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="4858e-109">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4858e-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="4858e-110">**Метод OpenView**</span><span class="sxs-lookup"><span data-stu-id="4858e-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="4858e-111">**Свойство SummaryInformation (объект Database)**</span><span class="sxs-lookup"><span data-stu-id="4858e-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="4858e-112">**Метод GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="4858e-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="4858e-113">**Метод Апплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="4858e-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="4858e-114">**Объект базы данных**</span><span class="sxs-lookup"><span data-stu-id="4858e-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="4858e-115">[**Метод Fetch**](view-fetch.md) [ **объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="4858e-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="4858e-116">**Свойство IsNull**</span><span class="sxs-lookup"><span data-stu-id="4858e-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="4858e-117">[**Свойство StringData**](record-stringdata.md) [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="4858e-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="4858e-118">\_Таблица переformview</span><span class="sxs-lookup"><span data-stu-id="4858e-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="4858e-119">Для использования этого примера требуется CScript.exe версия сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="4858e-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="4858e-120">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="4858e-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="4858e-121">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="4858e-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="4858e-122">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="4858e-122">or if too few arguments are specified.</span></span> <span data-ttu-id="4858e-123">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="4858e-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="4858e-124">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="4858e-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="4858e-125">**cscript WiDiffDb.vbs** *\[ путь к исходному пути базы данных \] \[ к \] измененной базе данных*</span><span class="sxs-lookup"><span data-stu-id="4858e-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="4858e-126">Укажите путь к исходной базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="4858e-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="4858e-127">Укажите путь к измененной базе данных.</span><span class="sxs-lookup"><span data-stu-id="4858e-127">Specify the path to the revised database.</span></span> <span data-ttu-id="4858e-128">В примере скрипта будет отображаться преобразование.</span><span class="sxs-lookup"><span data-stu-id="4858e-128">The sample script will display the transform.</span></span>

<span data-ttu-id="4858e-129">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4858e-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="4858e-130">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4858e-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



