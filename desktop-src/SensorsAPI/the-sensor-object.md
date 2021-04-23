---
description: Объект датчика представляет определенный датчик.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Объект датчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663795"
---
# <a name="the-sensor-object"></a><span data-ttu-id="bd605-103">Объект датчика</span><span class="sxs-lookup"><span data-stu-id="bd605-103">The Sensor Object</span></span>

<span data-ttu-id="bd605-104">Объект датчика представляет определенный датчик.</span><span class="sxs-lookup"><span data-stu-id="bd605-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="bd605-105">API датчика представляет каждый датчик как объект датчика.</span><span class="sxs-lookup"><span data-stu-id="bd605-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="bd605-106">Вы можете работать с определенным объектом датчика через его интерфейс [**исенсор**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) .</span><span class="sxs-lookup"><span data-stu-id="bd605-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="bd605-107">Этот интерфейс позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bd605-107">This interface enables you to:</span></span>

-   <span data-ttu-id="bd605-108">Получите метаданные о датчике, например его идентификатор, тип или понятное имя.</span><span class="sxs-lookup"><span data-stu-id="bd605-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="bd605-109">Получение сведений о конкретных данных, которые может предоставить датчик.</span><span class="sxs-lookup"><span data-stu-id="bd605-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="bd605-110">Синхронное извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="bd605-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="bd605-111">Получение сведений о состоянии, например о том, готов ли датчик к работе.</span><span class="sxs-lookup"><span data-stu-id="bd605-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="bd605-112">Укажите, какие события будут получены программой.</span><span class="sxs-lookup"><span data-stu-id="bd605-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="bd605-113">Укажите интерфейс обратного вызова, который API-интерфейс датчика может использовать для предоставления программы уведомлениям о событиях.</span><span class="sxs-lookup"><span data-stu-id="bd605-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



