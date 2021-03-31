---
title: Запрос переменных состояния
description: Интерфейс Иупнпсервице предоставляет метод Куеристатевариабле, возвращающий значение заданной переменной состояния.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329592"
---
# <a name="querying-state-variables"></a><span data-ttu-id="997ba-103">Запрос переменных состояния</span><span class="sxs-lookup"><span data-stu-id="997ba-103">Querying State Variables</span></span>

<span data-ttu-id="997ba-104">Интерфейс [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) предоставляет метод [**куеристатевариабле**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , возвращающий значение заданной переменной состояния.</span><span class="sxs-lookup"><span data-stu-id="997ba-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="997ba-105">Форум UPnP не рекомендует использовать [**куеристатевариабле**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="997ba-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="997ba-106">Для предоставления этих сведений разработчикам устройств рекомендуется написать соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="997ba-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="997ba-107">Модули записи устройств не обязаны реализовывать **куеристатевариабле**.</span><span class="sxs-lookup"><span data-stu-id="997ba-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="997ba-108">См. раздел [вызов действий](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="997ba-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




