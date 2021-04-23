---
description: Не используется. Ранее он запрашивает данные о стадиях конвейера.
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
ms.openlocfilehash: 9d344b7e128adf344f50a99ba41a420ca794baec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139643"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="5ba57-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Интерфейс IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="5ba57-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="5ba57-105">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5ba57-105">Not used.</span></span> <span data-ttu-id="5ba57-106">Ранее он запрашивает данные о стадиях конвейера.</span><span class="sxs-lookup"><span data-stu-id="5ba57-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="5ba57-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="5ba57-107">Members</span></span>

<span data-ttu-id="5ba57-108">Интерфейс **IPipeLineStagesRequest2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5ba57-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5ba57-109">**IPipeLineStagesRequest2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5ba57-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="5ba57-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5ba57-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="5ba57-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="5ba57-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="5ba57-112">Интерфейс **IPipeLineStagesRequest2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5ba57-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="5ba57-113">Метод</span><span class="sxs-lookup"><span data-stu-id="5ba57-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="5ba57-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5ba57-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5ba57-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>рекуесткомпутешадердатаасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ba57-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5ba57-116">Асинхронный запрос на получение данных шейдера вычислений для указанной диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="5ba57-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="5ba57-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>рекуесткомпутешадерстажеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ba57-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5ba57-118">Асинхронный запрос, получающий, использовался ли этап шейдера вычислений для указанного фрейма и события.</span><span class="sxs-lookup"><span data-stu-id="5ba57-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="5ba57-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5ba57-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5ba57-120">Header</span><span class="sxs-lookup"><span data-stu-id="5ba57-120">Header</span></span></p></td><td><span data-ttu-id="5ba57-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5ba57-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
