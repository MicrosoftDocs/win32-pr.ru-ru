---
title: Сообщение (веб-службы Windows)
description: Сообщение — это объект, инкапсулирующий передаваемые или получаемые данные.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Веб-службы сообщений для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657103"
---
# <a name="message-windows-web-services"></a>Сообщение (веб-службы Windows)

Сообщение — это объект, инкапсулирующий передаваемые или получаемые данные. Структура сообщения определяется SOAP и включает набор заголовков и текст. Заголовки всегда буферизуются в памяти, но текст считывается и записывается с помощью API потоковой передачи.

![Схема, на которой показано сообщение с заголовком, буферизованным и потоком текста.](images/messageenvelope.png)


Сообщения имеют набор свойств, которые можно использовать для указания необязательных параметров, управляющих поведением сообщения, и предоставления способа получения дополнительных сведений о полученных сообщениях (таких как сведения о безопасности). Полный список свойств сообщения см. в разделе [**\_ \_ \_ идентификатор свойства сообщения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .

Сообщение адресовано конкретному [адресу конечной точки](endpoint-address.md).

[**\_ Ошибка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) — это специальное сообщение, используемое для представления ошибок, возвращаемых из удаленной конечной точки.

Сообщения перед передачей преобразуются в кодировку, которая преобразует XML в линейный формат.

Дополнительные сведения о сообщениях см. в разделе [Обзор уровня каналов](channel-layer-overview.md) .

В следующих примерах показано использование сообщений в ВВСАПИ.

| Пример                                              | Описание                                  |
|------------------------------------------------------|----------------------------------------------|
| [кустомхеадерексампле](customheaderexample.md)       | Демонстрирует использование настраиваемых заголовков сообщений.    |
| [мессажеенкодинжексампле](messageencodingexample.md) | Демонстрирует кодирование и декодирование сообщения. |
| [форвардмессажеексампле](forwardmessageexample.md)   | Демонстрирует перенаправление сообщения.            |



 

С сообщениями используются следующие элементы API.

| Обратный вызов                                                        | Описание                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов сообщения WS Done \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Уведомляет вызывающий объект о том, что сообщение завершило использование \_ \_ структуры модуля чтения XML WS, предоставленной функции всреаденвелопестарт, или \_ \_ структуры модуля записи WS XML, предоставленной функции всвритинвелопестарт. |



 



| Перечисление                                                      | Описание                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_версия WS Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Версия спецификации, используемой для заголовков адресации.                                        |
| [**\_Версия конверта WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Версия спецификации, используемой для структуры конверта.                                        |
| [**\_атрибуты заголовка \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Набор флагов, представляющих атрибуты SOAP mustUnderstand и Relay заголовка.                    |
| [**\_тип заголовка \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Тип заголовка.                                                                                  |
| [**\_ \_ Инициализация сообщений WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Указывает, какие заголовки должны добавляться к сообщению [**всинитиализемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) . |
| [**\_ \_ идентификатор свойства сообщения \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | Идентификатор каждого свойства сообщения.                                                                         |
| [**\_состояние сообщения \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Состояние сообщения.                                                                                |



 



| Функция                                                             | Описание                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**всаддрессмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Назначает адрес назначения сообщению.                                                                                                            |
| [**всчеккмустундерстандхеадерс**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Проверяет, должны ли указанные заголовки правильно распознаются получателем.                                                                         |
| [**вскреатемессаже**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Создает экземпляр объекта [ \_ сообщения WS](ws-message.md) .                                                                                         |
| [**вскреатемессажефорчаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Создает сообщение, которое подходит для использования с конкретным каналом.                                                                                 |
| [**всфиллбоди**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Гарантирует наличие достаточного количества байтов, доступных для чтения в сообщении.                                                                |
| [**всфлушбоди**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Очищает все накопленные данные тела сообщения, которые были записаны.                                                                                       |
| [**всфримессаже**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Освобождает ресурс памяти, связанный с сообщением.                                                                                                |
| [**всжеткустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Находит заданный приложением заголовок сообщения и десериализует его.                                                                               |
| [**всжесеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Находит определенный стандартный заголовок в сообщении и десериализует его.                                                                                 |
| [**всжесеадераттрибутес**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Заполняет параметр ULONG [**\_ \_ атрибутами заголовка WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) из элемента Header, на котором расположен модуль чтения. |
| [**всжетмессажепроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Извлекает указанное свойство объекта сообщения.                                                                                                         |
| [**всинитиализемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Инициализирует заголовки для сообщения в процессе подготовки к обработке.                                                                                 |
| [**всмаркхеадерасундерстуд**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Помечает заголовок как понятный приложению.                                                                                                       |
| [**всреадбоди**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Десериализует значение из модуля чтения XML сообщения.                                                                                               |
| [**всреаденвелопинд**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Считывает закрывающие элементы сообщения.                                                                                                               |
| [**всреаденвелопестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Считывает заголовки сообщения и готовится к чтению элементов тела.                                                                               |
| [**всремовекустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Удаляет пользовательский заголовок из сообщения.                                                                                                              |
| [**всремовехеадер**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Удаляет из сообщения [**объект \_ \_ типа**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) "Стандартный" заголовка WS.                                                                 |
| [**всресетмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Возврат состояния сообщения в **\_ состояние WS сообщения \_ \_ Empty**.                                                                                          |
| [**вссесеадер**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Добавляет или заменяет указанный стандартный заголовок в сообщении.                                                                                         |
| [**всвритебоди**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Записывает значение в текст сообщения.                                                                                                               |
| [**всвритинвелопинд**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Записывает закрывающие элементы сообщения.                                                                                                              |
| [**всвритинвелопестарт**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Записывает начало сообщения, включая текущий набор заголовков сообщения, и готовится к записи элементов текста.                           |



 



| Дескриптор                        | Описание                                         |
|-------------------------------|-----------------------------------------------------|
| [\_сообщение WS](ws-message.md) | Непрозрачный тип, используемый для ссылки на объект сообщения. |



 



| Структура                                                | Описание                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_сбой WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Значение ошибки, которое переносится в текст сообщения, что указывает на ошибку обработки. |
| [**\_код ошибки \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Представляет код ошибки.                                                             |
| [**\_Причина сбоя \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Содержит описание ошибки.                                                |
| [**\_Свойства сообщения \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Задает набор структур [**\_ \_ свойств сообщений WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) .  |
| [**\_свойство WS Message \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Задает конкретный параметр сообщения.                                                |



 

 

 




