---
description: Ниже перечислены функции DbgHelp.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Функции DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8afacd44409004034ed727920c98487a0e2e34ad03e7af4ef5a2e5e13ab5303c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912774"
---
# <a name="dbghelp-functions"></a>Функции DbgHelp

Ниже перечислены функции DbgHelp.

## <a name="general"></a>Общие сведения

Ниже приведены общие вспомогательные функции.

<dl>

[**енумдиртри**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[**имажехлпапиверсион**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[**имажехлпапиверсионекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[**макесуредиректорипасексистс**](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[**сеарчтрифорфиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a>Отладчик

Функции службы отладки являются функциями, наиболее подходящими для использования отладчиком или кодом отладки в приложении. Эти функции можно использовать совместно с функциями обработчика символов для упрощения использования.

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**енумерателоадедмодулесекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[**финддебугинфофиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[**финддебугинфофиликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[**финдексекутаблеимаже**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[**финдексекутаблеимажеекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**симсетпарентвиндов**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[**ундекоратесимболнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a>Доступ к изображениям

Функции доступа к изображениям обращаются к данным в исполняемом образе. Функции предоставляют высокоуровневый доступ к основам образов и очень специфичный доступ к наиболее распространенным частям данных изображения.

<dl>

[**жеттиместампфорлоадедлибрари**](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[**Сбой imagedirectoryentrytodata.**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[**имажедиректорентритодатаекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[**имаженсеадер**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[**имажерватосектион**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[**имажерватова**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a>Обработчик символов

Функции [обработчика символов](symbol-handling.md) предоставляют приложениям простой и переносимый доступ к символической отладочной информации изображения. Эти функции следует использовать исключительно для обеспечения доступа к символьным данным. Это необходимо, так как эти функции изолируют приложение от формата символов.

<dl>

[**симаддсаурцестреам**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[**симаддсимбол**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[**симделетесимбол**](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**сименумлинес**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[**сименумпроцессес**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[**сименумсаурцефилес**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[**сименумсаурцелинес**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[**сименумсимболс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[**сименумсимболсфораддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[**сименумтипес**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[**сименумтипесбинаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[**симфинддебугинфофиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[**симфиндексекутаблеимаже**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[**симфиндфилеинпас**](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[**симфромаддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[**симфроминдекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[**симфромнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[**симфромтокен**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetFileLineOffsets64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[**симжесомедиректори**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**симжетомапс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[**симжетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[**симжетскопе**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[**симжетсеарчпас**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[**симжетсимболфиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[**симжеттипефромнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[**симжеттипеинфо**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[**симжеттипеинфоекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[**симматчфиленаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[**симматчстринг**](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[**симнекст**](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[**симпрев**](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[**симрефрешмодулелист**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**симсеарч**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[**симсетконтекст**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[**симсесомедиректори**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[**симсетскопефромаддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[**симсетскопефроминдекс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[**симсетсеарчпас**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a>Сервер символов

[Сервер символов](symbol-servers-and-symbol-stores.md) позволяет отладчикам автоматически получать правильные файлы символов без названий продуктов, выпусков или номеров сборки. На сервере символов используются следующие функции.

<dl>

[**симсрвделтанаме**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[**симсрвжетфилеиндексес**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[**симсрвжетфилеиндексинфо**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[**симсрвжетфилеиндексстринг**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[**симсрвжетсупплемент**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[**симсрвиссторе**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[**симсрвсторефиле**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[**симсрвсторесупплемент**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a>Файлы минидампа пользовательского режима

Функции минидампа предоставляют приложениям возможность создавать файлы аварийного дампа, содержащие полезные подмножества всего контекста процесса; Это называется [файлом минидампа](minidump-files.md). Для файлов минидампа используются следующие функции.

<dl>

[**минидумпкаллбакк**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**минидумпреаддумпстреам**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a>Исходный сервер

[Сервер-источник](source-server-and-source-indexing.md) позволяет клиенту получить точную версию исходных файлов, которые использовались для построения приложения. На исходном сервере используются следующие функции.

-   [**симжетсаурцефиле**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [**сименумсаурцефилетокенс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [**сименумсаурцефилетокенспрок**](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [**симжетсаурцефилефромтокен**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [**симжетсаурцефилетокен**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [**симжетсаурцеварфромтокен**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a>Устаревшие функции

<dl>

[**мапдебугинформатион**](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**унмапдебугинформатион**](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



