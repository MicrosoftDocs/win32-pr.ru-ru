---
title: Завершение индексирования
description: Завершение индексирования
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Пакет SDK для Windows Media Format, остановка индексирования
- Расширенный системный формат (ASF), остановка индексирования
- ASF (Расширенный системный формат), остановка индексирования
- индексы, остановка индексирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069590"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="10f30-107">Завершение индексирования</span><span class="sxs-lookup"><span data-stu-id="10f30-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="10f30-108">После начала индексирования с помощью вызова [**ивминдексер:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)индексатор обычно будет продолжать работу до индексирования файла.</span><span class="sxs-lookup"><span data-stu-id="10f30-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="10f30-109">Можно остановить операции индексирования, вызвав метод [**ивминдексер:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) .</span><span class="sxs-lookup"><span data-stu-id="10f30-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="10f30-110">После отмены индексирования можно снова вызвать **startIndex** , но индексатор будет начинаться с начала файла, а не возобновляться с момента отмены.</span><span class="sxs-lookup"><span data-stu-id="10f30-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="10f30-111">Поскольку **startIndex** является асинхронным вызовом, обычно требуется вызвать метод **Cancel** из другого потока или обработчика событий в приложении.</span><span class="sxs-lookup"><span data-stu-id="10f30-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="10f30-112">Как правило, **Cancel** вызывается из процедуры события, связанной с элементом управления "Кнопка" приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="10f30-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="10f30-113">При отмене индексирования индексатор передает сообщение о состоянии ВМТ \_ Closed, как будто файл был правильно проиндексирован.</span><span class="sxs-lookup"><span data-stu-id="10f30-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10f30-114">См. также</span><span class="sxs-lookup"><span data-stu-id="10f30-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f30-115">**Интерфейс Ивминдексер**</span><span class="sxs-lookup"><span data-stu-id="10f30-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="10f30-116">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="10f30-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




