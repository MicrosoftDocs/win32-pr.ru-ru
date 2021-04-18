---
description: В этом разделе описано, как задать время отмены воспроизведения при использовании сеанса мультимедиа.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Как задать время окончания воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701750"
---
# <a name="how-to-set-the-playback-stop-time"></a>Как задать время окончания воспроизведения

В этом разделе описано, как задать время отмены воспроизведения при использовании [сеанса мультимедиа](media-session.md).

## <a name="setting-the-stop-time-before-playback-begins"></a>Задание времени окончания до начала воспроизведения

Прежде чем поставить в очередь топологию для воспроизведения, можно указать время окончания с помощью атрибута [MF \_ топоноде \_ медиастоп](mf-toponode-mediastop-attribute.md) . Для каждого выходного узла в топологии установите для параметра MF \_ топоноде \_ медиастоп значение времени окончания в 100-наносекундных единицах.

Обратите внимание, что задание этого атрибута после начала воспроизведения не оказывает никакого воздействия. Поэтому задайте атрибут перед вызовом [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

В следующем коде показано, как задать время окончания для существующей топологии.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a>Задание времени окончания работы после начала воспроизведения

Существует способ задать время окончания воспроизведения после запуска [сеанса мультимедиа](media-session.md) с помощью интерфейса [**имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .

> [!IMPORTANT]
> Этот интерфейс имеет серьезные ограничения, так как время окончания указывается как 32-разрядное значение. Это означает, что максимальное время окончания, которое можно задать с помощью этого интерфейса, — 0xFFFFFFFF или только более 7 минут. Это ограничение связано с неправильным определением структуры.

 

Чтобы задать время окончания с помощью интерфейса [**имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , выполните следующие действия.

1.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить интерфейс [**Имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) из сеанса мультимедиа.
2.  Вызовите [**имфтопологи:: жеттопологид**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) , чтобы получить идентификатор топологии воспроизведения.
3.  Для каждого выходного узла в топологии вызовите [**имфтопологинодеаттрибутидитор:: упдатенодеаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Этот метод принимает идентификатор топологии и указатель на структуру [**\_ \_ обновления атрибута мфтопоноде**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) . Инициализируйте структуру следующим образом.

    | Член               | Значение                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | Идентификатор узла. Чтобы получить идентификатор узла, вызовите Call [**имфтопологиноде:: жеттопонодеид**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid). |
    | **гуидаттрибутекэй** | **MF \_ топоноде \_ медиастоп**                                                                                         |
    | **аттртипе**         | **\_Атрибуту MF \_ UINT64**                                                                                           |
    | **u64**              | Время окончания в 100-наносекундных единицах.                                                                             |

    

     

Будьте внимательны, чтобы правильно задать значение **аттртипе** . Несмотря на то, что **u64** является 32-битным типом, метод требует, чтобы **аттртипе** был установлен в значение свойства **MF \_ атрибута \_ UINT64**.

Эти действия показаны в следующем коде.


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> </dl>

 

 



