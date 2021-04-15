---
title: Примеры веб-служб Windows
description: В следующих примерах показано, как использовать API веб-служб Windows.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710043"
---
# <a name="windows-web-services-examples"></a>Примеры веб-служб Windows

В следующих примерах показано, как использовать API веб-служб Windows.

-   [Примеры модели службы](service-model-examples.md)
-   [Примеры уровня TCP-канала](tcp-channel-layer-examples.md)
-   [Примеры уровня канала HTTP](http-channel-layer-examples.md)
-   [Примеры уровня канала UDP](udp-channel-layer-examples.md)
-   [Примеры уровней каналов именованного канала](named-pipes-channel-layer-examples.md)
-   [Примеры сообщений](message-examples.md)
-   [Примеры XML](xml-examples.md)
-   [Примеры асинхронной модели](async-model-examples.md)
-   [Примеры уровней каналов безопасности](security-channel-layer-examples.md)
-   [Примеры репликации файлов](file-replication-examples.md)

## <a name="service-model-examples"></a>Примеры модели службы

Служба калькулятора: Клиент: [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md), сервер: [хттпкалкулаторсервицеексампле](httpcalculatorserviceexample.md).

Служба калькулятора с защитой транспорта SSL: Клиент: [хттпкалкулаторвиссслклиентексампле](httpcalculatorwithsslclientexample.md), сервер: [хттпкалкулаторвиссслсервицеексампле](httpcalculatorwithsslserviceexample.md).

Служба калькулятора с именем пользователя через SSL смешанного режима безопасности: Клиент: [хттпкалкулаторвисусернамеоверсслклиентексампле](httpcalculatorwithusernameoversslclientexample.md), сервер: [хттпкалкулаторвисусернамеоверсслсервицеексампле](httpcalculatorwithusernameoversslserviceexample.md).

Служба калькулятора с проверкой подлинности Kerberos через SSL в смешанном режиме: Клиент: [хттпкалкулаторвискерберосоверсслклиентексампле](httpcalculatorwithkerberosoversslclientexample.md), сервер: [хттпкалкулаторвискерберосоверсслсервицеексампле](httpcalculatorwithkerberosoversslserviceexample.md).

Служба заказов на покупку: Клиент: [хттппурчасеордерклиентексампле](httppurchaseorderclientexample.md), сервер: [хттппурчасеордерсервицеексампле](httppurchaseorderserviceexample.md).

Служба заказов на покупку с защитой транспорта SSL: Клиент: [хттппурчасеордервиссслклиентексампле](httppurchaseorderwithsslclientexample.md), сервер: [хттппурчасеордервиссслсервицеексампле](httppurchaseorderwithsslserviceexample.md).

Служба заказов на покупку с именем пользователя через SSL смешанный режим безопасности: Клиент: [хттппурчасеордервисусернамеоверсслклиентексампле](httppurchaseorderwithusernameoversslclientexample.md), сервер: [хттппурчасеордервисусернамеоверсслсервицеексампле](httppurchaseorderwithusernameoversslserviceexample.md).

Служба заказов на покупку с проверкой подлинности Kerberos через SSL в смешанном режиме: Клиент: [хттппурчасеордервискерберосоверсслклиентексампле](httppurchaseorderwithkerberosoversslclientexample.md), сервер: [хттппурчасеордервискерберосоверсслсервицеексампле](httppurchaseorderwithkerberosoversslserviceexample.md).

Нетипизированная служба заказа на покупку: сервер: [унтипедсервицеексампле](untypedserviceexample.md). Клиент: [унтипедклиентексампле](untypedclientexample.md)

Калькулятор сеансов: сервер: [сессионфуллкалкулаторсервицеексампле](sessionfullcalculatorserviceexample.md). Клиент:[сессионфуллкалкулаторклиентексампле](sessionfullcalculatorclientexample.md).

Калькулятор с использованием пользовательского канала и реализации прослушивателя: сервер:[хттпкалкулаторвислайередчаннелсервицеексампле](httpcalculatorwithlayeredchannelserviceexample.md). Клиент:[хттпкалкулаторвислайередчаннелклиентексампле](httpcalculatorwithlayeredchannelclientexample.md).

