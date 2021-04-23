---
description: В следующих разделах описываются файлы символов и функции, предоставляемые функциями DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: О DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141150"
---
# <a name="about-dbghelp"></a><span data-ttu-id="7c859-103">О DbgHelp</span><span class="sxs-lookup"><span data-stu-id="7c859-103">About DbgHelp</span></span>

<span data-ttu-id="7c859-104">В следующих разделах описываются файлы символов и функции, предоставляемые [функциями DBGHELP](dbghelp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7c859-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="7c859-105">Версии DbgHelp</span><span class="sxs-lookup"><span data-stu-id="7c859-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="7c859-106">Файлы символов</span><span class="sxs-lookup"><span data-stu-id="7c859-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="7c859-107">Обработка символов</span><span class="sxs-lookup"><span data-stu-id="7c859-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="7c859-108">Серверы символов и хранилища символов</span><span class="sxs-lookup"><span data-stu-id="7c859-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="7c859-109">Файлы минидампа</span><span class="sxs-lookup"><span data-stu-id="7c859-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="7c859-110">Исходный сервер</span><span class="sxs-lookup"><span data-stu-id="7c859-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="7c859-111">Поддержка платформы обновлена</span><span class="sxs-lookup"><span data-stu-id="7c859-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="7c859-112">Обратите внимание, что все [функции DBGHELP](dbghelp-functions.md) являются отдельными потоками.</span><span class="sxs-lookup"><span data-stu-id="7c859-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="7c859-113">Таким образом, вызовы из более чем одного потока в эту функцию, скорее всего, приведут к непредвиденному поведению или повреждению памяти.</span><span class="sxs-lookup"><span data-stu-id="7c859-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="7c859-114">Чтобы избежать этого, необходимо синхронизировать все одновременные вызовы из более чем одного потока в эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7c859-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



