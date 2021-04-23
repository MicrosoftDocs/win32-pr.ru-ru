---
description: Создание выходных узлов
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Создание выходных узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896582"
---
# <a name="creating-output-nodes"></a><span data-ttu-id="823a3-103">Создание выходных узлов</span><span class="sxs-lookup"><span data-stu-id="823a3-103">Creating Output Nodes</span></span>

<span data-ttu-id="823a3-104">Выходной узел представляет приемник потока в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="823a3-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="823a3-105">Существует два способа инициализации выходного узла:</span><span class="sxs-lookup"><span data-stu-id="823a3-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="823a3-106">Из указателя на приемник потока.</span><span class="sxs-lookup"><span data-stu-id="823a3-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="823a3-107">Из указателя на объект активации для приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="823a3-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="823a3-108">Если планируется загрузка топологии внутри защищенного пути к носителю (PMP), необходимо использовать объект активации, чтобы приемник мультимедиа можно было создать внутри защищенного процесса.</span><span class="sxs-lookup"><span data-stu-id="823a3-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="823a3-109">Первый подход (с использованием указателя на приемник потока) не работает с PMP.</span><span class="sxs-lookup"><span data-stu-id="823a3-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="823a3-110">Создание выходного узла из приемника потока</span><span class="sxs-lookup"><span data-stu-id="823a3-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="823a3-111">Чтобы создать выходной узел из приемника потока, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="823a3-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="823a3-112">Создайте экземпляр приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="823a3-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="823a3-113">Используйте интерфейс [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) приемника мультимедиа, чтобы получить указатель на нужный приемник потока.</span><span class="sxs-lookup"><span data-stu-id="823a3-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="823a3-114">(Интерфейс **имфмедиасинк** имеет несколько методов, которые возвращают указатели на приемник потока.)</span><span class="sxs-lookup"><span data-stu-id="823a3-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="823a3-115">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла вывода топологии MF** , чтобы создать выходной узел.</span><span class="sxs-lookup"><span data-stu-id="823a3-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="823a3-116">Вызовите [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель на интерфейс [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) приемника потока.</span><span class="sxs-lookup"><span data-stu-id="823a3-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="823a3-117">Задайте для атрибута [**MF \_ ТОПОНОДЕ \_ unshutdown \_ On \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) **значение false** (необязательно, но рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="823a3-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="823a3-118">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="823a3-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="823a3-119">В следующем примере создается и инициализируется выходной узел из приемника потока.</span><span class="sxs-lookup"><span data-stu-id="823a3-119">The following example creates and initializes an output node from a stream sink.</span></span>


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



<span data-ttu-id="823a3-120">Когда приложение завершает сеанс мультимедиа, сеанс мультимедиа автоматически завершает работу приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="823a3-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="823a3-121">Таким образом, нельзя повторно использовать приемник мультимедиа с другим экземпляром сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="823a3-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="823a3-122">Создание выходного узла из объекта активации</span><span class="sxs-lookup"><span data-stu-id="823a3-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="823a3-123">Любой доверенный приемник мультимедиа должен предоставлять объект активации, чтобы приемник мультимедиа можно было создать внутри защищенного процесса.</span><span class="sxs-lookup"><span data-stu-id="823a3-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="823a3-124">Дополнительные сведения см. в разделе [объекты активации](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="823a3-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="823a3-125">Конкретная функция, создающая объект активации, будет зависеть от приемника носителя.</span><span class="sxs-lookup"><span data-stu-id="823a3-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="823a3-126">Чтобы создать выходной узел из объекта активации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="823a3-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="823a3-127">Создайте объект активации и получите указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) объекта активации.</span><span class="sxs-lookup"><span data-stu-id="823a3-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="823a3-128">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла вывода топологии MF** , чтобы создать выходной узел.</span><span class="sxs-lookup"><span data-stu-id="823a3-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="823a3-129">При необходимости установите атрибут [**MF \_ топоноде \_ STREAMID**](mf-toponode-streamid-attribute.md) на узле, чтобы указать идентификатор потока приемника потока.</span><span class="sxs-lookup"><span data-stu-id="823a3-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="823a3-130">Если опустить этот атрибут, узел по умолчанию будет использовать приемник потока 0.</span><span class="sxs-lookup"><span data-stu-id="823a3-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="823a3-131">Присвойте атрибуту [**MF \_ ТОПОНОДЕ \_ unshutdown \_ On \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) **значение true** (необязательно, но рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="823a3-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="823a3-132">Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="823a3-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="823a3-133">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="823a3-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="823a3-134">В следующем примере создается и инициализируется выходной узел из объекта активации.</span><span class="sxs-lookup"><span data-stu-id="823a3-134">The following example creates and initializes an output node from an activation object.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="823a3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="823a3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="823a3-136">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="823a3-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="823a3-137">Создание топологий</span><span class="sxs-lookup"><span data-stu-id="823a3-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="823a3-138">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="823a3-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="823a3-139">Топологии</span><span class="sxs-lookup"><span data-stu-id="823a3-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



