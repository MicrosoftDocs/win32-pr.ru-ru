---
description: Создание исходных узлов
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Создание исходных узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701323"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="10f05-103">Создание исходных узлов</span><span class="sxs-lookup"><span data-stu-id="10f05-103">Creating Source Nodes</span></span>

<span data-ttu-id="10f05-104">Исходный узел представляет один поток из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10f05-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="10f05-105">Исходный узел должен содержать указатели на источник мультимедиа, дескриптор представления и дескриптор потока.</span><span class="sxs-lookup"><span data-stu-id="10f05-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="10f05-106">Чтобы добавить в топологию исходный узел, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10f05-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="10f05-107">Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла MF TOPOLOGY саурцестреам** , чтобы создать исходный узел.</span><span class="sxs-lookup"><span data-stu-id="10f05-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="10f05-108">Установите атрибут [**\_ Топоноде \_ источника MF**](mf-toponode-source-attribute.md) на узле с указателем на источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10f05-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="10f05-109">Задайте атрибут [**\_ \_ \_ дескриптора презентации MF топоноде**](mf-toponode-presentation-descriptor-attribute.md) на узле с указателем на дескриптор представления источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10f05-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="10f05-110">Задайте атрибут [**\_ \_ \_ дескриптора потока MF топоноде**](mf-toponode-stream-descriptor-attribute.md) на узле, указав указатель на дескриптор потока для потока.</span><span class="sxs-lookup"><span data-stu-id="10f05-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="10f05-111">Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="10f05-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="10f05-112">В следующем примере создается и инициализируется исходный узел.</span><span class="sxs-lookup"><span data-stu-id="10f05-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
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



## <a name="related-topics"></a><span data-ttu-id="10f05-113">См. также</span><span class="sxs-lookup"><span data-stu-id="10f05-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f05-114">Создание топологий</span><span class="sxs-lookup"><span data-stu-id="10f05-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="10f05-115">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="10f05-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="10f05-116">Топологии</span><span class="sxs-lookup"><span data-stu-id="10f05-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="10f05-117">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="10f05-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



