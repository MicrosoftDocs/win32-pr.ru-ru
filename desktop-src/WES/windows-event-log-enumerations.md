---
title: Перечисления журнала событий Windows
description: В журнале событий Windows определяются следующие перечисления.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691319"
---
# <a name="windows-event-log-enumerations"></a>Перечисления журнала событий Windows

В журнале событий Windows определяются следующие перечисления.



| Перечисление                                                                          | Описание                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ тип тактового сигнала для канала evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Определяет значения, указывающие тип отметки времени, используемой при записи в журнал канала событий.                                         |
| [**\_ \_ \_ идентификатор свойства конфигурации канала \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Определяет идентификаторы, определяющие свойства конфигурации канала.                                                   |
| [**\_ \_ тип изоляции канала \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Определяет разрешения на доступ по умолчанию, применяемые к каналу.                                                                    |
| [**\_ \_ Флаги ссылки на канал evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Определяет значения, указывающие, как осуществляется ссылка на канал.                                                                       |
| [**\_ \_ тип идентификатора безопасности канала evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Определяет значения, определяющие, включает ли событие идентификатор безопасности (SID) участника, который зарегистрировал событие. |
| [**\_Тип канала \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Определяет тип канала.                                                                                                     |
| [**\_ \_ \_ ИД свойства метаданных события \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Определяет идентификаторы, определяющие свойства метаданных определения события.                                              |
| [**\_ \_ ИД свойства события \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Определяет значения, определяющие получаемые сведения о запросе.                                                               |
| [**\_ \_ Флаги експортлог evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Определяет значения, которые указывают, поступают ли события из канала или файла журнала.                                                   |
| [**\_ \_ Флаги сообщения формата evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Определяет значения, указывающие строку сообщения из события для форматирования.                                                       |
| [**\_ \_ идентификатор свойства журнала \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Определяет идентификаторы, определяющие свойства метаданных файла журнала канала или файла журнала.                                   |
| [**\_класс входа \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Определяет типы методов подключения, которые можно использовать для подключения к удаленному компьютеру.                                             |
| [**\_ \_ Флаги журнала открытия evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Определяет значения, указывающие, следует ли открывать канал или экспортированный файл журнала.                                                    |
| [**\_ \_ \_ ИД свойства метаданных издателя \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Определяет идентификаторы, определяющие свойства метаданных поставщика.                                                       |
| [**\_ \_ флаги запроса evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Определяет значения, указывающие, как вернуть результаты запроса и выполняется ли запрос к каналу или файлу журнала.           |
| [**\_ \_ ИД свойства запроса \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Определяет идентификаторы, которые определяют сведения о запросе, которые можно получить.                                                 |
| [**\_ \_ Флаги контекста ПРОРИСОВКи evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Определяет значения, указывающие тип сведений, к которым осуществляется доступ из события.                                                  |
| [**\_Флаги рендеринга evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Определяет значения, указывающие, что следует визуализировать.                                                                                    |
| [**\_ \_ флаги имени входа для RPC evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Определяет типы проверки подлинности, которые можно использовать для проверки подлинности пользователя при подключении к удаленному компьютеру.                |
| [**\_ \_ Флаги поиска evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Определяет относительное положение в результирующем наборе, из которого будет осуществляться поиск.                                                                |
| [**\_ \_ Флаги подписки evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Определяет возможные значения, указывающие время начала подписки на события.                                                      |
| [**\_ \_ действие уведомления подписки \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Определяет возможные типы данных, которые служба подписки может доставлять в ответный вызов.                                     |
| [**\_идентификатор системного \_ свойства \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Определяет идентификаторы, которые определяют системные свойства события.                                                   |
| [**\_тип варианта \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Определяет возможные типы данных для элемента данных типа Variant.                                                                            |



 

 

 




