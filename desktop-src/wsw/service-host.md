---
title: Узел службы
description: Узел службы — это среда выполнения для размещения службы в рамках процесса.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Веб-службы узла службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a09a41714ce80402c5430e6849988ae86163770af7ae3eb060fdd7925e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838673"
---
# <a name="service-host"></a>Узел службы

Узел службы — это среда выполнения для размещения службы в рамках процесса.


Служба может настроить одну или несколько конечных точек внутри узла службы.

![Схема, показывающая структуру узла службы, содержащего конечную точку службы.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Создание узла службы

Прежде чем создавать узел службы, службе необходимо определить ее конечные точки. Конечная точка в узле службы указывается в структуре [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) и определяется следующими сведениями:

-   Адрес, представляющий собой физический универсальный код ресурса (URI), на котором будет размещена служба.
-   Структура [**\_ \_ типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , указывающая тип базового канала для конечной точки.
-   Структура [**\_ \_ привязки канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , указывающая привязку канала.
-   Структура [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , содержащая описание безопасности для конечной точки.
-   Структура [**\_ \_ контракта службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) , представляющая [контракт службы](contract.md) для конечной точки.
-   Структура [**\_ \_ \_ обратного вызова безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) , указывающая функцию обратного вызова авторизации для конечной точки.
-   Структура [**\_ \_ \_ свойств конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) , которая содержит массив свойств конечной точки службы.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

Для SOAP через UDP поддерживаются только односторонние контракты, представленные [**\_ \_ \_ привязкой канала WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) в перечислении **\_ \_ привязки канала WS** .

После определения конечной точки ее можно передать в функцию [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , которая принимает массив указателей на структуры [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Приложение может дополнительно предоставить массив [**свойств службы**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) для [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) для настройки пользовательских параметров на узле службы.

Приложение открывает узел службы, чтобы начать принимать клиентские запросы.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

После открытия узла службы приложение может закрыть его, если для него не требуется никаких операций. Обратите внимание, что это не освобождает ресурсы и может быть повторно открыто при последующем вызове [**всресетсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

После закрытия узла службы приложение может сбросить узел службы для повторного использования.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Когда приложение выполняется с помощью узла службы, можно освободить ресурсы, связанные с узлом службы, вызвав функцию [**всфрисервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) . Обратите внимание, что перед вызовом этой функции необходимо вызвать [**всклосесервицехост**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) .

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Сведения о присоединении пользовательского состояния к узлу службы см. в разделе [состояние узла пользователя](user-host-state.md) .

Сведения об авторизации в узле службы для данной конечной точки см. в разделе [Авторизация служб](service-authorization.md).

Сведения о реализации операций службы и контрактов служб для службы см. в разделах [Сервис Operations](server-side-service-operations.md) and [Service Contract](contract.md).

## <a name="security"></a>Безопасность

Приложение может использовать свойства для контроля за объемом ресурсов, выделяемых узлом службы от имени приложения:

-   [**Служба WS \_ \_ \_ \_ Максимальное число \_ \_ принимаемых каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id):
-   [**Служба WS \_ \_ \_ \_ Максимальная \_ степень параллелизма для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**Служба WS \_ \_ \_ \_ Максимальное число \_ каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id):
-   [**Служба WS \_ \_ \_ \_ \_ \_ максимальный \_ Размер кучи тела свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**Служба WS \_ \_свойство конечной точки службы: \_ \_ максимальный \_ \_ \_ размер пула вызовов**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**Служба WS \_ \_ \_ \_ Максимальное значение \_ \_ \_ размера пула каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Для каждого из этих свойств выбираются безопасные значения по умолчанию. приложение должно быть внимательным, если нужно изменить эти свойства. Помимо указанных выше свойств, свойства [канала](channel.md), [прослушивателя](listener.md) и сообщения, относящиеся к [сообщению](message.md) , также могут быть изменены приложением. Прежде чем изменять эти параметры, ознакомьтесь с вопросами безопасности этих компонентов.

Кроме того, при использовании API узла службы ВВСАПИ необходимо тщательно оценить следующие аспекты разработки приложений:

-   При использовании MEX приложения должны быть осторожными, чтобы не раскрывать какие бы то ни было конфиденциальные данные. Как минимум, если характер данных, предоставляемых через MEX, является конфиденциальным, приложения могут настроить конечную точку обмена метаданными с безопасной привязкой, которая требует проверки подлинности по крайней мере и реализуют авторизацию как часть конечной точки с помощью [**\_ \_ \_ обратного вызова безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   По умолчанию подробные сведения об ошибках с помощью ошибок отключены для узла службы с помощью свойства [**\_ \_ \_ \_ утечки ошибки свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) . Приложение может отсылать обширные сведения об ошибках в рамках сбоя. Однако это может привести к раскрытию информации, поэтому рекомендуется изменить этот параметр только для сценариев отладки.
-   Помимо проверки, выполненной для базового профиля 2,0 и XML-сериализации, узел службы не выполняет проверку содержимого данных, полученного в составе параметров операции службы. Приложение обязано выполнять все проверки параметров самостоятельно.
-   Авторизация не реализована в составе узла службы. Однако приложения могут реализовать собственную схему авторизации, используя [**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) и [**\_ \_ \_ обратный вызов безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Приложение обязано использовать для своей конечной точки безопасные привязки. Узел службы не обеспечивает никакой безопасности, помимо того, что настроено в конечной точке.

С узлом службы используются следующие элементы API.

| Обратный вызов                                                                             | Описание                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_ \_ \_ обратный вызов для приема канала службы \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Вызывается, когда узел службы принимает канал на прослушиватель конечной точки. |
| [**\_ \_ \_ обратный вызов для закрытия канала службы \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Вызывается, когда канал закрывается или прерывается в конечной точке.                     |



 



| Перечисление                                                                    | Описание                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ \_ идентификатор свойства конечной точки службы \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Необязательные параметры для [**настройки \_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**\_ \_ состояние узла службы \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Состояния, в которых может находиться узел службы.                                                   |
| [**\_ \_ идентификатор свойства службы \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Необязательные параметры для настройки узла службы.                                       |



 



| Функция                                                     | Описание                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**всабортсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Прерывает и прекращает выполнение текущих операций на узле службы.                          |
| [**всклосесервицехост**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Закрывает все прослушиватели, чтобы новые каналы не принимались с клиента.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Создает узел службы.                                                                      |
| [**всфрисервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Освобождает память, связанную с объектом узла службы.                                   |
| [**всжетсервицехостпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Извлекает указанное свойство узла службы.                                                 |
| [**всопенсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Открывает узел службы для взаимодействия и запускает прослушиватели на всех конечных точках.        |
| [**всресетсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Сбрасывает узел службы для повторного использования и сбрасывает базовый канал и прослушиватели для повторного использования. |



 



| Дескриптор                                       | Описание                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_узел службы \_ WS**](ws-service-host.md) | Непрозрачный тип, используемый для ссылки на узел службы. |



 



| Структура                                                                              | Описание                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_ \_ Конечная точка службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Представляет отдельную конечную точку на узле службы.                            |
| [**\_ \_ свойство конечной точки службы WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Задает зависящий от службы параметр.                                           |
| [**\_свойство службы \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Задает зависящий от службы параметр.                                           |
| [**\_ \_ \_ обратный вызов Accept для свойства службы WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Указывает обратный вызов, который вызывается, когда канал успешно принят. |
| [**\_ \_ \_ обратный вызов закрытия свойства службы WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Указывает обратный вызов, который вызывается при закрытии канала.    |



 

 

 




