---
description: Не используется. Ранее он является обратным вызовом для данных стадий конвейера.
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPipeLineStagesCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990019"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="6c3af-104"><span id="vspixengine.ipipelinestagescallback2"></span>Интерфейс IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="6c3af-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="6c3af-105">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6c3af-105">Not used.</span></span> <span data-ttu-id="6c3af-106">Ранее он является обратным вызовом для данных стадий конвейера.</span><span class="sxs-lookup"><span data-stu-id="6c3af-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="6c3af-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="6c3af-107">Members</span></span>

<span data-ttu-id="6c3af-108">Интерфейс **IPipeLineStagesCallback2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6c3af-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c3af-109">**IPipeLineStagesCallback2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6c3af-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="6c3af-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6c3af-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6c3af-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="6c3af-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6c3af-112">Интерфейс **IPipeLineStagesCallback2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6c3af-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6c3af-113">Метод</span><span class="sxs-lookup"><span data-stu-id="6c3af-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6c3af-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6c3af-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6c3af-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>среаддатадименсионкаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="6c3af-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6c3af-116">Обратный вызов, уведомляющий узел о количестве потоков и групп шейдера вычислений в связанном запросе.</span><span class="sxs-lookup"><span data-stu-id="6c3af-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="6c3af-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>среаддатанотаваилаблекаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="6c3af-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6c3af-118">Обратный вызов, уведомляющий узел о том, что Среаддата недоступен для определенного этапа и события конвейера.</span><span class="sxs-lookup"><span data-stu-id="6c3af-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6c3af-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3af-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6c3af-120">Header</span><span class="sxs-lookup"><span data-stu-id="6c3af-120">Header</span></span></p></td><td><span data-ttu-id="6c3af-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="6c3af-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
