---
title: Получение сообщений об ошибках из приемника
description: Получение сообщений об ошибках из приемника
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Расширенный формат систем (ASF), сообщения об ошибках из приемников
- ASF (Расширенный системный формат), сообщения об ошибках из приемников
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, сообщения об ошибках
- сообщения об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133499"
---
# <a name="getting-error-messages-from-a-sink"></a><span data-ttu-id="b00f9-109">Получение сообщений об ошибках из приемника</span><span class="sxs-lookup"><span data-stu-id="b00f9-109">Getting Error Messages from a Sink</span></span>

<span data-ttu-id="b00f9-110">Объект модуля записи не отправляет сообщения в метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="b00f9-110">The writer object does not send messages to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="b00f9-111">Однако можно настроить приемники записи для отправки сообщений в OnStatus.</span><span class="sxs-lookup"><span data-stu-id="b00f9-111">However, you can set writer sinks to send messages to OnStatus.</span></span> <span data-ttu-id="b00f9-112">Каждый приемник должен быть настроен для доставки состояния отдельно, но все приемники могут передавать данные в один и тот же обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="b00f9-112">Each sink must be set to deliver status separately, but all sinks can report to the same callback.</span></span>

<span data-ttu-id="b00f9-113">Чтобы настроить приемник для доставки сообщений о состоянии в **OnStatus**, вызовите метод [**Ивмрегистеркаллбакк:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .</span><span class="sxs-lookup"><span data-stu-id="b00f9-113">To set a sink to deliver status messages to **OnStatus**, call the [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) method.</span></span>

<span data-ttu-id="b00f9-114">В следующем примере кода показано, как настроить все приемники для доставки сообщений о состоянии обратному вызову **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="b00f9-114">The following example code demonstrates how to set all of the sinks to deliver status messages to an **OnStatus** callback.</span></span> <span data-ttu-id="b00f9-115">В этом примере индекс каждого приемника будет использоваться в качестве параметра контекста, чтобы метод **OnStatus** мог отличать сообщения от разных приемников.</span><span class="sxs-lookup"><span data-stu-id="b00f9-115">In this example, the index of each sink will be used as the context parameter so that the **OnStatus** method can differentiate between messages from the different sinks.</span></span> <span data-ttu-id="b00f9-116">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b00f9-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="b00f9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b00f9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b00f9-118">**Интерфейс Ивмрегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b00f9-118">**IWMRegisterCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[<span data-ttu-id="b00f9-119">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="b00f9-119">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