Калькулятор с использованием закодированного канала: сервер:[хттпкалкулаторвисенкодедчаннелсервицеексампле](httpcalculatorwithencodedchannelserviceexample.md). Клиент:[хттпкалкулаторвисенкодедчаннелклиентексампле](httpcalculatorwithencodedchannelclientexample.md).

Служба, обрабатывающая необработанные HTTP-запросы (не SOAP): Клиент:[хттправклиентексампле](httprawclientexample.md). Сервер:[хттправсервицеексампле](httprawserviceexample.md).

Уведомление об отмене операции службы: сервер: [блоккингсервицеексампле](blockingserviceexample.md). Клиент:[сервицеканцеллатионексампле](servicecancellationexample.md).

Отмена вызова: сервер: [сессионфуллкалкулаторсервицеексампле](sessionfullcalculatorserviceexample.md). Клиент:[каллабандонексампле](callabandonexample.md).

Создайте описание политики вручную и используйте его для создания прокси-сервера службы: [полицитемплатиксампле](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Примеры уровня TCP-канала

Пример TCP, отправляющий сообщения с использованием одностороннего шаблона: Клиент: [оневайткпклиентексампле](onewaytcpclientexample.md), сервер: [оневайткпсерверексампле](onewaytcpserverexample.md)

Пример TCP, отправляющий сообщения с помощью шаблона "запрос-ответ": Клиент: [рекуестреплиткпклиентексампле](requestreplytcpclientexample.md), сервер: [рекуестреплиткпсерверексампле](requestreplytcpserverexample.md)

Пример потоковой передачи TCP: Клиент: [стреамингткпклиентексампле](streamingtcpclientexample.md), сервер: [стреамингткпсерверексампле](streamingtcpserverexample.md)

Пример асинхронной потоковой передачи TCP: Клиент: [асинкстреамингткпклиентексампле](asyncstreamingtcpclientexample.md), сервер: [асинкстреамингткпсерверексампле](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Примеры уровня канала HTTP

Пример HTTP: Client: [хттпклиентексампле](httpclientexample.md), Server: [хттпсерверексампле](httpserverexample.md)

Пример HTTP, использующий API-интерфейсы потоковой передачи: Клиент: [стреамингхттпклиентексампле](streaminghttpclientexample.md), сервер: [стреамингхттпсерверексампле](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Примеры уровня канала UDP

Пример UDP, отправляющий сообщения с использованием одностороннего шаблона: Клиент: [оневайудпклиентексампле](onewayudpclientexample.md), сервер: [оневайудпсерверексампле](onewayudpserverexample.md)

Пример UDP, отправляющий сообщения с помощью шаблона ответа многоадресной рассылки: Клиент: [мултикастудпклиентексампле](multicastudpclientexample.md), сервер: [мултикастудпсерверексампле](multicastudpserverexample.md) следующий пример — использование IPv6-адресации: Клиент: [MulticastUdpClientExample6](multicastudpclientexample6.md), сервер: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Примеры уровней каналов именованных каналов

Пример именованных каналов, который отправляет сообщения с помощью шаблона "запрос-ответ": Клиент: [рекуестреплинамедпипесклиентексампле](requestreplynamedpipesclientexample.md), сервер: [рекуестреплинамедпипессерверексампле](requestreplynamedpipesserverexample.md)

Пример потоковой именованной каналы: Клиент: [стреамингнамедпипесклиентексампле](streamingnamedpipesclientexample.md), сервер: [стреамингнамедпипессерверексампле](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Примеры сообщений

Пример использования настраиваемых заголовков сообщений: [кустомхеадерексампле](customheaderexample.md)

Пример, который кодирует и декодирует сообщение: [мессажеенкодинжексампле](messageencodingexample.md)

Пример, в котором пересылается сообщение: [форвардмессажеексампле](forwardmessageexample.md)

## <a name="xml-examples"></a>Примеры XML

Пример, который записывает и считывает XML с помощью XML-буфера [реадвритексмлексампле](readwritexmlexample.md)

Пример, который записывает и считывает двоичные данные с помощью MTOM, Всвритебитес, Вспушбитес и Вспуллбитес [реадвритебитесксмлексампле](readwritebytesxmlexample.md)

Пример перехода по [навигатексмлексампле](navigatexmlexample.md) буфера XML

Пример, считывающий узел XML-документа по узлу [реадксмлексампле](readxmlexample.md)

Пример поиска и отображения атрибута XML [реадаттрибутиксампле](readattributeexample.md)

Пример, который записывает и считывает массив элементов [реадвритеаррайексампле](readwritearrayexample.md)

Пример вставки элемента в XML-буфер [инсертелементексампле](insertelementexample.md)

Пример, демонстрирующий использование некоторых вспомогательных функций буфера XML [ксмлбуфферексампле](xmlbufferexample.md)

Пример, который записывает и считывает производный тип с помощью созданных вспомогательных функций всутил [дериведтипиксампле](derivedtypeexample.md)

## <a name="async-model-examples"></a>Примеры асинхронной модели

Пример, иллюстрирующий модель для асинхронных функций. [асинкмоделексампле](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Примеры уровней каналов безопасности

Безопасность транспорта Windows через TCP: Клиент: [рекуестреплиткпклиентвисвиндовстранспортсекуритексампле](requestreplytcpclientwithwindowstransportsecurityexample.md), сервер: [рекуестреплиткпсервервисвиндовстранспортсекуритексампле](requestreplytcpserverwithwindowstransportsecurityexample.md).

Безопасность транспорта Windows через именованные каналы: Клиент: [рекуестреплинамедпипесклиентвисвиндовстранспортсекуритексампле](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), сервер: [рекуестреплинамедпипессервервисвиндовстранспортсекуритексампле](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Безопасность транспорта SSL: Клиент: [хттпклиентвиссслексампле](httpclientwithsslexample.md), сервер: [хттпсервервиссслексампле](httpserverwithsslexample.md).

Имя пользователя для смешанного режима безопасности SSL: Клиент: [хттпклиентвисусернамеоверсслексампле](httpclientwithusernameoversslexample.md), сервер: [хттпсервервисусернамеоверсслексампле](httpserverwithusernameoversslexample.md).

Имя пользователя для смешанного режима безопасности SSL: Клиент: [хттпклиентвискерберосоверсслексампле](httpclientwithkerberosoversslexample.md), сервер: [хттпсервервискерберосоверсслексампле](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Пример метаданных

В следующих примерах показано, как обрабатывать документы WSDL и политики с целью извлечения сведений о протоколе, поддерживаемом конечной точкой.

Имя пользователя в смешанном режиме безопасности SSL: [метадатаимпортвисусернамеоверсслексампле](metadataimportwithusernameoversslexample.md). Выданный маркер по безопасности смешанного режима SSL: [метадатаимпортвисиссуедтокеноверсслексампле](metadataimportwithissuedtokenoversslexample.md). Сертификат X509 в смешанном режиме безопасности SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>Пример Exchange WS-Metadata

В следующих примерах показано, как включить WS-MetadataExchange [на \_ \_ узле службы WS](ws-service-host.md).

Служба TCP с WS-MetadataExchange включена: [метадатаексчанжесампле](metadataexchangesample.md). Клиент моникера службы WCF, который вызывает службу TCP с WS-MetadataExchange включенным: [сервицемоникерсампле](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Пользовательские заголовки и модель службы

В следующих примерах показано, как использовать пользовательские заголовки [с \_ \_ прокси-сервером службы WS](ws-service-proxy.md) и [ \_ \_ узлом WS](ws-service-host.md) Service соответственно.

Клиент: [хттпкустомхеадерпурчасеордерклиентексампле](httpcustomheaderpurchaseorderclientexample.md), сервер: [хттпкустомхеадерпурчасеордерсервицеексампле](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Пример репликации файлов

Исчерпывающий пример, демонстрирующий реализацию службы репликации файлов: средство: [филерептулексампле](filereptoolexample.md), Service: [филерепсервицеексампле](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Взаимодействие общедоступной службы WCF

Клиент веб-служб Windows взаимодействует с клиентом службы WCF: [вкфпубликсервицесампле](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Пользовательский прокси-сервер HTTP

Клиент веб-служб Windows взаимодействует со службой ASMX TerraService с помощью настраиваемого прокси-клиента: [асмкстеррасервицесамплевискустомпрокси](asmxterraservicesamplewithcustomproxy.md)

 

 




