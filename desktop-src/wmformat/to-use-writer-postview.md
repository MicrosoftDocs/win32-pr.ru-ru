---
title: Использование записи для просмотра
description: Использование записи для просмотра
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Расширенный формат систем (ASF), просмотр записи
- ASF (Расширенный системный формат), пишущий Просмотр
- Расширенный формат систем (ASF), просмотр
- ASF (Расширенный системный формат), просмотр
- Просмотр для записи
- Просмотр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533053"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="237d5-109">Использование записи для просмотра</span><span class="sxs-lookup"><span data-stu-id="237d5-109">To Use Writer Postview</span></span>

<span data-ttu-id="237d5-110">Объект модуля записи предоставляет возможности просмотра, что позволяет проверять написание содержимого без необходимости настройки объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="237d5-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="237d5-111">Объект модуля записи не поддерживает просмотр аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="237d5-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="237d5-112">Модуль записи Writer работает во многом так же, как и асинхронный объект Reader, с меньшим числом функций.</span><span class="sxs-lookup"><span data-stu-id="237d5-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="237d5-113">Подробные сведения о чтении цифровых носителей см. в разделе [чтение файлов ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="237d5-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="237d5-114">Чтобы реализовать средство просмотра, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="237d5-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="237d5-115">Реализуйте обратный вызов [**ивмвритерпоствиевкаллбакк:: онпоствиевсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="237d5-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="237d5-116">Этот метод, по сути, аналогичен [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , за исключением того, что он указывает номера потоков вместо выходных данных.</span><span class="sxs-lookup"><span data-stu-id="237d5-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="237d5-117">Настройка для записи в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="237d5-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="237d5-118">Получите указатель на интерфейс [**ивмвритерпоствиев**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) объекта Writer, вызвав **Ивмвритер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="237d5-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="237d5-119">Задайте обратный вызов для проверяющего для использования с помощью вызова [**ивмвритерпоствиев:: сетпоствиевкаллбакк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span><span class="sxs-lookup"><span data-stu-id="237d5-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="237d5-120">Для каждого потока, для которого необходимо получить образцы просмотра, вызовите метод [**ивмвритерпоствиев:: сетрецеивепоствиевсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="237d5-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="237d5-121">Можно проверить, настроен ли поток на получение образцов просмотра с помощью вызова [**ивмвритерпоствиев:: жетрецеивепоствиевсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="237d5-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="237d5-122">Вы можете манипулировать образцами форматов, как в случае с выходными форматами в объекте Reader или синхронном объекте Reader.</span><span class="sxs-lookup"><span data-stu-id="237d5-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="237d5-123">Когда вы начинаете писать файл, вы начнете получать примеры в реализации метода обратного вызова **онпоствиевсампле** .</span><span class="sxs-lookup"><span data-stu-id="237d5-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="237d5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="237d5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="237d5-125">**Интерфейс Ивмвритерпоствиевкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="237d5-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="237d5-126">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="237d5-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




