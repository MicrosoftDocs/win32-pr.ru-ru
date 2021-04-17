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
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Создание прокси службы для службы WCF вручную

Самый простой способ создать прокси-службу клиента для службы Windows Communication Foundation (WCF) — на уровне [модели службы](service-model-layer-overview.md) с помощью средства всутил, как описано в разделе [Создание клиента](creating-a-client.md) . Однако при необходимости вы также можете создать прокси-сервер службы вручную. Этот API включает функцию [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) для создания прокси-сервера службы, а также структур, перечислений и т. д. для настройки свойств, необходимых для взаимодействия с WCF.

WCF предоставляет ряд стандартных привязок, каждый из которых предназначен для конкретного сценария использования. В свою очередь, привязка службы, к которой вы пытаетесь подключиться, определяет, какие свойства канала необходимо настроить для взаимодействия прокси-службы со службой.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Создание прокси-сервера службы для WSHttpBinding в WCF

WSHttpBinding предназначен для сценария магистрали Интернет-служб. Он использует более новую версию SOAP 1,2 и WS-Addressing версии 1,0, а также предоставляет широкий спектр параметров безопасности через общедоступные транспорты HTTP и HTTPS. ВВСАПИ не имеет эквивалента WSHttpBinding (или каких-либо стандартных привязок WCF), но, так как ее версия SOAP по умолчанию, WS-Addressing версия и формат кодировки соответствуют стандартам WSHttpBinding, создание прокси-сервера службы для службы, использующей WSHttpBinding, — это просто. Например, чтобы создать прокси-сервер службы для взаимодействия с конечной точкой WSHttpBinding без обеспечения безопасности, можно просто использовать код, подобный приведенному ниже (Объявление переменной, а создание кучи и создания ошибок, пропущено). Обратите внимание, что в вызове функции [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) не указаны свойства канала или описание безопасности.


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



Функция создает прокси-сервер службы и возвращает указатель на него в параметре *serviceProxy* (&прокси-сервер в вызове функции выше).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Создание прокси-сервера службы для BasicHttpBinding WCF

Однако при ручном создании прокси службы для службы WCF, которая использует привязку BasicHttpBinding, необходимо задать версию SOAP и WS-Addressing свойства канала. Это связано с тем, что ВВСАПИ по умолчанию используется SOAP версии 1,2 и WS-Addressing 1,0. BasicHttpBinding WCF, с другой стороны, использует SOAP версии 1,1 и без WS-Addressing.

Чтобы задать версию SOAP и WS-Addrssing свойства канала, объявите массив структур [**\_ \_ свойств канала WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) для хранения свойств канала и связанных сведений.


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



Затем передайте массив свойств канала (Чаннелпропертиес) и число свойств (Чаннелпропертикаунт) в [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (или [**вскреатечаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) , если вы работаете на уровне канала).


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



Массив, объявленный для хранения свойств, копируется в **вскреатесервицепрокси**, и в результате можно освободить память для массива свойств сразу же после вызова функции. Кроме того, при выделении памяти из стека (подобно приведенному выше фрагменту кода) можно также вернуться из функции сразу после вызова.

## <a name="other-bindings"></a>Другие привязки

Кроме того, ВВСАПИ предоставляет механизмы для создания прокси-серверов служб для взаимодействия со службами WCF с помощью других привязок, таких как NetTcpBinding и WSFederationHttpBinding. Для многих из этих привязок требуется задать дополнительные свойства канала, такие как дескрипторы безопасности. Примеры, иллюстрирующие использование других привязок, см. в разделе [примеры веб-служб Windows](windows-web-services-examples.md), в частности примеры [уровня канала TCP](tcp-channel-layer-examples.md), [Примеры уровня канала HTTP](http-channel-layer-examples.md)и [уровни каналов безопасности](security-channel-layer-examples.md) .

 

 




