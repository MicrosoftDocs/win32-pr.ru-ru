---
title: Создание прокси службы для службы WCF вручную
description: Самый простой способ создать прокси-службу клиента для службы Windows Communication Foundation (WCF) — на уровне модели службы с помощью средства Всутил, как описано в разделе Создание клиента.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691282"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="45209-103">Создание прокси службы для службы WCF вручную</span><span class="sxs-lookup"><span data-stu-id="45209-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="45209-104">Самый простой способ создать прокси-службу клиента для службы Windows Communication Foundation (WCF) — на уровне [модели службы](service-model-layer-overview.md) с помощью средства всутил, как описано в разделе [Создание клиента](creating-a-client.md) .</span><span class="sxs-lookup"><span data-stu-id="45209-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="45209-105">Однако при необходимости вы также можете создать прокси-сервер службы вручную.</span><span class="sxs-lookup"><span data-stu-id="45209-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="45209-106">Этот API включает функцию [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) для создания прокси-сервера службы, а также структур, перечислений и т. д. для настройки свойств, необходимых для взаимодействия с WCF.</span><span class="sxs-lookup"><span data-stu-id="45209-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="45209-107">WCF предоставляет ряд стандартных привязок, каждый из которых предназначен для конкретного сценария использования.</span><span class="sxs-lookup"><span data-stu-id="45209-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="45209-108">В свою очередь, привязка службы, к которой вы пытаетесь подключиться, определяет, какие свойства канала необходимо настроить для взаимодействия прокси-службы со службой.</span><span class="sxs-lookup"><span data-stu-id="45209-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="45209-109">Создание прокси-сервера службы для WSHttpBinding в WCF</span><span class="sxs-lookup"><span data-stu-id="45209-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="45209-110">WSHttpBinding предназначен для сценария магистрали Интернет-служб.</span><span class="sxs-lookup"><span data-stu-id="45209-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="45209-111">Он использует более новую версию SOAP 1,2 и WS-Addressing версии 1,0, а также предоставляет широкий спектр параметров безопасности через общедоступные транспорты HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="45209-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="45209-112">ВВСАПИ не имеет эквивалента WSHttpBinding (или каких-либо стандартных привязок WCF), но, так как ее версия SOAP по умолчанию, WS-Addressing версия и формат кодировки соответствуют стандартам WSHttpBinding, создание прокси-сервера службы для службы, использующей WSHttpBinding, — это просто.</span><span class="sxs-lookup"><span data-stu-id="45209-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="45209-113">Например, чтобы создать прокси-сервер службы для взаимодействия с конечной точкой WSHttpBinding без обеспечения безопасности, можно просто использовать код, подобный приведенному ниже (Объявление переменной, а создание кучи и создания ошибок, пропущено).</span><span class="sxs-lookup"><span data-stu-id="45209-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="45209-114">Обратите внимание, что в вызове функции [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) не указаны свойства канала или описание безопасности.</span><span class="sxs-lookup"><span data-stu-id="45209-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="45209-115">Функция создает прокси-сервер службы и возвращает указатель на него в параметре *serviceProxy* (&прокси-сервер в вызове функции выше).</span><span class="sxs-lookup"><span data-stu-id="45209-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="45209-116">Создание прокси-сервера службы для BasicHttpBinding WCF</span><span class="sxs-lookup"><span data-stu-id="45209-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="45209-117">Однако при ручном создании прокси службы для службы WCF, которая использует привязку BasicHttpBinding, необходимо задать версию SOAP и WS-Addressing свойства канала.</span><span class="sxs-lookup"><span data-stu-id="45209-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="45209-118">Это связано с тем, что ВВСАПИ по умолчанию используется SOAP версии 1,2 и WS-Addressing 1,0.</span><span class="sxs-lookup"><span data-stu-id="45209-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="45209-119">BasicHttpBinding WCF, с другой стороны, использует SOAP версии 1,1 и без WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="45209-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="45209-120">Чтобы задать версию SOAP и WS-Addrssing свойства канала, объявите массив структур [**\_ \_ свойств канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) для хранения свойств канала и связанных сведений.</span><span class="sxs-lookup"><span data-stu-id="45209-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



<span data-ttu-id="45209-121">Затем передайте массив свойств канала (Чаннелпропертиес) и число свойств (Чаннелпропертикаунт) в [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (или [**вскреатечаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) , если вы работаете на уровне канала).</span><span class="sxs-lookup"><span data-stu-id="45209-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="45209-122">Массив, объявленный для хранения свойств, копируется в **вскреатесервицепрокси**, и в результате можно освободить память для массива свойств сразу же после вызова функции.</span><span class="sxs-lookup"><span data-stu-id="45209-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="45209-123">Кроме того, при выделении памяти из стека (подобно приведенному выше фрагменту кода) можно также вернуться из функции сразу после вызова.</span><span class="sxs-lookup"><span data-stu-id="45209-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="45209-124">Другие привязки</span><span class="sxs-lookup"><span data-stu-id="45209-124">Other Bindings</span></span>

<span data-ttu-id="45209-125">Кроме того, ВВСАПИ предоставляет механизмы для создания прокси-серверов служб для взаимодействия со службами WCF с помощью других привязок, таких как NetTcpBinding и WSFederationHttpBinding.</span><span class="sxs-lookup"><span data-stu-id="45209-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="45209-126">Для многих из этих привязок требуется задать дополнительные свойства канала, такие как дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="45209-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="45209-127">Примеры, иллюстрирующие использование других привязок, см. в разделе [примеры веб-служб Windows](windows-web-services-examples.md), в частности примеры [уровня канала TCP](tcp-channel-layer-examples.md), [Примеры уровня канала HTTP](http-channel-layer-examples.md)и [уровни каналов безопасности](security-channel-layer-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="45209-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




