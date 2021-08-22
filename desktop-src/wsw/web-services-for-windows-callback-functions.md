---
title: Windows Функции обратного вызова веб-служб
description: Обратные вызовы позволяют приложению вызывать функцию, определенную на другом уровне или слое.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926874"
---
# <a name="windows-web-services-callback-functions"></a>Windows Функции обратного вызова веб-служб

Обратные вызовы позволяют приложению вызывать функцию, определенную на другом уровне или слое. Приложение регистрирует аргумент функции в качестве обработчика, который будет вызываться асинхронно позже, как требуется. Обратный вызов вызывается, если функция завершается асинхронно, указывая на успешность или ошибку функции. Обратный вызов не вызывается, если операция завершается синхронно.

API Windows веб-служб включает следующие функции обратного вызова:

-   [**\_ \_ \_ обратный вызов сообщения WS**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**\_ \_ обратный вызов канала WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_ \_ обратный вызов приема канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**\_асинхронная \_ функция WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_ \_ \_ \_ обратный вызов уведомления списка поставщиков \_ сертификатов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**\_ \_ обратный вызов проверки сертификата WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**\_ \_ обратный вызов закрытого канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**\_ \_ обратный вызов ПРОСЛУШИВАТЕЛя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**\_ \_ обратный вызов для создания канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**протокол \_ WS \_ Create \_ Channel \_ для \_ обратного вызова прослушивателя**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_обратный вызов для WS Create \_ декодера \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**\_ \_ обратный вызов кодировщика WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**\_ \_ обратный вызов создания ПРОСЛУШИВАТЕЛя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_ \_ обратный вызов декодирования ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**\_ \_ обратный вызов End ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**\_ \_ \_ \_ обратный вызов типа содержимого декодера WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**\_ \_ обратный вызов для запуска ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**\_ \_ обратный вызов сравнения ДЛИТЕЛЬности WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_ \_ обратный вызов динамической строки WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_ \_ обратный вызов кодирования КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**\_ \_ обратный вызов End КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**\_ \_ \_ \_ обратный вызов типа содержимого кодировщика WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**\_ \_ обратный вызов КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**\_ \_ обратный вызов бесплатных каналов WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**\_ \_ обратный вызов декодера WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**\_ \_ обратный вызов кодировщика WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_ \_ обратный вызов сертификата WS Get \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**\_ \_ \_ обратный вызов свойства WS Get Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**\_ \_ \_ обратный вызов свойства прослушивателя WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_ \_ обратный вызов перенаправления HTTP WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ является \_ \_ \_ обратным вызовом значения по умолчанию**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**\_ \_ обратный вызов сообщения WS Done \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**\_ \_ обратный вызов Open Channel WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_ \_ обратный вызов операции WS Cancel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**\_ \_ \_ обратный вызов свободного состояния WS Operation \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_ \_ обратный вызов сообщения прокси-сервера WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**\_ \_ обратный вызов по запросу WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_ \_ обратный вызов push-уведомлений WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_ \_ обратный вызов WS Read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**\_ \_ \_ обратный вызов конца сообщения WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**\_ \_ \_ обратный вызов начала чтения сообщения WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**\_ \_ обратный вызов типа WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_ \_ обратный вызов для сброса канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**\_ \_ обратный вызов прослушивателя WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_ \_ \_ обратный вызов для приема канала службы \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**\_ \_ \_ обратный вызов для закрытия канала службы \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**\_ \_ \_ \_ ответный вызов получения сообщения службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_ \_ обратный вызов безопасности службы WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_ \_ обратный вызов заглушки службы WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**\_ \_ \_ обратный вызов свойства WS Set Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**\_ \_ \_ обратный вызов свойства WS Set Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**\_ \_ \_ обратный вызов канала сеанса WS Shutdown \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**\_ \_ обратный вызов проверки пароля WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**\_ \_ \_ обратный вызов функции WS Validate SAML**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**\_ \_ обратный вызов записи WS**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**\_ \_ \_ обратный вызов конца сообщения записи WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**\_ \_ \_ обратный вызов для запуска \_ сообщения записи WS**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**\_ \_ обратный вызов типа записи WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




