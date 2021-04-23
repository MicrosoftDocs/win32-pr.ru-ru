---
description: Файл WiLangID.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Управление языком и кодовой страницей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674308"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="553e6-103">Управление языком и кодовой страницей</span><span class="sxs-lookup"><span data-stu-id="553e6-103">Manage Language and Codepage</span></span>

<span data-ttu-id="553e6-104">Файл WiLangID.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="553e6-105">В этом примере показано, как использовать скрипт для доступа к сведениям о языке и кодовой странице пакета.</span><span class="sxs-lookup"><span data-stu-id="553e6-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="553e6-106">Дополнительные сведения см. [в разделе локализация пакета установщик Windows](localizing-a-windows-installer-package.md) и [Обработка кодовой страницы (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="553e6-107">В примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="553e6-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="553e6-108">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="553e6-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="553e6-109">**СоздатьЗапись, метод**</span><span class="sxs-lookup"><span data-stu-id="553e6-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="553e6-110">[**Метод ластерроррекорд**](installer-lasterrorrecord.md) [ **объекта Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="553e6-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="553e6-111">**Метод OpenView**</span><span class="sxs-lookup"><span data-stu-id="553e6-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="553e6-112">[**Свойство SummaryInformation (объект Database)**](database-summaryinformation.md) [ **объекта Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="553e6-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="553e6-113">Для использования этого примера требуется CScript.exe или WScript.exe версии сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="553e6-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="553e6-114">Чтобы использовать CScript.exe для запуска этого образца, введите команду в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="553e6-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="553e6-115">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="553e6-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="553e6-116">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="553e6-116">or if too few arguments are specified.</span></span> <span data-ttu-id="553e6-117">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ *путь к файлу* \] .</span><span class="sxs-lookup"><span data-stu-id="553e6-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="553e6-118">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="553e6-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="553e6-119">**cscript WiLangID.vbs \[ путь к \] \[ \] \[ значению ключевого слова базы данных\]**</span><span class="sxs-lookup"><span data-stu-id="553e6-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="553e6-120">Укажите путь к базе данных установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="553e6-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="553e6-121">Чтобы изменить значение, укажите одно из следующих ключевых слов, за которым следует новое значение.</span><span class="sxs-lookup"><span data-stu-id="553e6-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="553e6-122">Если значение не указано, пример возвращает текущее значение.</span><span class="sxs-lookup"><span data-stu-id="553e6-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="553e6-123">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="553e6-123">Keyword</span></span>      | <span data-ttu-id="553e6-124">Описание</span><span class="sxs-lookup"><span data-stu-id="553e6-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553e6-125">**Пакет**</span><span class="sxs-lookup"><span data-stu-id="553e6-125">**Package**</span></span>  | <span data-ttu-id="553e6-126">Версии языка, поддерживаемые базой данных.</span><span class="sxs-lookup"><span data-stu-id="553e6-126">The language versions supported by the database.</span></span> <span data-ttu-id="553e6-127">Дополнительные сведения см. в разделе свойство [**сводки шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="553e6-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="553e6-128">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="553e6-128">**Product**</span></span>  | <span data-ttu-id="553e6-129">Язык, который должен использоваться установщиком для любых строк в пользовательском интерфейсе, не созданных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="553e6-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="553e6-130">Дополнительные сведения см. в разделе свойство [**продуктлангуаже**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="553e6-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="553e6-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="553e6-131">**Codepage**</span></span> | <span data-ttu-id="553e6-132">Одна кодовая страница ANSI для пула строк.</span><span class="sxs-lookup"><span data-stu-id="553e6-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="553e6-133">Дополнительные сведения см. в разделе [Обработка кодовых страниц (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="553e6-134">Дополнительные примеры сценариев см. в разделе [установщик Windows примеры сценариев](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="553e6-135">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [средства разработки установщик Windows](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="553e6-136">Дополнительные сведения см. в разделе [Определение кодовой страницы базы данных установки](determining-an-installation-database-s-code-page.md) и [Задание кодовой страницы базы данных](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="553e6-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



