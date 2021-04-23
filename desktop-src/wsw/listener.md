---
title: Прослушиватель
description: Клиент использует прослушиватель для приема входящего канала от службы.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Веб-службы прослушивателя для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414196"
---
# <a name="listener"></a><span data-ttu-id="c903a-106">Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="c903a-106">Listener</span></span>

<span data-ttu-id="c903a-107">Клиент использует прослушиватель для приема входящего [канала](channel.md) от службы.</span><span class="sxs-lookup"><span data-stu-id="c903a-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="c903a-108">Чтобы создать прослушивателя, укажите тип канала в виде значения перечисления [**\_ \_ типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , сведения о [привязке](binding.md) и [URL-адрес](url.md) для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="c903a-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="c903a-109">Чтобы начать прослушивание по URL-адресу, вызовите функцию [**всопенлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .</span><span class="sxs-lookup"><span data-stu-id="c903a-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="c903a-110">Чтобы принимать входящие подключения, вызовите [**всакцептчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span><span class="sxs-lookup"><span data-stu-id="c903a-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="c903a-111">Чтобы отменить ожидающие операции ввода-вывода для прослушивателя, вызовите [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span><span class="sxs-lookup"><span data-stu-id="c903a-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="c903a-112">Сведения о переходах состояний для прослушивателя см. в разделе Перечисление [**\_ \_ состояния прослушивателя WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="c903a-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="c903a-113">Следующие обратные вызовы являются частью прослушивателя:</span><span class="sxs-lookup"><span data-stu-id="c903a-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="c903a-114">**\_ \_ обратный вызов прослушивателя WS Abort \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="c903a-115">**\_ \_ обратный вызов приема канала WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="c903a-116">**\_ \_ обратный вызов ПРОСЛУШИВАТЕЛя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="c903a-117">**протокол \_ WS \_ Create \_ Channel \_ для \_ обратного вызова прослушивателя**</span><span class="sxs-lookup"><span data-stu-id="c903a-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="c903a-118">**\_ \_ обратный вызов создания ПРОСЛУШИВАТЕЛя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="c903a-119">**\_ \_ обратный вызов прослушивателя WS Free \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="c903a-120">**\_ \_ \_ обратный вызов свойства прослушивателя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="c903a-121">**\_ \_ обратный вызов прослушивателя WS Open \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="c903a-122">**\_ \_ обратный вызов прослушивателя WS Reset \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="c903a-123">**\_ \_ \_ обратный вызов свойства WS Set Listener \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="c903a-124">Следующие перечисления являются частью прослушивателя:</span><span class="sxs-lookup"><span data-stu-id="c903a-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="c903a-125">**\_версия протокола \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c903a-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="c903a-126">**\_идентификатор свойства прослушивателя WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="c903a-127">**\_Состояние прослушивателя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="c903a-128">Следующие функции являются частью прослушивателя:</span><span class="sxs-lookup"><span data-stu-id="c903a-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="c903a-129">**всабортлистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="c903a-130">**всакцептчаннел**</span><span class="sxs-lookup"><span data-stu-id="c903a-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="c903a-131">**всклоселистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="c903a-132">**вскреателистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="c903a-133">**всфрилистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="c903a-134">**всжетлистенерпроперти**</span><span class="sxs-lookup"><span data-stu-id="c903a-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="c903a-135">**всопенлистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="c903a-136">**всресетлистенер**</span><span class="sxs-lookup"><span data-stu-id="c903a-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="c903a-137">**вссетлистенерпроперти**</span><span class="sxs-lookup"><span data-stu-id="c903a-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="c903a-138">Следующий маркер является частью прослушивателя:</span><span class="sxs-lookup"><span data-stu-id="c903a-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="c903a-139">\_прослушиватель WS</span><span class="sxs-lookup"><span data-stu-id="c903a-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="c903a-140">Следующие структуры являются частью прослушивателя:</span><span class="sxs-lookup"><span data-stu-id="c903a-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="c903a-141">**\_ \_ обратные вызовы настраиваемого ПРОСЛУШИВАТЕЛя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="c903a-142">**\_НЕдопустимые \_ \_ \_ ПОДстроки агента пользователя WS**</span><span class="sxs-lookup"><span data-stu-id="c903a-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="c903a-143">**\_имена узлов \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c903a-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="c903a-144">**\_свойства прослушивателя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="c903a-145">**\_свойство прослушивателя WS \_**</span><span class="sxs-lookup"><span data-stu-id="c903a-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




