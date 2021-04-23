---
title: Файлы МДМЕРЖЕ и Metadata
description: Объединяет несколько файлов метаданных (WinMD) в несколько выходных файлов метаданных на основе пространства имен.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- метаданные
- WINMD-файл
- Метаданные Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986209"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="cef36-106">Файлы МДМЕРЖЕ и Metadata</span><span class="sxs-lookup"><span data-stu-id="cef36-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="cef36-107">Объединяет несколько файлов метаданных (WinMD) в несколько выходных файлов метаданных на основе пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cef36-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="cef36-108">Использование</span><span class="sxs-lookup"><span data-stu-id="cef36-108">Usage</span></span>

<span data-ttu-id="cef36-109">Запустите МДМЕРЖЕ из командной строки с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="cef36-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="cef36-110"> *< ***Параметры*** мдмерже>*</span><span class="sxs-lookup"><span data-stu-id="cef36-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="cef36-111">где *<  параметры >* представляют параметры командной строки, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="cef36-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="cef36-112">Создайте файлы метаданных для пользовательских компонентов среда выполнения Windows с помощью компилятора MIDLRT.</span><span class="sxs-lookup"><span data-stu-id="cef36-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="cef36-113">Дополнительные сведения см. в разделе [компоненты MIDLRT и среда выполнения Windows](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="cef36-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="cef36-114">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="cef36-114">Command-line switches</span></span>

<span data-ttu-id="cef36-115">В следующем списке приведены параметры командной строки, используемые МДМЕРЖЕ.</span><span class="sxs-lookup"><span data-stu-id="cef36-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="cef36-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="cef36-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="cef36-117">**/Метадата \_ dir**</span><span class="sxs-lookup"><span data-stu-id="cef36-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="cef36-118">**параметра**</span><span class="sxs-lookup"><span data-stu-id="cef36-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="cef36-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="cef36-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="cef36-120">**/партиал**</span><span class="sxs-lookup"><span data-stu-id="cef36-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="cef36-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="cef36-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="cef36-122">Полный список переключателей и параметров компилятора МДМЕРЖЕ доступен при использовании параметра **-h** и **/?**</span><span class="sxs-lookup"><span data-stu-id="cef36-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="cef36-123">аргументы.</span><span class="sxs-lookup"><span data-stu-id="cef36-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef36-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cef36-124">Remarks</span></span>

<span data-ttu-id="cef36-125">Композиция метаданных позволяет нескольким IDL-файлам содержать определения для среда выполнения Windows компонентов в одном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="cef36-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="cef36-126">Это освобождает от определения всех типов в пространстве имен в одном IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="cef36-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="cef36-127">Скорее всего, у вас есть множество среда выполнения Windows компонентов, используемых приложениями.</span><span class="sxs-lookup"><span data-stu-id="cef36-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="cef36-128">При выполнении последнего шага для создания развертываемых среда выполнения Windows сборок метаданных можно настроить МДМЕРЖЕ для слияния компонентов из нескольких каталогов метаданных, таких как установленные вместе с системой (% WINDOWS% \\ system32 \\ винметадата), типы Foundation и каталог сборки текущего проекта.</span><span class="sxs-lookup"><span data-stu-id="cef36-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="cef36-129">Все необходимые типы объединяются в правильные, развертываемые сборки метаданных, которые можно упаковать для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="cef36-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="cef36-130">С помощью параметра [**/n**](-mdmerge-n.md) можно указать поддерживаемую глубину пространства имен для создания сборок метаданных.</span><span class="sxs-lookup"><span data-stu-id="cef36-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="cef36-131">Это позволяет настроить горячее разбиение для компонентов среда выполнения Windows, чтобы упаковано только один WINMD-файл, а не многие из них.</span><span class="sxs-lookup"><span data-stu-id="cef36-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="cef36-132">Это сокращает время загрузки и файловый ввод-вывод, необходимые для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="cef36-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cef36-133">См. также</span><span class="sxs-lookup"><span data-stu-id="cef36-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef36-134">Компоненты MIDLRT и среда выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="cef36-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




