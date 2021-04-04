---
title: Канал (веб-службы Windows)
description: Каналы инкапсулируют контекст связи между двумя или более сторонами и используются для отправки и получения сообщений.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Веб-службы канала для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93819057f2de4ecf82b2def9cdc4fe14dd1b0ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103988123"
---
# <a name="channel-windows-web-services"></a>Канал (веб-службы Windows)

Каналы инкапсулируют контекст связи между двумя или более сторонами и используются для отправки и получения сообщений.


На клиенте используйте [**вскреатечаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) для создания канала. На сервере используйте [**вскреатечаннелфорлистенер**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) , чтобы создать канал, который может быть принят клиентом с помощью [прослушивателя](listener.md).

При создании канала необходимо указать следующие сведения, определяющие локальное поведение канала и используемый протокол передачи данных.

-   [**\_ \_ Тип канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), который определяет шаблон обмена сообщениями для канала.
-   [**\_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), которая определяет используемый протокол передачи.
-   [**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), которое указывает безопасность, используемую для канала. При создании каналов для использования на сервере этот параметр указывается один раз для всех каналов, которые будут приниматься для данного прослушивателя.
-   Задать [**\_ \_ Свойства канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), которые указывают дополнительные необязательные параметры (список этих параметров см. в разделе перечисления [**\_ \_ \_ идентификаторов свойств канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Прежде чем использовать канал, его необходимо открыть, вызвав функцию [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) и указав адрес канала и [конечной точки](endpoint-address.md)вместе с другими дополнительными сведениями.

Сведения о переходах состояний для канала см. в разделе " [**состояния каналов**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) ".

Дополнительные сведения о каналах см. в разделе [Обзор уровня каналов](channel-layer-overview.md) .

С каналами используются следующие элементы API.

| Обратный вызов                                                                                  | Описание                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ обратный вызов сообщения WS**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Обрабатывает вызов [**всабандонмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) для канала с пользовательской привязкой канала.                                              |
| [**\_ \_ обратный вызов канала WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Обрабатывает вызов [**всабортчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) для канала с пользовательской привязкой канала.                                                  |
| [**\_ \_ обратный вызов закрытого канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Обрабатывает вызов [**всклосечаннел**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) для канала с пользовательской привязкой канала.                                                  |
| [**\_ \_ обратный вызов для создания канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Обрабатывает вызов [**всклосечаннел**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) для канала с пользовательской привязкой канала.                                                  |
| [**\_обратный вызов для WS Create \_ декодера \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Обрабатывает создание экземпляра декодера.                                                                                                                  |
| [**\_ \_ обратный вызов кодировщика WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Обрабатывает создание экземпляра кодировщика.                                                                                                                 |
| [**\_ \_ обратный вызов декодирования ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Декодирует сообщение.                                                                                                                                    |
| [**\_ \_ обратный вызов End ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Декодирует конец сообщения.                                                                                                                         |
| [**\_ \_ \_ \_ обратный вызов типа содержимого декодера WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Возвращает тип источника сообщения.                                                                                                                 |
| [**\_ \_ обратный вызов для запуска ДЕКОДЕРа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Начинает декодировать сообщение.                                                                                                                            |
| [**\_ \_ обратный вызов кодирования КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Кодирует сообщение.                                                                                                                                    |
| [**\_ \_ обратный вызов End КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Кодирует конец сообщения.                                                                                                                         |
| [**\_ \_ \_ \_ обратный вызов типа содержимого кодировщика WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Возвращает тип источника сообщения.                                                                                                                 |
| [**\_ \_ обратный вызов КОДИРОВЩИКа WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Начинает кодирование сообщения.                                                                                                                            |
| [**\_ \_ обратный вызов бесплатных каналов WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Обрабатывает вызов [**всфричаннел**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) для канала с пользовательской привязкой канала.                                                    |
| [**\_ \_ обратный вызов декодера WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Обрабатывает освобождение экземпляра декодера.                                                                                                                   |
| [**\_ \_ обратный вызов кодировщика WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Обрабатывает освобождение экземпляра кодировщика.                                                                                                                  |
| [**\_ \_ \_ обратный вызов свойства WS Get Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Обрабатывает вызов [**всжетчаннелпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) для канала с пользовательской привязкой канала.                                      |
| [**\_ \_ обратный вызов перенаправления HTTP WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Вызывается, когда сообщение собирается автоматически перенаправляться в другую службу с использованием функции автоматического перенаправления HTTP, как описано в RFC2616. |
| [**\_ \_ обратный вызов Open Channel WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Обрабатывает вызов [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) для канала с пользовательской привязкой канала.                                                    |
| [**\_ \_ \_ обратный вызов конца сообщения WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Обрабатывает вызов [**всреадмессажеенд**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) для канала с пользовательской привязкой канала.                                              |
| [**\_ \_ \_ обратный вызов начала чтения сообщения WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Обрабатывает вызов [**всреадмессажеенд**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) для канала с пользовательской привязкой канала.                                              |
| [**\_ \_ обратный вызов для сброса канала WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Обрабатывает вызов [**всресетчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) для канала с пользовательской привязкой канала.                                                  |
| [**\_ \_ \_ обратный вызов свойства WS Set Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Обрабатывает вызов [**вссетчаннелпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) для канала с пользовательской привязкой канала.                                      |
| [**\_ \_ \_ обратный вызов канала сеанса WS Shutdown \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Обрабатывает вызов [**всшутдовнсессиончаннел**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) для канала с пользовательской привязкой канала.                              |
| [**\_ \_ \_ обратный вызов конца сообщения записи WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Обрабатывает вызов [**всвритемессажеенд**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) для канала с пользовательской привязкой канала.                                            |
| [**\_ \_ \_ обратный вызов для запуска \_ сообщения записи WS**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Обрабатывает вызов [**всвритемессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) для канала с пользовательской привязкой канала.                                        |



 



| Перечисление                                                 | Описание                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Привязка канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Указывает стек протокола, используемый для канала.                                                                                      |
| [**\_ \_ идентификатор свойства канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Идентифицирует каждое свойство канала по ИДЕНТИФИКАТОРу.                                                                                                |
| [**\_состояние канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Состояние канала.                                                                                                                 |
| [**\_Тип канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Указывает основные характеристики канала, например, является ли он сеансом и какие направления взаимодействия поддерживаются. |
| [**\_Кодировка WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Различные кодировки (форматы сообщений).                                                                                                |
| [**\_параметр получения \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Указывает, требуется ли сообщение при получении из канала.                                                                    |
| [**\_режим пересылки WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Указывает, являются ли отправленные или получаемые сообщения потоковой или буферизованными.                                                            |



 



| Функция                                                         | Описание                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**всабандонмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Пропускает оставшуюся часть сообщения для канала.                                                              |
| [**всабортчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Прерывает все ожидающие операции ввода-вывода в указанном канале и устанавливает состояние канала в состояние **WS \_ канала с \_ \_ ошибкой**. |
| [**всклосечаннел**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Закрывает канал, когда он больше не нужен.                                                                |
| [**вскреатечаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Создает канал.                                                                                           |
| [**вскреатечаннелфорлистенер**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Создает канал для прослушивателя.                                                                            |
| [**всфричаннел**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Освобождает ресурсы памяти, связанные с каналом.                                                     |
| [**всжетчаннелпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Извлекает свойство канала, на которое ссылается параметр канала.                                     |
| [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Открывает канал для конечной точки.                                                                              |
| [**всреадмессажеенд**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Считывает закрывающие элементы сообщения из канала.                                                      |
| [**всреадмессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Считывает заголовки следующего сообщения из канала и готовится к чтению элементов тела.               |
| [**всрецеивемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Получает сообщение и десериализует текст сообщения в виде значения.                                      |
| [**всрекуестрепли**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Отправляет сообщение запроса и получает коррелированное ответное сообщение.                                             |
| [**всресетчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Сбросьте канал, чтобы его можно было использовать повторно.                                                                         |
| [**вссендмессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Отправляет сообщение по каналу, используя сериализацию для записи элемента Body.                                  |
| [**вссендреплимессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Отправляет сообщение, которое является ответом на полученное сообщение.                                                       |
| [**вссетчаннелпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Задает свойство канала.                                                                                |
| [**вссетмессажепроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Задает свойство сообщения.                                                                                |
| [**всвритемессажеенд**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Записывает закрывающие элементы сообщения в канал.                                                     |
| [**всвритемессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Запишите заголовки сообщения в канал и подготовится к записи элементов текста.                   |



 



| Дескриптор                        | Описание                                 |
|-------------------------------|---------------------------------------------|
| [\_канал WS](ws-channel.md) | Непрозрачный тип, используемый для ссылки на канал. |



 



| Структура                                                                          | Описание                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_декодер каналов \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Набор обратных вызовов, которые преобразуют тип содержимого и закодированные байты полученного сообщения.                                                                                                      |
| [**\_кодировщик канала \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Набор обратных вызовов, которые могут преобразовывать тип содержимого и закодированные байты отправленного сообщения.                                                                                                      |
| [**\_Свойства канала \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Набор структур [**\_ \_ свойств канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) .                                                                                                                        |
| [**\_свойство канала \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Параметр, зависящий от канала.                                                                                                                                                                      |
| [**\_пользовательские \_ \_ обратные вызовы канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Набор обратных вызовов, образующих реализацию пользовательского канала.                                                                                                                             |
| [**\_настраиваемый \_ \_ прокси-сервер HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | используется для указания настраиваемого прокси-сервера для канала с использованием **\_ \_ \_ настраиваемого значения \_ HTTP-прокси свойства канала** WS \_ для перечисления [**\_ \_ \_ идентификаторов свойств канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) . |
| [**\_ \_ сопоставление заголовка WS \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Представляет отдельный заголовок, сопоставленный как часть [**\_ \_ \_ сопоставления сообщений HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**\_сопоставление HTTP- \_ сообщений \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Сведения о том, как HTTP-запрос или ответ должен быть представлен в объекте сообщения.                                                                                                     |
| [**\_ \_ \_ контекст обратного вызова ПЕРЕнаправления HTTP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Указывает функцию обратного вызова и состояние для управления поведением автоматического перенаправления HTTP.                                                                                               |
| [**\_Описание сообщения \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Схема для входного и выходного [ \_ сообщения WS](ws-message.md) для данного описания операции.                                                                                             |



 

 

 




