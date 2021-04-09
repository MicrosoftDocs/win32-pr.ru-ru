---
description: Файл WiCompon.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Этот пример скрипта можно использовать для перечисления компонентов в базе данных установщик Windows.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Составить список компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809928"
---
# <a name="list-components"></a><span data-ttu-id="bd329-104">Составить список компонентов</span><span class="sxs-lookup"><span data-stu-id="bd329-104">List Components</span></span>

<span data-ttu-id="bd329-105">Файл WiCompon.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-105">The VBScript file WiCompon.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="bd329-106">Этот пример скрипта можно использовать для перечисления компонентов в базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bd329-106">This sample script can be used to list the components in a Windows Installer database.</span></span>

<span data-ttu-id="bd329-107">В этом примере демонстрируется использование различных первичных ключей в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-107">This sample demonstrates using the various primary key in the [Component table](component-table.md).</span></span>

<span data-ttu-id="bd329-108">В этом примере также демонстрируется:</span><span class="sxs-lookup"><span data-stu-id="bd329-108">The sample also demonstrates:</span></span>

-   <span data-ttu-id="bd329-109">Метод [**опендатабасе (объект установщика)**](installer-opendatabase.md), [**метод СоздатьЗапись**](installer-createrecord.md)и [**метод ластерроррекорд**](installer-lasterrorrecord.md) [**объекта установщика**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-109">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md).</span></span>
-   <span data-ttu-id="bd329-110">[**Метод OpenView**](database-openview.md), [**свойство Таблеперсистент**](database-tablepersistent.md)и [**свойство примарикэйс**](database-primarykeys.md) [**объекта Database**](database-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-110">[**OpenView method**](database-openview.md), the [**TablePersistent property**](database-tablepersistent.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md).</span></span>
-   <span data-ttu-id="bd329-111">[**Метод Execute**](view-execute.md) и [**метод Fetch**](view-fetch.md) [**объекта View**](view-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-111">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md).</span></span>
-   <span data-ttu-id="bd329-112">Свойство [**Свойства StringData**](record-stringdata.md) [**объекта Record**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-112">[**StringData property**](record-stringdata.md) property of the [**Record Object**](record-object.md).</span></span>

<span data-ttu-id="bd329-113">Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="bd329-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="bd329-114">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="bd329-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="bd329-115">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="bd329-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="bd329-116">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="bd329-116">or if too few arguments are specified.</span></span> <span data-ttu-id="bd329-117">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="bd329-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="bd329-118">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="bd329-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="bd329-119">**cscript WiCompon.vbs \[ путь к \] \[ имени компонента базы данных\]**</span><span class="sxs-lookup"><span data-stu-id="bd329-119">**cscript WiCompon.vbs \[path to database\]\[component name\]**</span></span>

<span data-ttu-id="bd329-120">Укажите путь к базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="bd329-120">Specify path to the Windows Installer database.</span></span> <span data-ttu-id="bd329-121">Укажите имя компонента.</span><span class="sxs-lookup"><span data-stu-id="bd329-121">Specify the name of the component.</span></span> <span data-ttu-id="bd329-122">Имя должно быть указано в столбце Component [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-122">The name must be listed in the Component column of the [Component table](component-table.md).</span></span> <span data-ttu-id="bd329-123">Если имя компонента пропущено, будут перечислены все компоненты.</span><span class="sxs-lookup"><span data-stu-id="bd329-123">If the name of the component is omitted all the components are listed.</span></span> <span data-ttu-id="bd329-124">Если в \* качестве имени компонента используется звездочка (), WiCompon.vbs отображает список всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="bd329-124">If an asterisk (\*) is used as the component name, WiCompon.vbs lists the composition of all components.</span></span> <span data-ttu-id="bd329-125">Обратите внимание, что большие базы данных лучше отображать с помощью CScript, а не WScript.</span><span class="sxs-lookup"><span data-stu-id="bd329-125">Note that large databases are better displayed using CScript rather than WScript.</span></span>

<span data-ttu-id="bd329-126">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-126">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="bd329-127">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bd329-127">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



