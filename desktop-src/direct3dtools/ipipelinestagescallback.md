---
description: Не используется. Ранее он является обратным вызовом для данных стадий конвейера.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипипелинестажескаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895117"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="b27ed-104"><span id="vspixengine.ipipelinestagescallback"></span>Интерфейс Ипипелинестажескаллбакк</span><span class="sxs-lookup"><span data-stu-id="b27ed-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="b27ed-105">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b27ed-105">Not used.</span></span> <span data-ttu-id="b27ed-106">Ранее он является обратным вызовом для данных стадий конвейера.</span><span class="sxs-lookup"><span data-stu-id="b27ed-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="b27ed-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b27ed-107">Members</span></span>

<span data-ttu-id="b27ed-108">Интерфейс **ипипелинестажескаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b27ed-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b27ed-109">**Ипипелинестажескаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b27ed-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="b27ed-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b27ed-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="b27ed-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="b27ed-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="b27ed-112">Интерфейс **ипипелинестажескаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b27ed-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="b27ed-113">Метод</span><span class="sxs-lookup"><span data-stu-id="b27ed-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="b27ed-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b27ed-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b27ed-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>жетсуппортедстажес</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27ed-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b27ed-116">Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.</span><span class="sxs-lookup"><span data-stu-id="b27ed-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="b27ed-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>мешдатанотаваилаблекаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27ed-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b27ed-118">Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.</span><span class="sxs-lookup"><span data-stu-id="b27ed-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b27ed-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>мешдатаверткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27ed-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b27ed-120">Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.</span><span class="sxs-lookup"><span data-stu-id="b27ed-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="b27ed-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ресулткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="b27ed-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b27ed-122">Обратный вызов, уведомляющий узел о том, что данные образа этапа конвейера возвращены запросом связана.</span><span class="sxs-lookup"><span data-stu-id="b27ed-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="b27ed-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b27ed-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b27ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="b27ed-124">Header</span></span></p></td><td><span data-ttu-id="b27ed-125">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="b27ed-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
