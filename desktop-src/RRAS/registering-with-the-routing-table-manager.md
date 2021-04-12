---
title: Регистрация в диспетчере таблиц маршрутизации
description: Прежде чем клиент сможет получить доступ к таблице маршрутизации, сначала необходимо зарегистрировать диспетчер таблиц маршрутизации с помощью функции Ртмрегистерентити.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Диспетчер таблиц маршрутизации версия 2 RRAS, регистрация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253199"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="8e208-104">Регистрация в диспетчере таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="8e208-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="8e208-105">Прежде чем клиент сможет получить доступ к таблице маршрутизации, сначала необходимо зарегистрировать диспетчер таблиц маршрутизации с помощью функции [**ртмрегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .</span><span class="sxs-lookup"><span data-stu-id="8e208-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="8e208-106">Когда клиент регистрируется, он передается в диспетчер таблиц маршрутизации к структуре [**\_ \_ сведений об сущности RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="8e208-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="8e208-107">Эта структура содержит сведения, которые однозначно идентифицируют клиента, семейство адресов и экземпляр диспетчера таблиц маршрутизации, с которым регистрируется клиент.</span><span class="sxs-lookup"><span data-stu-id="8e208-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="8e208-108">Клиент также может установить обратный вызов [**\_ \_ обратного вызова для события RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) .</span><span class="sxs-lookup"><span data-stu-id="8e208-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="8e208-109">Диспетчер таблиц маршрутизации будет использовать этот обратный вызов для уведомления клиента о событиях, таких как уведомления об изменениях и регистрации клиентов.</span><span class="sxs-lookup"><span data-stu-id="8e208-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="8e208-110">Диспетчер таблиц маршрутизации завершает свою обработку регистрации и возвращает клиенту маркер.</span><span class="sxs-lookup"><span data-stu-id="8e208-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="8e208-111">Клиент должен использовать этот обработчик для всех последующих вызовов функций RTMv2.</span><span class="sxs-lookup"><span data-stu-id="8e208-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="8e208-112">Функция [**ртмрегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) , используемая в RTMv2, аналогична функции [**ртмрегистерклиент**](rtmregisterclient.md) , которая используется в RTMv1.</span><span class="sxs-lookup"><span data-stu-id="8e208-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="8e208-113">Функция **ртмрегистерклиент** устарела, за исключением клиентов, использующих протокол IPX.</span><span class="sxs-lookup"><span data-stu-id="8e208-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="8e208-114">После того как клиент завершит взаимодействие с диспетчером таблиц маршрутизации, он должен вызвать [**ртмдерегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span><span class="sxs-lookup"><span data-stu-id="8e208-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="8e208-115">Диспетчер таблиц маршрутизации уничтожает связанный с клиентом маркер.</span><span class="sxs-lookup"><span data-stu-id="8e208-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="8e208-116">Чтобы избежать утечек памяти, клиент должен убедиться, что он освобождает все дескрипторы и все маршруты и следующие прыжки, которыми он владеет, перед вызовом **ртмдерегистерентити**.</span><span class="sxs-lookup"><span data-stu-id="8e208-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="8e208-117">Пример кода, демонстрирующий использование этих функций, см. в разделе [Регистрация в диспетчере таблиц маршрутизации](register-with-the-routing-table-manager.md) и [Использование обратного вызова уведомления о событиях](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="8e208-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




