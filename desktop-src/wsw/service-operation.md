---
title: Операция службы
description: Операция службы — это код и метаданные, связанные с определенной операцией службы.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Веб-службы операций службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acde0c2151dea483a3e82f45c7031fa201614076f7a5ea624926fbe08e7588b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026271"
---
# <a name="service-operation"></a>Операция службы

Операция службы — это код и метаданные, связанные с определенной операцией службы.


С точки зрения языка WSDL каждая операция WSDL:, определенная в документе WSDL для заданного portType, является операцией службы.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Каждая операция службы в модели службы задается как [**\_ \_ Описание операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). \_Описание операции WS \_ создается [wsutil.exe](web-service-compiler-tool.md).

Для каждой операции WSDL: Программа создает отдельное [**\_ \_ Описание операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Схема, показывающая, как wsutil.exe создает WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

С точки зрения кода каждая операция службы имеет связанную с ней функцию. Определение этой функции отличается для клиентов и серверов.

Операции службы классифицируются в,

-   [Операции службы на стороне клиента](client-side-service-operations.md)
-   [Операции службы на стороне сервера](server-side-service-operations.md)

Эта классификация в основном основана на макете подписи сервера и реализации операций службы на стороне клиента.

См. также [раздел Поддержка языка WSDL](wsdl-support.md).

С операциями службы используются следующие перечисления.

-   [**\_тип параметра \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**\_ \_ Причина отмены службы \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**\_ \_ \_ параметр сообщения операции службы \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Для операций службы используются следующие структуры:

-   [**\_Описание сообщения \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**\_Описание операции \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_Описание параметра \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




