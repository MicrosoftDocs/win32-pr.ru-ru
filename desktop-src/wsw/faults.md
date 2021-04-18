---
title: Ошибки
description: Сообщение об ошибке используется для того, чтобы сообщить о сбое на удаленной конечной точке.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Ошибки веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710045"
---
# <a name="faults"></a>Ошибки

Сообщение об ошибке используется для того, чтобы сообщить о сбое на удаленной конечной точке. Сообщение об ошибке похоже на любое другое сообщение, за исключением того, что формат текста сообщения имеет стандартный формат. Ошибки могут использоваться как с помощью протоколов инфраструктуры, таких как WS-Addressing, так и протоколами приложений более высокого уровня.

-   [Обзор](#overview)
-   [Создание ошибок в службе](#generating-faults-in-a-service)
-   [Обработка ошибок на клиенте](#handling-faults-on-a-client)
-   [Использование ошибок с сообщениями](#using-faults-with-messages)

## <a name="overview"></a>Обзор

Содержимое текста сообщения об ошибке представлено в этом API с использованием структуры [**\_ ошибок WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) . Хотя ошибка имеет фиксированный набор полей, которые используются для предоставления сведений об ошибке (например, [**\_ \_ код ошибки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) , определяющий тип сбоя, и [**\_ \_ Причина сбоя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) , содержащая текст, описывающий ошибку), она также содержит поле сведений, которое можно использовать для указания произвольного XML-содержимого, связанного с ошибкой.

## <a name="generating-faults-in-a-service"></a>Создание ошибок в службе

Как правило, служба отправит ошибку из-за ошибки, возникшей во время обработки запроса. Модель, используемая этим API, заключается в том, что код в службе, который встречает ошибку обработки, захватывает необходимые сведения об ошибках в объекте [WS \_ Error](ws-error.md) , а затем код на более высоком уровне в цепочке вызовов фактически отправит ошибку, используя сведения, полученные на более низком уровне. Эта схема позволяет изолировать код, который отправляет ошибку, от того, как ошибки сопоставлены с ошибками, в то же время позволяя отправлять сообщения об ошибках.

Следующие свойства можно использовать с [**вссетфаултеррорпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) для записи сведений об [ \_ ошибке для объекта ошибки WS](ws-error.md) :

-   [**Служба WS \_ \_ \_ \_ действие свойства ошибки сбоя**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Указывает действие, которое будет использоваться для сообщения об ошибке. Если этот аргумент не указан, предоставляется действие по умолчанию.
-   [**Служба WS \_ сбой \_ \_ свойства ошибки \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Содержит структуру [**\_ ошибки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , которая отправляется в тексте сообщения об ошибке.
-   [**Служба WS \_ \_ \_ \_ заголовок свойства ошибки сбоя**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Некоторые ошибки включают заголовки сообщений, которые добавляются к сообщению об ошибке для передачи ошибок обработки, связанных с заголовками сообщения запроса. Это свойство можно использовать для указания [ \_ XML- \_ буфера WS](ws-xml-buffer.md) , содержащего заголовок, добавляемый к сообщению об ошибке.

Все строки ошибок, добавленные в объект [ \_ ошибки WS](ws-error.md) , используются в качестве текста в отправляемом сбое. Строки ошибок могут быть добавлены к объекту Error с помощью [**всаддеррорстринг**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

Для установки этих свойств объекта [ \_ ошибки WS](ws-error.md) можно использовать функцию [**вссетфаултеррорпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) .

Чтобы задать подробные сведения об ошибке, хранящейся в объекте [WS \_ Error](ws-error.md) , используйте функцию [**вссетфаултеррордетаил**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) . Эта функция может использоваться для связывания произвольного XML-содержимого с ошибкой.

[Узел службы](service-host.md) будет автоматически отсылать ошибки, используя приведенные выше сведения об объекте [ \_ ошибки WS](ws-error.md) . Свойство [**« \_ \_ \_ \_ утечка ошибки свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) » может использоваться для управления тем, как будет отправлена информация об ошибке.

При работе на уровне канала ошибки могут отправляться для объекта [WS \_ Error](ws-error.md) с помощью [**вссендфаултмессажефореррор**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Обработка ошибок на клиенте

Если клиент получает сообщение об ошибке при использовании [прокси-сервера службы](service-proxy.md) или через [**всрекуестрепли**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) или [**всрецеивемессаже**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), будет возвращена ошибка **\_ \_ конечной точки \_ \_ WS E** . (Дополнительные сведения см. в разделе [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md).) Эти функции также будут заполнять объект [ \_ ошибки WS](ws-error.md) , переданный в вызов, сведениями о полученных сбоях.

Следующие свойства объекта [ \_ ошибки WS](ws-error.md) можно запросить с помощью [**всжетфаултеррорпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) , чтобы получить сведения о полученном сбое:

-   [**Служба WS \_ \_ \_ \_ действие свойства ошибки сбоя**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Указывает значение действия сообщения об ошибке.
-   [**Служба WS \_ сбой \_ \_ свойства ошибки \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Содержит структуру [**\_ ошибки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , десериализованную из тела сообщения об ошибке.

Ошибка может содержать произвольное дополнительное XML-содержимое в деталях ошибки. Для доступа к этому можно использовать функцию [**всжетфаултеррордетаил**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) .

## <a name="using-faults-with-messages"></a>Использование ошибок с сообщениями

Следующий раздел применим непосредственно к содержимому тела сообщения об ошибке.

Содержимое текста сообщения об ошибке представлено стандартной структурой [**\_ ошибок WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , которая имеет встроенную поддержку сериализации.

Например, следующий код можно использовать для записи ошибки в текст сообщения:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Следующий код можно использовать для считывания ошибки из текста сообщения:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Чтобы узнать, является ли полученное сообщение ошибкой или нет, можно обратиться к [**\_ \_ свойству WS Message \_ — \_ Ошибка**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Это свойство задается в зависимости от того, является ли первый элемент в теле элементом Fault во время [**всреадмессажестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) или [**всреаденвелопестарт**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).

Чтобы создать ошибку [**WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) с помощью [ \_ ошибки WS](ws-error.md), используйте функцию [**вскреатефаултфромеррор**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) .

Следующие перечисления являются частью ошибок:

-   [**\_раскрытие ошибок WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**\_ \_ \_ идентификатор свойства ошибки сбоя \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Следующие функции являются частью ошибок:

-   [**вскреатефаултфромеррор**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**всжетфаултеррордетаил**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**всжетфаултеррорпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**вссетфаултеррордетаил**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**вссетфаултеррорпроперти**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Следующие структуры являются частью ошибок:

-   [**\_сбой WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_код ошибки \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_ \_ подробное описание ошибки WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**\_Причина сбоя \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




