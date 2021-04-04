---
title: Средство Command-Line MkTypLib
description: MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов. Его также можно использовать для создания заголовочного файла C или C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794130"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="0aa9c-104">Средство Command-Line MkTypLib</span><span class="sxs-lookup"><span data-stu-id="0aa9c-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="0aa9c-105">\[Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="0aa9c-106">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="0aa9c-107">Если требуется обратная совместимость со старыми программами автоматизации, используйте компилятор MIDL с параметром **/mktyplib203** .\]</span><span class="sxs-lookup"><span data-stu-id="0aa9c-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="0aa9c-108">MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="0aa9c-109">Его также можно использовать для создания заголовочного файла C или C++.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="0aa9c-110">Создание библиотеки типов из ODL-файла:</span><span class="sxs-lookup"><span data-stu-id="0aa9c-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="0aa9c-111">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0aa9c-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="0aa9c-112">\**Мктиплибâ \* \* \* имя_файла*</span><span class="sxs-lookup"><span data-stu-id="0aa9c-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="0aa9c-113">где *filename*— имя ODL-файла.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="0aa9c-114">MkTypLib также поддерживает несколько необязательных параметров.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="0aa9c-115">Для выполнения полного списка выполните следующую командную строку:</span><span class="sxs-lookup"><span data-stu-id="0aa9c-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="0aa9c-116">**MkTypLib/?**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-116">**mktyplib /?**</span></span>

<span data-ttu-id="0aa9c-117">Поскольку MkTypLib является устаревшим приложением, он не может анализировать IDL-файлы или файлы с интерфейсами, определенными вне [**библиотечной**](/windows/desktop/Midl/library) инструкции.</span><span class="sxs-lookup"><span data-stu-id="0aa9c-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="0aa9c-118">Дополнительные сведения см. в разделе [различия между MIDL и MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="0aa9c-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa9c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0aa9c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa9c-120">Преобразование в C++</span><span class="sxs-lookup"><span data-stu-id="0aa9c-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 