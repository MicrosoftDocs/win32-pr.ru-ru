---
title: Событие Транспортпараметерсупдате
description: Происходит при каждом обновлении любого из наборов параметров транспорта в ДМР.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API потоковой передачи мультимедиа для события Транспортпараметерсупдате
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890600"
---
# <a name="transportparametersupdate-event"></a><span data-ttu-id="a0003-104">Событие Транспортпараметерсупдате</span><span class="sxs-lookup"><span data-stu-id="a0003-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="a0003-105">Происходит при каждом обновлении любого из наборов параметров транспорта в ДМР.</span><span class="sxs-lookup"><span data-stu-id="a0003-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0003-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0003-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="a0003-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0003-107">Parameters</span></span>

<span data-ttu-id="a0003-108">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a0003-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0003-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0003-109">Return value</span></span>

<span data-ttu-id="a0003-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0003-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0003-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0003-111">Remarks</span></span>

<span data-ttu-id="a0003-112">Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**транспортпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) с помощью метода [**Add \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="a0003-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="a0003-113">Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="a0003-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 