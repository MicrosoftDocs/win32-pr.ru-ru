---
title: Контракт
description: Контракт службы содержит метаданные, которые определяют, как служба обрабатывает сообщения канала.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Веб-службы контрактов для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566995"
---
# <a name="contract"></a>Контракт

Контракт службы содержит метаданные, которые определяют, как служба обрабатывает сообщения канала.


[**\_ \_ Контракт службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) содержит метаданные для службы, которая обрабатывает [ \_ сообщение WS](ws-message.md).

![Схема, показывающая WS_SERVICE_CONTRACT метаданных в сообщении в конечную точку службы.](images/servicecontractintro.png)

Он содержит [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) и таблицу функций. Приложение может дополнительно указать [**\_ \_ \_ \_ обратный вызов приема сообщений WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Если [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) и Таблица функций не заданы, приложение должно указать [**\_ \_ \_ \_ обратный вызов получения сообщения службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Схема, демонстрирующая операции добавления и вычитания службы в контракте службы ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Дополнительные сведения см. в примере [калькулятора](httpcalculatorserviceexample.md) .

Описание контракта

[**Служба WS \_ \_Описание контракта**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) — это метаданные, определяющие тип-контракт службы. Создано [wsutil.exe](web-service-compiler-tool.md).

В терминах WSDL [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) сопоставляется с WSDL: PortType. Для каждого WSDL: portType в документе WSDL будет создано отдельное **\_ \_ Описание контракта WS** .

Описание контракта состоит из нескольких [операций службы](service-operation.md)или более. Эти операции задаются в виде массива [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Схема, показывающая WS_CONTRACT_DESCRIPTION в виде массива WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Дополнительные сведения о преобразовании [**\_ \_ описания контракта**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) WSDL: portType в WS см. в [разделе выходные данные WSDL](wsdl-support.md).

Пример: [ **\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Таблица функций

Таблица функций представляет собой структуру указателей функций, представляющих каждую из [операций службы](service-operation.md) в контракте службы. Определение таблицы функции также создается [wsutil.exe](web-service-compiler-tool.md).

Пример: Таблица функций

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Использование [ **\_ \_ \_ \_ обратного вызова получения сообщения службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**Служба WS \_ \_ \_ \_ Обратный вызов приема сообщений службы**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) имеет двойную взаимоисключающую роль.

Если в [**\_ \_ контракте службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)задано [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , оно становится обработчиком сообщений по умолчанию для всех действий, которые не поддерживаются указанным **\_ \_ описанием контракта WS**. В противном случае, если в **\_ \_ контракте службы WS** не задано **\_ \_ Описание контракта WS** , а в **\_ \_ контракте службы** WS указан [**\_ \_ \_ \_ ответный вызов Receive службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) , все поступившие [сообщения](ws-message.md) передаются в этот обратный вызов.

Дополнительные примеры см. в разделе

-   [Пример нетипизированной службы](untypedserviceexample.md)
-   [Пример службы калькулятора](httpcalculatorserviceexample.md)
-   [Операции службы](service-operation.md)

Следующие обратные вызовы являются частью контракта:

-   [**\_ \_ \_ \_ ответный вызов получения сообщения службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_ \_ обратный вызов заглушки службы WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Следующие структуры являются частью контракта:

-   [**\_Описание контракта \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_контракт службы \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




