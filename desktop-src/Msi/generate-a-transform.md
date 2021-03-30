---
description: Файл WiGenXfm.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Этот пример скрипта может создать преобразование из двух установщик Windows баз данных. Дополнительные сведения см. в разделе преобразования баз данных.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Создание преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815216"
---
# <a name="generate-a-transform"></a><span data-ttu-id="aa9e2-105">Создание преобразования</span><span class="sxs-lookup"><span data-stu-id="aa9e2-105">Generate a Transform</span></span>

<span data-ttu-id="aa9e2-106">Файл WiGenXfm.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="aa9e2-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="aa9e2-107">Этот пример скрипта может создать преобразование из двух установщик Windows баз данных.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="aa9e2-108">Дополнительные сведения см. в разделе [преобразования баз данных](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="aa9e2-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="aa9e2-109">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="aa9e2-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="aa9e2-110">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="aa9e2-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="aa9e2-111">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="aa9e2-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="aa9e2-112">[**Метод GenerateTransform**](database-generatetransform.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="aa9e2-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="aa9e2-113">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="aa9e2-114">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="aa9e2-115">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="aa9e2-116">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-116">or if too few arguments are specified.</span></span> <span data-ttu-id="aa9e2-117">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="aa9e2-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="aa9e2-118">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="aa9e2-119">**cscript WiGenXfm.vbs \[ путь к исходному пути базы данных \] \[ к измененному пути базы данных \] \[ к файлу преобразования\]**</span><span class="sxs-lookup"><span data-stu-id="aa9e2-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="aa9e2-120">Укажите путь к исходной базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="aa9e2-121">Укажите путь к измененной базе данных.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-121">Specify the path to the revised database.</span></span> <span data-ttu-id="aa9e2-122">Укажите путь к создаваемому файлу преобразования.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="aa9e2-123">Если путь к файлу преобразования опущен, то сравниваются только две базы данных.</span><span class="sxs-lookup"><span data-stu-id="aa9e2-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="aa9e2-124">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="aa9e2-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="aa9e2-125">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="aa9e2-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="aa9e2-126">Обратите внимание, что [в примере локализации](a-localization-example.md) демонстрируется [Создание преобразования настройки](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="aa9e2-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



