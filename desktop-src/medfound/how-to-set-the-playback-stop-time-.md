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
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="102ae-103">Как задать время окончания воспроизведения</span><span class="sxs-lookup"><span data-stu-id="102ae-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="102ae-104">В этом разделе описано, как задать время отмены воспроизведения при использовании [сеанса мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="102ae-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="102ae-105">Задание времени окончания до начала воспроизведения</span><span class="sxs-lookup"><span data-stu-id="102ae-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="102ae-106">Прежде чем поставить в очередь топологию для воспроизведения, можно указать время окончания с помощью атрибута [MF \_ топоноде \_ медиастоп](mf-toponode-mediastop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="102ae-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="102ae-107">Для каждого выходного узла в топологии установите для параметра MF \_ топоноде \_ медиастоп значение времени окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="102ae-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="102ae-108">Обратите внимание, что задание этого атрибута после начала воспроизведения не оказывает никакого воздействия.</span><span class="sxs-lookup"><span data-stu-id="102ae-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="102ae-109">Поэтому задайте атрибут перед вызовом [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="102ae-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="102ae-110">В следующем коде показано, как задать время окончания для существующей топологии.</span><span class="sxs-lookup"><span data-stu-id="102ae-110">The following code shows how to set the stop time on an existing topology.</span></span>


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



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="102ae-111">Задание времени окончания работы после начала воспроизведения</span><span class="sxs-lookup"><span data-stu-id="102ae-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="102ae-112">Существует способ задать время окончания воспроизведения после запуска [сеанса мультимедиа](media-session.md) с помощью интерфейса [**имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .</span><span class="sxs-lookup"><span data-stu-id="102ae-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="102ae-113">Этот интерфейс имеет серьезные ограничения, так как время окончания указывается как 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="102ae-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="102ae-114">Это означает, что максимальное время окончания, которое можно задать с помощью этого интерфейса, — 0xFFFFFFFF или только более 7 минут.</span><span class="sxs-lookup"><span data-stu-id="102ae-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="102ae-115">Это ограничение связано с неправильным определением структуры.</span><span class="sxs-lookup"><span data-stu-id="102ae-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="102ae-116">Чтобы задать время окончания с помощью интерфейса [**имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="102ae-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="102ae-117">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить интерфейс [**Имфтопологинодеаттрибутидитор**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="102ae-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="102ae-118">Вызовите [**имфтопологи:: жеттопологид**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) , чтобы получить идентификатор топологии воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="102ae-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="102ae-119">Для каждого выходного узла в топологии вызовите [**имфтопологинодеаттрибутидитор:: упдатенодеаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="102ae-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="102ae-120">Этот метод принимает идентификатор топологии и указатель на структуру [**\_ \_ обновления атрибута мфтопоноде**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) .</span><span class="sxs-lookup"><span data-stu-id="102ae-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="102ae-121">Инициализируйте структуру следующим образом.</span><span class="sxs-lookup"><span data-stu-id="102ae-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="102ae-122">Член</span><span class="sxs-lookup"><span data-stu-id="102ae-122">Member</span></span>               | <span data-ttu-id="102ae-123">Значение</span><span class="sxs-lookup"><span data-stu-id="102ae-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="102ae-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="102ae-124">**NodeId**</span></span>           | <span data-ttu-id="102ae-125">Идентификатор узла.</span><span class="sxs-lookup"><span data-stu-id="102ae-125">The node ID.</span></span> <span data-ttu-id="102ae-126">Чтобы получить идентификатор узла, вызовите Call [**имфтопологиноде:: жеттопонодеид**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="102ae-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="102ae-127">**гуидаттрибутекэй**</span><span class="sxs-lookup"><span data-stu-id="102ae-127">**guidAttributeKey**</span></span> | <span data-ttu-id="102ae-128">**MF \_ топоноде \_ медиастоп**</span><span class="sxs-lookup"><span data-stu-id="102ae-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="102ae-129">**аттртипе**</span><span class="sxs-lookup"><span data-stu-id="102ae-129">**attrType**</span></span>         | <span data-ttu-id="102ae-130">**\_Атрибуту MF \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="102ae-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="102ae-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="102ae-131">**u64**</span></span>              | <span data-ttu-id="102ae-132">Время окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="102ae-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="102ae-133">Будьте внимательны, чтобы правильно задать значение **аттртипе** .</span><span class="sxs-lookup"><span data-stu-id="102ae-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="102ae-134">Несмотря на то, что **u64** является 32-битным типом, метод требует, чтобы **аттртипе** был установлен в значение свойства **MF \_ атрибута \_ UINT64**.</span><span class="sxs-lookup"><span data-stu-id="102ae-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="102ae-135">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="102ae-135">The following code shows these steps.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="102ae-136">См. также</span><span class="sxs-lookup"><span data-stu-id="102ae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="102ae-137">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="102ae-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



