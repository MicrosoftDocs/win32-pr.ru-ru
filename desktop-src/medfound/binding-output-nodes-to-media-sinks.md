---
description: Привязка выходных узлов к приемникам мультимедиа
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Привязка выходных узлов к приемникам мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547330"
---
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="9dd62-103">Привязка выходных узлов к приемникам мультимедиа</span><span class="sxs-lookup"><span data-stu-id="9dd62-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="9dd62-104">В этом разделе описывается инициализация выходных узлов в топологии, если вы используете загрузчик топологии за пределами сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="9dd62-105">Выходной узел изначально содержит один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="9dd62-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="9dd62-106">Указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="9dd62-107">Указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="9dd62-108">В последнем случае указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) должен быть преобразован в указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) , прежде чем загрузчик топологии разрешит топологию.</span><span class="sxs-lookup"><span data-stu-id="9dd62-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="9dd62-109">В большинстве сценариев этот процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9dd62-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="9dd62-110">Приложение помещает в очередь частичную топологию в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="9dd62-111">Для всех выходных узлов сеанс мультимедиа преобразует указатели [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) в указатели [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="9dd62-112">Этот процесс называется *привязкой* выходного узла к приемнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="9dd62-113">Сеанс мультимедиа отправляет измененную топологию методу [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="9dd62-114">Однако если вы используете загрузчик топологии напрямую (за пределами носителя сеансе), приложение должно привязать выходные узлы перед вызовом [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span><span class="sxs-lookup"><span data-stu-id="9dd62-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="9dd62-115">Чтобы привязать выходной узел, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9dd62-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="9dd62-116">Вызовите метод [**имфтопологиноде:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) , чтобы получить указатель на объект узла.</span><span class="sxs-lookup"><span data-stu-id="9dd62-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="9dd62-117">Запросите указатель объекта для интерфейса [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="9dd62-118">Если этот вызов завершился с ошибкой, больше ничего делать не нужно, поэтому пропустите оставшиеся шаги.</span><span class="sxs-lookup"><span data-stu-id="9dd62-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="9dd62-119">Если предыдущий шаг завершился неудачей, запросите указатель объекта для интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="9dd62-120">Создайте приемник мультимедиа, вызвав [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="9dd62-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="9dd62-121">Укажите **IID \_ имфмедиасинк** , чтобы получить указатель на интерфейс [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="9dd62-122">Запросите у узла атрибут [**MF \_ топоноде \_ STREAMID**](mf-toponode-streamid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="9dd62-123">Значение этого атрибута является идентификатором приемника потока для этого узла.</span><span class="sxs-lookup"><span data-stu-id="9dd62-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="9dd62-124">Если атрибут **MF \_ топоноде \_ STREAMID** не установлен, идентификатор потока по умолчанию равен нулю.</span><span class="sxs-lookup"><span data-stu-id="9dd62-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="9dd62-125">Возможно, соответствующий приемник потока уже существует в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="9dd62-126">Чтобы проверить, вызовите [**имфмедиасинк:: жетстреамсинкбид**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dd62-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="9dd62-127">Если приемник потока существует, метод возвращает указатель на его интерфейс [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="9dd62-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="9dd62-128">Если этот вызов завершается неудачей, попробуйте добавить новый приемник потока путем вызова [**имфмедиасинк:: аддстреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="9dd62-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="9dd62-129">Если оба вызова завершаются сбоем, это означает, что приемник мультимедиа не поддерживает запрошенный идентификатор потока, и этот узел топологии настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="9dd62-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="9dd62-130">Возвратите код ошибки и пропустите следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="9dd62-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="9dd62-131">Вызовите [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), передав указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) из предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="9dd62-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="9dd62-132">Этот вызов заменяет указатель на объект узла, чтобы узел содержал указатель на приемник потока, а не указатель на объект активации.</span><span class="sxs-lookup"><span data-stu-id="9dd62-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="9dd62-133">В следующем коде показано, как привязать выходной узел.</span><span class="sxs-lookup"><span data-stu-id="9dd62-133">The following code shows how to bind an output node.</span></span>


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="9dd62-134">В этом примере функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9dd62-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="9dd62-135">В следующем примере показано, как привязать все выходные узлы в топологии.</span><span class="sxs-lookup"><span data-stu-id="9dd62-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="9dd62-136">В этом примере используется метод [**имфтопологи:: жетаутпутнодеколлектион**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) для получения коллекции выходных узлов из топологии.</span><span class="sxs-lookup"><span data-stu-id="9dd62-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="9dd62-137">Затем он вызывает функцию, показанную в предыдущем примере на каждом из этих узлов, в свою очередь.</span><span class="sxs-lookup"><span data-stu-id="9dd62-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9dd62-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9dd62-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dd62-139">Создание расширенной топологии</span><span class="sxs-lookup"><span data-stu-id="9dd62-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="9dd62-140">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="9dd62-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="9dd62-141">**имфтополоадер**</span><span class="sxs-lookup"><span data-stu-id="9dd62-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



