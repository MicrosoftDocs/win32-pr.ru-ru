---
title: привязка каналов
description: Привязки указывают протокол передачи и локальное поведение канала.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Привязка веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330496"
---
# <a name="channel-binding"></a><span data-ttu-id="cb39c-106">привязка каналов</span><span class="sxs-lookup"><span data-stu-id="cb39c-106">Channel Binding</span></span>

<span data-ttu-id="cb39c-107">Привязки указывают протокол передачи и локальное поведение канала.</span><span class="sxs-lookup"><span data-stu-id="cb39c-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="cb39c-108">Привязки состоят из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="cb39c-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="cb39c-109">[**\_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), которая определяет используемый протокол передачи.</span><span class="sxs-lookup"><span data-stu-id="cb39c-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="cb39c-110">[**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), которое указывает, как защитить канал.</span><span class="sxs-lookup"><span data-stu-id="cb39c-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="cb39c-111">Задает [**\_ \_ Свойства канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), которые указывают дополнительные необязательные параметры (см. [**также \_ \_ \_ идентификатор свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span><span class="sxs-lookup"><span data-stu-id="cb39c-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




