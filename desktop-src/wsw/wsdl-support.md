---
title: WSDL и контракты служб
description: Служебная программа Wsutil.exe создает заглушку языка C в соответствии с предоставленными метаданными WSDL, а также определения типов данных и описания типов данных, описанных в XML-схемах, созданных пользователем.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Поддержка языка WSDL
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203ee1819a596d2d49a7d0b7c789d5f4e1269b6d8d75f78e2db0913b6a97ec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880744"
---
# <a name="wsdl-and-service-contracts"></a>WSDL и контракты служб

Служебная программа [Wsutil.exe](web-service-compiler-tool.md) создает заглушку языка C в соответствии с предоставленными метаданными WSDL, а также определения типов данных и описания типов данных, описанных в XML-схемах, созданных пользователем.


Ниже приведен пример документа WSDL и XML-схемы, которая служит основанием для обсуждения:

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

В этом примере представлен контракт Исимплесервице с одним методом Симплемесод. "Симплемесод" имеет два входных параметра типа **целое число**, *a* и *b*, которые отправляются от клиента к службе. Аналогично, Симплемесод имеет два выходных параметра типа **Integer**, *b* и *c*, которые возвращаются клиенту после успешного завершения. В синтаксисе C с заметками SAL определение метода выглядит следующим образом:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

В этом определении Исимплесервице является контрактом службы с одной операцией службы: Симплемесод.

Выходной файл заголовка содержит определения и описания для внешней ссылки. В том числе:

