---
description: API датчика может предоставлять уведомления о событиях.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Сведения о событиях API датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912239"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="262d6-103">Сведения о событиях API датчика</span><span class="sxs-lookup"><span data-stu-id="262d6-103">About Sensor API Events</span></span>

<span data-ttu-id="262d6-104">API датчика может предоставлять уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="262d6-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="262d6-105">При регистрации для получения событий с помощью [**исенсор:: сетевентсинк**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) или [**Исенсорманажер:: сетевентсинк**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)необходимо предоставить указатель на интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="262d6-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="262d6-106">В коде необходимо реализовать методы интерфейса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="262d6-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="262d6-107">API датчика определяет следующие интерфейсы обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="262d6-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="262d6-108">[**Исенсоревентс**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="262d6-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="262d6-109">Реализуйте этот интерфейс для получения событий от датчиков.</span><span class="sxs-lookup"><span data-stu-id="262d6-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="262d6-110">Датчики могут уведомлять ваше приложение о новых данных, изменениях состояния датчика, отключении датчика и пользовательских событиях, определенных производителем датчика.</span><span class="sxs-lookup"><span data-stu-id="262d6-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="262d6-111">[**Исенсорманажеревентс**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="262d6-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="262d6-112">Реализуйте этот интерфейс для получения событий от диспетчера датчиков.</span><span class="sxs-lookup"><span data-stu-id="262d6-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="262d6-113">Диспетчер датчиков может уведомлять приложение при подключении датчика и, следовательно, может быть доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="262d6-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="262d6-114">Вы можете отменить уведомления о событиях, вызвав [**сетевентсинк**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) еще раз. это время передает значение **null** через параметр.</span><span class="sxs-lookup"><span data-stu-id="262d6-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="262d6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="262d6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="262d6-116">Использование событий API датчика</span><span class="sxs-lookup"><span data-stu-id="262d6-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
