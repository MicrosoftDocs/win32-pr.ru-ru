---
title: Поиск номеров потоков и выходных номеров
description: Поиск номеров потоков и выходных номеров
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Расширенный системный формат (ASF), Номера потоков
- ASF (Расширенный системный формат), создание чисел
- Расширенный формат систем (ASF), Поиск выходных номеров
- ASF (Расширенный системный формат), Поиск выходных номеров
- синхронные читатели, Номера потоков
- синхронные читатели, Поиск выходных номеров
- потоки, Поиск чисел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788737"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="407a8-110">Поиск номеров потоков и выходных номеров</span><span class="sxs-lookup"><span data-stu-id="407a8-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="407a8-111">Синхронный модуль чтения поддерживает более упрощенное переключение между потоком и выходными номерами для воспроизведения, чем асинхронный модуль чтения.</span><span class="sxs-lookup"><span data-stu-id="407a8-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="407a8-112">Поэтому важно иметь возможность определить, какие номера потоков эквивалентны выходным номерам или наоборот.</span><span class="sxs-lookup"><span data-stu-id="407a8-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="407a8-113">Чтобы найти номер выхода, соответствующий номеру потока, вызовите метод [**ивмсинкреадер:: жетаутпутнумберфорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="407a8-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="407a8-114">Чтобы найти номер потока, соответствующий выходному номеру, вызовите метод [ **ивмсинкреадер:: жетстреамнумберфораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="407a8-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="407a8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="407a8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="407a8-116">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="407a8-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="407a8-117">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="407a8-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="407a8-118">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="407a8-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




