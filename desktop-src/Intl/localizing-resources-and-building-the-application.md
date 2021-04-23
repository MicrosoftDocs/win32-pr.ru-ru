---
description: В этом разделе описывается создание стандартного приложения MUI.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Локализация ресурсов и сборка приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683002"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="1686d-103">Локализация ресурсов и сборка приложения</span><span class="sxs-lookup"><span data-stu-id="1686d-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="1686d-104">В этом разделе описывается создание стандартного приложения MUI.</span><span class="sxs-lookup"><span data-stu-id="1686d-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="1686d-105">Предполагается, что вы используете Microsoft Visual Studio для написания кода и Microsoft Visual Studio или командную строку Visual Studio для сборки.</span><span class="sxs-lookup"><span data-stu-id="1686d-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="1686d-106">Предполагается использование файла решения. sln для приложения и поддержка файла resource. h для отражения файла ресурсов базового языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="1686d-107">При использовании командной строки Visual Studio для сборки вы будете использовать команду **VCBuild** для сборки файла решения.</span><span class="sxs-lookup"><span data-stu-id="1686d-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="1686d-108">Файлы приложения создаются отдельно для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-108">Application files are built separately for each language.</span></span> <span data-ttu-id="1686d-109">Каждая сборка создает идентичные, не зависящие от языка exe-файлы и языки MUI.</span><span class="sxs-lookup"><span data-stu-id="1686d-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="1686d-110">Кроме того, разные файлы копируются в соответствующие папки выпуска.</span><span class="sxs-lookup"><span data-stu-id="1686d-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="1686d-111">Сборка приложения зависит от типа ресурсов и типа локализации, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="1686d-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="1686d-112">Для локализации перед сборкой имеется одна копия файла базового языка, локализованная для каждого поддерживаемого языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="1686d-113">Для локализации после сборки можно скопировать MUI-файл, полученный в результате сборки исполняемого файла и модуля ресурсов, и предоставить эти копии локализаторам.</span><span class="sxs-lookup"><span data-stu-id="1686d-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="1686d-114">В следующей процедуре предполагается, что ресурсы Win32 PE с одним проектом Visual Studio созданы для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="1686d-115">Базовые языковые ресурсы предоставляются в RC-файле и загружаются с помощью модуля DLL.</span><span class="sxs-lookup"><span data-stu-id="1686d-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="1686d-116">Процедуру можно повторить по мере необходимости для сборки для всех поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="1686d-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="1686d-117">**Построение приложения**</span><span class="sxs-lookup"><span data-stu-id="1686d-117">**To build the application**</span></span>

1.  <span data-ttu-id="1686d-118">Настройте проект Visual Studio для базового языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="1686d-119">Если вы заинтересованы в использовании файла конфигурации ресурсов с инструментами ресурсов, настройте его, как описано в разделе [Подготовка файла конфигурации ресурсов](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="1686d-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="1686d-120">Задайте параметры, необходимые служебной программе компилятора RC, на страницах свойств проекта в разделе **Свойства конфигурации > ресурсы > Командная строка → дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="1686d-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="1686d-121">Запустите компилятор RC.</span><span class="sxs-lookup"><span data-stu-id="1686d-121">Run RC Compiler.</span></span> <span data-ttu-id="1686d-122">Программа компилирует и разделяет нелокализованные и локализуемые ресурсы в два разных объектных файла, используя данные конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1686d-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="1686d-123">На этом шаге ресурсы, независимые от языка, связаны с LN-файлом.</span><span class="sxs-lookup"><span data-stu-id="1686d-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="1686d-124">Дополнительные сведения см. в описании служебной программы в разделе [Служебные программы](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="1686d-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="1686d-125">Чтобы связать ресурсы, относящиеся к конкретному языку, в файл MUI конкретного языка, задайте событие после сборки для проекта на страницах свойств в разделе **Свойства конфигурации > события построения → после сборки событие → Командная строка**.</span><span class="sxs-lookup"><span data-stu-id="1686d-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="1686d-126">Задайте событие после сборки, чтобы применить значение контрольной суммы из LN-файла к MUI-файлу для языка.</span><span class="sxs-lookup"><span data-stu-id="1686d-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="1686d-127">Для этого шага можно использовать служебную программу МУИРКТ.</span><span class="sxs-lookup"><span data-stu-id="1686d-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="1686d-128">Дополнительные сведения см. в описании служебной программы в разделе [Служебные программы](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="1686d-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="1686d-129">Используйте командную строку события после сборки, чтобы добавить команды для копирования файлов в соответствующую структуру папок выпуска.</span><span class="sxs-lookup"><span data-stu-id="1686d-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1686d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1686d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1686d-131">Использование многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="1686d-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="1686d-132">Подготовка файла конфигурации ресурса</span><span class="sxs-lookup"><span data-stu-id="1686d-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="1686d-133">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="1686d-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



