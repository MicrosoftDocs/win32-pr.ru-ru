---
description: Создание узлов преобразования
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Создание узлов преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539611"
---
# <a name="creating-transform-nodes"></a><span data-ttu-id="4e31b-103">Создание узлов преобразования</span><span class="sxs-lookup"><span data-stu-id="4e31b-103">Creating Transform Nodes</span></span>

<span data-ttu-id="4e31b-104">Узел преобразования представляет Media Foundation преобразование (MFT), например декодер или кодировщик.</span><span class="sxs-lookup"><span data-stu-id="4e31b-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="4e31b-105">Существует несколько различных способов инициализации узла преобразования.</span><span class="sxs-lookup"><span data-stu-id="4e31b-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="4e31b-106">Из указателя на MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="4e31b-107">Из идентификатора CLSID для MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="4e31b-108">Из указателя на объект активации для MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="4e31b-109">Если вы собираетесь загрузить топологию внутри защищенного пути к носителю (PMP), необходимо использовать либо CLSID, либо объект активации, чтобы можно было создать таблицу MFT внутри защищенного процесса.</span><span class="sxs-lookup"><span data-stu-id="4e31b-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="4e31b-110">Первый подход (при использовании указателя на MFT) не работает с PMP.</span><span class="sxs-lookup"><span data-stu-id="4e31b-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="4e31b-111">Создание узла преобразования из MFT</span><span class="sxs-lookup"><span data-stu-id="4e31b-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="4e31b-112">Чтобы создать узел преобразования из MFT, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e31b-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="4e31b-113">Создайте экземпляр MFT и получите указатель на интерфейс [**ИМФТРАНСФОРМ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="4e31b-114">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.</span><span class="sxs-lookup"><span data-stu-id="4e31b-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="4e31b-115">Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="4e31b-116">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="4e31b-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="4e31b-117">В следующем примере создается и инициализируется узел преобразования из MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-117">The following example creates and initializes a transform node from an MFT.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="4e31b-118">Создание узла преобразования из идентификатора CLSID</span><span class="sxs-lookup"><span data-stu-id="4e31b-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="4e31b-119">Чтобы создать узел преобразования из идентификатора CLSID, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e31b-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="4e31b-120">Найдите идентификатор CLSID MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="4e31b-121">Функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) можно использовать для поиска идентификаторов CLSID МФТС по категории, например декодеров или кодировщиков.</span><span class="sxs-lookup"><span data-stu-id="4e31b-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="4e31b-122">Возможно, вы также узнаете идентификатор CLSID конкретной MFT, который вы хотите использовать (например, если вы реализовали собственный пользовательский MFT).</span><span class="sxs-lookup"><span data-stu-id="4e31b-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="4e31b-123">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.</span><span class="sxs-lookup"><span data-stu-id="4e31b-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="4e31b-124">Установите атрибут **\_ ObjectID топоноде \_ Transform \_** для узла.</span><span class="sxs-lookup"><span data-stu-id="4e31b-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="4e31b-125">Значением атрибута является CLSID.</span><span class="sxs-lookup"><span data-stu-id="4e31b-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="4e31b-126">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="4e31b-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="4e31b-127">В следующем примере создается и инициализируется узел преобразования из идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="4e31b-127">The following example creates and initializes a transform node from a CLSID.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="4e31b-128">Создание узла преобразования из объекта активации</span><span class="sxs-lookup"><span data-stu-id="4e31b-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="4e31b-129">Некоторые МФТС предоставляют объекты активации.</span><span class="sxs-lookup"><span data-stu-id="4e31b-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="4e31b-130">Например, функция [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) возвращает объект активации для кодировщика Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="4e31b-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="4e31b-131">Точная функция зависит от MFT.</span><span class="sxs-lookup"><span data-stu-id="4e31b-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="4e31b-132">Не каждая MFT предоставляет объект активации.</span><span class="sxs-lookup"><span data-stu-id="4e31b-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="4e31b-133">Дополнительные сведения см. в разделе [объекты активации](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4e31b-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="4e31b-134">Можно также получить объект активации MFT, вызвав функцию [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="4e31b-135">Чтобы создать узел преобразования из объекта активации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e31b-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="4e31b-136">Создайте объект активации и получите указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) объекта активации.</span><span class="sxs-lookup"><span data-stu-id="4e31b-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="4e31b-137">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.</span><span class="sxs-lookup"><span data-stu-id="4e31b-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="4e31b-138">Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="4e31b-139">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="4e31b-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="4e31b-140">В следующем примере создается и инициализируется узел преобразования из объекта активации.</span><span class="sxs-lookup"><span data-stu-id="4e31b-140">The following example creates and initializes a transform node from an activation object.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4e31b-141">См. также</span><span class="sxs-lookup"><span data-stu-id="4e31b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e31b-142">Создание топологий</span><span class="sxs-lookup"><span data-stu-id="4e31b-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="4e31b-143">Топологии</span><span class="sxs-lookup"><span data-stu-id="4e31b-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="4e31b-144">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="4e31b-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



