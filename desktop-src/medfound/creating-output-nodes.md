---
description: Создание выходных узлов
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Создание выходных узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943024"
---
# <a name="creating-output-nodes"></a>Создание выходных узлов

Выходной узел представляет приемник потока в приемнике мультимедиа. Существует два способа инициализации выходного узла:

-   Из указателя на приемник потока.
-   Из указателя на объект активации для приемника мультимедиа.

Если планируется загрузка топологии внутри защищенного пути к носителю (PMP), необходимо использовать объект активации, чтобы приемник мультимедиа можно было создать внутри защищенного процесса. Первый подход (с использованием указателя на приемник потока) не работает с PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Создание выходного узла из приемника потока

Чтобы создать выходной узел из приемника потока, выполните следующие действия.

1.  Создайте экземпляр приемника мультимедиа.
2.  Используйте интерфейс [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) приемника мультимедиа, чтобы получить указатель на нужный приемник потока. (Интерфейс **имфмедиасинк** имеет несколько методов, которые возвращают указатели на приемник потока.)
3.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла вывода топологии MF** , чтобы создать выходной узел.
4.  Вызовите [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель на интерфейс [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) приемника потока.
5.  Задайте для атрибута [**MF \_ ТОПОНОДЕ \_ unshutdown \_ On \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) **значение false** (необязательно, но рекомендуется).
6.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется выходной узел из приемника потока.


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



Когда приложение завершает сеанс мультимедиа, сеанс мультимедиа автоматически завершает работу приемника мультимедиа. Таким образом, нельзя повторно использовать приемник мультимедиа с другим экземпляром сеанса мультимедиа.

## <a name="creating-an-output-node-from-an-activation-object"></a>Создание выходного узла из объекта активации

Любой доверенный приемник мультимедиа должен предоставлять объект активации, чтобы приемник мультимедиа можно было создать внутри защищенного процесса. Дополнительные сведения см. в разделе [объекты активации](activation-objects.md). Конкретная функция, создающая объект активации, будет зависеть от приемника носителя.

Чтобы создать выходной узел из объекта активации, выполните следующие действия.

1.  Создайте объект активации и получите указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) объекта активации.
2.  Вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) с флагом **\_ \_ \_ узла вывода топологии MF** , чтобы создать выходной узел.
3.  При необходимости установите атрибут [**MF \_ топоноде \_ STREAMID**](mf-toponode-streamid-attribute.md) на узле, чтобы указать идентификатор потока приемника потока. Если опустить этот атрибут, узел по умолчанию будет использовать приемник потока 0.
4.  Присвойте атрибуту [**MF \_ ТОПОНОДЕ \_ unshutdown \_ On \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) **значение true** (необязательно, но рекомендуется).
5.  Вызовите метод [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) и передайте указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
6.  Вызовите [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , чтобы добавить узел в топологию.

В следующем примере создается и инициализируется выходной узел из объекта активации.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Создание топологий](creating-topologies.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> <dt>

[Топологий](topologies.md)
</dt> </dl>

 

 



