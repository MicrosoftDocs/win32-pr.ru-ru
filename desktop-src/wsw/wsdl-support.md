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
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797280"
---
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="4e779-106">WSDL и контракты служб</span><span class="sxs-lookup"><span data-stu-id="4e779-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="4e779-107">Служебная программа [Wsutil.exe](web-service-compiler-tool.md) создает заглушку языка C в соответствии с предоставленными метаданными WSDL, а также определения типов данных и описания типов данных, описанных в XML-схемах, созданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="4e779-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="4e779-108">Ниже приведен пример документа WSDL и XML-схемы, которая служит основанием для обсуждения:</span><span class="sxs-lookup"><span data-stu-id="4e779-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

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

<span data-ttu-id="4e779-109">В этом примере представлен контракт Исимплесервице с одним методом Симплемесод.</span><span class="sxs-lookup"><span data-stu-id="4e779-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="4e779-110">"Симплемесод" имеет два входных параметра типа **целое число**, *a* и *b*, которые отправляются от клиента к службе.</span><span class="sxs-lookup"><span data-stu-id="4e779-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="4e779-111">Аналогично, Симплемесод имеет два выходных параметра типа **Integer**, *b* и *c*, которые возвращаются клиенту после успешного завершения.</span><span class="sxs-lookup"><span data-stu-id="4e779-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="4e779-112">В синтаксисе C с заметками SAL определение метода выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e779-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="4e779-113">В этом определении Исимплесервице является контрактом службы с одной операцией службы: Симплемесод.</span><span class="sxs-lookup"><span data-stu-id="4e779-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="4e779-114">Выходной файл заголовка содержит определения и описания для внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="4e779-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="4e779-115">В том числе:</span><span class="sxs-lookup"><span data-stu-id="4e779-115">This includes:</span></span>

-   <span data-ttu-id="4e779-116">Определения структур C для глобальных типов элементов.</span><span class="sxs-lookup"><span data-stu-id="4e779-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="4e779-117">Прототип операции, определенный в текущем файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="4e779-118">Прототип таблицы функций для контрактов, указанных в WSDL-файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="4e779-119">Клиентский прокси и прототипы заглушки службы для всех функций, указанных в текущем файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="4e779-120">Структура [**данных \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) для элементов глобальной схемы, определенных в текущем файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="4e779-121">Структура [**данных \_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) для всех сообщений, указанных в текущем файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="4e779-122">Структура [**данных \_ \_ описания контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для всех контрактов, указанных в текущем файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="4e779-123">Создается одна глобальная структура для инкапсуляции всех глобальных описаний типов схем и моделей служб, на которые может ссылаться приложение.</span><span class="sxs-lookup"><span data-stu-id="4e779-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="4e779-124">Структура именуется с использованием нормализованного имени файла.</span><span class="sxs-lookup"><span data-stu-id="4e779-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="4e779-125">В этом примере Wsutil.exe создает структуру глобальных определений с именем Example \_ WSDL, которая содержит все описания веб-служб.</span><span class="sxs-lookup"><span data-stu-id="4e779-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="4e779-126">Определение структуры создается в файле заглушки.</span><span class="sxs-lookup"><span data-stu-id="4e779-126">The structure definition is generated in the stub file.</span></span>

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

