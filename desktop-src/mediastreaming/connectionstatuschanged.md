---
title: Событие Коннектионстатусчанжед
description: Происходит при изменении состояния сетевого подключения устройства.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API потоковой передачи мультимедиа для события Коннектионстатусчанжед
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791221"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="77b82-104">Событие Коннектионстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="77b82-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="77b82-105">Происходит при изменении состояния сетевого подключения устройства.</span><span class="sxs-lookup"><span data-stu-id="77b82-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b82-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77b82-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="77b82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77b82-107">Parameters</span></span>

<span data-ttu-id="77b82-108">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="77b82-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77b82-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77b82-109">Return value</span></span>

<span data-ttu-id="77b82-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="77b82-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77b82-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77b82-111">Remarks</span></span>

<span data-ttu-id="77b82-112">Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) с помощью метода [**Add \_ коннектионстатусчанжед**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="77b82-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="77b82-113">Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ коннектионстатусчанжед**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="77b82-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 