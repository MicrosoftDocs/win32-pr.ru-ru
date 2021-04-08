---
description: Уведомление об удалении устройства
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Уведомление об удалении устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990302"
---
# <a name="device-removal-notification"></a><span data-ttu-id="a7e1d-103">Уведомление об удалении устройства</span><span class="sxs-lookup"><span data-stu-id="a7e1d-103">Device Removal Notification</span></span>

<span data-ttu-id="a7e1d-104">Если пользователь удаляет самонастраивающийся устройство, используемое графом, диспетчер графа фильтров публикует событие " [**\_ \_ потеря устройства EC**](ec-device-lost.md) ".</span><span class="sxs-lookup"><span data-stu-id="a7e1d-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="a7e1d-105">Если устройство снова станет доступным, диспетчер графа фильтров отправляет другое событие **" \_ \_ потеря устройства EC** ".</span><span class="sxs-lookup"><span data-stu-id="a7e1d-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="a7e1d-106">Однако предыдущее состояние фильтра записи больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="a7e1d-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="a7e1d-107">Приложение должно перестроить граф для использования устройства.</span><span class="sxs-lookup"><span data-stu-id="a7e1d-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="a7e1d-108">DirectShow не отправляет никаких событий при подключении нового устройства.</span><span class="sxs-lookup"><span data-stu-id="a7e1d-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="a7e1d-109">Чтобы узнать, когда доступно новое устройство, приложение может отслеживать \_ окна сообщений WM девицечанже.</span><span class="sxs-lookup"><span data-stu-id="a7e1d-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="a7e1d-110">Дополнительные сведения см. в разделе "Управление устройствами" в документации по Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="a7e1d-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7e1d-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a7e1d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e1d-112">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a7e1d-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



