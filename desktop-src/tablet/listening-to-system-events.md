---
description: Приложения могут прослушивать системные события с помощью объекта InkCollector и ожидать на нем событие Системжестуре.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Прослушивание системных событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081540"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="0632f-103">Прослушивание системных событий</span><span class="sxs-lookup"><span data-stu-id="0632f-103">Listening to System Events</span></span>

<span data-ttu-id="0632f-104">Приложения могут прослушивать системные события с помощью объекта [**InkCollector**](inkcollector-class.md) и ожидать на нем событие [**системжестуре**](inkcollector-systemgesture.md) .</span><span class="sxs-lookup"><span data-stu-id="0632f-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="0632f-105">Вы можете задать события, которые прослушивает приложение.</span><span class="sxs-lookup"><span data-stu-id="0632f-105">You can set which events an application listens to.</span></span> <span data-ttu-id="0632f-106">При выполнении действия планшетного пера соответствующее событие **системжестуре** отправляется в приложение на объекте **InkCollector** .</span><span class="sxs-lookup"><span data-stu-id="0632f-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="0632f-107">Приложение может отменить сообщение мыши, соответствующее заданному событию **системжестуре** при получении события.</span><span class="sxs-lookup"><span data-stu-id="0632f-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="0632f-108">Дополнительные сведения об отмене сообщений мыши см. в разделе **системжестуре** Event.</span><span class="sxs-lookup"><span data-stu-id="0632f-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



