---
description: Пример файла кода VBScript WiTextIn.vbs предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Копирование файла ANSI в поле базы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663582"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="4f6d6-103">Копирование файла ANSI в поле базы данных</span><span class="sxs-lookup"><span data-stu-id="4f6d6-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="4f6d6-104">Пример файла кода VBScript WiTextIn.vbs предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4f6d6-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="4f6d6-105">В этом примере показано, как скрипт может быть использован для копирования файла в текстовое поле установщик Windows базы данных и демонстрирует обработку данных первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="4f6d6-106">В примере кода также показано следующее:</span><span class="sxs-lookup"><span data-stu-id="4f6d6-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="4f6d6-107">[**Метод опендатабасе (объект установщика)**](installer-opendatabase.md) и [**метод ластерроррекорд**](installer-lasterrorrecord.md) [**объекта установщика**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4f6d6-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="4f6d6-108">[**Метод OpenView**](database-openview.md), [**метод Commit**](database-commit.md)и [**свойство примарикэйс**](database-primarykeys.md) [**объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="4f6d6-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="4f6d6-109">[**Метод Fetch**](view-fetch.md) и [**метод Modify**](view-modify.md) [**объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="4f6d6-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="4f6d6-110">[**Свойство StringData**](record-stringdata.md) и [**метод реадстреам**](record-readstream.md) [**объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="4f6d6-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="4f6d6-111">Чтобы использовать пример кода, требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="4f6d6-112">**Использование CScript.exe для запуска этого примера**</span><span class="sxs-lookup"><span data-stu-id="4f6d6-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="4f6d6-113">В командной строке введите следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="4f6d6-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="4f6d6-114">**cscript WiTextIn.vbs \[ путь к \] \[ имени таблицы базы данных \] \[ значения первичного ключа имя \] \[ столбца \] \[ путь к файлу\]**</span><span class="sxs-lookup"><span data-stu-id="4f6d6-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="4f6d6-115">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="4f6d6-116">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="4f6d6-117">**Перенаправление выходных данных в файл**</span><span class="sxs-lookup"><span data-stu-id="4f6d6-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="4f6d6-118">Завершите командную строку следующим образом: **VBS > \[ путь к файлу \] . T**</span><span class="sxs-lookup"><span data-stu-id="4f6d6-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="4f6d6-119">Пример возвращает значение 0 (ноль) для успешного выполнения, 1 (один), если вызывается Справка, и 2 (два) в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="4f6d6-120">В следующем списке указаны элементы, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="4f6d6-121">Укажите путь к базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="4f6d6-122">Укажите имя таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="4f6d6-123">Укажите все значения первичного ключа для строки по порядку и объедините их с помощью двоеточий.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="4f6d6-124">Укажите имя столбца, который не является ключевым.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="4f6d6-125">Это столбец, данные которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="4f6d6-126">Укажите путь к копируемому текстовому файлу.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="4f6d6-127">Если последний аргумент пропущен, отображается текущее значение в поле.</span><span class="sxs-lookup"><span data-stu-id="4f6d6-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="4f6d6-128">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4f6d6-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="4f6d6-129">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4f6d6-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



