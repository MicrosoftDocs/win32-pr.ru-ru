---
title: Перечисление зарегистрированных сущностей
description: После регистрации клиента Клиент может получить список всех других клиентов, зарегистрированных в диспетчере таблиц маршрутизации. Некоторые клиенты должны выполнять определенные операции, если обнаружено присутствие определенного типа клиента.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068025"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="d134f-104">Перечисление зарегистрированных сущностей</span><span class="sxs-lookup"><span data-stu-id="d134f-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="d134f-105">После регистрации клиента Клиент может получить список всех других клиентов, зарегистрированных в диспетчере таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d134f-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="d134f-106">Некоторые клиенты должны выполнять определенные операции, если обнаружено присутствие определенного типа клиента.</span><span class="sxs-lookup"><span data-stu-id="d134f-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="d134f-107">Клиент может вызвать функцию [**ртмжетрегистередентитиес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) .</span><span class="sxs-lookup"><span data-stu-id="d134f-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="d134f-108">Возвращается буфер структур [**\_ \_ сведений сущности RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="d134f-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="d134f-109">После того как клиент обработал эту информацию, клиент должен вызвать [**ртмрелеасинтитиес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) , чтобы освободить дескрипторы в структурах **\_ \_ сведений о сущности RTM** .</span><span class="sxs-lookup"><span data-stu-id="d134f-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="d134f-110">Если клиент диспетчера таблиц маршрутизации представил функцию обратного вызова в вызове [**ртмрегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), клиент получает уведомления при регистрации или отмене регистрации других клиентов.</span><span class="sxs-lookup"><span data-stu-id="d134f-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="d134f-111">Пример кода, демонстрирующий использование этих функций, см. в разделе [перечисление зарегистрированных сущностей](enumerate-the-registered-entities.md) и [Использование обратного вызова уведомления о событиях](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="d134f-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




