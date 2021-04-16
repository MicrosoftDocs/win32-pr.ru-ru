---
description: Файл WiDialog.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере показано, как использовать скрипт для предварительного просмотра диалоговых окон в установщик Windows базе данных.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Предварительный просмотр пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650854"
---
# <a name="preview-user-interface"></a><span data-ttu-id="967aa-104">Предварительный просмотр пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="967aa-104">Preview User Interface</span></span>

<span data-ttu-id="967aa-105">Файл WiDialog.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="967aa-105">The VBScript file WiDialog.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="967aa-106">В этом примере показано, как использовать скрипт для предварительного просмотра диалоговых окон в установщик Windows базе данных.</span><span class="sxs-lookup"><span data-stu-id="967aa-106">This sample shows how script is used to preview dialogs in a Windows Installer database.</span></span>

<span data-ttu-id="967aa-107">В этом примере демонстрируются следующее:</span><span class="sxs-lookup"><span data-stu-id="967aa-107">This sample demonstrates:</span></span>

-   <span data-ttu-id="967aa-108">[**Метод опендатабасе (объект установщика)**](installer-opendatabase.md), [**метод СоздатьЗапись**](installer-createrecord.md)и [**метод ластерроррекорд**](installer-lasterrorrecord.md) [**объекта установщика**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="967aa-108">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="967aa-109">[**Метод OpenView**](database-openview.md) и [**метод енаблеуипревиев**](database-enableuipreview.md) [**объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="967aa-109">[**OpenView method**](database-openview.md) and the [**EnableUIpreview method**](database-enableuipreview.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="967aa-110">[**Метод Execute**](view-execute.md) и [**метод Fetch**](view-fetch.md) [**объекта View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="967aa-110">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="967aa-111">[**Свойство StringData**](record-stringdata.md) Пропертйоф [ **объекта Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="967aa-111">[**StringData property**](record-stringdata.md) propertyof the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="967aa-112">Для работы с этим образцом требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="967aa-112">This sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="967aa-113">Чтобы использовать CScript.exe для этого примера, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="967aa-113">To use CScript.exe for this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="967aa-114">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="967aa-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="967aa-115">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="967aa-115">or if too few arguments are specified.</span></span> <span data-ttu-id="967aa-116">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="967aa-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="967aa-117">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="967aa-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="967aa-118">**cscript WiDialog.vbs** *\[ путь к \] \[ именам \] диалоговых окон базы данных*</span><span class="sxs-lookup"><span data-stu-id="967aa-118">**cscript WiDialog.vbs** *\[path to database\]\[Dialog names\]*</span></span>

<span data-ttu-id="967aa-119">Укажите путь к установщик Windows базе данных.</span><span class="sxs-lookup"><span data-stu-id="967aa-119">Specify the path to a Windows Installer database.</span></span> <span data-ttu-id="967aa-120">Укажите имя диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="967aa-120">Specify the name of a dialog.</span></span> <span data-ttu-id="967aa-121">Это имя должно быть указано в столбце диалоговых окон [таблицы диалоговых](dialog-table.md)окон.</span><span class="sxs-lookup"><span data-stu-id="967aa-121">This name must be listed in the Dialog column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="967aa-122">Чтобы просмотреть объявление, добавьте имя диалогового окна в имя элемента управления из [таблицы управления](control-table.md) и добавьте его к имени объявления в [таблице объявлений](billboard-table.md).</span><span class="sxs-lookup"><span data-stu-id="967aa-122">To view a billboard, append the dialog's name with the control's name from the [Control table](control-table.md) and append this to the name of the billboard in the [Billboard table](billboard-table.md).</span></span> <span data-ttu-id="967aa-123">Если диалоговые окна не указаны, последовательно отображаются все диалоговые окна в диалоговой таблице.</span><span class="sxs-lookup"><span data-stu-id="967aa-123">If no dialogs are specified, all dialogs in Dialog table are displayed sequentially.</span></span>

<span data-ttu-id="967aa-124">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="967aa-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="967aa-125">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="967aa-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



