---
title: Событие Рендерингпараметерсупдате
description: Возникает при обновлении любого из набора параметров элемента управления отрисовки в ДМР.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API потоковой передачи мультимедиа для события Рендерингпараметерсупдате
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337092"
---
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="0c46b-104">Событие Рендерингпараметерсупдате</span><span class="sxs-lookup"><span data-stu-id="0c46b-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="0c46b-105">Возникает при обновлении любого из набора параметров элемента управления отрисовки в ДМР.</span><span class="sxs-lookup"><span data-stu-id="0c46b-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c46b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c46b-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="0c46b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c46b-107">Parameters</span></span>

<span data-ttu-id="0c46b-108">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="0c46b-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c46b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c46b-109">Return value</span></span>

<span data-ttu-id="0c46b-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0c46b-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c46b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c46b-111">Remarks</span></span>

<span data-ttu-id="0c46b-112">Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**рендерингпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) с помощью метода [**Add \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="0c46b-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="0c46b-113">Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="0c46b-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 