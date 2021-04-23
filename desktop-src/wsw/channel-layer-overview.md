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
# <a name="channel-layer-overview"></a><span data-ttu-id="da056-106">Обзор уровня канала</span><span class="sxs-lookup"><span data-stu-id="da056-106">Channel Layer Overview</span></span>

<span data-ttu-id="da056-107">Уровень канала предоставляет абстракцию транспортного канала, а также сообщения, отправленные по каналу.</span><span class="sxs-lookup"><span data-stu-id="da056-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="da056-108">Он также включает функции для сериализации типов данных C в структуры SOAP и обратно.</span><span class="sxs-lookup"><span data-stu-id="da056-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="da056-109">Уровень канала обеспечивает полный контроль взаимодействия с помощью [сообщений](message.md) , состоящих из отправленных или полученных данных и содержащих тексты и заголовки, а также [каналов](channel.md) , которые являются абстрактными протоколами обмена сообщениями и предоставляют свойства для настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="da056-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="da056-110">Сообщение</span><span class="sxs-lookup"><span data-stu-id="da056-110">Message</span></span>

<span data-ttu-id="da056-111">[Сообщение](message.md) — это объект, инкапсулирующий сетевые данные, а именно данные, передаваемые или получаемые по сети.</span><span class="sxs-lookup"><span data-stu-id="da056-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="da056-112">Структура сообщения определяется протоколом SOAP с дискретным набором заголовков и текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="da056-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="da056-113">Заголовки помещаются в буфер памяти, а текст сообщения считывается или записывается с помощью API потока.</span><span class="sxs-lookup"><span data-stu-id="da056-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Схема, показывающая заголовок и текст сообщения.](images/messageenvelope.png)

