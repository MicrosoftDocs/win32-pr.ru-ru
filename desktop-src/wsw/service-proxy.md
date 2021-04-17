---
title: Прокси-сервер службы
description: Прокси службы — это прокси-сервер на стороне клиента для службы.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Веб-службы прокси службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105684732"
---
# <a name="service-proxy"></a>Прокси-сервер службы

Прокси службы — это прокси-сервер на стороне клиента для службы. Прокси-сервер службы позволяет приложениям отправлять и получать [сообщения](message.md) по [каналу](channel.md) в виде вызовов методов.

Прокси-серверы служб создаются по мере необходимости, открываются, используются для вызова службы и закрываются, когда они больше не нужны. Кроме того, приложение может повторно использовать прокси-сервер службы для многократного подключения к той же службе без затрат времени и ресурсов, необходимых для инитиалисинг прокси службы. На следующей схеме показана последовательность возможных состояний прокси-сервера службы и вызовов функций или событий, ведущих от одного состояния к другому.

![Схема, показывающая состояния прокси-сервера службы и вызовов функций или событий, ведущих от одного состояния к другому.](images/serviceproxystates.png)

Эти состояния прокси-службы перечисляются в перечислении [**\_ \_ \_ состояния прокси-службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .

Как показано на предыдущей схеме и следующем коде, прокси службы создается путем вызова функции [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) . В качестве параметров для этого вызова ВВСАПИ предоставляет следующие перечисления:

-   [**\_Тип канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**\_Привязка канала \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Он также принимает необязательные параметры, используя следующие типы данных:

-   [**\_идентификатор свойства прокси-сервера WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**\_Описание безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

После создания прокси-сервера службы функция **вскреатесервицепрокси** возвращает ссылку на прокси-сервер службы [WS \_ \_ -proxy](ws-service-proxy.md)с помощью параметра out.

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

После создания прокси-сервера службы приложение может открыть прокси-сервер службы для взаимодействия со службой, вызвав функцию [**всопенсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , передав структуру [**адресов**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) , содержащую сетевой адрес конечной точки службы для подключения.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

При открытии прокси-сервера службы приложение может использовать его для выполнения вызовов к службе.

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

Если приложению больше не требуется прокси-сервер службы, он закрывает прокси-сервер службы, вызывая функцию [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) . Он также освобождает связанную память путем вызова [**всфрисервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a>Повторное использование прокси-сервера службы

Кроме того, после вызова [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) приложение может повторно использовать прокси-сервер службы, вызвав функцию [**всресетсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Дополнительные сведения о том, как прокси-серверы служб используются в разных контекстах, см. в следующих разделах:

-   [Прокси-сервер службы и сеансы](service-proxy-and-sessions.md)
-   [Операция службы](service-operation.md)
-   [Операции службы на стороне клиента](client-side-service-operations.md)
-   [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md)

### <a name="security"></a>Безопасность

При использовании API прокси-сервера службы ВВСАПИ следует внимательно отметить следующие аспекты проектирования приложений:

-   Прокси-сервер службы не будет выполнять проверку данных после проверки базового профиля 2,0 и сериализации XML. Это приложение отвечает за проверку данных, содержащихся в параметрах, которые они получают обратно в рамках вызова.
-   Настройка максимального количества ожидающих вызовов на прокси-сервере службы с помощью значения перечисления [**\_ \_ \_ идентификатора свойства прокси-**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) сервера WS **\_ Максимальное число \_ \_ \_ ожидающих \_ вызовов**, обеспечивающее защиту от сервера, на котором выполняется задержка. Максимальное значение по умолчанию — 100. Приложения должны соблюдать осторожность при изменении значений по умолчанию.
-   Прокси-сервер службы не предоставляет гарантий безопасности, кроме тех, которые указаны в структуре [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , используемой для взаимодействия с сервером.
-   Следите за внесением изменений в [сообщения](message.md) и [каналы](channel.md) по умолчанию на прокси-сервере службы. Прежде чем изменять какие либо связанные свойства, прочтите вопросы безопасности, связанные с сообщениями и каналами.
-   Прокси-сервер службы шифрует все учетные данные, которые он хранит в памяти.

Следующие элементы API связаны с прокси-серверами служб.

| Обратный вызов                                                          | Описание                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ обратный вызов сообщения прокси-сервера WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Вызывается при отправке заголовков входного сообщения или при получении только тех выходных заголовков сообщений. |



 



| Перечисление                                                 | Описание                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_ \_ идентификатор свойства вызова \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Перечисляет необязательные параметры для настройки вызова в операции службы на стороне клиента. |
| [**\_идентификатор свойства прокси-сервера WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Перечисляет необязательные параметры для настройки прокси-сервера службы.                         |
| [**\_ \_ состояние прокси-сервера службы WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Состояние прокси-сервера службы.                                                           |



 



| Функция                                                       | Описание                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Прерывает указанный вызов для указанного прокси-сервера службы.                           |
| [**всабортсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Отменяет все ожидающие входные и выходные данные для указанного прокси-сервера службы.                |
| [**вскалл**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Только для внутреннего использования. Сериализует аргументы в сообщение и отправляет их по каналу. |
| [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Закрывает прокси-сервер службы для связи.                                         |
| [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Создает прокси-сервер службы.                                                          |
| [**всфрисервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Освобождает память, связанную с прокси-сервером службы.                              |
| [**всжетсервицепроксипроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Извлекает указанное свойство прокси-сервера службы.                                     |
| [**всопенсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Открывает прокси-сервер службы для конечной точки службы.                                      |
| [**всресетсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Сбрасывает прокси-сервер службы.                                                             |



 



| Дескриптор                                     | Описание                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_ \_ прокси-сервер службы WS](ws-service-proxy.md) | Непрозрачный тип, используемый для ссылки на прокси-сервер службы. |



 



| Структура                                         | Описание                 |
|---------------------------------------------------|-----------------------------|
| [**\_свойство Call вызова WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Задает свойство Call.  |
| [**Служба WS \_ \_свойство прокси-сервера**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Задает свойство прокси-сервера. |



 

 

 




