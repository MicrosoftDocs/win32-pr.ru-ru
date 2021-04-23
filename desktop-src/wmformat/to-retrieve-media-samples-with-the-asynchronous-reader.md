---
title: Получение примеров мультимедиа с помощью асинхронного модуля чтения
description: Получение примеров мультимедиа с помощью асинхронного модуля чтения
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Расширенный формат систем (ASF), получение примеров мультимедиа
- ASF (Расширенный системный формат), получение примеров мультимедиа
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, получение примеров мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069553"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="bdce1-108">Получение примеров мультимедиа с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="bdce1-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="bdce1-109">После получения \_ сообщения о состоянии Open ВМТ в реализации [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)можно начать получать примеры, вызвав [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span><span class="sxs-lookup"><span data-stu-id="bdce1-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="bdce1-110">Асинхронный читатель предоставляет примеры для реализации [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="bdce1-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="bdce1-111">Образцы предоставляются в порядке, определенном во время презентации.</span><span class="sxs-lookup"><span data-stu-id="bdce1-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="bdce1-112">**Start** — это асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="bdce1-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="bdce1-113">Он возвратит практически сразу и продолжит работу в отдельных потоках.</span><span class="sxs-lookup"><span data-stu-id="bdce1-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="bdce1-114">Асинхронный модуль чтения использует несколько потоков при декодировании содержимого и доставке образцов.</span><span class="sxs-lookup"><span data-stu-id="bdce1-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="bdce1-115">По достижении конца файла средство чтения отправляет \_ сообщение о состоянии ВМТ EOF в реализацию обратного вызова **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="bdce1-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="bdce1-116">При \_ отправке ВМТ EOF модуль чтения останавливает собственную обработку; вам не нужно отвечать на ВМТ \_ EOF с вызовом [**Ивмреадер:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span><span class="sxs-lookup"><span data-stu-id="bdce1-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdce1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="bdce1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdce1-118">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="bdce1-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="bdce1-119">**Реализация сообщений модуля чтения в обратном вызове OnStatus**</span><span class="sxs-lookup"><span data-stu-id="bdce1-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="bdce1-120">**Реализация обратного вызова OnSample**</span><span class="sxs-lookup"><span data-stu-id="bdce1-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




