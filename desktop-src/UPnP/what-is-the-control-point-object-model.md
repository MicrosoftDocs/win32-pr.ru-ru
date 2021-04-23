---
title: Что такое объектная модель точки управления
description: На следующем рисунке показана базовая объектная модель контрольной точки.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332443"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="88e35-103">Что такое объектная модель контрольной точки?</span><span class="sxs-lookup"><span data-stu-id="88e35-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="88e35-104">На следующем рисунке показана базовая объектная модель контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="88e35-104">The following illustration shows the basic Control Point object model.</span></span>

![Объектная модель точки управления](images/upnp-object-model.png)

<span data-ttu-id="88e35-106">Поиск устройств с помощью интерфейса поиска устройств создает коллекцию устройств.</span><span class="sxs-lookup"><span data-stu-id="88e35-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="88e35-107">Коллекция устройств содержит ноль или более объектов устройств.</span><span class="sxs-lookup"><span data-stu-id="88e35-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="88e35-108">Приложения могут использовать различные методы коллекции устройств для доступа к отдельным объектам устройств.</span><span class="sxs-lookup"><span data-stu-id="88e35-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="88e35-109">Объекты устройств всегда содержат коллекцию служб, содержащую один или несколько объектов службы.</span><span class="sxs-lookup"><span data-stu-id="88e35-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="88e35-110">Эти объекты службы используются приложениями для взаимодействия с устройствами и управления им.</span><span class="sxs-lookup"><span data-stu-id="88e35-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