-   Определения структур C для глобальных типов элементов.
-   Прототип операции, определенный в текущем файле.
-   Прототип таблицы функций для контрактов, указанных в WSDL-файле.
-   Клиентский прокси и прототипы заглушки службы для всех функций, указанных в текущем файле.
-   Структура [**данных \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) для элементов глобальной схемы, определенных в текущем файле.
-   Структура [**данных \_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) для всех сообщений, указанных в текущем файле.
-   Структура [**данных \_ \_ описания контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для всех контрактов, указанных в текущем файле.

Создается одна глобальная структура для инкапсуляции всех глобальных описаний типов схем и моделей служб, на которые может ссылаться приложение. Структура именуется с использованием нормализованного имени файла. В этом примере Wsutil.exe создает структуру глобальных определений с именем Example \_ WSDL, которая содержит все описания веб-служб. Определение структуры создается в файле заглушки.

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

Для определений глобальных элементов в документе схемы XML (XSD) один прототип [**\_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , а также соответствующее определение типа C создаются для каждого элемента. Прототипы описаний элементов для Симплемесод и Симплемесодреспонсе создаются как элементы в приведенной выше структуре. Структуры C создаются следующим образом:

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

Аналогично глобальным сложным типам Wsutil.exe создает определения структур типа C, как показано выше, без совпадающих описаний элементов.

Для входных данных WSDL Wsutil.exe создает следующие прототипы и определения:

-   Для описания сообщения создается прототип [**\_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) . Это описание может использоваться моделью службы, а также уровнем сообщений. Структуры описания сообщений — это поля с именами «мессаженаме» в глобальной структуре. В этом примере описание сообщения создается как \_ поле исимплесервице симплемесод \_ инпутмессаже в \_ структуре исимплесервице симплемесод \_ инпутмессаже, как указано в WSDL-файле.
-   [**Служба WS \_ Прототип \_ описания контракта**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) создается для описания контракта. Это описание используется моделью службы. Структуры описания контракта — это поля с именами «ContractName» в глобальной структуре. В этом примере описание контракта создается как \_ поле дефаултбиндинг исимплесервице в структуре " \_ example \_ WSDL".

Спецификации операций и типов являются общими для прокси-серверов и заглушек и создаются в обоих файлах. Wsutil.exe создает одну копию, только если в одном файле создаются прокси-серверы и заглушки.

## <a name="identifier-generation"></a>Создание идентификатора

Автоматически созданные структуры C, перечисленные выше, создаются на основе имени, указанного в WSDL-файле. NCName XML, как правило, не считается допустимым идентификатором C, а имена при необходимости нормализуются. Шестнадцатеричные значения не преобразуются, а распространенные буквы, такие как ":", "/" и ".", преобразуются в символ подчеркивания " \_ " для повышения удобочитаемости.

## <a name="header-for-the-stub"></a>Заголовок для заглушки

Для каждой операции в контракте службы создается одна подпрограммы обратного вызова с именем <operationname> callback. (Например, операция "Симплемесод" в примере контракта службы имеет созданный обратный вызов с именем "Симплемесодкаллбакк".)

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Для каждого Wsutil.exe WSDL **portType** формирует таблицу функций, представляющую **portType**. Каждая операция с **portType** имеет соответствующий указатель на функцию обратного вызова, присутствующую в таблице функций.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Прототипы прокси-сервера создаются для всех операций. Имя прототипа — это имя операции (в данном случае «Симплемесод»), указанное в WSDL-файле для контракта службы.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Создание прототипа описания только для локального кода

Прокси-файлы андстуб содержат определение для структуры глобальных определений, включая прототипы и определения для структур, содержащих только локальные описания и реализации прокси-сервера и заглушки клиента.

Все прототипы и определения, локальные для файла заглушки, создаются в составе структуры инкапсуляции. Эта реструктуризация структуры локальных описаний предоставляет четкую иерархию описаний, необходимых уровню сериализации и модели службы. Локальная структура описания имеет прототипы, аналогичные показанным ниже.

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a>Ссылки на определения из других файлов

Локальные определения могут ссылаться на описания, созданные в другом файле. Например, сообщение может быть определено в файле кода C, созданном из WSDL-файла, но элемент Message может быть определен в любом расположении в файле кода C, созданном из XSD-файла. В этом случае Wsutil.exe создает ссылку на глобальный элемент из файла, содержащего определение сообщения, как показано ниже:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Глобальные описания элементов

Для каждого глобального элемента, определенного в файле WSDL: Type или XSD, существует совпадающее поле с именем **ElementName** внутри поля **глобалелемент** . В этом примере создается структура с именем Симплемесод:

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

Другие описания, необходимые для описания элемента, создаются как часть содержащей их структуры. Если элемент является простым элементом типа, то существует только одно поле [**\_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) . Если тип элемента является структурой, все связанные поля и описания структуры создаются как часть структуры элемента. В этом примере элемент Симплемесод является структурой, содержащей два поля, **a** и **b**. Wsutil.exe создает структуру следующим образом:

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

Внедренные структуры и внедренные элементы создаются как вложенные структуры по мере необходимости.

## <a name="wsdl-related-definitions"></a>Определения, связанные с WSDL

Wsutil.exe создает поле в разделе WSDL для каждого из значений **portType** , определенных в заданной службе WSDL: Service.

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

Wsutil.exe создает одно поле f, содержащее все описания, необходимые для операции, массив единый указателей на каждое описание операции для каждого метода и одно [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для указанного **portType**.

Все описания, необходимые для операций, создаются внутри поля **operationName** в указанном **portType**. К ним относятся [**поле \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , а также вложенная структура для входных и выходных параметров. Аналогично, [**поля \_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) для входного сообщения и необязательное выходное сообщение включаются вместе с. [**Служба WS \_ Поле со списком \_ Описание параметра**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) для всех параметров операции и поле [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) для самой операции. В этом примере создается структура кода для описания Симплемесод, как показано ниже:

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a>Определения, связанные с словарем XML

Имена и пространства имен, используемые в различных описаниях, создаются как поля типа [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string). Все эти строки создаются как часть словаря констант для каждого файла. Список строк и поле [**\_ \_ словаря WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (с именем **словарь** в примере ниже) создаются как часть поля DICTIONARY структуры **филенамелокал** .

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

Массив [**\_ \_ строк WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)(s) создается как ряд полей типа **WS \_ XML \_ String** с именем с понятными именами пользователей. Созданная заглушка использует понятные имена пользователей в различных описаниях для повышения удобочитаемости.

Клиентский прокси-сервер для операций WSDL

Wsutil.exe создает клиентский прокси-сервер для всех операций. Приложения могут перезаписывать сигнатуру метода с помощью префиксного параметра командной строки.

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

Вызывающий объект операции должен передать допустимый параметр *кучи* . Выходные параметры выделяются с помощью \_ значения WS Heap, указанного в параметре *heap* . Вызывающая функция может сбросить или освободить кучу, чтобы освободить память для всех выходных параметров. Если операция завершается неудачно, дополнительные сведения об ошибке можно получить из необязательного объекта ошибки, если он доступен.

Wsutil.exe создает заглушку службы для всех операций, описанных в разделе Binding.

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

В приведенном выше разделе описывается прототип локальной структуры, содержащей все определения, локальные только для файла заглушки. В последующих разделах описаны определения описаний.

## <a name="wsdl-definition-generation"></a>Создание определения WSDL

Wsutil.exe создает константную статическую структуру (**const static**) с именем *<\_ имя файла>* локалдефинитионс типа *<имя службы \_>* Local, которая содержит все локальные определения.

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

Поддерживаются следующие описания WSDL:

-   WSDL: Service
-   WSDL: Binding
-   WSDL: portType
-   WSDL: Operation
-   WSDL: Message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Обработка WSDL: Operation и WSDL: Message

Каждая операция, указанная в документе WSDL, сопоставляется с операцией службы с помощью [Wsutil.exe](web-service-compiler-tool.md). Средство создает отдельные определения операций службы как для сервера, так и для клиента.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Макет элементов данных входных сообщений андаутпут вычисляется средством для создания метаданных сериализации для инфраструктуры, а также фактической сигнатуры итоговой операции службы, с которой связаны входные и выходные сообщения.

Метаданные каждой операции в определенном **portType** имеют входные данные и, при необходимости, выходное сообщение, каждое из этих сообщений сопоставляется [**с \_ \_ описанием сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). В этом примере входные и выходные сообщения для операции в portType сопоставлены с Инпутмессажедескриптион и, по желанию, Аутпутмессажедескриптион в [**\_ \_ описании операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) соответственно.

Для каждого сообщения WSDL средство создает [**\_ \_ Описание сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) , которое ссылается на [**определение \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , как показано ниже:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Описание сообщения относится к описанию элемента ввода. Поскольку элемент определен глобально, описание сообщения ссылается на глобальное определение, а не на локальный статический элемент. Аналогично, если элемент определен в другом файле, Wsutil.exe создает ссылку на глобально определенную структуру в этом файле. Например, если Симплемесодреспонсе определен в другом файле example. xsd, вместо этого Wsutil.exe создает следующее:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Каждое описание сообщения содержит действие и конкретное описание элемента (поле типа « [**\_ \_ Описание элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)») для всех элементов данных сообщения. В случае сообщения в стиле RPC или сообщения с несколькими частями создается элемент-оболочка для инкапсуляции дополнительной информации.

## <a name="rpc-style-support"></a>Поддержка стиля RPC

Wsutil.exe поддерживает стиль документа и операции в стиле RPC согласно спецификации привязки WSDL 1,1 для SOAP 1,2. Операции RPC и в стиле литерала помечаются как \_ \_ литеральная \_ Операция WS RPC. Модель службы игнорирует имя элемента оболочки текста ответа в операциях RPC/Literal.

Wsutil.exe изначально не поддерживает операции в стиле кодировки. \_ \_ Параметр буфера WS XML создается для кодирования сообщений, и разработчики должны непосредственно заполнять непрозрачный буфер.

## <a name="multiple-message-parts-support"></a>Поддержка нескольких частей сообщений

Wsutil.exe поддерживает несколько частей сообщений в одном сообщении. Сообщение с несколькими частями можно указать следующим образом:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe создает поле [**\_ \_ типа структуры WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) для элемента Message, если сообщение содержит несколько частей. Если сообщение представлено с использованием стиля документа, Wsutil.exe создает элемент-оболочку с типом struct. Элемент упаковщика не имеет имени или определенного пространства имен, а структура оболочки содержит все элементы во всех частях как поля. Элемент оболочки предназначен только для внутреннего использования и не будет сериализован в тексте сообщения.

Если сообщение использует представление RPC или литерального стиля, Wsutil.exe создает элемент-оболочку с именем операции в виде имени элемента и указанного пространства имен в качестве пространства имен службы в соответствии со спецификацией расширения SOAP WSDL. Структура элемента содержит массив полей, представляющих типы, указанные в частях сообщения. Элемент-оболочка сопоставляется с фактическим верхним элементом в теле сообщения, как указано в спецификации SOAP.

На стороне сервера каждая операция приводит к определению typedef результирующей операции службы сервера. Это определение типа используется для ссылки на операцию в таблице функций, как описано выше. Каждая операция также приводит к созданию функции-заглушки, которая нфраструктуре вызов от имени делегата к фактическому методу.

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

Для операции Симплемесод определение typedef Симплемесодоператион определено выше. Обратите внимание, что созданный метод имеет развернутый аргумент, листвис часть сообщения для входного и выходного сообщения для операции Симплемесод в виде именованных параметров.

На стороне клиента каждая операция сопоставлена с операцией прокси-службы.

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a>Обработка WSDL: Binding

Модель службы ВВСАПИ поддерживает расширение привязки Сесоап. Для каждой привязки существует связанный **portType**.

Транспорт, указанный в расширении привязки SOAP, относится только к советам. Приложение должно предоставить сведения о транспорте при создании канала. В настоящее время поддерживаются привязки WS \_ HTTP \_ и привязки WS- \_ TCP \_ .

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

В нашем примере WSDL-документа у нас есть только один **portType** для исимплесервице. Предоставленная привязка SOAP указывает транспорт HTTP, который указывается как \_ Привязка WS HTTP \_ . Обратите внимание, что эта структура не имеет статических декорирований, так как эта структура должна быть доступна для приложения.

Обработка WSDL: portType

Каждый **portType** в WSDL состоит из одной или нескольких операций. Операция должна соответствовать расширению SOAP-привязки, указанному в WSDL: Binding.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

В этом примере Исимплесервице **portType** содержит только операцию симплемесод. Это согласуется с разделом Binding, где существует только одна операция WSDL, сопоставленная с действием SOAP.

Так как Исимплесервице **portType** имеет только одну операцию — симплемесод — соответствующая таблица function содержит только симплемесод в качестве операции службы.

С точки зрения метаданных каждый **portType** сопоставляется по Wsutil.exe с [**\_ \_ описанием контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Каждая операция в **portType** сопоставляется с [**\_ \_ описанием операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

В этом примере **portType** средство создает [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для исимплесервице. Это описание контракта содержит определенное количество операций, доступных в Исимплесервице **portType** , а также массив [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , представляющий отдельные операции, определенные в PortType для исимплесервице. Так как в Исимплесервице portType для Исимплесервице имеется только одна операция, имеется также только одно определение **\_ \_ описания операции WS** .

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a>Обработка WSDL: Service

WsUtil.exe использует службы для поиска привязки или порттипес и создает структуру контракта, описывающую типы, сообщения, определения PortType и т. д. Описания контрактов доступны извне, и они создаются как часть структуры глобального определения, заданной в созданном заголовке.

WsUtil.exe поддерживает расширения EndpointReference, определенные в WSDL: Port. Ссылка на конечную точку определяется в WS-ADDRESSing как способ описания сведений о [конечной точке](endpoint-address.md) службы. Текст расширения ссылки на входную конечную точку, сохраненный как [**\_ \_ строка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), вместе с соответствующим [**\_ \_ \_ описанием адреса конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) , создается в разделе ендпоинтреференцес в глобальной структуре.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

Чтобы создать [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) с помощью созданных метаданных всутил, сделайте следующее:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Постоянные строки в прокси клиента или заглушке службы создаются как поля типа WS \_ XML \_ , а для всех строк в файле прокси или заглушки существует словарь констант. Каждая строка в словаре создается как поле в словарной части локальной структуры для повышения удобочитаемости.

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a>Обработка WSDL: Type

Wsutil.exe поддерживает только документы XML-схемы (XSD) в WSDL: Type Specification. Один из особых случаев — когда порт сообщения задает глобальное определение элемента. Дополнительные сведения о эвристике, используемой в этих случаях, см. в следующем разделе.

## <a name="parameter-processing-heuristics"></a>Эвристика обработки параметров

В модели службы сообщения WSDL сопоставляются с конкретными параметрами в методе. Wsutil.exe имеет два стиля создания параметров: в первом стиле операция имеет один параметр для входного сообщения и один параметр для выходного сообщения (при необходимости); во втором стиле Wsutil.exe использует эвристику для соотнесения и расширения полей в структурах для входных сообщений и вывода сообщений с различными параметрами в операции. Для создания этого второго подхода как входные, так и выходные сообщения должны иметь элементы сообщения типа Structure.

При создании параметров операции из входных и выходных сообщений Wsutil.exe использует следующие правила.

-   Для входных и выходных сообщений с несколькими частями сообщения каждая часть сообщения является отдельным параметром в операции, а имя части сообщения — именем параметра.
-   Для сообщения в стиле RPC с одной частью сообщения часть сообщения является параметром операции, имя части сообщения в качестве имени параметра.
-   Для входных и выходных сообщений в стиле документа с одной частью сообщения:
    -   Если часть сообщения имеет имя "Parameters", а тип элемента является структурой, каждое поле в структуре обрабатывается как отдельный параметр с именем поля, именем параметра.
    -   Если имя части сообщения не "Parameters", сообщение является параметром в операции с именем сообщения, используемым в качестве соответствующего имени параметра.
-   Для входного и выходного сообщений стиля документа с нулевым элементом сообщение сопоставляется с одним параметром с именем части сообщения в качестве имени параметра. Добавлен один дополнительный уровень косвенного обращения, указывающий, что указатель может иметь **значение NULL**.
-   Если поле отображается только в элементе входного сообщения, Поле обрабатывается как \[ \] параметр in.
-   Если поле отображается только в элементе выходного сообщения, Поле обрабатывается как выходной \[ \] параметр.
-   Если имеется поле с тем же именем и типом, которое отображается как во входном сообщении, так и в выходном сообщении, Поле обрабатывается как входной \[ , выходной \] параметр.

Для определения направления параметров используются следующие средства:

-   Если поле отображается только в элементе входного сообщения, Поле обрабатывается как только в параметре.
-   Если поле отображается только в элементе выходного сообщения, Поле обрабатывается как параметр только out.
-   Если имеется поле с тем же именем и типом, которое отображается как в сообщении ввода, так и в выходном сообщении, Поле обрабатывается как входной, выходной параметр.

Wsutil.exe поддерживает только виртуализированные элементы. Он отклоняет недопустимый порядок относительно \[ в, параметры out, \] Если Wsutil.exe не может сочетать параметры in и out в одном списке параметров. Суффиксы можно добавить в имена параметров, чтобы избежать конфликта имен.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe считает поля в TNS: Симплемесод и TNS: Симплемесодреспонсе ATO параметрами, как показано в определениях параметров ниже:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

Wsutil.exe раскрывает список параметров из полей в приведенном выше списке и создает структуру **парамструкт** в следующем примере кода. Во время выполнения модели службы можно использовать эту структуру для передачи аргументов в заглушки клиента и сервера.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Эта структура используется только для описания кадра стека на стороне клиента и сервера. Изменение описания сообщения или описания элементов, на которые ссылается описание сообщения, отсутствуют.

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

Как правило, для всех \[ параметров out и out добавляется один уровень косвенного обращения \] \[ \] .

## <a name="parameterless-operation"></a>Операция без параметров

Для операций с документами и литералами Wsutil.exe обрабатывает операцию как один входной параметр и один выходной параметр, если:

-   Входное или выходное сообщение содержит более одной части.
-   Существует только одна часть сообщения, а имя части сообщения не "Parameters".

.. В приведенном выше примере, предполагая, что части сообщения именуются как *paramd* и *param*, сигнатура метода становится следующим кодом:

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

Wsutil.exe создает подпись версии для описания операции, так что обработчик модели службы Вскалл и серверной стороны может проверить, применимо ли сформированное описание к текущей платформе.

Эта информация о версии создается как часть структуры [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) . Номер версии можно рассматривать как селектор ARM-объединения, чтобы сделать структуру расширяемой. Сейчас **versionID** задается TO1 без последующих полей. В будущем версиосн может увеличить номер версии и при необходимости включить дополнительные поля. Например, Wsutil.exe в настоящее время создает следующий код на основе идентификатора версии:

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

В будущем его можно расширить следующим образом:

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a>Безопасность

См. раздел Security (безопасность) в разделе [средства компилятора всутил](wsutil-compiler-tool.md) .

 

 




