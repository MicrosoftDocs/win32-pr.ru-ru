---
description: Правильная настройка символов для отладки может быть сложной задачей, особенно для отладки ядра.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Сервер символов и хранилища символов"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262582"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="ffc25-103">  Сервер символов и хранилища символов</span><span class="sxs-lookup"><span data-stu-id="ffc25-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="ffc25-104">Правильная настройка символов для отладки может быть сложной задачей, особенно для отладки ядра.</span><span class="sxs-lookup"><span data-stu-id="ffc25-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="ffc25-105">Часто требуется знание имен и выпусков всех продуктов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ffc25-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="ffc25-106">Отладчик должен иметь возможность размещать файлы символов, соответствующие каждому выпуску продукта и пакету обновления.</span><span class="sxs-lookup"><span data-stu-id="ffc25-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="ffc25-107">Это может привести к созданию слишком длинного пути к символу, состоящего из длинного списка каталогов.</span><span class="sxs-lookup"><span data-stu-id="ffc25-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="ffc25-108">Для упрощения этих трудностей при координации файлов символов используйте *сервер символов*.</span><span class="sxs-lookup"><span data-stu-id="ffc25-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="ffc25-109">Сервер символов позволяет отладчикам автоматически получать правильные файлы символов без названий продуктов, выпусков или номеров сборки.</span><span class="sxs-lookup"><span data-stu-id="ffc25-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="ffc25-110">Средства отладки для Windows содержат сервер символов SymSrv.</span><span class="sxs-lookup"><span data-stu-id="ffc25-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="ffc25-111">Сервер символов активируется путем включения в путь к символам определенной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="ffc25-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="ffc25-112">Каждый раз, когда отладчику нужно загрузить символы для вновь загруженного модуля, он вызывает сервер символов для размещения соответствующих файлов символов.</span><span class="sxs-lookup"><span data-stu-id="ffc25-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="ffc25-113">Сервер символов находит файлы в *хранилище символов*.</span><span class="sxs-lookup"><span data-stu-id="ffc25-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="ffc25-114">Это коллекция файлов символов, индексов и средств, которые администратор может использовать для добавления и удаления файлов.</span><span class="sxs-lookup"><span data-stu-id="ffc25-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="ffc25-115">Файлы индексируются в соответствии с уникальными параметрами, такими как метка времени и размер изображения.</span><span class="sxs-lookup"><span data-stu-id="ffc25-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="ffc25-116">Средства отладки для Windows содержат инструмент для хранения символов с именем SymStore.</span><span class="sxs-lookup"><span data-stu-id="ffc25-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="ffc25-117">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="ffc25-117">For more information, see:</span></span>

-   [<span data-ttu-id="ffc25-118">Использование SymSrv</span><span class="sxs-lookup"><span data-stu-id="ffc25-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="ffc25-119">Использование SymStore</span><span class="sxs-lookup"><span data-stu-id="ffc25-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="ffc25-120">Использование других хранилищ символов</span><span class="sxs-lookup"><span data-stu-id="ffc25-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="ffc25-121">Параметры Command-Line SymStore</span><span class="sxs-lookup"><span data-stu-id="ffc25-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="ffc25-122">Сервер символов и брандмауэры Интернета</span><span class="sxs-lookup"><span data-stu-id="ffc25-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="ffc25-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ffc25-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffc25-124">Файлы символов</span><span class="sxs-lookup"><span data-stu-id="ffc25-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



