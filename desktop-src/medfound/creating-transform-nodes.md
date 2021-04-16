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
# <a name="creating-transform-nodes"></a>Создание узлов преобразования

Узел преобразования представляет Media Foundation преобразование (MFT), например декодер или кодировщик. Существует несколько различных способов инициализации узла преобразования.

-   Из указателя на MFT.
-   Из идентификатора CLSID для MFT.
-   Из указателя на объект активации для MFT.

Если вы собираетесь загрузить топологию внутри защищенного пути к носителю (PMP), необходимо использовать либо CLSID, либо объект активации, чтобы можно было создать таблицу MFT внутри защищенного процесса. Первый подход (при использовании указателя на MFT) не работает с PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Создание узла преобразования из MFT

Чтобы создать узел преобразования из MFT, выполните следующие действия.

1.  Создайте экземпляр MFT и получите указатель на интерфейс [**ИМФТРАНСФОРМ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) MFT.
2.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.
3.  Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .
4.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется узел преобразования из MFT.


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



## <a name="creating-a-transform-node-from-a-clsid"></a>Создание узла преобразования из идентификатора CLSID

Чтобы создать узел преобразования из идентификатора CLSID, выполните следующие действия.

1.  Найдите идентификатор CLSID MFT. Функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) можно использовать для поиска идентификаторов CLSID МФТС по категории, например декодеров или кодировщиков. Возможно, вы также узнаете идентификатор CLSID конкретной MFT, который вы хотите использовать (например, если вы реализовали собственный пользовательский MFT).
2.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.
3.  Установите атрибут **\_ ObjectID топоноде \_ Transform \_** для узла. Значением атрибута является CLSID.
4.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется узел преобразования из идентификатора CLSID.


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



## <a name="creating-a-transform-node-from-an-activation-object"></a>Создание узла преобразования из объекта активации

Некоторые МФТС предоставляют объекты активации. Например, функция [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) возвращает объект активации для кодировщика Windows Media Audio (WMA). Точная функция зависит от MFT. Не каждая MFT предоставляет объект активации. Дополнительные сведения см. в разделе [объекты активации](activation-objects.md).

Можно также получить объект активации MFT, вызвав функцию [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Чтобы создать узел преобразования из объекта активации, выполните следующие действия.

1.  Создайте объект активации и получите указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) объекта активации.
2.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла преобразования топологии MF** , чтобы создать узел преобразования.
3.  Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется узел преобразования из объекта активации.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание топологий](creating-topologies.md)
</dt> <dt>

[Топологии](topologies.md)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



