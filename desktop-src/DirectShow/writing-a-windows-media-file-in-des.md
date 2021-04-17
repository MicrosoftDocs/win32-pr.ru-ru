---
description: Запись файла Windows Media в DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Запись файла Windows Media в DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684784"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="2aedf-103">Запись файла Windows Media в DES</span><span class="sxs-lookup"><span data-stu-id="2aedf-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="2aedf-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="2aedf-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2aedf-105">В этом разделе описывается, как записать файл Windows Media с помощью [служб редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="2aedf-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aedf-106">Не используйте интеллектуальный модуль визуализации для записи файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2aedf-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="2aedf-107">Всегда используйте базовый механизм визуализации (CLSID \_ рендеренгине).</span><span class="sxs-lookup"><span data-stu-id="2aedf-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="2aedf-108">Чтобы записать файл Windows Media, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2aedf-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="2aedf-109">Вызовите **SetSite** в подсистеме визуализации, указав указатель на поставщика ключа.</span><span class="sxs-lookup"><span data-stu-id="2aedf-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="2aedf-110">Создание внешнего интерфейса графа.</span><span class="sxs-lookup"><span data-stu-id="2aedf-110">Build the front end of the graph.</span></span> <span data-ttu-id="2aedf-111">(См. раздел [Подготовка проекта к просмотру](rendering-a-project.md).)</span><span class="sxs-lookup"><span data-stu-id="2aedf-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="2aedf-112">Создайте фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) и добавьте его в граф.</span><span class="sxs-lookup"><span data-stu-id="2aedf-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="2aedf-113">Чтобы задать имя файла, используйте интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) в фильтре модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="2aedf-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="2aedf-114">Настройка модуля записи WM ASF для использования профиля Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2aedf-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="2aedf-115">Каждый профиль имеет предопределенное количество потоков.</span><span class="sxs-lookup"><span data-stu-id="2aedf-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="2aedf-116">Необходимо выбрать профиль, соответствующий группам в проекте.</span><span class="sxs-lookup"><span data-stu-id="2aedf-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="2aedf-117">Интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) содержит несколько различных методов настройки профиля.</span><span class="sxs-lookup"><span data-stu-id="2aedf-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="2aedf-118">Например, метод **конфигурефилтерусингпрофилегуид** указывает системный профиль в виде идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="2aedf-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="2aedf-119">Или можно использовать методы формата Windows Media для получения указателя **ивмпрофиле** , а затем вызвать [**Иконфигасфвритер:: конфигурефилтерусингпрофиле**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span><span class="sxs-lookup"><span data-stu-id="2aedf-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="2aedf-120">Дополнительные сведения см. [в разделе Настройка модуля записи ASF](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="2aedf-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="2aedf-121">Подключите внешний интерфейс к модулю записи ASF.</span><span class="sxs-lookup"><span data-stu-id="2aedf-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="2aedf-122">Внешний интерфейс графа содержит один выходной ПИН-код для каждой группы.</span><span class="sxs-lookup"><span data-stu-id="2aedf-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="2aedf-123">Если вы указали совместимый профиль, модуль записи ASF должен иметь соответствующий набор входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="2aedf-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="2aedf-124">Соедините каждый выходной закрепление с соответствующим входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="2aedf-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="2aedf-125">Проще всего это сделать с помощью метода [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="2aedf-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="2aedf-126">Сначала создайте новый экземпляр [построителя графа записи](capture-graph-builder.md) и инициализируйте его с помощью указателя на диспетчер графа фильтров:</span><span class="sxs-lookup"><span data-stu-id="2aedf-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="2aedf-127">Затем извлеките выходной ПИН-код для каждой группы, вызвав метод [**ирендеренгине:: жетграупаутпутпин**](irenderengine-getgroupoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2aedf-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="2aedf-128">Вызовите **RenderStream** , чтобы подключить ПИН-код к модулю записи ASF:</span><span class="sxs-lookup"><span data-stu-id="2aedf-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2aedf-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2aedf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aedf-130">Использование Windows Media с службами редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="2aedf-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



