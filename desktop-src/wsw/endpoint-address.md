---
title: Адрес конечной точки
description: Адрес конечной точки представляет адрес службы в сети.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Веб-службы адреса конечной точки для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104569027"
---
# <a name="endpoint-address"></a><span data-ttu-id="3b6a4-106">Адрес конечной точки</span><span class="sxs-lookup"><span data-stu-id="3b6a4-106">Endpoint Address</span></span>

<span data-ttu-id="3b6a4-107">Адрес конечной точки представляет адрес службы в сети.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="3b6a4-108">При открытии [канала](channel.md)путем вызова функции [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) необходимо указать адрес конечной точки службы, с которой будет осуществляться взаимодействие, а также указать канал, который вы хотите открыть.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="3b6a4-109">Адрес конечной точки состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="3b6a4-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="3b6a4-110">[URL-адрес](url.md)</span><span class="sxs-lookup"><span data-stu-id="3b6a4-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="3b6a4-111">набор заголовков (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3b6a4-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="3b6a4-112">набор расширений (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3b6a4-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="3b6a4-113">необязательное [удостоверение](endpoint-identity.md) , представляющее идентификатор безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="3b6a4-114">При адресации сообщения URL-адрес становится заголовком «To» сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="3b6a4-115">Все заголовки, которые являются частью адреса конечной точки, также добавляются в сообщение.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Схема, показывающая заголовки адресов конечных точек, добавляемые в сообщение.](images/endpointaddress.png)

<span data-ttu-id="3b6a4-117">Каналы автоматически отправляют отправленные сообщения с помощью структуры [**\_ \_ адресов конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) , которая была передана в [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span><span class="sxs-lookup"><span data-stu-id="3b6a4-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="3b6a4-118">Можно также использовать функцию [**всаддрессмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) для переопределения этого поведения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="3b6a4-119">Если [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) передается в качестве параметра, функции [**всопенчаннел**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) и [**Всопенсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) создают копию параметра **\_ \_ адреса конечной точки WS** в памяти, а ее размер ограничен 65536 байтами.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="3b6a4-120">[**Всаддрессмессаже**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) не имеет этого ограничения, так как не требует создания копии параметра **\_ \_ адреса конечной точки WS** .</span><span class="sxs-lookup"><span data-stu-id="3b6a4-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="3b6a4-121">Расширения, указанные в поле **Extensions** [**\_ \_ адреса конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) , не используются для адресации сообщения, а являются механизмом расширяемости, который можно использовать для предоставления дополнительных сведений (например, метаданных) о службе.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="3b6a4-122">Общие расширения можно считывать с помощью функции [**всреадендпоинтаддрессекстенсион**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .</span><span class="sxs-lookup"><span data-stu-id="3b6a4-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="3b6a4-123">Необязательное поле удостоверения в адресе конечной точки может включать в себя, например, DNS-имя компьютера, на котором запущена служба, или UPN учетной записи Windows, от имени которой запущена служба.</span><span class="sxs-lookup"><span data-stu-id="3b6a4-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="3b6a4-124">Поле Identity не используется при обращении к сообщению, но может использоваться для получения маркера безопасности для службы (например, для получения билета Kerberos для целевого имени участника-пользователя) и для проверки подлинности ответов службы (например, идентификатор DNS, используемый для проверки имен в сертификате службы, возвращенном во время SSL).</span><span class="sxs-lookup"><span data-stu-id="3b6a4-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="3b6a4-125">Адреса конечных точек можно считывать и записывать с помощью [сериализации](serialization.md) со значением перечисления **\_ \_ \_ типа адреса конечной точки WS** из [**\_ типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="3b6a4-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="3b6a4-126">Примечание. для сериализации адреса конечной точки необходимо определить версию спецификации, используемой для заголовков адресации, как указано в перечислении [**\_ \_ версии WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="3b6a4-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




