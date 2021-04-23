---
description: Чтобы сэкономить время и память при работе с множеством файлов символов, используйте функцию Симсетоптионс, чтобы установить параметр отложенной загрузки символов (СИМОПТ \_ отложенных \_ загрузок).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Отложенная загрузка символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990323"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="692c1-103">Отложенная загрузка символов</span><span class="sxs-lookup"><span data-stu-id="692c1-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="692c1-104">Чтобы экономить время и память при работе с множеством файлов символов, используйте функцию [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) , чтобы установить параметр отложенной загрузки символов (симопт отложенных загрузок \_ \_ ), а затем используйте функцию [**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) или [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) для загрузки символов, отложенных для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="692c1-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="692c1-105">Обработчик символов будет отображать символы, доступные для модулей, но не будет сопоставлять отладочную информацию с памятью, пока не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="692c1-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="692c1-106">Это предпочтительный метод эффективного использования отладочных символов.</span><span class="sxs-lookup"><span data-stu-id="692c1-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="692c1-107">Для всех функций, использующих символы, зависят отложенная загрузка символов.</span><span class="sxs-lookup"><span data-stu-id="692c1-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 



