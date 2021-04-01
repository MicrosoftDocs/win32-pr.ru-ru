---
title: Поддержка схем
description: WsUtil.exe поддерживает схему XSD, указанную в схеме XML.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Веб-службы поддержки схемы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987229"
---
# <a name="schema-support"></a><span data-ttu-id="c02a1-106">Поддержка схем</span><span class="sxs-lookup"><span data-stu-id="c02a1-106">Schema support</span></span>

<span data-ttu-id="c02a1-107">WsUtil.exe поддерживает схему XSD, указанную в [схеме XML](https://www.w3.org/XML/Schema).</span><span class="sxs-lookup"><span data-stu-id="c02a1-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="c02a1-108">XSD-файл и WSDL: Type должны рассматриваться в одной категории с исключением в WSDL: Type, если глобальный элемент может быть списком параметров.</span><span class="sxs-lookup"><span data-stu-id="c02a1-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="c02a1-109">Wsutil.exe создает описания элементов для всех определений глобальных элементов, которые могут использоваться в сериализаторе, с дополнительными выходными данными для структуры параметра, указанной в [поддержке WSDL](wsdl-support.md).</span><span class="sxs-lookup"><span data-stu-id="c02a1-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="c02a1-110">Уровень поддержки схемы XSD</span><span class="sxs-lookup"><span data-stu-id="c02a1-110">XSD Schema Support Level</span></span>

<span data-ttu-id="c02a1-111">WsUtil.exe не поддерживает полную область схемы XSD.</span><span class="sxs-lookup"><span data-stu-id="c02a1-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="c02a1-112">Текущий уровень поддержки определяется на [уровне поддержки схемы](schema-support-level.md).</span><span class="sxs-lookup"><span data-stu-id="c02a1-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="c02a1-113">Создание идентификатора</span><span class="sxs-lookup"><span data-stu-id="c02a1-113">Identifier generation</span></span>

<span data-ttu-id="c02a1-114">Имя элемента или типа в схеме, возможно, не является допустимым идентификатором C, а имена нормализованы до сформированных допустимых имен C.</span><span class="sxs-lookup"><span data-stu-id="c02a1-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="c02a1-115">Недопустимые символы идентификатора C преобразуются в шестнадцатеричное имя, а в \_ случае необходимости имя подчеркивания "" может начинаться с префикса.</span><span class="sxs-lookup"><span data-stu-id="c02a1-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="c02a1-116">Анонимные типы именуются после имени включающего элемента, но с префиксом подчеркивания " \_ " во избежание конфликта имен.</span><span class="sxs-lookup"><span data-stu-id="c02a1-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="c02a1-117">Глобальные имена типов сохраняются, так как после нормализации недопустимых символов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="c02a1-118">Вложенные анонимные типы имеют префикс с именем родительского типа.</span><span class="sxs-lookup"><span data-stu-id="c02a1-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="c02a1-119">Для каждого определения глобального элемента wsutil.exe создает [**\_ \_ Описание элемента WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) в структуре глобального описания.</span><span class="sxs-lookup"><span data-stu-id="c02a1-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="c02a1-120">Для каждого определения глобального типа wsutil.exe создает описание типа в структуре глобального описания, на которую будет ссылаться приложение.</span><span class="sxs-lookup"><span data-stu-id="c02a1-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="c02a1-121">Для каждого поля структуры wsutil.exe создает [**\_ \_ Описание поля WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) , внедренное как часть структуры корпуса.</span><span class="sxs-lookup"><span data-stu-id="c02a1-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="c02a1-122">Простые типы</span><span class="sxs-lookup"><span data-stu-id="c02a1-122">Simple Types</span></span>

<span data-ttu-id="c02a1-123">Типы значений, как указано в [**\_ \_ типе значения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), обрабатываются как простые типы.</span><span class="sxs-lookup"><span data-stu-id="c02a1-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="c02a1-124">Обратите внимание, что \_ тип WS value \_ является подмножеством [**\_ типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="c02a1-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="c02a1-125">Он включает базовые типы данных интегралов и float, а также ДЕСЯТИЧные, WS \_ DateTime и UUID.</span><span class="sxs-lookup"><span data-stu-id="c02a1-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="c02a1-126">В модели службы простые типы передаются по значению, а out и in, а простые типы передаются по ссылке.</span><span class="sxs-lookup"><span data-stu-id="c02a1-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="c02a1-127">Всутил создайте простое описание элемента, как показано ниже, для глобального элемента, содержащего простые типы.</span><span class="sxs-lookup"><span data-stu-id="c02a1-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="c02a1-128">Всутил создает описание элемента ниже:</span><span class="sxs-lookup"><span data-stu-id="c02a1-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="c02a1-129">Эта структура создается как часть структуры глобального описания, созданной в файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="c02a1-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="c02a1-130">Массивы</span><span class="sxs-lookup"><span data-stu-id="c02a1-130">Arrays</span></span>

<span data-ttu-id="c02a1-131">Элемент с maxOccurs больше 1 или Sequence с одним элементом, а дочерний элемент имеет значение maxOccurs больше 1, считается массивом.</span><span class="sxs-lookup"><span data-stu-id="c02a1-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="c02a1-132">Для элемента массива в схеме wsutil.exe создает два поля: одно поле Count, которое не переходит по каналу, и одно поле указателя, содержащее тип массива.</span><span class="sxs-lookup"><span data-stu-id="c02a1-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="c02a1-133">Файл заголовка содержит определение структуры C для массива с учетом значения поля, указывающего количество массива.</span><span class="sxs-lookup"><span data-stu-id="c02a1-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="c02a1-134">Ниже приведена часть прототипа Локалдефинитион, описывающего массив:</span><span class="sxs-lookup"><span data-stu-id="c02a1-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="c02a1-135">Ниже приведены созданные определения описанных выше определений. Обратите внимание на \_ \_ сопоставление поля элемента WS повторяющихся элементов, \_ \_ которое указывает поле как поле массива.</span><span class="sxs-lookup"><span data-stu-id="c02a1-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="c02a1-136">Если массив является полем параметра в сообщении ввода-вывода, для метода будут созданы два фактических параметра.</span><span class="sxs-lookup"><span data-stu-id="c02a1-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="c02a1-137">Если массив является выходным или входным, параметром out будет один дополнительный уровень косвенного обращения для обоих полей в Парамструкт.</span><span class="sxs-lookup"><span data-stu-id="c02a1-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="c02a1-138">Диапазон в массиве</span><span class="sxs-lookup"><span data-stu-id="c02a1-138">Range on Array</span></span>

<span data-ttu-id="c02a1-139">Рекомендуется не указывать Максоккур = "unboundd" для массивов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="c02a1-140">Вместо этого следует указать фиксированное целое число, чтобы установить верхнюю границу допустимого числа массивов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="c02a1-141">диапазон поддерживается для целочисленных типов, а также для строк, массивов байтов и универсальных массивов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="c02a1-142">Эвристика для переноса в противоположность развернутому массиву</span><span class="sxs-lookup"><span data-stu-id="c02a1-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="c02a1-143">Иногда массивы упаковываются внутри другой структуры для внедрения в структуру верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="c02a1-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="c02a1-144">В этом случае следует удалить промежуточный слой-оболочку.</span><span class="sxs-lookup"><span data-stu-id="c02a1-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="c02a1-145">WsUtil.exe создает тот же прототип и описания, что и Симплеаррай, описанный выше.</span><span class="sxs-lookup"><span data-stu-id="c02a1-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="c02a1-146">Всутил обнаруживает, что Симплеаррайвраппер является оболочкой для Симплеаррай и создает только следующие структуры, с отдельной структурой для Симплеаррай</span><span class="sxs-lookup"><span data-stu-id="c02a1-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="c02a1-147">wsutil.exe создает следующие определения для приведенного выше прототипа, обратите внимание, что в поле Описание поля поля имя оболочки и пространство имен упаковщика заполнены.</span><span class="sxs-lookup"><span data-stu-id="c02a1-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="c02a1-148">Структуры</span><span class="sxs-lookup"><span data-stu-id="c02a1-148">Structures</span></span>

<span data-ttu-id="c02a1-149">ComplexType с несколькими элементами в последовательности является структурой.</span><span class="sxs-lookup"><span data-stu-id="c02a1-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="c02a1-150">Например,</span><span class="sxs-lookup"><span data-stu-id="c02a1-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="c02a1-151">Wsutil.exe создает прототип структуры следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c02a1-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="c02a1-152">всутил создает следующий прототип для Локалдефинитион:</span><span class="sxs-lookup"><span data-stu-id="c02a1-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="c02a1-153">Определение структуры выглядит так, как показано ниже, с двумя описаниями полей в структуре.</span><span class="sxs-lookup"><span data-stu-id="c02a1-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="c02a1-154">Для поддержки расширяемости внедренные структуры всегда определяются передаваемыми по ссылке.</span><span class="sxs-lookup"><span data-stu-id="c02a1-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="c02a1-155">В службе все структуры out и out передаются двойным указателем, чтобы разрешить будущее расширение структуры, а также разрешение на ненулевую структуру.</span><span class="sxs-lookup"><span data-stu-id="c02a1-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="c02a1-156">Рекурсивные структуры</span><span class="sxs-lookup"><span data-stu-id="c02a1-156">Recursive Structures</span></span>

<span data-ttu-id="c02a1-157">Поддерживаются рекурсивные структуры, а внедренные типы передаются по ссылке.</span><span class="sxs-lookup"><span data-stu-id="c02a1-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="c02a1-158">Для следующего WSDL:</span><span class="sxs-lookup"><span data-stu-id="c02a1-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="c02a1-159">Всутил создает следующие определения типов, а также описания типов:</span><span class="sxs-lookup"><span data-stu-id="c02a1-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="c02a1-160">Определение создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c02a1-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="c02a1-161">Структура наследованием</span><span class="sxs-lookup"><span data-stu-id="c02a1-161">Structure inheritence</span></span>

<span data-ttu-id="c02a1-162">всутил поддерживает расширение сложного типа, где один сложный тип является расширением другого сложного типа.</span><span class="sxs-lookup"><span data-stu-id="c02a1-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="c02a1-163">Приведенный выше фрагмент XSD указывает, что Дериведлинклист является производным от линклист.</span><span class="sxs-lookup"><span data-stu-id="c02a1-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="c02a1-164">Wsutil.exe создает вспомогательные подпрограммы для C и C++, чтобы упростить для приложения настройку сведений о типе базового типа и производных типов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="c02a1-165">В следующем коде \_ \_ макрос WS кплусплус используется для различения определения языка C и C++:</span><span class="sxs-lookup"><span data-stu-id="c02a1-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="c02a1-166">В вспомогательном приложении в стиле C, перед сериалиатион, приложение вызывает всутил Generated линклист \_ init для инициализации структуры и задает описание типа линклист Description Type.</span><span class="sxs-lookup"><span data-stu-id="c02a1-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="c02a1-167">После десериализации приложение может вызвать линклист \_ как \_ дериведлинклист для получения производного типа.</span><span class="sxs-lookup"><span data-stu-id="c02a1-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="c02a1-168">Чтобы получить сведения о типах во время выполнения, всутил создает первое поле базового типа с помощью [**спецификации WS для типа \_ \_ описания**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* и сопоставления поля [**\_ \_ атрибута \_ \_ типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) для описания сведений xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="c02a1-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="c02a1-169">Приложение может непосредственно установить или проверить поле, чтобы определить фактический тип структур.</span><span class="sxs-lookup"><span data-stu-id="c02a1-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="c02a1-170">Например, следующий код задает тип структуры для Дриведлинклист:</span><span class="sxs-lookup"><span data-stu-id="c02a1-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="c02a1-171">После десериализации структуры приложение может напрямую сравнить описание типа, чтобы определить десериализованный тип:</span><span class="sxs-lookup"><span data-stu-id="c02a1-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="c02a1-172">всутил создать класс для базовой структуры и производной структуры.</span><span class="sxs-lookup"><span data-stu-id="c02a1-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="c02a1-173">Конструктор по умолчанию инициализирует тип и описание соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="c02a1-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="c02a1-174">Подпрограммы Асдериведтипе помогают выполнять приведение безопасного типа между типами.</span><span class="sxs-lookup"><span data-stu-id="c02a1-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="c02a1-175">nillable</span><span class="sxs-lookup"><span data-stu-id="c02a1-175">nillable</span></span>

<span data-ttu-id="c02a1-176">атрибут "обнуляемых" поддерживается для строк, структур и массивов байтов.</span><span class="sxs-lookup"><span data-stu-id="c02a1-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="c02a1-177">\_Атрибут WS Field \_ обнуляемых будет добавлен в поля с нулевым атрибутом.</span><span class="sxs-lookup"><span data-stu-id="c02a1-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="c02a1-178">Если элемент является нулевым, указатель будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="c02a1-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="c02a1-179">Поле с нулевым именем в структуре обрабатывается как указатель.</span><span class="sxs-lookup"><span data-stu-id="c02a1-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="c02a1-180">Структура параметра с нулевым атрибутом будет передана по ссылке.</span><span class="sxs-lookup"><span data-stu-id="c02a1-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="c02a1-181">указатели</span><span class="sxs-lookup"><span data-stu-id="c02a1-181">pointers</span></span>

<span data-ttu-id="c02a1-182">Тип значения должен передаваться по значению или по ссылке для параметров out.</span><span class="sxs-lookup"><span data-stu-id="c02a1-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="c02a1-183">Двойной указатель не допускается, кроме структур только для out.</span><span class="sxs-lookup"><span data-stu-id="c02a1-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="c02a1-184">Использование без параметров</span><span class="sxs-lookup"><span data-stu-id="c02a1-184">Parameterless</span></span>

<span data-ttu-id="c02a1-185">Вспомним наше прежнее обсуждение с именем Parameters для части сообщения.</span><span class="sxs-lookup"><span data-stu-id="c02a1-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="c02a1-186">Если указан этот параметр, будет предпринята попытка создать объединенный кадр для входного и выходного сообщения для итоговой операции службы.</span><span class="sxs-lookup"><span data-stu-id="c02a1-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="c02a1-187">Если это не указано, то итоговая операция службы будет содержать входные и выходные сообщения в качестве параметров в качестве структур.</span><span class="sxs-lookup"><span data-stu-id="c02a1-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="c02a1-188">Таким образом, для нашей операции Симплемесод подпись службы и клиент будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="c02a1-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="c02a1-189">Безопасность</span><span class="sxs-lookup"><span data-stu-id="c02a1-189">Security</span></span>

<span data-ttu-id="c02a1-190">См. раздел "безопасность" в [средстве компилятора всутил](wsutil-compiler-tool.md) , а также в разделе " [сериализация](serialization.md) ".</span><span class="sxs-lookup"><span data-stu-id="c02a1-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




