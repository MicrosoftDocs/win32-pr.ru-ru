---
title: Обзор уровня канала
description: Уровень канала предоставляет абстракцию транспортного канала, а также сообщения, отправленные по каналу.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Обзор уровня канала веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104552915"
---
# <a name="channel-layer-overview"></a>Обзор уровня канала

Уровень канала предоставляет абстракцию транспортного канала, а также сообщения, отправленные по каналу. Он также включает функции для сериализации типов данных C в структуры SOAP и обратно. Уровень канала обеспечивает полный контроль взаимодействия с помощью [сообщений](message.md) , состоящих из отправленных или полученных данных и содержащих тексты и заголовки, а также [каналов](channel.md) , которые являются абстрактными протоколами обмена сообщениями и предоставляют свойства для настройки параметров.

## <a name="message"></a>Сообщение

[Сообщение](message.md) — это объект, инкапсулирующий сетевые данные, а именно данные, передаваемые или получаемые по сети. Структура сообщения определяется протоколом SOAP с дискретным набором заголовков и текстом сообщения. Заголовки помещаются в буфер памяти, а текст сообщения считывается или записывается с помощью API потока.

![Схема, показывающая заголовок и текст сообщения.](images/messageenvelope.png)

Несмотря на то, что модель данных сообщения всегда является моделью XML-данных, реальный формат сети является гибким. Перед передачей сообщения оно кодируется с использованием определенной кодировки (например, текста, двоичного файла или MTOM). Дополнительные сведения о кодировках см. в разделе [**\_ Кодировка WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .

![Схема, в которой показаны несколько форматов кодирования сообщений.](images/messageandencodings.png)

## <a name="channel"></a>Канал

[Канал](channel.md) — это объект, используемый для отправки и получения сообщений в сети между двумя или более конечными точками.

Каналы имеют связанные данные, описывающие способ [адресации](endpoint-address.md) сообщения при его отправке. Отправка сообщения по каналу аналогично размещению его в желобе — канал включает сведения, куда должно попасть сообщение, и способ его получения.

![Диаграмма, на которой показаны каналы для сообщений.](images/channelsaschute.png)

Каналы подразделяются на [**типы каналов**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Тип канала указывает, какие направления сообщений могут поступать. Тип канала также определяет, является ли канал сеансом или безсеансом. Сеанс определяется как абстрактный способ корреляции сообщений между двумя или более сторонами. Примером канала сеанса является TCP-канал, который использует TCP-соединение в качестве реализации конкретного сеанса. Примером бессеансового канала является UDP, который не имеет базового механизма сеанса. Хотя HTTP имеет базовые TCP-подключения, этот факт не предоставляется напрямую через этот API, поэтому HTTP также считается каналом без сеанса.

![Схема, в которой показаны типы каналов с сеансами и сеансами.](images/channeltypes.png)

Несмотря на то, что типы каналов описывают направление и сведения о сеансе для канала, они не указывают способ реализации канала. Какой протокол должен использоваться каналом? Насколько трудно, чтобы канал попытается доставить сообщение? Какой тип безопасности используется? Является ли он одиночным или многоадресным? Эти параметры называются "привязкой" канала. Привязка состоит из следующих элементов:

-   [**\_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), которая определяет используемый протокол передачи (TCP, UDP, HTTP, помощью канала NamedPipe).
-   [**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), которое указывает, как защитить канал.
-   Задает [**\_ \_ Свойства канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), которые указывают дополнительные необязательные параметры. Список свойств см. в разделе [**\_ \_ \_ идентификатор свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .

![Схема, показывающая список свойств канала.](images/channelsandbindings.png)

## <a name="listener"></a>Прослушиватель

Чтобы начать обмен данными, клиент создает объект канала. Но как служба получает объект канала? Для этого создается [прослушиватель](listener.md). Для создания прослушивателя требуются те же сведения о привязке, которые необходимы для создания канала. После создания прослушивателя приложение может принимать каналы от прослушивателя. Так как приложение может относиться к приему каналов, прослушиватели обычно сохраняют в очереди каналы, готовые к приему (до некоторой квоты).

![Схема, показывающая каналы в очереди прослушивателя.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Инициирующая связь (клиент)

Чтобы инициировать обмен данными на клиенте, используйте следующую последовательность.

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a>Принятие связи (сервер)

Чтобы принимать входящие подключения на сервере, используйте следующую последовательность.

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a>Отправка сообщений (клиент или сервер)

Для отправки сообщений используйте следующую последовательность.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

Функция [**вссендмессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) не поддерживает потоковую передачу и предполагает, что текст содержит только один элемент. Чтобы избежать этих ограничений, используйте следующую последовательность, а не **вссендмессаже**.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

Функция [**всвритебоди**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) использует сериализацию для записи элементов тела. Для записи данных непосредственно в модуль записи XML используйте следующую последовательность, а не **всвритебоди**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

Функция [**всаддкустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) использует сериализацию для установки заголовков в буфер заголовков сообщения. Чтобы использовать модуль записи XML для записи заголовка, используйте следующую последовательность, а не **всаддкустомхеадер**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Получение сообщений (клиент или сервер)

Для получения сообщений используйте следующую последовательность.

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

Функция [**всрецеивемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) не поддерживает потоковую передачу и предполагает, что текст содержит только один элемент, и что тип сообщения (действие и схема тела) известен заранее. Чтобы избежать этих ограничений, используйте следующую последовательность, а не **всрецеивемессаже**.

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

Функция [**всреадбоди**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) использует сериализацию для чтения элементов тела. Для чтения данных непосредственно из [средства чтения XML](xml-reader.md)используйте следующую последовательность, а не **всреадбоди**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Функции [**всжеткустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) используют сериализацию для получения заголовков из буфера заголовков сообщения. Чтобы использовать [средство чтения XML](xml-reader.md) для чтения заголовка, используйте следующую последовательность, а не **всжеткустомхеадер**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a>Ответ на запрос (клиент)

Запрос-ответ на клиенте можно выполнить с помощью следующей последовательности.

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

Функция [**всрекуестрепли**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) предполагает наличие одного элемента для текста сообщения запроса и ответа, а также то, что тип сообщения (действие и схема тела) известен заранее. Чтобы избежать этих ограничений, сообщение запроса и ответа можно отправить вручную, как показано в следующей последовательности. Эта последовательность соответствует предыдущей последовательности для отправки и получения сообщения, за исключением случаев, когда отмечено.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a>Запрос ответа (сервер)

Чтобы получить сообщение запроса на сервере, используйте ту же последовательность, которая описана в предыдущем разделе о получении сообщений.

Чтобы отправить ответ или сообщение об ошибке, используйте следующую последовательность.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

Функция [**вссендреплимессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) предполагает наличие одного элемента в теле и не допускает потоковой передачи. Чтобы избежать этих ограничений, используйте следующую последовательность. Это то же самое, что и Предыдущая последовательность отправки сообщения, но при инициализации использует [**\_ \_ сообщение ответа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) вместо **WS \_ Blank \_** .

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a>Шаблоны обмена сообщениями

[**\_ \_ Тип канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) определяет шаблон обмена сообщениями для данного канала. Поддерживаемый тип, зависит от привязки, как показано ниже.

-   [**Служба WS \_ \_ \_ Привязка канала HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ \_ \_ запрос типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) для клиента и **\_ \_ \_ ответа типа WS-канала** на сервере.
-   [**Служба WS \_ \_ \_ Привязка TCP-канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ многоканальный \_ \_ \_ сеанс связи типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) на клиенте и на сервере **\_ канале \_ \_ двустороннего \_ подключения типа WS** .
-   [**Служба WS \_ \_ \_ Привязка канала UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ канал WS \_ типа " \_ дуплекс**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " на клиенте и **\_ \_ тип \_ канала WS** на сервере.
-   [**Служба WS \_ \_ \_ Привязка канала помощью канала NamedPipe**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ канал WS \_ типа " \_ дуплекс**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " на клиенте и **\_ \_ тип \_ канала WS** на сервере.

## <a name="message-loops"></a>Циклы сообщений

Для каждого шаблона обмена сообщениями существует отдельный цикл, который можно использовать для отправки или получения сообщений. В цикле описывается юридический порядок операций, необходимых для отправки и получения нескольких сообщений. Циклы описаны ниже как грамматические продукты. Термин «End» («конец») возвращает значение Where **WS \_ S \_** (см. раздел [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md)), что означает, что на канале больше нет доступных сообщений. Параллельное производство указывает, что для Parallel (x & y) Эта операция x может выполняться параллельно с y.

На клиенте используются следующие циклы.

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

На сервере используются следующие циклы.

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

Для использования [**\_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) на сервере требуется успешное получение, прежде чем отправка будет разрешена даже с каналом [**типа \_ канал \_ WS \_ \_ сеанс дуплекса**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). После первого получения. применяется обычный цикл.

Обратите внимание, что каналы типа " [**\_ \_ \_ запрос типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " и " **\_ \_ Тип канала \_ WS** " можно использовать для отправки и получения односторонних сообщений (а также стандартного шаблона "запрос — ответ"). Это достигается путем закрытия канала ответа без отправки ответа. В этом случае в канале запроса не будет получен ответ. Возвращаемое значение **WS \_ S \_** с использованием [**\_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) на сервере требует успешного получения, прежде чем отправка будет разрешена даже с каналом типа **WS \_ канал типа \_ \_ дуплексного \_ сеанса**. После первого приема используется обычный цикл.

будет возвращено значение, указывающее, что сообщение недоступно.

Циклы клиента или сервера могут выполняться параллельно друг с другом с помощью нескольких экземпляров каналов.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Фильтрация сообщений

Серверный канал может фильтровать полученные сообщения, которые не предназначены для приложения, например сообщения, которые устанавливают [контекст безопасности](security-context.md). В этом случае **Служба \_ WS \_ S** будет возвращена из [**всреадмессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) , а сообщения приложений не будут доступны в этом канале. Однако это не сигнализирует, что клиент предназначен для завершения взаимодействия с сервером. На другом канале могут быть доступны дополнительные сообщения. См. [**всшутдовнсессиончаннел**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Отмена

Функция [**всабортчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) используется для отмены ожидающих ввода-вывода для канала. Этот API не будет ожидать завершения операций ввода-вывода. Дополнительные сведения см. в схеме состояния [**\_ \_ состояния канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) и документации по **всабортчаннел** .

API [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) используется для отмены ожидающих операций ввода-вывода для прослушивателя. Этот API не будет ожидать завершения операций ввода-вывода. Прерывание прослушивателя приведет к прерыванию отложенного приема. Дополнительные сведения см. в схеме состояния [**\_ прослушивателя \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) и **всабортлистенер** .

## <a name="tcp"></a>TCP

[**\_ Привязка TCP- \_ канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через TCP. Спецификация SOAP по TCP строится на основе механизма кадрирования .NET.

Общий доступ к портам не поддерживается в этой версии. Каждый открытый прослушиватель должен использовать другой номер порта.

## <a name="udp"></a>UDP

[**\_ \_ \_ Привязка канала WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через UDP.

Существует ряд ограничений, касающихся привязки UDP:

-   Обеспечение безопасности не поддерживается.
-   Сообщения могут быть потеряны или дублироваться.
-   Поддерживается только одна кодировка: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   Сообщения имеют фундаментальное ограничение до 64 КБ, и часто они теряются, если размер превышает MTU сети.

## <a name="http"></a>HTTP

[**\_ \_ \_ Привязка канала WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через HTTP.

Сведения об управлении заголовками HTTP на клиенте и сервере см. в разделе [**\_ \_ \_ сопоставление HTTP-сообщений WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Для отправки и получения сообщений, не относящихся к протоколу SOAP, на сервере используйте [**\_ кодировку WS \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) для [**\_ \_ \_ кодирования свойств канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>намедпипес

[**\_ \_ \_ Привязка канала WS помощью канала NamedPipe**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через именованные каналы, что позволяет обмениваться данными со службой Windows Communication Foundation (WCF) с помощью NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Корреляция сообщений "запрос-ответ"

Сообщения типа "запрос-ответ" сопоставляются одним из двух способов:

-   Корреляция выполняется с помощью канала в качестве механизма корреляции. Например, при использовании [**\_ \_ \_ транспорта версии WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) и [**\_ \_ \_ привязки канала WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) ответ для сообщения запроса сопоставляется с ЗАПРОСОМ по факту, что это текст сущности HTTP-ответа.
-   Корреляция выполняется с помощью заголовков MessageID и «переводятся». Этот механизм используется с [**WS \_ Addressing \_ Version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) и **WS \_ Addressing \_ Version \_ 0 \_ 9** (даже при [**использовании \_ \_ \_ привязки канала HTTP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). В этом случае сообщение запроса содержит заголовок MessageID. Ответное сообщение содержит заголовок «текст сообщения», содержащий значение заголовка MessageID запроса. Заголовок области отправки позволяет клиенту сопоставить ответ с отправленным запросом.

Следующие интерфейсы API уровня канала автоматически используют соответствующие механизмы корреляции на основе [**\_ \_ версии канала WS Address**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

-   [**всрекуестрепли**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**вссендреплимессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**вссендфаултмессажефореррор**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Если эти API не используются, заголовки можно добавить вручную и получить к ним доступ с помощью [**вссесеадер**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) или [**всжесеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).

## <a name="custom-channels-and-listeners"></a>Пользовательские каналы и прослушиватели

Если предопределенный набор привязок каналов не удовлетворяет потребностям приложения, то реализацию пользовательского канала и прослушивателя можно определить, указав [**\_ настраиваемую \_ \_ привязку каналов WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) при создании канала или прослушивателя. Фактическая реализация канала или прослушивателя задается в виде набора обратных вызовов с [**помощью \_ \_ \_ пользовательских \_ \_ обратных вызовов свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) или свойств [**\_ \_ \_ \_ \_ обратного вызова настраиваемого прослушивателя свойства прослушивателя WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) . После создания пользовательского канала или прослушивателя результатом является объект [WS \_ Channel](ws-channel.md) или [WS- \_ Listener](ws-listener.md) , который можно использовать с существующими API.

Пользовательский канал и прослушиватель также можно использовать с прокси-сервером службы [и узлом службы](service-host.md) , указав **значение \_ \_ \_ привязки настраиваемого канала WS** в перечислении [**\_ \_ привязки WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , а также свойства обратного вызова настраиваемого прослушивателя для свойства [**\_ канала WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) и пользовательского [**\_ \_ \_ \_ \_ обратных вызовов свойства прослушивателя**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) WS при создании прокси службы или узла службы.

## <a name="security"></a>Безопасность

Канал позволяет ограничить объем памяти, используемый для различных аспектов операций, с помощью таких свойств, как:

-   [**Служба WS \_ свойство канала: \_ \_ максимальный \_ \_ \_ Размер буферизованного сообщения**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**Служба WS \_ \_ \_ максимальный \_ \_ \_ Размер потокового сообщения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ максимальный \_ \_ \_ Размер запускаемого потока свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ максимальный \_ \_ \_ \_ \_ Размер буфера заголовков HTTP-запросов для свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**Служба WS \_ \_Максимальное значение \_ \_ \_ \_ размера словаря сеанса для свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Эти свойства имеют значения по умолчанию, которые являются консервативными и безопасными для большинства сценариев. Значения по умолчанию и любые изменения в них следует тщательно оценить по потенциальным направлениям атак, что может привести к отказу в обслуживании удаленного пользователя.

Канал позволяет задавать значения времени ожидания для различных аспектов операций с помощью таких свойств, как:

-   [**Служба WS \_ \_ \_ \_ время ожидания соединения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ \_ время ожидания отправки свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ \_ \_ время ожидания ответа получения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**Служба WS \_ \_ \_ \_ время ожидания получения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ \_ время ожидания разрешения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**Служба WS \_ \_ \_ \_ время ожидания закрытия свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Эти свойства имеют значения по умолчанию, которые являются консервативными и безопасными для большинства сценариев. Увеличение значений времени ожидания увеличивает время, в течение которого удаленная сторона может сохранить активность локального ресурса, например память, сокеты и потоки, выполняющие синхронный ввод-вывод. Приложение должно оценивать значения по умолчанию и соблюдать осторожность при увеличении времени ожидания, так как оно может открыть потенциальные направления атак, что может привести к отказу в обслуживании с удаленного компьютера.

Некоторые другие параметры конфигурации и рекомендации по проектированию приложений, которые следует тщательно оценить при использовании API канала ВВСАПИ:

-   При использовании уровня канала или прослушивателя приложение создает и принимает каналы на стороне сервера. Аналогично, приложение может создавать и открывать каналы на стороне клиента. Приложение должно разместить верхнюю границу этих операций, так как каждый канал потребляет память и другие ограниченные ресурсы, такие как сокеты. Приложение должно быть особенно осторожным при создании канала в ответ на любые действия, активируемые удаленной стороной.
-   Приложение может написать логику для создания каналов и их принятия. Каждый канал потребляет ограниченные ресурсы, такие как память и сокеты. Приложение должно иметь верхнюю границу количества каналов, которые он желает принимать, или удаленная сторона может создать множество подключений, что приведет к недостаточности и отказу в обслуживании. Он также должен активно принимать сообщения от этих подключений, используя небольшое время ожидания. Если сообщения не получены, время ожидания операции истечет, и подключение должно быть освобождено.
-   Приложение может отправить ответ или ошибку, обрабатывая заголовки SOAP ReplyTo или FaultTo. Безопасной практикой является использование только заголовка ReplyTo или FaultTo, который является "анонимным". Это означает, что для отправки ответа SOAP следует использовать существующее соединение (TCP, HTTP) или исходный IP-адрес (UDP). Приложения должны соблюдать особую осторожность при создании ресурсов (например, канала), чтобы ответить на другой адрес, если только сообщение не было подписано стороной, которую можно проговаривать по адресу, на который отправляется ответ.
-   Проверка целостности данных, выполненная на уровне канала, не является заменой при обеспечении безопасности. Приложение должно полагаться на функции безопасности ВВСАПИ, чтобы убедиться, что он взаимодействует с доверенной сущностью, а также должен полагаться на безопасность, чтобы обеспечить целостность данных.

Аналогично, существуют параметры конфигурации сообщений и рекомендации по проектированию приложений, которые следует тщательно оценить при использовании API сообщений ВВСАПИ:

-   Размер кучи, используемой для хранения заголовков сообщения, можно настроить с помощью свойства [**Свойства " \_ \_ \_ куча \_ Свойства сообщения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) ". Увеличение этого значения позволяет использовать больше памяти для заголовков сообщения, что может привести к некоторому получению.
-   Пользователь объекта Message должен понимать, что API доступа к заголовку имеют значение O (n) в отношении количества заголовков в сообщении, так как они проверяют наличие дубликатов. Схемы, требующие большого количества заголовков в сообщении, могут привести к чрезмерному использованию ЦП.
-   Максимальное количество заголовков в сообщении можно настроить с помощью свойства [**WS \_ Message \_ Property \_ Max \_ обработанные \_ заголовки**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Также существует неявное ограничение, основанное на размере кучи сообщения. Увеличение этих значений позволяет получить больше заголовков, что увеличивает время, необходимое для поиска заголовка (при использовании API доступа к заголовку).

 

 




