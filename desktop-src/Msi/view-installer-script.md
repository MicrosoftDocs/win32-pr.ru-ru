---
description: Файл WiLstScr.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. В этом примере скрипта демонстрируется средство просмотра скриптов установщик Windows.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Просмотреть скрипт установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673427"
---
# <a name="view-installer-script"></a><span data-ttu-id="dc2d6-104">Просмотреть скрипт установщика</span><span class="sxs-lookup"><span data-stu-id="dc2d6-104">View Installer Script</span></span>

<span data-ttu-id="dc2d6-105">Файл WiLstScr.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="dc2d6-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="dc2d6-106">В этом примере скрипта демонстрируется средство просмотра скриптов установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="dc2d6-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="dc2d6-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="dc2d6-108">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="dc2d6-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="dc2d6-109">Метод [**ластерроррекорд**](installer-lasterrorrecord.md) объекта [**Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="dc2d6-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="dc2d6-110">Метод [**OpenView**](database-openview.md) объекта [**Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="dc2d6-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="dc2d6-111">Метод [**Fetch**](view-fetch.md) объекта [**View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="dc2d6-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="dc2d6-112">Метод [**форматтекст**](record-formattext.md)</span><span class="sxs-lookup"><span data-stu-id="dc2d6-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="dc2d6-113">[**FieldCount**](record-fieldcount.md) , свойство</span><span class="sxs-lookup"><span data-stu-id="dc2d6-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="dc2d6-114">Свойство [**StringData**](record-stringdata.md) объекта [**Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="dc2d6-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="dc2d6-115">\_Таблица переformview</span><span class="sxs-lookup"><span data-stu-id="dc2d6-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="dc2d6-116">Для использования этого примера требуется CScript.exe версия сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="dc2d6-117">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="dc2d6-118">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="dc2d6-119">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-119">or if too few arguments are specified.</span></span> <span data-ttu-id="dc2d6-120">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="dc2d6-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="dc2d6-121">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="dc2d6-122">**cscript WiLstScr.vbs** *\[ путь к установщик Windows скрипту \] выполнения*</span><span class="sxs-lookup"><span data-stu-id="dc2d6-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="dc2d6-123">Укажите путь к скрипту выполнения установщика.</span><span class="sxs-lookup"><span data-stu-id="dc2d6-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="dc2d6-124">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="dc2d6-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="dc2d6-125">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dc2d6-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



