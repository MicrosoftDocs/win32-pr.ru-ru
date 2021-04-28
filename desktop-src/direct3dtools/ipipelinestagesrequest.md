---
description: <span id="vspixengine.ipipelinestagesrequest"></span>Интерфейс Ипипелинестажесрекуест — не используется. Ранее он запрашивает данные о стадиях конвейера.
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипипелинестажесрекуест
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bb87e8a4f2daee78146929df64dbee1f61774ed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114262"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="26c59-104"><span id="vspixengine.ipipelinestagesrequest"></span>Интерфейс Ипипелинестажесрекуест</span><span class="sxs-lookup"><span data-stu-id="26c59-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="26c59-105">Не используется.</span><span class="sxs-lookup"><span data-stu-id="26c59-105">Not used.</span></span> <span data-ttu-id="26c59-106">Ранее он запрашивает данные о стадиях конвейера.</span><span class="sxs-lookup"><span data-stu-id="26c59-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="26c59-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="26c59-107">Members</span></span>

<span data-ttu-id="26c59-108">Интерфейс **ипипелинестажесрекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="26c59-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26c59-109">**Ипипелинестажесрекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26c59-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="26c59-110">Методы</span><span class="sxs-lookup"><span data-stu-id="26c59-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="26c59-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="26c59-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="26c59-112">Интерфейс **ипипелинестажесрекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="26c59-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="26c59-113">Метод</span><span class="sxs-lookup"><span data-stu-id="26c59-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="26c59-114">Описание</span><span class="sxs-lookup"><span data-stu-id="26c59-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="26c59-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>рекуестасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="26c59-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="26c59-116">Асинхронный запрос на получение изображений предварительного просмотра для окна "Этапы графического конвейера".</span><span class="sxs-lookup"><span data-stu-id="26c59-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="26c59-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>рекуестсуппортедстажесасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="26c59-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="26c59-118">Асинхронный запрос на получение списка этапов, используемых для указанного фрейма и события.</span><span class="sxs-lookup"><span data-stu-id="26c59-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="26c59-119">Требования</span><span class="sxs-lookup"><span data-stu-id="26c59-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="26c59-120">Header</span><span class="sxs-lookup"><span data-stu-id="26c59-120">Header</span></span></p></td><td><span data-ttu-id="26c59-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="26c59-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
