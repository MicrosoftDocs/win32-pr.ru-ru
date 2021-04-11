---
title: Получение примеров Stream с помощью синхронного модуля чтения
description: Получение примеров Stream с помощью синхронного модуля чтения
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Расширенный системный формат (ASF), получение примеров потоков
- ASF (Расширенный системный формат), получение примеров потоков
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, получение примеров потоков
- потоки, получение примеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133487"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="5cbeb-109">Получение примеров Stream с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="5cbeb-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="5cbeb-110">Как и асинхронное средство чтения, синхронный читатель может получать выборки по номеру потока.</span><span class="sxs-lookup"><span data-stu-id="5cbeb-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="5cbeb-111">В отличие от асинхронного модуля чтения, синхронный читатель может доставлять образцы потоков как сжатые, так и несжатые.</span><span class="sxs-lookup"><span data-stu-id="5cbeb-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="5cbeb-112">Чтобы получить примеры потоков, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5cbeb-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="5cbeb-113">В любой момент до или во время воспроизведения вызовите [**ивмсинкреадер:: сетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) , передав нужный номер потока.</span><span class="sxs-lookup"><span data-stu-id="5cbeb-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="5cbeb-114">Получите примеры с продолжающимися вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="5cbeb-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="5cbeb-115">Вы можете проверить, выбран ли поток для выборки, вызвав [**ивмсинкреадер:: жетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span><span class="sxs-lookup"><span data-stu-id="5cbeb-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cbeb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5cbeb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbeb-117">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="5cbeb-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="5cbeb-118">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="5cbeb-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




