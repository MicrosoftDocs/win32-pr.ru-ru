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
# <a name="binding-output-nodes-to-media-sinks"></a>Привязка выходных узлов к приемникам мультимедиа

В этом разделе описывается инициализация выходных узлов в топологии, если вы используете загрузчик топологии за пределами сеанса мультимедиа. Выходной узел изначально содержит один из следующих элементов:

-   Указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .
-   Указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

В последнем случае указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) должен быть преобразован в указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) , прежде чем загрузчик топологии разрешит топологию. В большинстве сценариев этот процесс работает следующим образом:

1.  Приложение помещает в очередь частичную топологию в сеансе мультимедиа.
2.  Для всех выходных узлов сеанс мультимедиа преобразует указатели [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) в указатели [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Этот процесс называется *привязкой* выходного узла к приемнику мультимедиа.
3.  Сеанс мультимедиа отправляет измененную топологию методу [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Однако если вы используете загрузчик топологии напрямую (за пределами носителя сеансе), приложение должно привязать выходные узлы перед вызовом [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load). Чтобы привязать выходной узел, выполните следующие действия.

1.  Вызовите метод [**имфтопологиноде:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) , чтобы получить указатель на объект узла.
2.  Запросите указатель объекта для интерфейса [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Если этот вызов завершился с ошибкой, больше ничего делать не нужно, поэтому пропустите оставшиеся шаги.
3.  Если предыдущий шаг завершился неудачей, запросите указатель объекта для интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Создайте приемник мультимедиа, вызвав [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Укажите **IID \_ имфмедиасинк** , чтобы получить указатель на интерфейс [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) приемника мультимедиа.
5.  Запросите у узла атрибут [**MF \_ топоноде \_ STREAMID**](mf-toponode-streamid-attribute.md) . Значение этого атрибута является идентификатором приемника потока для этого узла. Если атрибут **MF \_ топоноде \_ STREAMID** не установлен, идентификатор потока по умолчанию равен нулю.
6.  Возможно, соответствующий приемник потока уже существует в приемнике мультимедиа. Чтобы проверить, вызовите [**имфмедиасинк:: жетстреамсинкбид**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) в приемнике мультимедиа. Если приемник потока существует, метод возвращает указатель на его интерфейс [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Если этот вызов завершается неудачей, попробуйте добавить новый приемник потока путем вызова [**имфмедиасинк:: аддстреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Если оба вызова завершаются сбоем, это означает, что приемник мультимедиа не поддерживает запрошенный идентификатор потока, и этот узел топологии настроен неправильно. Возвратите код ошибки и пропустите следующий шаг.
7.  Вызовите [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), передав указатель [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) из предыдущего шага. Этот вызов заменяет указатель на объект узла, чтобы узел содержал указатель на приемник потока, а не указатель на объект активации.

В следующем коде показано, как привязать выходной узел.


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
> В этом примере функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса.

 

В следующем примере показано, как привязать все выходные узлы в топологии. В этом примере используется метод [**имфтопологи:: жетаутпутнодеколлектион**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) для получения коллекции выходных узлов из топологии. Затем он вызывает функцию, показанную в предыдущем примере на каждом из этих узлов, в свою очередь.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание расширенной топологии](advanced-topology-building.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> <dt>

[**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



