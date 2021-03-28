---
description: Демонстрирует реализацию расширения пространства имен оболочки, включая поведение контекстного меню и пользовательские задачи в браузере.
title: 'Пример: поставщик данных в проводнике'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272326"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="7988c-103">Пример: поставщик данных в проводнике</span><span class="sxs-lookup"><span data-stu-id="7988c-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="7988c-104">Демонстрирует реализацию расширения пространства имен оболочки, включая поведение контекстного меню и пользовательские задачи в браузере.</span><span class="sxs-lookup"><span data-stu-id="7988c-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="7988c-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7988c-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7988c-106">Требования</span><span class="sxs-lookup"><span data-stu-id="7988c-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7988c-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7988c-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7988c-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="7988c-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7988c-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7988c-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="7988c-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7988c-110">Requirements</span></span>



| <span data-ttu-id="7988c-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="7988c-111">Product</span></span>                                | <span data-ttu-id="7988c-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="7988c-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="7988c-113">Windows</span><span class="sxs-lookup"><span data-stu-id="7988c-113">Windows</span></span>                                | <span data-ttu-id="7988c-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7988c-114">Windows Vista</span></span>           |
| <span data-ttu-id="7988c-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7988c-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="7988c-116">6.1</span><span class="sxs-lookup"><span data-stu-id="7988c-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7988c-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7988c-117">Downloading the Sample</span></span>

| <span data-ttu-id="7988c-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="7988c-118">Location</span></span>      | <span data-ttu-id="7988c-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="7988c-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7988c-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="7988c-120">GitHub</span></span>  | [<span data-ttu-id="7988c-121">Пример Експлорердатапровидер</span><span class="sxs-lookup"><span data-stu-id="7988c-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="7988c-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="7988c-122">Building the Sample</span></span>

<span data-ttu-id="7988c-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7988c-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="7988c-124">Откройте окно командной строки и перейдите в каталог проекта **експлорердатапровидер** .</span><span class="sxs-lookup"><span data-stu-id="7988c-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="7988c-125">Введите `msbuild ExplorerDataProvider.sln`.</span><span class="sxs-lookup"><span data-stu-id="7988c-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="7988c-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="7988c-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="7988c-127">Откройте проводник Windows и перейдите в каталог проекта **експлорердатапровидер** .</span><span class="sxs-lookup"><span data-stu-id="7988c-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="7988c-128">Дважды щелкните значок файла Експлорердатапровидер. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7988c-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="7988c-129">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="7988c-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="7988c-130">Библиотека DLL будет построена в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="7988c-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="7988c-131">В версии этого образца, включенной в Windows SDK, конфигурация для 64-разрядной сборки выпуска не включает файл Експлорердатапровидер. DEF в параметре **файла определения модуля** компоновщика.</span><span class="sxs-lookup"><span data-stu-id="7988c-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="7988c-132">Необходимо указать этот файл перед сборкой в 64-разрядной среде.</span><span class="sxs-lookup"><span data-stu-id="7988c-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="7988c-133">Добавьте строку `ModuleDefinitionFile="ExplorerDataProvider.def"` в раздел VCLinkerTool (начинается в строке 329) файла експлорердатапровидер. vcproj, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="7988c-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="7988c-134">Версия этого примера, загружаемая из коллекции кода, была исправлена для этой проблемы, и для вашей части не требуется никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="7988c-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="7988c-135">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7988c-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="7988c-136">Перейдите в каталог, содержащий новый файл. dll и. пропдеск, используя командную строку или проводник Windows.</span><span class="sxs-lookup"><span data-stu-id="7988c-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="7988c-137">В командной строке введите `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="7988c-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="7988c-138">Если выполнить эту команду из командной строки с повышенными привилегиями, при автоматической регистрации также будет автоматически зарегистрирован файл. пропдеск.</span><span class="sxs-lookup"><span data-stu-id="7988c-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="7988c-139">Если она выполняется из командной строки без повышенных привилегий, расширение пространства имен будет работать, но без функциональности настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="7988c-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="7988c-140">Откройте папку **Мой компьютер** и просмотрите новое расширение пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7988c-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