<span data-ttu-id="da056-115">Несмотря на то, что модель данных сообщения всегда является моделью XML-данных, реальный формат сети является гибким.</span><span class="sxs-lookup"><span data-stu-id="da056-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="da056-116">Перед передачей сообщения оно кодируется с использованием определенной кодировки (например, текста, двоичного файла или MTOM).</span><span class="sxs-lookup"><span data-stu-id="da056-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="da056-117">Дополнительные сведения о кодировках см. в разделе [**\_ Кодировка WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .</span><span class="sxs-lookup"><span data-stu-id="da056-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Схема, в которой показаны несколько форматов кодирования сообщений.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="da056-119">Канал</span><span class="sxs-lookup"><span data-stu-id="da056-119">Channel</span></span>

<span data-ttu-id="da056-120">[Канал](channel.md) — это объект, используемый для отправки и получения сообщений в сети между двумя или более конечными точками.</span><span class="sxs-lookup"><span data-stu-id="da056-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="da056-121">Каналы имеют связанные данные, описывающие способ [адресации](endpoint-address.md) сообщения при его отправке.</span><span class="sxs-lookup"><span data-stu-id="da056-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="da056-122">Отправка сообщения по каналу аналогично размещению его в желобе — канал включает сведения, куда должно попасть сообщение, и способ его получения.</span><span class="sxs-lookup"><span data-stu-id="da056-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Диаграмма, на которой показаны каналы для сообщений.](images/channelsaschute.png)

<span data-ttu-id="da056-124">Каналы подразделяются на [**типы каналов**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="da056-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="da056-125">Тип канала указывает, какие направления сообщений могут поступать.</span><span class="sxs-lookup"><span data-stu-id="da056-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="da056-126">Тип канала также определяет, является ли канал сеансом или безсеансом.</span><span class="sxs-lookup"><span data-stu-id="da056-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="da056-127">Сеанс определяется как абстрактный способ корреляции сообщений между двумя или более сторонами.</span><span class="sxs-lookup"><span data-stu-id="da056-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="da056-128">Примером канала сеанса является TCP-канал, который использует TCP-соединение в качестве реализации конкретного сеанса.</span><span class="sxs-lookup"><span data-stu-id="da056-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="da056-129">Примером бессеансового канала является UDP, который не имеет базового механизма сеанса.</span><span class="sxs-lookup"><span data-stu-id="da056-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="da056-130">Хотя HTTP имеет базовые TCP-подключения, этот факт не предоставляется напрямую через этот API, поэтому HTTP также считается каналом без сеанса.</span><span class="sxs-lookup"><span data-stu-id="da056-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Схема, в которой показаны типы каналов с сеансами и сеансами.](images/channeltypes.png)

<span data-ttu-id="da056-132">Несмотря на то, что типы каналов описывают направление и сведения о сеансе для канала, они не указывают способ реализации канала.</span><span class="sxs-lookup"><span data-stu-id="da056-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="da056-133">Какой протокол должен использоваться каналом?</span><span class="sxs-lookup"><span data-stu-id="da056-133">What protocol should the channel use?</span></span> <span data-ttu-id="da056-134">Насколько трудно, чтобы канал попытается доставить сообщение?</span><span class="sxs-lookup"><span data-stu-id="da056-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="da056-135">Какой тип безопасности используется?</span><span class="sxs-lookup"><span data-stu-id="da056-135">What kind of security is used?</span></span> <span data-ttu-id="da056-136">Является ли он одиночным или многоадресным?</span><span class="sxs-lookup"><span data-stu-id="da056-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="da056-137">Эти параметры называются "привязкой" канала.</span><span class="sxs-lookup"><span data-stu-id="da056-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="da056-138">Привязка состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="da056-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="da056-139">[**\_ \_ Привязка канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), которая определяет используемый протокол передачи (TCP, UDP, HTTP, помощью канала NamedPipe).</span><span class="sxs-lookup"><span data-stu-id="da056-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="da056-140">[**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), которое указывает, как защитить канал.</span><span class="sxs-lookup"><span data-stu-id="da056-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="da056-141">Задает [**\_ \_ Свойства канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), которые указывают дополнительные необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="da056-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="da056-142">Список свойств см. в разделе [**\_ \_ \_ идентификатор свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .</span><span class="sxs-lookup"><span data-stu-id="da056-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Схема, показывающая список свойств канала.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="da056-144">Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="da056-144">Listener</span></span>

<span data-ttu-id="da056-145">Чтобы начать обмен данными, клиент создает объект канала.</span><span class="sxs-lookup"><span data-stu-id="da056-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="da056-146">Но как служба получает объект канала?</span><span class="sxs-lookup"><span data-stu-id="da056-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="da056-147">Для этого создается [прослушиватель](listener.md).</span><span class="sxs-lookup"><span data-stu-id="da056-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="da056-148">Для создания прослушивателя требуются те же сведения о привязке, которые необходимы для создания канала.</span><span class="sxs-lookup"><span data-stu-id="da056-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="da056-149">После создания прослушивателя приложение может принимать каналы от прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="da056-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="da056-150">Так как приложение может относиться к приему каналов, прослушиватели обычно сохраняют в очереди каналы, готовые к приему (до некоторой квоты).</span><span class="sxs-lookup"><span data-stu-id="da056-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Схема, показывающая каналы в очереди прослушивателя.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="da056-152">Инициирующая связь (клиент)</span><span class="sxs-lookup"><span data-stu-id="da056-152">Initiating Communication (client)</span></span>

<span data-ttu-id="da056-153">Чтобы инициировать обмен данными на клиенте, используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-153">To initiate communication on the client, use the following sequence.</span></span>

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

## <a name="accepting-communication-server"></a><span data-ttu-id="da056-154">Принятие связи (сервер)</span><span class="sxs-lookup"><span data-stu-id="da056-154">Accepting Communication (server)</span></span>

<span data-ttu-id="da056-155">Чтобы принимать входящие подключения на сервере, используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-155">To accept incoming communications on the server, use the following sequence.</span></span>

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

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="da056-156">Отправка сообщений (клиент или сервер)</span><span class="sxs-lookup"><span data-stu-id="da056-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="da056-157">Для отправки сообщений используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="da056-158">Функция [**вссендмессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) не поддерживает потоковую передачу и предполагает, что текст содержит только один элемент.</span><span class="sxs-lookup"><span data-stu-id="da056-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="da056-159">Чтобы избежать этих ограничений, используйте следующую последовательность, а не **вссендмессаже**.</span><span class="sxs-lookup"><span data-stu-id="da056-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

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

<span data-ttu-id="da056-160">Функция [**всвритебоди**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) использует сериализацию для записи элементов тела.</span><span class="sxs-lookup"><span data-stu-id="da056-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="da056-161">Для записи данных непосредственно в модуль записи XML используйте следующую последовательность, а не **всвритебоди**.</span><span class="sxs-lookup"><span data-stu-id="da056-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="da056-162">Функция [**всаддкустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) использует сериализацию для установки заголовков в буфер заголовков сообщения.</span><span class="sxs-lookup"><span data-stu-id="da056-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="da056-163">Чтобы использовать модуль записи XML для записи заголовка, используйте следующую последовательность, а не **всаддкустомхеадер**.</span><span class="sxs-lookup"><span data-stu-id="da056-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="da056-164">Получение сообщений (клиент или сервер)</span><span class="sxs-lookup"><span data-stu-id="da056-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="da056-165">Для получения сообщений используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-165">To receive messages, use the following sequence.</span></span>

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

<span data-ttu-id="da056-166">Функция [**всрецеивемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) не поддерживает потоковую передачу и предполагает, что текст содержит только один элемент, и что тип сообщения (действие и схема тела) известен заранее.</span><span class="sxs-lookup"><span data-stu-id="da056-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="da056-167">Чтобы избежать этих ограничений, используйте следующую последовательность, а не **всрецеивемессаже**.</span><span class="sxs-lookup"><span data-stu-id="da056-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

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

<span data-ttu-id="da056-168">Функция [**всреадбоди**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) использует сериализацию для чтения элементов тела.</span><span class="sxs-lookup"><span data-stu-id="da056-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="da056-169">Для чтения данных непосредственно из [средства чтения XML](xml-reader.md)используйте следующую последовательность, а не **всреадбоди**.</span><span class="sxs-lookup"><span data-stu-id="da056-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="da056-170">Функции [**всжеткустомхеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) используют сериализацию для получения заголовков из буфера заголовков сообщения.</span><span class="sxs-lookup"><span data-stu-id="da056-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="da056-171">Чтобы использовать [средство чтения XML](xml-reader.md) для чтения заголовка, используйте следующую последовательность, а не **всжеткустомхеадер**.</span><span class="sxs-lookup"><span data-stu-id="da056-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

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

## <a name="request-reply-client"></a><span data-ttu-id="da056-172">Ответ на запрос (клиент)</span><span class="sxs-lookup"><span data-stu-id="da056-172">Request Reply (client)</span></span>

<span data-ttu-id="da056-173">Запрос-ответ на клиенте можно выполнить с помощью следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="da056-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

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

<span data-ttu-id="da056-174">Функция [**всрекуестрепли**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) предполагает наличие одного элемента для текста сообщения запроса и ответа, а также то, что тип сообщения (действие и схема тела) известен заранее.</span><span class="sxs-lookup"><span data-stu-id="da056-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="da056-175">Чтобы избежать этих ограничений, сообщение запроса и ответа можно отправить вручную, как показано в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="da056-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="da056-176">Эта последовательность соответствует предыдущей последовательности для отправки и получения сообщения, за исключением случаев, когда отмечено.</span><span class="sxs-lookup"><span data-stu-id="da056-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

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

## <a name="request-reply-server"></a><span data-ttu-id="da056-177">Запрос ответа (сервер)</span><span class="sxs-lookup"><span data-stu-id="da056-177">Request Reply (server)</span></span>

<span data-ttu-id="da056-178">Чтобы получить сообщение запроса на сервере, используйте ту же последовательность, которая описана в предыдущем разделе о получении сообщений.</span><span class="sxs-lookup"><span data-stu-id="da056-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="da056-179">Чтобы отправить ответ или сообщение об ошибке, используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="da056-180">Функция [**вссендреплимессаже**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) предполагает наличие одного элемента в теле и не допускает потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="da056-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="da056-181">Чтобы избежать этих ограничений, используйте следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="da056-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="da056-182">Это то же самое, что и Предыдущая последовательность отправки сообщения, но при инициализации использует [**\_ \_ сообщение ответа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) вместо **WS \_ Blank \_** .</span><span class="sxs-lookup"><span data-stu-id="da056-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

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

## <a name="message-exchange-patterns"></a><span data-ttu-id="da056-183">Шаблоны обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="da056-183">Message Exchange Patterns</span></span>

<span data-ttu-id="da056-184">[**\_ \_ Тип канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) определяет шаблон обмена сообщениями для данного канала.</span><span class="sxs-lookup"><span data-stu-id="da056-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="da056-185">Поддерживаемый тип, зависит от привязки, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="da056-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="da056-186">[**Служба WS \_ \_ \_ Привязка канала HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ \_ \_ запрос типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) для клиента и **\_ \_ \_ ответа типа WS-канала** на сервере.</span><span class="sxs-lookup"><span data-stu-id="da056-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="da056-187">[**Служба WS \_ \_ \_ Привязка TCP-канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ многоканальный \_ \_ \_ сеанс связи типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) на клиенте и на сервере **\_ канале \_ \_ двустороннего \_ подключения типа WS** .</span><span class="sxs-lookup"><span data-stu-id="da056-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="da056-188">[**Служба WS \_ \_ \_ Привязка канала UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ канал WS \_ типа " \_ дуплекс**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " на клиенте и **\_ \_ тип \_ канала WS** на сервере.</span><span class="sxs-lookup"><span data-stu-id="da056-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="da056-189">[**Служба WS \_ \_ \_ Привязка канала помощью канала NamedPipe**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает [**\_ канал WS \_ типа " \_ дуплекс**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " на клиенте и **\_ \_ тип \_ канала WS** на сервере.</span><span class="sxs-lookup"><span data-stu-id="da056-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="da056-190">Циклы сообщений</span><span class="sxs-lookup"><span data-stu-id="da056-190">Message Loops</span></span>

<span data-ttu-id="da056-191">Для каждого шаблона обмена сообщениями существует отдельный цикл, который можно использовать для отправки или получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="da056-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="da056-192">В цикле описывается юридический порядок операций, необходимых для отправки и получения нескольких сообщений.</span><span class="sxs-lookup"><span data-stu-id="da056-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="da056-193">Циклы описаны ниже как грамматические продукты.</span><span class="sxs-lookup"><span data-stu-id="da056-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="da056-194">Термин «End» («конец») возвращает значение Where **WS \_ S \_** (см. раздел [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md)), что означает, что на канале больше нет доступных сообщений.</span><span class="sxs-lookup"><span data-stu-id="da056-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="da056-195">Параллельное производство указывает, что для Parallel (x & y) Эта операция x может выполняться параллельно с y.</span><span class="sxs-lookup"><span data-stu-id="da056-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="da056-196">На клиенте используются следующие циклы.</span><span class="sxs-lookup"><span data-stu-id="da056-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="da056-197">На сервере используются следующие циклы.</span><span class="sxs-lookup"><span data-stu-id="da056-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="da056-198">Для использования [**\_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) на сервере требуется успешное получение, прежде чем отправка будет разрешена даже с каналом [**типа \_ канал \_ WS \_ \_ сеанс дуплекса**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="da056-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="da056-199">После первого получения.</span><span class="sxs-lookup"><span data-stu-id="da056-199">After the first receive.</span></span> <span data-ttu-id="da056-200">применяется обычный цикл.</span><span class="sxs-lookup"><span data-stu-id="da056-200">the regular loop applies.</span></span>

<span data-ttu-id="da056-201">Обратите внимание, что каналы типа " [**\_ \_ \_ запрос типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " и " **\_ \_ Тип канала \_ WS** " можно использовать для отправки и получения односторонних сообщений (а также стандартного шаблона "запрос — ответ").</span><span class="sxs-lookup"><span data-stu-id="da056-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="da056-202">Это достигается путем закрытия канала ответа без отправки ответа.</span><span class="sxs-lookup"><span data-stu-id="da056-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="da056-203">В этом случае в канале запроса не будет получен ответ.</span><span class="sxs-lookup"><span data-stu-id="da056-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="da056-204">Возвращаемое значение **WS \_ S \_** с использованием [**\_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) на сервере требует успешного получения, прежде чем отправка будет разрешена даже с каналом типа **WS \_ канал типа \_ \_ дуплексного \_ сеанса**.</span><span class="sxs-lookup"><span data-stu-id="da056-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="da056-205">После первого приема используется обычный цикл.</span><span class="sxs-lookup"><span data-stu-id="da056-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="da056-206">будет возвращено значение, указывающее, что сообщение недоступно.</span><span class="sxs-lookup"><span data-stu-id="da056-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="da056-207">Циклы клиента или сервера могут выполняться параллельно друг с другом с помощью нескольких экземпляров каналов.</span><span class="sxs-lookup"><span data-stu-id="da056-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="da056-208">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="da056-208">Message Filtering</span></span>

<span data-ttu-id="da056-209">Серверный канал может фильтровать полученные сообщения, которые не предназначены для приложения, например сообщения, которые устанавливают [контекст безопасности](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="da056-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="da056-210">В этом случае **Служба \_ WS \_ S** будет возвращена из [**всреадмессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) , а сообщения приложений не будут доступны в этом канале.</span><span class="sxs-lookup"><span data-stu-id="da056-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="da056-211">Однако это не сигнализирует, что клиент предназначен для завершения взаимодействия с сервером.</span><span class="sxs-lookup"><span data-stu-id="da056-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="da056-212">На другом канале могут быть доступны дополнительные сообщения.</span><span class="sxs-lookup"><span data-stu-id="da056-212">More messages may be available on another channel.</span></span> <span data-ttu-id="da056-213">См. [**всшутдовнсессиончаннел**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="da056-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="da056-214">Отмена</span><span class="sxs-lookup"><span data-stu-id="da056-214">Cancellation</span></span>

<span data-ttu-id="da056-215">Функция [**всабортчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) используется для отмены ожидающих ввода-вывода для канала.</span><span class="sxs-lookup"><span data-stu-id="da056-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="da056-216">Этот API не будет ожидать завершения операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="da056-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="da056-217">Дополнительные сведения см. в схеме состояния [**\_ \_ состояния канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) и документации по **всабортчаннел** .</span><span class="sxs-lookup"><span data-stu-id="da056-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="da056-218">API [**всабортлистенер**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) используется для отмены ожидающих операций ввода-вывода для прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="da056-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="da056-219">Этот API не будет ожидать завершения операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="da056-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="da056-220">Прерывание прослушивателя приведет к прерыванию отложенного приема.</span><span class="sxs-lookup"><span data-stu-id="da056-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="da056-221">Дополнительные сведения см. в схеме состояния [**\_ прослушивателя \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) и **всабортлистенер** .</span><span class="sxs-lookup"><span data-stu-id="da056-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="da056-222">TCP</span><span class="sxs-lookup"><span data-stu-id="da056-222">TCP</span></span>

<span data-ttu-id="da056-223">[**\_ Привязка TCP- \_ канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через TCP.</span><span class="sxs-lookup"><span data-stu-id="da056-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="da056-224">Спецификация SOAP по TCP строится на основе механизма кадрирования .NET.</span><span class="sxs-lookup"><span data-stu-id="da056-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="da056-225">Общий доступ к портам не поддерживается в этой версии.</span><span class="sxs-lookup"><span data-stu-id="da056-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="da056-226">Каждый открытый прослушиватель должен использовать другой номер порта.</span><span class="sxs-lookup"><span data-stu-id="da056-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="da056-227">UDP</span><span class="sxs-lookup"><span data-stu-id="da056-227">UDP</span></span>

<span data-ttu-id="da056-228">[**\_ \_ \_ Привязка канала WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через UDP.</span><span class="sxs-lookup"><span data-stu-id="da056-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="da056-229">Существует ряд ограничений, касающихся привязки UDP:</span><span class="sxs-lookup"><span data-stu-id="da056-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="da056-230">Обеспечение безопасности не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da056-230">There is no support for security.</span></span>
-   <span data-ttu-id="da056-231">Сообщения могут быть потеряны или дублироваться.</span><span class="sxs-lookup"><span data-stu-id="da056-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="da056-232">Поддерживается только одна кодировка: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="da056-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="da056-233">Сообщения имеют фундаментальное ограничение до 64 КБ, и часто они теряются, если размер превышает MTU сети.</span><span class="sxs-lookup"><span data-stu-id="da056-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="da056-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="da056-234">HTTP</span></span>

<span data-ttu-id="da056-235">[**\_ \_ \_ Привязка канала WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через HTTP.</span><span class="sxs-lookup"><span data-stu-id="da056-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="da056-236">Сведения об управлении заголовками HTTP на клиенте и сервере см. в разделе [**\_ \_ \_ сопоставление HTTP-сообщений WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="da056-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="da056-237">Для отправки и получения сообщений, не относящихся к протоколу SOAP, на сервере используйте [**\_ кодировку WS \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) для [**\_ \_ \_ кодирования свойств канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="da056-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="da056-238">намедпипес</span><span class="sxs-lookup"><span data-stu-id="da056-238">NAMEDPIPES</span></span>

<span data-ttu-id="da056-239">[**\_ \_ \_ Привязка канала WS помощью канала NamedPipe**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) поддерживает протокол SOAP через именованные каналы, что позволяет обмениваться данными со службой Windows Communication Foundation (WCF) с помощью NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="da056-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="da056-240">Корреляция сообщений "запрос-ответ"</span><span class="sxs-lookup"><span data-stu-id="da056-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="da056-241">Сообщения типа "запрос-ответ" сопоставляются одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="da056-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="da056-242">Корреляция выполняется с помощью канала в качестве механизма корреляции.</span><span class="sxs-lookup"><span data-stu-id="da056-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="da056-243">Например, при использовании [**\_ \_ \_ транспорта версии WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) и [**\_ \_ \_ привязки канала WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) ответ для сообщения запроса сопоставляется с ЗАПРОСОМ по факту, что это текст сущности HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="da056-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="da056-244">Корреляция выполняется с помощью заголовков MessageID и «переводятся».</span><span class="sxs-lookup"><span data-stu-id="da056-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="da056-245">Этот механизм используется с [**WS \_ Addressing \_ Version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) и **WS \_ Addressing \_ Version \_ 0 \_ 9** (даже при [**использовании \_ \_ \_ привязки канала HTTP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="da056-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="da056-246">В этом случае сообщение запроса содержит заголовок MessageID.</span><span class="sxs-lookup"><span data-stu-id="da056-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="da056-247">Ответное сообщение содержит заголовок «текст сообщения», содержащий значение заголовка MessageID запроса.</span><span class="sxs-lookup"><span data-stu-id="da056-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="da056-248">Заголовок области отправки позволяет клиенту сопоставить ответ с отправленным запросом.</span><span class="sxs-lookup"><span data-stu-id="da056-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="da056-249">Следующие интерфейсы API уровня канала автоматически используют соответствующие механизмы корреляции на основе [**\_ \_ версии канала WS Address**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="da056-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="da056-250">**всрекуестрепли**</span><span class="sxs-lookup"><span data-stu-id="da056-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="da056-251">**вссендреплимессаже**</span><span class="sxs-lookup"><span data-stu-id="da056-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="da056-252">**вссендфаултмессажефореррор**</span><span class="sxs-lookup"><span data-stu-id="da056-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="da056-253">Если эти API не используются, заголовки можно добавить вручную и получить к ним доступ с помощью [**вссесеадер**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) или [**всжесеадер**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span><span class="sxs-lookup"><span data-stu-id="da056-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="da056-254">Пользовательские каналы и прослушиватели</span><span class="sxs-lookup"><span data-stu-id="da056-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="da056-255">Если предопределенный набор привязок каналов не удовлетворяет потребностям приложения, то реализацию пользовательского канала и прослушивателя можно определить, указав [**\_ настраиваемую \_ \_ привязку каналов WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) при создании канала или прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="da056-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="da056-256">Фактическая реализация канала или прослушивателя задается в виде набора обратных вызовов с [**помощью \_ \_ \_ пользовательских \_ \_ обратных вызовов свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) или свойств [**\_ \_ \_ \_ \_ обратного вызова настраиваемого прослушивателя свойства прослушивателя WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) .</span><span class="sxs-lookup"><span data-stu-id="da056-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="da056-257">После создания пользовательского канала или прослушивателя результатом является объект [WS \_ Channel](ws-channel.md) или [WS- \_ Listener](ws-listener.md) , который можно использовать с существующими API.</span><span class="sxs-lookup"><span data-stu-id="da056-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="da056-258">Пользовательский канал и прослушиватель также можно использовать с прокси-сервером службы [и узлом службы](service-host.md) , указав **значение \_ \_ \_ привязки настраиваемого канала WS** в перечислении [**\_ \_ привязки WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , а также свойства обратного вызова настраиваемого прослушивателя для свойства [**\_ канала WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) и пользовательского [**\_ \_ \_ \_ \_ обратных вызовов свойства прослушивателя**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) WS при создании прокси службы или узла службы.</span><span class="sxs-lookup"><span data-stu-id="da056-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="da056-259">Безопасность</span><span class="sxs-lookup"><span data-stu-id="da056-259">Security</span></span>

<span data-ttu-id="da056-260">Канал позволяет ограничить объем памяти, используемый для различных аспектов операций, с помощью таких свойств, как:</span><span class="sxs-lookup"><span data-stu-id="da056-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="da056-261">[**Служба WS \_ свойство канала: \_ \_ максимальный \_ \_ \_ Размер буферизованного сообщения**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="da056-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-262">[**Служба WS \_ \_ \_ максимальный \_ \_ \_ Размер потокового сообщения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-263">[**Служба WS \_ \_ \_ максимальный \_ \_ \_ Размер запускаемого потока свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-264">[**Служба WS \_ \_ \_ максимальный \_ \_ \_ \_ \_ Размер буфера заголовков HTTP-запросов для свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="da056-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-265">[**Служба WS \_ \_Максимальное значение \_ \_ \_ \_ размера словаря сеанса для свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="da056-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="da056-266">Эти свойства имеют значения по умолчанию, которые являются консервативными и безопасными для большинства сценариев.</span><span class="sxs-lookup"><span data-stu-id="da056-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="da056-267">Значения по умолчанию и любые изменения в них следует тщательно оценить по потенциальным направлениям атак, что может привести к отказу в обслуживании удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="da056-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="da056-268">Канал позволяет задавать значения времени ожидания для различных аспектов операций с помощью таких свойств, как:</span><span class="sxs-lookup"><span data-stu-id="da056-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="da056-269">[**Служба WS \_ \_ \_ \_ время ожидания соединения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-270">[**Служба WS \_ \_ \_ \_ время ожидания отправки свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-271">[**Служба WS \_ \_ \_ \_ \_ время ожидания ответа получения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="da056-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-272">[**Служба WS \_ \_ \_ \_ время ожидания получения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-273">[**Служба WS \_ \_ \_ \_ время ожидания разрешения свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="da056-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="da056-274">[**Служба WS \_ \_ \_ \_ время ожидания закрытия свойства канала**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="da056-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="da056-275">Эти свойства имеют значения по умолчанию, которые являются консервативными и безопасными для большинства сценариев.</span><span class="sxs-lookup"><span data-stu-id="da056-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="da056-276">Увеличение значений времени ожидания увеличивает время, в течение которого удаленная сторона может сохранить активность локального ресурса, например память, сокеты и потоки, выполняющие синхронный ввод-вывод.</span><span class="sxs-lookup"><span data-stu-id="da056-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="da056-277">Приложение должно оценивать значения по умолчанию и соблюдать осторожность при увеличении времени ожидания, так как оно может открыть потенциальные направления атак, что может привести к отказу в обслуживании с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="da056-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="da056-278">Некоторые другие параметры конфигурации и рекомендации по проектированию приложений, которые следует тщательно оценить при использовании API канала ВВСАПИ:</span><span class="sxs-lookup"><span data-stu-id="da056-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="da056-279">При использовании уровня канала или прослушивателя приложение создает и принимает каналы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="da056-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="da056-280">Аналогично, приложение может создавать и открывать каналы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="da056-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="da056-281">Приложение должно разместить верхнюю границу этих операций, так как каждый канал потребляет память и другие ограниченные ресурсы, такие как сокеты.</span><span class="sxs-lookup"><span data-stu-id="da056-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="da056-282">Приложение должно быть особенно осторожным при создании канала в ответ на любые действия, активируемые удаленной стороной.</span><span class="sxs-lookup"><span data-stu-id="da056-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="da056-283">Приложение может написать логику для создания каналов и их принятия.</span><span class="sxs-lookup"><span data-stu-id="da056-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="da056-284">Каждый канал потребляет ограниченные ресурсы, такие как память и сокеты.</span><span class="sxs-lookup"><span data-stu-id="da056-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="da056-285">Приложение должно иметь верхнюю границу количества каналов, которые он желает принимать, или удаленная сторона может создать множество подключений, что приведет к недостаточности и отказу в обслуживании.</span><span class="sxs-lookup"><span data-stu-id="da056-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="da056-286">Он также должен активно принимать сообщения от этих подключений, используя небольшое время ожидания.</span><span class="sxs-lookup"><span data-stu-id="da056-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="da056-287">Если сообщения не получены, время ожидания операции истечет, и подключение должно быть освобождено.</span><span class="sxs-lookup"><span data-stu-id="da056-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="da056-288">Приложение может отправить ответ или ошибку, обрабатывая заголовки SOAP ReplyTo или FaultTo.</span><span class="sxs-lookup"><span data-stu-id="da056-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="da056-289">Безопасной практикой является использование только заголовка ReplyTo или FaultTo, который является "анонимным". Это означает, что для отправки ответа SOAP следует использовать существующее соединение (TCP, HTTP) или исходный IP-адрес (UDP).</span><span class="sxs-lookup"><span data-stu-id="da056-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="da056-290">Приложения должны соблюдать особую осторожность при создании ресурсов (например, канала), чтобы ответить на другой адрес, если только сообщение не было подписано стороной, которую можно проговаривать по адресу, на который отправляется ответ.</span><span class="sxs-lookup"><span data-stu-id="da056-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="da056-291">Проверка целостности данных, выполненная на уровне канала, не является заменой при обеспечении безопасности.</span><span class="sxs-lookup"><span data-stu-id="da056-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="da056-292">Приложение должно полагаться на функции безопасности ВВСАПИ, чтобы убедиться, что он взаимодействует с доверенной сущностью, а также должен полагаться на безопасность, чтобы обеспечить целостность данных.</span><span class="sxs-lookup"><span data-stu-id="da056-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="da056-293">Аналогично, существуют параметры конфигурации сообщений и рекомендации по проектированию приложений, которые следует тщательно оценить при использовании API сообщений ВВСАПИ:</span><span class="sxs-lookup"><span data-stu-id="da056-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="da056-294">Размер кучи, используемой для хранения заголовков сообщения, можно настроить с помощью свойства [**Свойства " \_ \_ \_ куча \_ Свойства сообщения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) ".</span><span class="sxs-lookup"><span data-stu-id="da056-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="da056-295">Увеличение этого значения позволяет использовать больше памяти для заголовков сообщения, что может привести к некоторому получению.</span><span class="sxs-lookup"><span data-stu-id="da056-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="da056-296">Пользователь объекта Message должен понимать, что API доступа к заголовку имеют значение O (n) в отношении количества заголовков в сообщении, так как они проверяют наличие дубликатов.</span><span class="sxs-lookup"><span data-stu-id="da056-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="da056-297">Схемы, требующие большого количества заголовков в сообщении, могут привести к чрезмерному использованию ЦП.</span><span class="sxs-lookup"><span data-stu-id="da056-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="da056-298">Максимальное количество заголовков в сообщении можно настроить с помощью свойства [**WS \_ Message \_ Property \_ Max \_ обработанные \_ заголовки**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="da056-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="da056-299">Также существует неявное ограничение, основанное на размере кучи сообщения.</span><span class="sxs-lookup"><span data-stu-id="da056-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="da056-300">Увеличение этих значений позволяет получить больше заголовков, что увеличивает время, необходимое для поиска заголовка (при использовании API доступа к заголовку).</span><span class="sxs-lookup"><span data-stu-id="da056-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




