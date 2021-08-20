---
description: Создание исходных узлов
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Создание исходных узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2358ca9ee0e5f3e114df8775108f8cdfeb8eeae2e3aeb35bccb66118118e4deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064593"
---
# <a name="creating-source-nodes"></a>Создание исходных узлов

Исходный узел представляет один поток из источника мультимедиа. Исходный узел должен содержать указатели на источник мультимедиа, дескриптор представления и дескриптор потока.

Чтобы добавить в топологию исходный узел, выполните следующие действия.

1.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла MF TOPOLOGY саурцестреам** , чтобы создать исходный узел.
2.  Установите атрибут [**\_ Топоноде \_ источника MF**](mf-toponode-source-attribute.md) на узле с указателем на источник мультимедиа.
3.  Задайте атрибут [**\_ \_ \_ дескриптора презентации MF топоноде**](mf-toponode-presentation-descriptor-attribute.md) на узле с указателем на дескриптор представления источника мультимедиа.
4.  Задайте атрибут [**\_ \_ \_ дескриптора потока MF топоноде**](mf-toponode-stream-descriptor-attribute.md) на узле, указав указатель на дескриптор потока для потока.
5.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется исходный узел.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание топологий](creating-topologies.md)
</dt> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Топологий](topologies.md)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