<span data-ttu-id="4e779-127">Для определений глобальных элементов в документе схемы XML (XSD) один прототип [**\_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , а также соответствующее определение типа C создаются для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="4e779-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="4e779-128">Прототипы описаний элементов для Симплемесод и Симплемесодреспонсе создаются как элементы в приведенной выше структуре.</span><span class="sxs-lookup"><span data-stu-id="4e779-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="4e779-129">Структуры C создаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e779-129">The C structures are generated as follows:</span></span>

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

<span data-ttu-id="4e779-130">Аналогично глобальным сложным типам Wsutil.exe создает определения структур типа C, как показано выше, без совпадающих описаний элементов.</span><span class="sxs-lookup"><span data-stu-id="4e779-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="4e779-131">Для входных данных WSDL Wsutil.exe создает следующие прототипы и определения:</span><span class="sxs-lookup"><span data-stu-id="4e779-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="4e779-132">Для описания сообщения создается прототип [**\_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) .</span><span class="sxs-lookup"><span data-stu-id="4e779-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="4e779-133">Это описание может использоваться моделью службы, а также уровнем сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e779-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="4e779-134">Структуры описания сообщений — это поля с именами «мессаженаме» в глобальной структуре.</span><span class="sxs-lookup"><span data-stu-id="4e779-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="4e779-135">В этом примере описание сообщения создается как \_ поле исимплесервице симплемесод \_ инпутмессаже в \_ структуре исимплесервице симплемесод \_ инпутмессаже, как указано в WSDL-файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="4e779-136">[**Служба WS \_ Прототип \_ описания контракта**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) создается для описания контракта.</span><span class="sxs-lookup"><span data-stu-id="4e779-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="4e779-137">Это описание используется моделью службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-137">This description is used by service model.</span></span> <span data-ttu-id="4e779-138">Структуры описания контракта — это поля с именами «ContractName» в глобальной структуре.</span><span class="sxs-lookup"><span data-stu-id="4e779-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="4e779-139">В этом примере описание контракта создается как \_ поле дефаултбиндинг исимплесервице в структуре " \_ example \_ WSDL".</span><span class="sxs-lookup"><span data-stu-id="4e779-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="4e779-140">Спецификации операций и типов являются общими для прокси-серверов и заглушек и создаются в обоих файлах.</span><span class="sxs-lookup"><span data-stu-id="4e779-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="4e779-141">Wsutil.exe создает одну копию, только если в одном файле создаются прокси-серверы и заглушки.</span><span class="sxs-lookup"><span data-stu-id="4e779-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="4e779-142">Создание идентификатора</span><span class="sxs-lookup"><span data-stu-id="4e779-142">Identifier generation</span></span>

<span data-ttu-id="4e779-143">Автоматически созданные структуры C, перечисленные выше, создаются на основе имени, указанного в WSDL-файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="4e779-144">NCName XML, как правило, не считается допустимым идентификатором C, а имена при необходимости нормализуются.</span><span class="sxs-lookup"><span data-stu-id="4e779-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="4e779-145">Шестнадцатеричные значения не преобразуются, а распространенные буквы, такие как ":", "/" и ".", преобразуются в символ подчеркивания " \_ " для повышения удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="4e779-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="4e779-146">Заголовок для заглушки</span><span class="sxs-lookup"><span data-stu-id="4e779-146">Header for the stub</span></span>

<span data-ttu-id="4e779-147">Для каждой операции в контракте службы создается одна подпрограммы обратного вызова с именем <operationname> callback.</span><span class="sxs-lookup"><span data-stu-id="4e779-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="4e779-148">(Например, операция "Симплемесод" в примере контракта службы имеет созданный обратный вызов с именем "Симплемесодкаллбакк".)</span><span class="sxs-lookup"><span data-stu-id="4e779-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="4e779-149">Для каждого Wsutil.exe WSDL **portType** формирует таблицу функций, представляющую **portType**.</span><span class="sxs-lookup"><span data-stu-id="4e779-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="4e779-150">Каждая операция с **portType** имеет соответствующий указатель на функцию обратного вызова, присутствующую в таблице функций.</span><span class="sxs-lookup"><span data-stu-id="4e779-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="4e779-151">Прототипы прокси-сервера создаются для всех операций.</span><span class="sxs-lookup"><span data-stu-id="4e779-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="4e779-152">Имя прототипа — это имя операции (в данном случае «Симплемесод»), указанное в WSDL-файле для контракта службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="4e779-153">Создание прототипа описания только для локального кода</span><span class="sxs-lookup"><span data-stu-id="4e779-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="4e779-154">Прокси-файлы андстуб содержат определение для структуры глобальных определений, включая прототипы и определения для структур, содержащих только локальные описания и реализации прокси-сервера и заглушки клиента.</span><span class="sxs-lookup"><span data-stu-id="4e779-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="4e779-155">Все прототипы и определения, локальные для файла заглушки, создаются в составе структуры инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="4e779-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="4e779-156">Эта реструктуризация структуры локальных описаний предоставляет четкую иерархию описаний, необходимых уровню сериализации и модели службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="4e779-157">Локальная структура описания имеет прототипы, аналогичные показанным ниже.</span><span class="sxs-lookup"><span data-stu-id="4e779-157">The local description structure has prototypes similar to the one shown below:</span></span>

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

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="4e779-158">Ссылки на определения из других файлов</span><span class="sxs-lookup"><span data-stu-id="4e779-158">Referencing definitions from other files</span></span>

<span data-ttu-id="4e779-159">Локальные определения могут ссылаться на описания, созданные в другом файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="4e779-160">Например, сообщение может быть определено в файле кода C, созданном из WSDL-файла, но элемент Message может быть определен в любом расположении в файле кода C, созданном из XSD-файла.</span><span class="sxs-lookup"><span data-stu-id="4e779-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="4e779-161">В этом случае Wsutil.exe создает ссылку на глобальный элемент из файла, содержащего определение сообщения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4e779-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="4e779-162">Глобальные описания элементов</span><span class="sxs-lookup"><span data-stu-id="4e779-162">Global element descriptions</span></span>

<span data-ttu-id="4e779-163">Для каждого глобального элемента, определенного в файле WSDL: Type или XSD, существует совпадающее поле с именем **ElementName** внутри поля **глобалелемент** .</span><span class="sxs-lookup"><span data-stu-id="4e779-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="4e779-164">В этом примере создается структура с именем Симплемесод:</span><span class="sxs-lookup"><span data-stu-id="4e779-164">In this example, a structure named SimpleMethod is generated:</span></span>

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

<span data-ttu-id="4e779-165">Другие описания, необходимые для описания элемента, создаются как часть содержащей их структуры.</span><span class="sxs-lookup"><span data-stu-id="4e779-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="4e779-166">Если элемент является простым элементом типа, то существует только одно поле [**\_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) .</span><span class="sxs-lookup"><span data-stu-id="4e779-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="4e779-167">Если тип элемента является структурой, все связанные поля и описания структуры создаются как часть структуры элемента.</span><span class="sxs-lookup"><span data-stu-id="4e779-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="4e779-168">В этом примере элемент Симплемесод является структурой, содержащей два поля, **a** и **b**.</span><span class="sxs-lookup"><span data-stu-id="4e779-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="4e779-169">Wsutil.exe создает структуру следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e779-169">Wsutil.exe generates the structure as follows:</span></span>

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

<span data-ttu-id="4e779-170">Внедренные структуры и внедренные элементы создаются как вложенные структуры по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4e779-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="4e779-171">Определения, связанные с WSDL</span><span class="sxs-lookup"><span data-stu-id="4e779-171">WSDL related definitions</span></span>

<span data-ttu-id="4e779-172">Wsutil.exe создает поле в разделе WSDL для каждого из значений **portType** , определенных в заданной службе WSDL: Service.</span><span class="sxs-lookup"><span data-stu-id="4e779-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

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

<span data-ttu-id="4e779-173">Wsutil.exe создает одно поле f, содержащее все описания, необходимые для операции, массив единый указателей на каждое описание операции для каждого метода и одно [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для указанного **portType**.</span><span class="sxs-lookup"><span data-stu-id="4e779-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="4e779-174">Все описания, необходимые для операций, создаются внутри поля **operationName** в указанном **portType**.</span><span class="sxs-lookup"><span data-stu-id="4e779-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="4e779-175">К ним относятся [**поле \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , а также вложенная структура для входных и выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="4e779-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="4e779-176">Аналогично, [**поля \_ \_ описания сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) для входного сообщения и необязательное выходное сообщение включаются вместе с. [**Служба WS \_ Поле со списком \_ Описание параметра**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) для всех параметров операции и поле [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) для самой операции.</span><span class="sxs-lookup"><span data-stu-id="4e779-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="4e779-177">В этом примере создается структура кода для описания Симплемесод, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4e779-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

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

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="4e779-178">Определения, связанные с словарем XML</span><span class="sxs-lookup"><span data-stu-id="4e779-178">XML dictionary related definitions</span></span>

<span data-ttu-id="4e779-179">Имена и пространства имен, используемые в различных описаниях, создаются как поля типа [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span><span class="sxs-lookup"><span data-stu-id="4e779-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="4e779-180">Все эти строки создаются как часть словаря констант для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="4e779-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="4e779-181">Список строк и поле [**\_ \_ словаря WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (с именем **словарь** в примере ниже) создаются как часть поля DICTIONARY структуры **филенамелокал** .</span><span class="sxs-lookup"><span data-stu-id="4e779-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

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

<span data-ttu-id="4e779-182">Массив [**\_ \_ строк WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)(s) создается как ряд полей типа **WS \_ XML \_ String** с именем с понятными именами пользователей.</span><span class="sxs-lookup"><span data-stu-id="4e779-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="4e779-183">Созданная заглушка использует понятные имена пользователей в различных описаниях для повышения удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="4e779-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="4e779-184">Клиентский прокси-сервер для операций WSDL</span><span class="sxs-lookup"><span data-stu-id="4e779-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="4e779-185">Wsutil.exe создает клиентский прокси-сервер для всех операций.</span><span class="sxs-lookup"><span data-stu-id="4e779-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="4e779-186">Приложения могут перезаписывать сигнатуру метода с помощью префиксного параметра командной строки.</span><span class="sxs-lookup"><span data-stu-id="4e779-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

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

<span data-ttu-id="4e779-187">Вызывающий объект операции должен передать допустимый параметр *кучи* .</span><span class="sxs-lookup"><span data-stu-id="4e779-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="4e779-188">Выходные параметры выделяются с помощью \_ значения WS Heap, указанного в параметре *heap* .</span><span class="sxs-lookup"><span data-stu-id="4e779-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="4e779-189">Вызывающая функция может сбросить или освободить кучу, чтобы освободить память для всех выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="4e779-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="4e779-190">Если операция завершается неудачно, дополнительные сведения об ошибке можно получить из необязательного объекта ошибки, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="4e779-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="4e779-191">Wsutil.exe создает заглушку службы для всех операций, описанных в разделе Binding.</span><span class="sxs-lookup"><span data-stu-id="4e779-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

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

<span data-ttu-id="4e779-192">В приведенном выше разделе описывается прототип локальной структуры, содержащей все определения, локальные только для файла заглушки.</span><span class="sxs-lookup"><span data-stu-id="4e779-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="4e779-193">В последующих разделах описаны определения описаний.</span><span class="sxs-lookup"><span data-stu-id="4e779-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="4e779-194">Создание определения WSDL</span><span class="sxs-lookup"><span data-stu-id="4e779-194">WSDL Definition Generation</span></span>

<span data-ttu-id="4e779-195">Wsutil.exe создает константную статическую структуру (**const static**) с именем *<\_ имя файла>* локалдефинитионс типа *<имя службы \_>* Local, которая содержит все локальные определения.</span><span class="sxs-lookup"><span data-stu-id="4e779-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

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

<span data-ttu-id="4e779-196">Поддерживаются следующие описания WSDL:</span><span class="sxs-lookup"><span data-stu-id="4e779-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="4e779-197">WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="4e779-197">wsdl:service</span></span>
-   <span data-ttu-id="4e779-198">WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="4e779-198">wsdl:binding</span></span>
-   <span data-ttu-id="4e779-199">WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="4e779-199">wsdl:portType</span></span>
-   <span data-ttu-id="4e779-200">WSDL: Operation</span><span class="sxs-lookup"><span data-stu-id="4e779-200">wsdl:operation</span></span>
-   <span data-ttu-id="4e779-201">WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="4e779-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="4e779-202">Обработка WSDL: Operation и WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="4e779-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="4e779-203">Каждая операция, указанная в документе WSDL, сопоставляется с операцией службы с помощью [Wsutil.exe](web-service-compiler-tool.md).</span><span class="sxs-lookup"><span data-stu-id="4e779-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="4e779-204">Средство создает отдельные определения операций службы как для сервера, так и для клиента.</span><span class="sxs-lookup"><span data-stu-id="4e779-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

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

<span data-ttu-id="4e779-205">Макет элементов данных входных сообщений андаутпут вычисляется средством для создания метаданных сериализации для инфраструктуры, а также фактической сигнатуры итоговой операции службы, с которой связаны входные и выходные сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e779-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="4e779-206">Метаданные каждой операции в определенном **portType** имеют входные данные и, при необходимости, выходное сообщение, каждое из этих сообщений сопоставляется [**с \_ \_ описанием сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span><span class="sxs-lookup"><span data-stu-id="4e779-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="4e779-207">В этом примере входные и выходные сообщения для операции в portType сопоставлены с Инпутмессажедескриптион и, по желанию, Аутпутмессажедескриптион в [**\_ \_ описании операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) соответственно.</span><span class="sxs-lookup"><span data-stu-id="4e779-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="4e779-208">Для каждого сообщения WSDL средство создает [**\_ \_ Описание сообщения WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) , которое ссылается на [**определение \_ \_ описания элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4e779-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="4e779-209">Описание сообщения относится к описанию элемента ввода.</span><span class="sxs-lookup"><span data-stu-id="4e779-209">The message description refers to the input element description.</span></span> <span data-ttu-id="4e779-210">Поскольку элемент определен глобально, описание сообщения ссылается на глобальное определение, а не на локальный статический элемент.</span><span class="sxs-lookup"><span data-stu-id="4e779-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="4e779-211">Аналогично, если элемент определен в другом файле, Wsutil.exe создает ссылку на глобально определенную структуру в этом файле.</span><span class="sxs-lookup"><span data-stu-id="4e779-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="4e779-212">Например, если Симплемесодреспонсе определен в другом файле example. xsd, вместо этого Wsutil.exe создает следующее:</span><span class="sxs-lookup"><span data-stu-id="4e779-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="4e779-213">Каждое описание сообщения содержит действие и конкретное описание элемента (поле типа « [**\_ \_ Описание элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)») для всех элементов данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e779-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="4e779-214">В случае сообщения в стиле RPC или сообщения с несколькими частями создается элемент-оболочка для инкапсуляции дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="4e779-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="4e779-215">Поддержка стиля RPC</span><span class="sxs-lookup"><span data-stu-id="4e779-215">RPC style support</span></span>

<span data-ttu-id="4e779-216">Wsutil.exe поддерживает стиль документа и операции в стиле RPC согласно спецификации привязки WSDL 1,1 для SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="4e779-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="4e779-217">Операции RPC и в стиле литерала помечаются как \_ \_ литеральная \_ Операция WS RPC.</span><span class="sxs-lookup"><span data-stu-id="4e779-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="4e779-218">Модель службы игнорирует имя элемента оболочки текста ответа в операциях RPC/Literal.</span><span class="sxs-lookup"><span data-stu-id="4e779-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="4e779-219">Wsutil.exe изначально не поддерживает операции в стиле кодировки.</span><span class="sxs-lookup"><span data-stu-id="4e779-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="4e779-220">\_ \_ Параметр буфера WS XML создается для кодирования сообщений, и разработчики должны непосредственно заполнять непрозрачный буфер.</span><span class="sxs-lookup"><span data-stu-id="4e779-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="4e779-221">Поддержка нескольких частей сообщений</span><span class="sxs-lookup"><span data-stu-id="4e779-221">Multiple message parts support</span></span>

<span data-ttu-id="4e779-222">Wsutil.exe поддерживает несколько частей сообщений в одном сообщении.</span><span class="sxs-lookup"><span data-stu-id="4e779-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="4e779-223">Сообщение с несколькими частями можно указать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e779-223">A multi-part message can be specified as follows:</span></span>

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

<span data-ttu-id="4e779-224">Wsutil.exe создает поле [**\_ \_ типа структуры WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) для элемента Message, если сообщение содержит несколько частей.</span><span class="sxs-lookup"><span data-stu-id="4e779-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="4e779-225">Если сообщение представлено с использованием стиля документа, Wsutil.exe создает элемент-оболочку с типом struct.</span><span class="sxs-lookup"><span data-stu-id="4e779-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="4e779-226">Элемент упаковщика не имеет имени или определенного пространства имен, а структура оболочки содержит все элементы во всех частях как поля.</span><span class="sxs-lookup"><span data-stu-id="4e779-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="4e779-227">Элемент оболочки предназначен только для внутреннего использования и не будет сериализован в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e779-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="4e779-228">Если сообщение использует представление RPC или литерального стиля, Wsutil.exe создает элемент-оболочку с именем операции в виде имени элемента и указанного пространства имен в качестве пространства имен службы в соответствии со спецификацией расширения SOAP WSDL.</span><span class="sxs-lookup"><span data-stu-id="4e779-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="4e779-229">Структура элемента содержит массив полей, представляющих типы, указанные в частях сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e779-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="4e779-230">Элемент-оболочка сопоставляется с фактическим верхним элементом в теле сообщения, как указано в спецификации SOAP.</span><span class="sxs-lookup"><span data-stu-id="4e779-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="4e779-231">На стороне сервера каждая операция приводит к определению typedef результирующей операции службы сервера.</span><span class="sxs-lookup"><span data-stu-id="4e779-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="4e779-232">Это определение типа используется для ссылки на операцию в таблице функций, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="4e779-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="4e779-233">Каждая операция также приводит к созданию функции-заглушки, которая нфраструктуре вызов от имени делегата к фактическому методу.</span><span class="sxs-lookup"><span data-stu-id="4e779-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

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

<span data-ttu-id="4e779-234">Для операции Симплемесод определение typedef Симплемесодоператион определено выше.</span><span class="sxs-lookup"><span data-stu-id="4e779-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="4e779-235">Обратите внимание, что созданный метод имеет развернутый аргумент, листвис часть сообщения для входного и выходного сообщения для операции Симплемесод в виде именованных параметров.</span><span class="sxs-lookup"><span data-stu-id="4e779-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="4e779-236">На стороне клиента каждая операция сопоставлена с операцией прокси-службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-236">On the client side each operation is mapped to a proxy service operation.</span></span>

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

## <a name="processing-wsdlbinding"></a><span data-ttu-id="4e779-237">Обработка WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="4e779-237">Processing wsdl:binding</span></span>

<span data-ttu-id="4e779-238">Модель службы ВВСАПИ поддерживает расширение привязки Сесоап.</span><span class="sxs-lookup"><span data-stu-id="4e779-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="4e779-239">Для каждой привязки существует связанный **portType**.</span><span class="sxs-lookup"><span data-stu-id="4e779-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="4e779-240">Транспорт, указанный в расширении привязки SOAP, относится только к советам.</span><span class="sxs-lookup"><span data-stu-id="4e779-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="4e779-241">Приложение должно предоставить сведения о транспорте при создании канала.</span><span class="sxs-lookup"><span data-stu-id="4e779-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="4e779-242">В настоящее время поддерживаются привязки WS \_ HTTP \_ и привязки WS- \_ TCP \_ .</span><span class="sxs-lookup"><span data-stu-id="4e779-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

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

<span data-ttu-id="4e779-243">В нашем примере WSDL-документа у нас есть только один **portType** для исимплесервице.</span><span class="sxs-lookup"><span data-stu-id="4e779-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="4e779-244">Предоставленная привязка SOAP указывает транспорт HTTP, который указывается как \_ Привязка WS HTTP \_ .</span><span class="sxs-lookup"><span data-stu-id="4e779-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="4e779-245">Обратите внимание, что эта структура не имеет статических декорирований, так как эта структура должна быть доступна для приложения.</span><span class="sxs-lookup"><span data-stu-id="4e779-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="4e779-246">Обработка WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="4e779-246">Processing wsdl:portType</span></span>

<span data-ttu-id="4e779-247">Каждый **portType** в WSDL состоит из одной или нескольких операций.</span><span class="sxs-lookup"><span data-stu-id="4e779-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="4e779-248">Операция должна соответствовать расширению SOAP-привязки, указанному в WSDL: Binding.</span><span class="sxs-lookup"><span data-stu-id="4e779-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

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

<span data-ttu-id="4e779-249">В этом примере Исимплесервице **portType** содержит только операцию симплемесод.</span><span class="sxs-lookup"><span data-stu-id="4e779-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="4e779-250">Это согласуется с разделом Binding, где существует только одна операция WSDL, сопоставленная с действием SOAP.</span><span class="sxs-lookup"><span data-stu-id="4e779-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="4e779-251">Так как Исимплесервице **portType** имеет только одну операцию — симплемесод — соответствующая таблица function содержит только симплемесод в качестве операции службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="4e779-252">С точки зрения метаданных каждый **portType** сопоставляется по Wsutil.exe с [**\_ \_ описанием контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span><span class="sxs-lookup"><span data-stu-id="4e779-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="4e779-253">Каждая операция в **portType** сопоставляется с [**\_ \_ описанием операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span><span class="sxs-lookup"><span data-stu-id="4e779-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="4e779-254">В этом примере **portType** средство создает [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) для исимплесервице.</span><span class="sxs-lookup"><span data-stu-id="4e779-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="4e779-255">Это описание контракта содержит определенное количество операций, доступных в Исимплесервице **portType** , а также массив [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , представляющий отдельные операции, определенные в PortType для исимплесервице.</span><span class="sxs-lookup"><span data-stu-id="4e779-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="4e779-256">Так как в Исимплесервице portType для Исимплесервице имеется только одна операция, имеется также только одно определение **\_ \_ описания операции WS** .</span><span class="sxs-lookup"><span data-stu-id="4e779-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

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

## <a name="processing-wsdlservice"></a><span data-ttu-id="4e779-257">Обработка WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="4e779-257">Processing wsdl:service</span></span>

<span data-ttu-id="4e779-258">WsUtil.exe использует службы для поиска привязки или порттипес и создает структуру контракта, описывающую типы, сообщения, определения PortType и т. д.</span><span class="sxs-lookup"><span data-stu-id="4e779-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="4e779-259">Описания контрактов доступны извне, и они создаются как часть структуры глобального определения, заданной в созданном заголовке.</span><span class="sxs-lookup"><span data-stu-id="4e779-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="4e779-260">WsUtil.exe поддерживает расширения EndpointReference, определенные в WSDL: Port.</span><span class="sxs-lookup"><span data-stu-id="4e779-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="4e779-261">Ссылка на конечную точку определяется в WS-ADDRESSing как способ описания сведений о [конечной точке](endpoint-address.md) службы.</span><span class="sxs-lookup"><span data-stu-id="4e779-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="4e779-262">Текст расширения ссылки на входную конечную точку, сохраненный как [**\_ \_ строка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), вместе с соответствующим [**\_ \_ \_ описанием адреса конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) , создается в разделе ендпоинтреференцес в глобальной структуре.</span><span class="sxs-lookup"><span data-stu-id="4e779-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

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

<span data-ttu-id="4e779-263">Чтобы создать [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) с помощью созданных метаданных всутил, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="4e779-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="4e779-264">Постоянные строки в прокси клиента или заглушке службы создаются как поля типа WS \_ XML \_ , а для всех строк в файле прокси или заглушки существует словарь констант.</span><span class="sxs-lookup"><span data-stu-id="4e779-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="4e779-265">Каждая строка в словаре создается как поле в словарной части локальной структуры для повышения удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="4e779-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

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

## <a name="processing-wsdltype"></a><span data-ttu-id="4e779-266">Обработка WSDL: Type</span><span class="sxs-lookup"><span data-stu-id="4e779-266">Processing wsdl:type</span></span>

<span data-ttu-id="4e779-267">Wsutil.exe поддерживает только документы XML-схемы (XSD) в WSDL: Type Specification.</span><span class="sxs-lookup"><span data-stu-id="4e779-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="4e779-268">Один из особых случаев — когда порт сообщения задает глобальное определение элемента.</span><span class="sxs-lookup"><span data-stu-id="4e779-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="4e779-269">Дополнительные сведения о эвристике, используемой в этих случаях, см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="4e779-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="4e779-270">Эвристика обработки параметров</span><span class="sxs-lookup"><span data-stu-id="4e779-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="4e779-271">В модели службы сообщения WSDL сопоставляются с конкретными параметрами в методе.</span><span class="sxs-lookup"><span data-stu-id="4e779-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="4e779-272">Wsutil.exe имеет два стиля создания параметров: в первом стиле операция имеет один параметр для входного сообщения и один параметр для выходного сообщения (при необходимости); во втором стиле Wsutil.exe использует эвристику для соотнесения и расширения полей в структурах для входных сообщений и вывода сообщений с различными параметрами в операции.</span><span class="sxs-lookup"><span data-stu-id="4e779-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="4e779-273">Для создания этого второго подхода как входные, так и выходные сообщения должны иметь элементы сообщения типа Structure.</span><span class="sxs-lookup"><span data-stu-id="4e779-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="4e779-274">При создании параметров операции из входных и выходных сообщений Wsutil.exe использует следующие правила.</span><span class="sxs-lookup"><span data-stu-id="4e779-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="4e779-275">Для входных и выходных сообщений с несколькими частями сообщения каждая часть сообщения является отдельным параметром в операции, а имя части сообщения — именем параметра.</span><span class="sxs-lookup"><span data-stu-id="4e779-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="4e779-276">Для сообщения в стиле RPC с одной частью сообщения часть сообщения является параметром операции, имя части сообщения в качестве имени параметра.</span><span class="sxs-lookup"><span data-stu-id="4e779-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="4e779-277">Для входных и выходных сообщений в стиле документа с одной частью сообщения:</span><span class="sxs-lookup"><span data-stu-id="4e779-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="4e779-278">Если часть сообщения имеет имя "Parameters", а тип элемента является структурой, каждое поле в структуре обрабатывается как отдельный параметр с именем поля, именем параметра.</span><span class="sxs-lookup"><span data-stu-id="4e779-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="4e779-279">Если имя части сообщения не "Parameters", сообщение является параметром в операции с именем сообщения, используемым в качестве соответствующего имени параметра.</span><span class="sxs-lookup"><span data-stu-id="4e779-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="4e779-280">Для входного и выходного сообщений стиля документа с нулевым элементом сообщение сопоставляется с одним параметром с именем части сообщения в качестве имени параметра.</span><span class="sxs-lookup"><span data-stu-id="4e779-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="4e779-281">Добавлен один дополнительный уровень косвенного обращения, указывающий, что указатель может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e779-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="4e779-282">Если поле отображается только в элементе входного сообщения, Поле обрабатывается как \[ \] параметр in.</span><span class="sxs-lookup"><span data-stu-id="4e779-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="4e779-283">Если поле отображается только в элементе выходного сообщения, Поле обрабатывается как выходной \[ \] параметр.</span><span class="sxs-lookup"><span data-stu-id="4e779-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="4e779-284">Если имеется поле с тем же именем и типом, которое отображается как во входном сообщении, так и в выходном сообщении, Поле обрабатывается как входной \[ , выходной \] параметр.</span><span class="sxs-lookup"><span data-stu-id="4e779-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="4e779-285">Для определения направления параметров используются следующие средства:</span><span class="sxs-lookup"><span data-stu-id="4e779-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="4e779-286">Если поле отображается только в элементе входного сообщения, Поле обрабатывается как только в параметре.</span><span class="sxs-lookup"><span data-stu-id="4e779-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="4e779-287">Если поле отображается только в элементе выходного сообщения, Поле обрабатывается как параметр только out.</span><span class="sxs-lookup"><span data-stu-id="4e779-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="4e779-288">Если имеется поле с тем же именем и типом, которое отображается как в сообщении ввода, так и в выходном сообщении, Поле обрабатывается как входной, выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="4e779-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="4e779-289">Wsutil.exe поддерживает только виртуализированные элементы.</span><span class="sxs-lookup"><span data-stu-id="4e779-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="4e779-290">Он отклоняет недопустимый порядок относительно \[ в, параметры out, \] Если Wsutil.exe не может сочетать параметры in и out в одном списке параметров.</span><span class="sxs-lookup"><span data-stu-id="4e779-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="4e779-291">Суффиксы можно добавить в имена параметров, чтобы избежать конфликта имен.</span><span class="sxs-lookup"><span data-stu-id="4e779-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

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

<span data-ttu-id="4e779-292">Wsutil.exe считает поля в TNS: Симплемесод и TNS: Симплемесодреспонсе ATO параметрами, как показано в определениях параметров ниже:</span><span class="sxs-lookup"><span data-stu-id="4e779-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

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

<span data-ttu-id="4e779-293">Wsutil.exe раскрывает список параметров из полей в приведенном выше списке и создает структуру **парамструкт** в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="4e779-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="4e779-294">Во время выполнения модели службы можно использовать эту структуру для передачи аргументов в заглушки клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="4e779-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="4e779-295">Эта структура используется только для описания кадра стека на стороне клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="4e779-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="4e779-296">Изменение описания сообщения или описания элементов, на которые ссылается описание сообщения, отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="4e779-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

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

<span data-ttu-id="4e779-297">Как правило, для всех \[ параметров out и out добавляется один уровень косвенного обращения \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="4e779-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="4e779-298">Операция без параметров</span><span class="sxs-lookup"><span data-stu-id="4e779-298">Parameterless operation</span></span>

<span data-ttu-id="4e779-299">Для операций с документами и литералами Wsutil.exe обрабатывает операцию как один входной параметр и один выходной параметр, если:</span><span class="sxs-lookup"><span data-stu-id="4e779-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="4e779-300">Входное или выходное сообщение содержит более одной части.</span><span class="sxs-lookup"><span data-stu-id="4e779-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="4e779-301">Существует только одна часть сообщения, а имя части сообщения не "Parameters".</span><span class="sxs-lookup"><span data-stu-id="4e779-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="4e779-302">..</span><span class="sxs-lookup"><span data-stu-id="4e779-302">..</span></span> <span data-ttu-id="4e779-303">В приведенном выше примере, предполагая, что части сообщения именуются как *paramd* и *param*, сигнатура метода становится следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="4e779-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

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

<span data-ttu-id="4e779-304">Wsutil.exe создает подпись версии для описания операции, так что обработчик модели службы Вскалл и серверной стороны может проверить, применимо ли сформированное описание к текущей платформе.</span><span class="sxs-lookup"><span data-stu-id="4e779-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="4e779-305">Эта информация о версии создается как часть структуры [**\_ \_ описания операции WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) .</span><span class="sxs-lookup"><span data-stu-id="4e779-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="4e779-306">Номер версии можно рассматривать как селектор ARM-объединения, чтобы сделать структуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="4e779-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="4e779-307">Сейчас **versionID** задается TO1 без последующих полей.</span><span class="sxs-lookup"><span data-stu-id="4e779-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="4e779-308">В будущем версиосн может увеличить номер версии и при необходимости включить дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="4e779-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="4e779-309">Например, Wsutil.exe в настоящее время создает следующий код на основе идентификатора версии:</span><span class="sxs-lookup"><span data-stu-id="4e779-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

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

<span data-ttu-id="4e779-310">В будущем его можно расширить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e779-310">In the future, it could be expanded as follows:</span></span>

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

## <a name="security"></a><span data-ttu-id="4e779-311">Безопасность</span><span class="sxs-lookup"><span data-stu-id="4e779-311">Security</span></span>

<span data-ttu-id="4e779-312">См. раздел Security (безопасность) в разделе [средства компилятора всутил](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="4e779-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




