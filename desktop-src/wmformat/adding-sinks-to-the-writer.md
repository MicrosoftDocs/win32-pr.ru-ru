---
title: Добавление приемников в модуль записи
description: Добавление приемников в модуль записи
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Расширенный системный формат (ASF), Добавление приемников в модуль записи
- ASF (Расширенный системный формат), Добавление приемников в модуль записи
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- Расширенный формат систем (ASF), приемники записи
- ASF (Расширенный системный формат), приемники записи
- приемники, добавление в модуль записи
- Приемники модуля записи, добавление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412523"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="97eb9-111">Добавление приемников в модуль записи</span><span class="sxs-lookup"><span data-stu-id="97eb9-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="97eb9-112">Приемники модуля записи — это отдельные объекты из модуля записи, которые необходимо добавить в модуль записи для использования.</span><span class="sxs-lookup"><span data-stu-id="97eb9-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="97eb9-113">При записи в файл можно просто вызвать [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), который автоматически настроит приемник файла.</span><span class="sxs-lookup"><span data-stu-id="97eb9-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="97eb9-114">В противном случае для добавления приемника в модуль записи вызовите метод [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) .</span><span class="sxs-lookup"><span data-stu-id="97eb9-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="97eb9-115">**Аддсинк** требует указатель на интерфейс [**ивмвритерсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) приемника.</span><span class="sxs-lookup"><span data-stu-id="97eb9-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="97eb9-116">По завершении использования приемника его необходимо закрыть, вызвав соответствующий метод, в зависимости от типа приемника, а затем удалить его из модуля записи, вызвав [**ивмвритерадванцед:: ремовесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span><span class="sxs-lookup"><span data-stu-id="97eb9-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="97eb9-117">В следующем примере кода показано, как создать приемник файла модуля записи и добавить его в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="97eb9-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="97eb9-118">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="97eb9-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="97eb9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="97eb9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97eb9-120">**Получение сообщений об ошибках из приемника**</span><span class="sxs-lookup"><span data-stu-id="97eb9-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="97eb9-121">**Интерфейс Ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="97eb9-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="97eb9-122">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="97eb9-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




