---
description: Интерфейс для удаленного обмена данными о vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипиртопиренгине
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701130"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="bcd93-103"><span id="vspixengine.ipeertopeerengine"></span>Интерфейс Ипиртопиренгине</span><span class="sxs-lookup"><span data-stu-id="bcd93-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="bcd93-104">Интерфейс для удаленного обмена данными о vsglog.</span><span class="sxs-lookup"><span data-stu-id="bcd93-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="bcd93-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="bcd93-105">Members</span></span>

<span data-ttu-id="bcd93-106">Интерфейс **ипиртопиренгине** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bcd93-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bcd93-107">**Ипиртопиренгине** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bcd93-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="bcd93-108">Методы</span><span class="sxs-lookup"><span data-stu-id="bcd93-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="bcd93-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="bcd93-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="bcd93-110">Интерфейс **ипиртопиренгине** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bcd93-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="bcd93-111">Метод</span><span class="sxs-lookup"><span data-stu-id="bcd93-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="bcd93-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bcd93-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bcd93-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>канцелсетплайбаккендпоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="bcd93-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bcd93-114">Отменяет предыдущий запрос для настройки удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="bcd93-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bcd93-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>жетплайбаккендпоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="bcd93-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bcd93-116">Возвращает адрес конечной точки удаленного модуля.</span><span class="sxs-lookup"><span data-stu-id="bcd93-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bcd93-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>сетплайбаккендпоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="bcd93-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bcd93-118">Задает адрес конечной точки, используемый для подключения к удаленному модулю.</span><span class="sxs-lookup"><span data-stu-id="bcd93-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="bcd93-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bcd93-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bcd93-120">Header</span><span class="sxs-lookup"><span data-stu-id="bcd93-120">Header</span></span></p></td><td><span data-ttu-id="bcd93-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="bcd93-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
