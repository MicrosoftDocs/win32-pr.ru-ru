---
title: Компоненты MIDLRT и среда выполнения Windows
description: Показывает, как создать файлы метаданных (WinMD), представляющие API для пользовательских компонентов среда выполнения Windows.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL компилятора MIDL
- MIDL компилятора MIDL, MIDL и среда выполнения Windows WinRT
- среда выполнения Windows MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533602"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="840f7-106">Компоненты MIDLRT и среда выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="840f7-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="840f7-107">Показывает, как создать файлы метаданных (WinMD), представляющие API для пользовательских компонентов среда выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="840f7-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="840f7-108">Используйте компилятор MIDLRT для создания файлов метаданных (WinMD) для пользовательских компонентов среда выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="840f7-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="840f7-109">При создании файлов метаданных их можно составить в более эффективный пакет с помощью служебной программы МДМЕРЖЕ.</span><span class="sxs-lookup"><span data-stu-id="840f7-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="840f7-110">Дополнительные сведения см. в разделе [мдмерже и файлы метаданных](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="840f7-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="840f7-111">Использование MIDLRT аналогично использованию компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="840f7-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="840f7-112">Запустите MIDLRT из командной строки с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="840f7-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="840f7-113">**midlrt**  *<* **Параметры** _>_ **filename. idl**</span><span class="sxs-lookup"><span data-stu-id="840f7-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="840f7-114">Здесь **Параметры** \* < \* _>_ представляют параметры командной строки, которые необходимо использовать, а filename. IDL — имя IDL-файла для компиляции.</span><span class="sxs-lookup"><span data-stu-id="840f7-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="840f7-115">В следующем списке приведены параметры командной строки, которые MIDLRT.EXE использует.</span><span class="sxs-lookup"><span data-stu-id="840f7-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="840f7-116">**\_класс/енум**</span><span class="sxs-lookup"><span data-stu-id="840f7-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="840f7-117">**/Метадата \_ dir**</span><span class="sxs-lookup"><span data-stu-id="840f7-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="840f7-118">**/номидл**</span><span class="sxs-lookup"><span data-stu-id="840f7-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="840f7-119">**/номд**</span><span class="sxs-lookup"><span data-stu-id="840f7-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="840f7-120">**\_префикс/НС**</span><span class="sxs-lookup"><span data-stu-id="840f7-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="840f7-121">**/WinMD**</span><span class="sxs-lookup"><span data-stu-id="840f7-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="840f7-122">**/WinRT**</span><span class="sxs-lookup"><span data-stu-id="840f7-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="840f7-123">Полный список ключей и параметров компилятора MIDLRT доступен при использовании компилятора MIDLRT [**/Help**](-help-.md) и/?</span><span class="sxs-lookup"><span data-stu-id="840f7-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="840f7-124">аргументы.</span><span class="sxs-lookup"><span data-stu-id="840f7-124">switches.</span></span> <span data-ttu-id="840f7-125">Параметры упорядочены по категориям.</span><span class="sxs-lookup"><span data-stu-id="840f7-125">The switches are organized by categories.</span></span> <span data-ttu-id="840f7-126">Дополнительные сведения см. в [справочнике по языку MIDL Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="840f7-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="840f7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="840f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="840f7-128">Файлы МДМЕРЖЕ и Metadata</span><span class="sxs-lookup"><span data-stu-id="840f7-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




