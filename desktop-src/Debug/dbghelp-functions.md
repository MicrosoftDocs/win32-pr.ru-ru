---
description: Ниже перечислены функции DbgHelp.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Функции DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db65e46fe407b26b1a6ec9ae3cb8d5d7301d5821
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539206"
---
# <a name="dbghelp-functions"></a><span data-ttu-id="2cc37-103">Функции DbgHelp</span><span class="sxs-lookup"><span data-stu-id="2cc37-103">DbgHelp Functions</span></span>

<span data-ttu-id="2cc37-104">Ниже перечислены функции DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="2cc37-104">The following are the DbgHelp functions.</span></span>

## <a name="general"></a><span data-ttu-id="2cc37-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2cc37-105">General</span></span>

<span data-ttu-id="2cc37-106">Ниже приведены общие вспомогательные функции.</span><span class="sxs-lookup"><span data-stu-id="2cc37-106">The following are general helper functions:</span></span>

<dl>

[<span data-ttu-id="2cc37-107">**енумдиртри**</span><span class="sxs-lookup"><span data-stu-id="2cc37-107">**EnumDirTree**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[<span data-ttu-id="2cc37-108">**имажехлпапиверсион**</span><span class="sxs-lookup"><span data-stu-id="2cc37-108">**ImagehlpApiVersion**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[<span data-ttu-id="2cc37-109">**имажехлпапиверсионекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-109">**ImagehlpApiVersionEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[<span data-ttu-id="2cc37-110">**макесуредиректорипасексистс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-110">**MakeSureDirectoryPathExists**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[<span data-ttu-id="2cc37-111">**сеарчтрифорфиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-111">**SearchTreeForFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a><span data-ttu-id="2cc37-112">Отладчик</span><span class="sxs-lookup"><span data-stu-id="2cc37-112">Debugger</span></span>

<span data-ttu-id="2cc37-113">Функции службы отладки являются функциями, наиболее подходящими для использования отладчиком или кодом отладки в приложении.</span><span class="sxs-lookup"><span data-stu-id="2cc37-113">The debugging service functions are the functions most suited for use by a debugger or the debugging code in an application.</span></span> <span data-ttu-id="2cc37-114">Эти функции можно использовать совместно с функциями обработчика символов для упрощения использования.</span><span class="sxs-lookup"><span data-stu-id="2cc37-114">These functions can be used in concert with the symbol handler functions for easier use.</span></span>

<dl>

[<span data-ttu-id="2cc37-115">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-115">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="2cc37-116">**енумерателоадедмодулесекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-116">**EnumerateLoadedModulesEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[<span data-ttu-id="2cc37-117">**финддебугинфофиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-117">**FindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[<span data-ttu-id="2cc37-118">**финддебугинфофиликс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-118">**FindDebugInfoFileEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[<span data-ttu-id="2cc37-119">**финдексекутаблеимаже**</span><span class="sxs-lookup"><span data-stu-id="2cc37-119">**FindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[<span data-ttu-id="2cc37-120">**финдексекутаблеимажеекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-120">**FindExecutableImageEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[<span data-ttu-id="2cc37-121">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-121">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="2cc37-122">**симсетпарентвиндов**</span><span class="sxs-lookup"><span data-stu-id="2cc37-122">**SymSetParentWindow**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[<span data-ttu-id="2cc37-123">**ундекоратесимболнаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-123">**UnDecorateSymbolName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a><span data-ttu-id="2cc37-124">Доступ к изображениям</span><span class="sxs-lookup"><span data-stu-id="2cc37-124">Image Access</span></span>

<span data-ttu-id="2cc37-125">Функции доступа к изображениям обращаются к данным в исполняемом образе.</span><span class="sxs-lookup"><span data-stu-id="2cc37-125">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="2cc37-126">Функции предоставляют высокоуровневый доступ к основам образов и очень специфичный доступ к наиболее распространенным частям данных изображения.</span><span class="sxs-lookup"><span data-stu-id="2cc37-126">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="2cc37-127">**жеттиместампфорлоадедлибрари**</span><span class="sxs-lookup"><span data-stu-id="2cc37-127">**GetTimestampForLoadedLibrary**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[<span data-ttu-id="2cc37-128">**Сбой imagedirectoryentrytodata.**</span><span class="sxs-lookup"><span data-stu-id="2cc37-128">**ImageDirectoryEntryToData**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[<span data-ttu-id="2cc37-129">**имажедиректорентритодатаекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-129">**ImageDirectoryEntryToDataEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[<span data-ttu-id="2cc37-130">**имаженсеадер**</span><span class="sxs-lookup"><span data-stu-id="2cc37-130">**ImageNtHeader**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[<span data-ttu-id="2cc37-131">**имажерватосектион**</span><span class="sxs-lookup"><span data-stu-id="2cc37-131">**ImageRvaToSection**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[<span data-ttu-id="2cc37-132">**имажерватова**</span><span class="sxs-lookup"><span data-stu-id="2cc37-132">**ImageRvaToVa**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a><span data-ttu-id="2cc37-133">Обработчик символов</span><span class="sxs-lookup"><span data-stu-id="2cc37-133">Symbol Handler</span></span>

<span data-ttu-id="2cc37-134">Функции [обработчика символов](symbol-handling.md) предоставляют приложениям простой и переносимый доступ к символической отладочной информации изображения.</span><span class="sxs-lookup"><span data-stu-id="2cc37-134">The [symbol handler](symbol-handling.md) functions give applications easy and portable access to the symbolic debugging information of an image.</span></span> <span data-ttu-id="2cc37-135">Эти функции следует использовать исключительно для обеспечения доступа к символьным данным.</span><span class="sxs-lookup"><span data-stu-id="2cc37-135">These functions should be used exclusively to ensure access to symbolic information.</span></span> <span data-ttu-id="2cc37-136">Это необходимо, так как эти функции изолируют приложение от формата символов.</span><span class="sxs-lookup"><span data-stu-id="2cc37-136">This is necessary because these functions isolate the application from the symbol format.</span></span>

<dl>

[<span data-ttu-id="2cc37-137">**симаддсаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="2cc37-137">**SymAddSourceStream**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[<span data-ttu-id="2cc37-138">**симаддсимбол**</span><span class="sxs-lookup"><span data-stu-id="2cc37-138">**SymAddSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[<span data-ttu-id="2cc37-139">**симклеануп**</span><span class="sxs-lookup"><span data-stu-id="2cc37-139">**SymCleanup**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[<span data-ttu-id="2cc37-140">**симделетесимбол**</span><span class="sxs-lookup"><span data-stu-id="2cc37-140">**SymDeleteSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[<span data-ttu-id="2cc37-141">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-141">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="2cc37-142">**сименумлинес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-142">**SymEnumLines**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[<span data-ttu-id="2cc37-143">**сименумпроцессес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-143">**SymEnumProcesses**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[<span data-ttu-id="2cc37-144">**сименумсаурцефилес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-144">**SymEnumSourceFiles**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[<span data-ttu-id="2cc37-145">**сименумсаурцелинес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-145">**SymEnumSourceLines**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[<span data-ttu-id="2cc37-146">**сименумсимболс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-146">**SymEnumSymbols**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[<span data-ttu-id="2cc37-147">**сименумсимболсфораддр**</span><span class="sxs-lookup"><span data-stu-id="2cc37-147">**SymEnumSymbolsForAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[<span data-ttu-id="2cc37-148">**сименумтипес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-148">**SymEnumTypes**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[<span data-ttu-id="2cc37-149">**сименумтипесбинаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-149">**SymEnumTypesByName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[<span data-ttu-id="2cc37-150">**симфинддебугинфофиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-150">**SymFindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[<span data-ttu-id="2cc37-151">**симфиндексекутаблеимаже**</span><span class="sxs-lookup"><span data-stu-id="2cc37-151">**SymFindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[<span data-ttu-id="2cc37-152">**симфиндфилеинпас**</span><span class="sxs-lookup"><span data-stu-id="2cc37-152">**SymFindFileInPath**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[<span data-ttu-id="2cc37-153">**симфромаддр**</span><span class="sxs-lookup"><span data-stu-id="2cc37-153">**SymFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[<span data-ttu-id="2cc37-154">**симфроминдекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-154">**SymFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[<span data-ttu-id="2cc37-155">**симфромнаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-155">**SymFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[<span data-ttu-id="2cc37-156">**симфромтокен**</span><span class="sxs-lookup"><span data-stu-id="2cc37-156">**SymFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[<span data-ttu-id="2cc37-157">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-157">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="2cc37-158">**SymGetFileLineOffsets64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-158">**SymGetFileLineOffsets64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[<span data-ttu-id="2cc37-159">**симжесомедиректори**</span><span class="sxs-lookup"><span data-stu-id="2cc37-159">**SymGetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[<span data-ttu-id="2cc37-160">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-160">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="2cc37-161">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-161">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="2cc37-162">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-162">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="2cc37-163">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-163">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="2cc37-164">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-164">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="2cc37-165">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-165">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="2cc37-166">**симжетомапс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-166">**SymGetOmaps**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[<span data-ttu-id="2cc37-167">**симжетоптионс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-167">**SymGetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[<span data-ttu-id="2cc37-168">**симжетскопе**</span><span class="sxs-lookup"><span data-stu-id="2cc37-168">**SymGetScope**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[<span data-ttu-id="2cc37-169">**симжетсеарчпас**</span><span class="sxs-lookup"><span data-stu-id="2cc37-169">**SymGetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[<span data-ttu-id="2cc37-170">**симжетсимболфиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-170">**SymGetSymbolFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[<span data-ttu-id="2cc37-171">**симжеттипефромнаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-171">**SymGetTypeFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[<span data-ttu-id="2cc37-172">**симжеттипеинфо**</span><span class="sxs-lookup"><span data-stu-id="2cc37-172">**SymGetTypeInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[<span data-ttu-id="2cc37-173">**симжеттипеинфоекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-173">**SymGetTypeInfoEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[<span data-ttu-id="2cc37-174">**симинитиализе**</span><span class="sxs-lookup"><span data-stu-id="2cc37-174">**SymInitialize**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[<span data-ttu-id="2cc37-175">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-175">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="2cc37-176">**симлоадмодуликс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-176">**SymLoadModuleEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[<span data-ttu-id="2cc37-177">**симматчфиленаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-177">**SymMatchFileName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[<span data-ttu-id="2cc37-178">**симматчстринг**</span><span class="sxs-lookup"><span data-stu-id="2cc37-178">**SymMatchString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[<span data-ttu-id="2cc37-179">**симнекст**</span><span class="sxs-lookup"><span data-stu-id="2cc37-179">**SymNext**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[<span data-ttu-id="2cc37-180">**симпрев**</span><span class="sxs-lookup"><span data-stu-id="2cc37-180">**SymPrev**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[<span data-ttu-id="2cc37-181">**симрефрешмодулелист**</span><span class="sxs-lookup"><span data-stu-id="2cc37-181">**SymRefreshModuleList**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[<span data-ttu-id="2cc37-182">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-182">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="2cc37-183">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-183">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="2cc37-184">**симсеарч**</span><span class="sxs-lookup"><span data-stu-id="2cc37-184">**SymSearch**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[<span data-ttu-id="2cc37-185">**симсетконтекст**</span><span class="sxs-lookup"><span data-stu-id="2cc37-185">**SymSetContext**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[<span data-ttu-id="2cc37-186">**симсесомедиректори**</span><span class="sxs-lookup"><span data-stu-id="2cc37-186">**SymSetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[<span data-ttu-id="2cc37-187">**симсетоптионс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-187">**SymSetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[<span data-ttu-id="2cc37-188">**симсетскопефромаддр**</span><span class="sxs-lookup"><span data-stu-id="2cc37-188">**SymSetScopeFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[<span data-ttu-id="2cc37-189">**симсетскопефроминдекс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-189">**SymSetScopeFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[<span data-ttu-id="2cc37-190">**симсетсеарчпас**</span><span class="sxs-lookup"><span data-stu-id="2cc37-190">**SymSetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[<span data-ttu-id="2cc37-191">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-191">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="2cc37-192">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-192">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a><span data-ttu-id="2cc37-193">Сервер символов</span><span class="sxs-lookup"><span data-stu-id="2cc37-193">Symbol Server</span></span>

<span data-ttu-id="2cc37-194">[Сервер символов](symbol-servers-and-symbol-stores.md) позволяет отладчикам автоматически получать правильные файлы символов без названий продуктов, выпусков или номеров сборки.</span><span class="sxs-lookup"><span data-stu-id="2cc37-194">The [symbol server](symbol-servers-and-symbol-stores.md) enables debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="2cc37-195">На сервере символов используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="2cc37-195">The following functions are used with the symbol server.</span></span>

<dl>

[<span data-ttu-id="2cc37-196">**симсрвделтанаме**</span><span class="sxs-lookup"><span data-stu-id="2cc37-196">**SymSrvDeltaName**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[<span data-ttu-id="2cc37-197">**симсрвжетфилеиндексес**</span><span class="sxs-lookup"><span data-stu-id="2cc37-197">**SymSrvGetFileIndexes**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[<span data-ttu-id="2cc37-198">**симсрвжетфилеиндексинфо**</span><span class="sxs-lookup"><span data-stu-id="2cc37-198">**SymSrvGetFileIndexInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[<span data-ttu-id="2cc37-199">**симсрвжетфилеиндексстринг**</span><span class="sxs-lookup"><span data-stu-id="2cc37-199">**SymSrvGetFileIndexString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[<span data-ttu-id="2cc37-200">**симсрвжетсупплемент**</span><span class="sxs-lookup"><span data-stu-id="2cc37-200">**SymSrvGetSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[<span data-ttu-id="2cc37-201">**симсрвиссторе**</span><span class="sxs-lookup"><span data-stu-id="2cc37-201">**SymSrvIsStore**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[<span data-ttu-id="2cc37-202">**симсрвсторефиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-202">**SymSrvStoreFile**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[<span data-ttu-id="2cc37-203">**симсрвсторесупплемент**</span><span class="sxs-lookup"><span data-stu-id="2cc37-203">**SymSrvStoreSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a><span data-ttu-id="2cc37-204">Файлы минидампа пользовательского режима</span><span class="sxs-lookup"><span data-stu-id="2cc37-204">User-mode Minidump Files</span></span>

<span data-ttu-id="2cc37-205">Функции минидампа предоставляют приложениям возможность создавать файлы аварийного дампа, содержащие полезные подмножества всего контекста процесса; Это называется [файлом минидампа](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="2cc37-205">The minidump functions provide a way for applications to produce crashdump files that contain a useful subset of the entire process context; this is known as a [minidump file](minidump-files.md).</span></span> <span data-ttu-id="2cc37-206">Для файлов минидампа используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="2cc37-206">The following functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="2cc37-207">**минидумпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="2cc37-207">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="2cc37-208">**минидумпреаддумпстреам**</span><span class="sxs-lookup"><span data-stu-id="2cc37-208">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="2cc37-209">**минидумпвритедумп**</span><span class="sxs-lookup"><span data-stu-id="2cc37-209">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a><span data-ttu-id="2cc37-210">Исходный сервер</span><span class="sxs-lookup"><span data-stu-id="2cc37-210">Source Server</span></span>

<span data-ttu-id="2cc37-211">[Сервер-источник](source-server-and-source-indexing.md) позволяет клиенту получить точную версию исходных файлов, которые использовались для построения приложения.</span><span class="sxs-lookup"><span data-stu-id="2cc37-211">[Source server](source-server-and-source-indexing.md) enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="2cc37-212">На исходном сервере используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="2cc37-212">The following functions are used with source server.</span></span>

-   [<span data-ttu-id="2cc37-213">**симжетсаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="2cc37-213">**SymGetSourceFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [<span data-ttu-id="2cc37-214">**сименумсаурцефилетокенс**</span><span class="sxs-lookup"><span data-stu-id="2cc37-214">**SymEnumSourceFileTokens**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [<span data-ttu-id="2cc37-215">**сименумсаурцефилетокенспрок**</span><span class="sxs-lookup"><span data-stu-id="2cc37-215">**SymEnumSourceFileTokensProc**</span></span>](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [<span data-ttu-id="2cc37-216">**симжетсаурцефилефромтокен**</span><span class="sxs-lookup"><span data-stu-id="2cc37-216">**SymGetSourceFileFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [<span data-ttu-id="2cc37-217">**симжетсаурцефилетокен**</span><span class="sxs-lookup"><span data-stu-id="2cc37-217">**SymGetSourceFileToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [<span data-ttu-id="2cc37-218">**симжетсаурцеварфромтокен**</span><span class="sxs-lookup"><span data-stu-id="2cc37-218">**SymGetSourceVarFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a><span data-ttu-id="2cc37-219">Устаревшие функции</span><span class="sxs-lookup"><span data-stu-id="2cc37-219">Obsolete Functions</span></span>

<dl>

[<span data-ttu-id="2cc37-220">**мапдебугинформатион**</span><span class="sxs-lookup"><span data-stu-id="2cc37-220">**MapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[<span data-ttu-id="2cc37-221">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-221">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="2cc37-222">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-222">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="2cc37-223">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-223">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="2cc37-224">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-224">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="2cc37-225">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="2cc37-225">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="2cc37-226">**унмапдебугинформатион**</span><span class="sxs-lookup"><span data-stu-id="2cc37-226">**UnMapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



