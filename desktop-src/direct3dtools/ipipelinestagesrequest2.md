---
description: <span id="vspixengine.ipipelinestagesrequest2"></span>Интерфейс IPipeLineStagesRequest2 — не используется. Ранее он запрашивает данные о стадиях конвейера.
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPipeLineStagesRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107072"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="9d7a4-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Интерфейс IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="9d7a4-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="9d7a4-105">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-105">Not used.</span></span> <span data-ttu-id="9d7a4-106">Ранее он запрашивает данные о стадиях конвейера.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="9d7a4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="9d7a4-107">Members</span></span>

<span data-ttu-id="9d7a4-108">Интерфейс **IPipeLineStagesRequest2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9d7a4-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d7a4-109">**IPipeLineStagesRequest2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d7a4-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="9d7a4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9d7a4-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="9d7a4-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="9d7a4-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="9d7a4-112">Интерфейс **IPipeLineStagesRequest2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="9d7a4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9d7a4-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="9d7a4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9d7a4-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="9d7a4-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>рекуесткомпутешадердатаасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="9d7a4-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="9d7a4-116">Асинхронный запрос на получение данных шейдера вычислений для указанной диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="9d7a4-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>рекуесткомпутешадерстажеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="9d7a4-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="9d7a4-118">Асинхронный запрос, получающий, использовался ли этап шейдера вычислений для указанного фрейма и события.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="9d7a4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9d7a4-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9d7a4-120">Header</span><span class="sxs-lookup"><span data-stu-id="9d7a4-120">Header</span></span></p></td><td><span data-ttu-id="9d7a4-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="9d7a4-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
