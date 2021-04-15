---
title: Реализация обратного вызова OnSample
description: Реализация обратного вызова OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Расширенный системный формат (ASF), реализация обратного вызова OnStatus
- ASF (Расширенный системный формат), реализация обратного вызова OnStatus
- Расширенный формат систем (ASF), обратный вызов OnStatus
- ASF (Расширенный системный формат), обратный вызов OnStatus
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, реализация обратного вызова OnStatus
- Метод обратного вызова OnStatus, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336647"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="83d4b-111">Реализация обратного вызова OnSample</span><span class="sxs-lookup"><span data-stu-id="83d4b-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="83d4b-112">Асинхронный модуль чтения предоставляет образцы для управляющего приложения в порядке времени презентации, выполнив вызовы метода обратного вызова [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="83d4b-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="83d4b-113">При создании приложения с помощью асинхронного модуля чтения необходимо реализовать **OnSample** , чтобы работать с несжатыми примерами.</span><span class="sxs-lookup"><span data-stu-id="83d4b-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="83d4b-114">Обычно функции или методы, созданные для отрисовки содержимого, будут вызываться из **OnSample**.</span><span class="sxs-lookup"><span data-stu-id="83d4b-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="83d4b-115">Типичная реализация обратного вызова **OnSample** включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="83d4b-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="83d4b-116">Получите расположение и размер буфера, содержащего образец, вызвав [**инссбуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) в буфере, переданном как *псампле*.</span><span class="sxs-lookup"><span data-stu-id="83d4b-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="83d4b-117">Поветвление логики в зависимости от номера выхода.</span><span class="sxs-lookup"><span data-stu-id="83d4b-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="83d4b-118">Выходной номер передается в **OnSample** как *дваутпутнумбер*.</span><span class="sxs-lookup"><span data-stu-id="83d4b-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="83d4b-119">Включите логику отрисовки для каждого выходного номера, который требуется поддерживать.</span><span class="sxs-lookup"><span data-stu-id="83d4b-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="83d4b-120">При отрисовке образцов из нескольких выходов может потребоваться синхронизация отрисовки.</span><span class="sxs-lookup"><span data-stu-id="83d4b-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="83d4b-121">Приложения, которые доставляют сжатые образцы из файлов ASF, должны реализовывать метод обратного вызова [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="83d4b-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="83d4b-122">Функции **онстреамсампле** практически идентичны, за исключением **того, что** он получает сжатые образцы по номеру потока вместо несжатых выборок по номеру выхода.</span><span class="sxs-lookup"><span data-stu-id="83d4b-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83d4b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="83d4b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83d4b-124">**Интерфейс Ивмреадеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="83d4b-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="83d4b-125">**Интерфейс Ивмреадеркаллбаккадванцед**</span><span class="sxs-lookup"><span data-stu-id="83d4b-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="83d4b-126">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="83d4b-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="83d4b-127">**Использование методов обратного вызова**</span><span class="sxs-lookup"><span data-stu-id="83d4b-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




