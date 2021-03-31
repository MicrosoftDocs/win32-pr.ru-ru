---
title: Обзор уровня модели службы
description: API-интерфейс модели службы ВВСАПИ моделирует связь между клиентом и службой в качестве вызовов метода, а не сообщений данных.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Обзор уровня модели службы веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104351115"
---
# <a name="service-model-layer-overview"></a>Обзор уровня модели службы

API-интерфейс модели службы ВВСАПИ моделирует связь между клиентом и службой в качестве вызовов метода, а не сообщений данных. В отличие от [уровня канала](channel-layer-overview.md), который поддерживает более традиционные обмены [сообщениями](message.md) между клиентом и службой, модель службы автоматически управляет связью с помощью прокси-сервера службы на клиенте и узла службы в службе. Это означает, что клиент вызывает созданные функции, а сервер реализует обратные вызовы.


Например, рассмотрим службу калькулятора, которая выполняет сложение и вычитание двух чисел. Сложение и вычитание — это операции, естественно представленные в виде вызовов методов.

![Диаграмма, показывающая, как служба калькулятора взаимодействует с клиентом, используя вызовы методов для сложения и вычитания.](images/servicemodelintro.png)

Модель службы представляет взаимодействие между клиентом и службой в виде объявленных вызовов методов, поэтому скрывает сведения о связи базового уровня канала из приложения, упрощая реализацию службы.

## <a name="specifying-a-service"></a>Указание службы

Служба должна быть указана с точки зрения его шаблонов обмена сообщениями, а также его представления данных сети. Для служб эта спецификация обычно предоставляется в виде документов WSDL и XML-схем.

Документ WSDL представляет собой XML-документ, содержащий привязку канала и шаблоны обмена сообщениями службы, в то время как документ схемы XML представляет собой XML-документ, определяющий представление данных отдельных сообщений.

Для службы калькулятора и ее операций сложения и вычитания документ WSDL может выглядеть, как в следующем примере:

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

Аналогичным образом ее XML-схема может быть определена следующим образом:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Преобразование метаданных в код

Модель службы предоставляет [WsUtil.exe](web-service-compiler-tool.md) в качестве средства для обработки этих документов метаданных, преобразования WSDL-файла в заголовок C и исходные файлы.

![Схема, показывающая, как WsUtil.exe преобразует WSDL-файл в заголовок C и исходные файлы.](images/doctotool.png)

[WsUtil.exe](web-service-compiler-tool.md) создает заголовок и источники для реализации службы, а также операции службы на стороне клиента для клиента.

## <a name="calling-the-calculator-service-from-a-client"></a>Вызов службы калькулятора из клиента

Как и в случае с реализацией службы, клиент должен включать созданный заголовок или заголовки.

``` syntax
#include "CalculatorProxyStub.h"
```

Теперь клиентское приложение может создать и открыть прокси-сервер службы, чтобы начать обмен данными со службой калькулятора.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

Приложение может вызвать операцию добавления в службе калькулятора с помощью следующего кода:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Ознакомьтесь с примером кода в [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md) для полной реализации службы калькулятора.

## <a name="service-model-components"></a>Компоненты модели службы

Взаимодействие отдельных компонентов модели службы ВВСАПИ в примере калькулятора выглядит следующим образом:

-   Клиент создает [прокси-сервер службы](service-proxy.md) и открывает его.
-   Клиент вызывает функцию добавления службы и передает прокси-сервер службы.
-   Сообщение сериализуется в соответствии с метаданными сериализации в заголовке и исходных файлах, созданных средством метаданных ([WsUtil.exe](web-service-compiler-tool.md)).
-   Сообщение записывается в канал и передается по сети службе.
-   На стороне сервера служба размещается внутри узла службы и имеет конечную точку, которая прослушивает контракт ICalculator.
-   Используя метаданные модели службы в заглушке, служба десериализует сообщение от клиента и отправляет его в заглушку.
-   Служба на стороне сервера вызывает метод Add, передавая ему контекст операции. Этот контекст операции содержит ссылку на входящее сообщение.

![Схема, демонстрирующая взаимодействие отдельных компонентов модели службы ВВСАПИ.](images/servicemodellayout.png)

Компоненты

-   [Узел службы](service-host.md): размещает службу.
-   [Прокси-сервер службы](service-proxy.md): определяет, как клиент взаимодействует со службой.
-   [Контекст](context.md): контейнер свойств, предназначенный для предоставления сведений о состоянии для операции службы.
-   [Контракт](contract.md): определение интерфейса службы. Например, ICalculator представляет контракт для службы калькулятора в нашем примере кода.
-   [WsUtil.exe](web-service-compiler-tool.md): средство метаданных модели службы для создания прокси-серверов и заглушек.

 

 




