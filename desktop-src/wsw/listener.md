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
# <a name="listener"></a>Прослушиватель

Клиент использует прослушиватель для приема входящего [канала](channel.md) от службы.

Чтобы создать прослушивателя, укажите тип канала в виде значения перечисления [**\_ \_ типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , сведения о [привязке](binding.md) и [URL-адрес](url.md) для прослушивания.


Чтобы начать прослушивание по URL-адресу, вызовите функцию [**всопенлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .

Чтобы принимать входящие подключения, вызовите [**всакцептчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Чтобы отменить ожидающие операции ввода-вывода для прослушивателя, вызовите [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Сведения о переходах состояний для прослушивателя см. в разделе Перечисление [**\_ \_ состояния прослушивателя WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

Следующие обратные вызовы являются частью прослушивателя:

-   [**\_ \_ обратный вызов прослушивателя WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_ \_ обратный вызов приема канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_ \_ обратный вызов ПРОСЛУШИВАТЕЛя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**протокол \_ WS \_ Create \_ Channel \_ для \_ обратного вызова прослушивателя**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_ \_ обратный вызов создания ПРОСЛУШИВАТЕЛя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_ \_ \_ обратный вызов свойства прослушивателя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_ \_ \_ обратный вызов свойства WS Set Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Следующие перечисления являются частью прослушивателя:

-   [**\_версия протокола \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**\_идентификатор свойства прослушивателя WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**\_Состояние прослушивателя WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Следующие функции являются частью прослушивателя:

-   [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**всакцептчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**всклоселистенер**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**вскреателистенер**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**всфрилистенер**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**всжетлистенерпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**всопенлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**всресетлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**вссетлистенерпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

Следующий маркер является частью прослушивателя:

-   [\_прослушиватель WS](ws-listener.md)

Следующие структуры являются частью прослушивателя:

-   [**\_ \_ обратные вызовы настраиваемого ПРОСЛУШИВАТЕЛя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_НЕдопустимые \_ \_ \_ ПОДстроки агента пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_имена узлов \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**\_свойства прослушивателя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**\_свойство прослушивателя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




