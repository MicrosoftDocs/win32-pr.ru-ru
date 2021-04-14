---
title: Метаданные службы
description: Узел службы ВВСАПИ поддерживает WS-MetadataExchange для своих конечных точек.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Собственные метаданные службы — веб-службы
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488568"
---
# <a name="service-metadata"></a><span data-ttu-id="81258-106">Метаданные службы</span><span class="sxs-lookup"><span data-stu-id="81258-106">Service Metadata</span></span>

<span data-ttu-id="81258-107">Узел службы ВВСАПИ поддерживает WS-MetadataExchange для своих конечных точек.</span><span class="sxs-lookup"><span data-stu-id="81258-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="81258-108">Включить такой обмен метаданными на узле службы можно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="81258-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="81258-109">Укажите документы метаданных в свойстве [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) на [ \_ \_ узле службы WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="81258-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="81258-110">Укажите имя службы в свойстве [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) на [ \_ \_ узле службы WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="81258-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="81258-111">Укажите порт для отдельных конечных точек с помощью [**свойства \_ \_ метаданных для \_ свойства \_ конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) WS в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="81258-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="81258-112">Включите одну или несколько [**структур \_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) для обслуживания запросов WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="81258-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="81258-113">При необходимости укажите **\_ \_ \_ \_ \_ \_ \_ суффикс URL-адреса обмена метаданных свойств конечной точки службы WS** в перечислении [**\_ \_ \_ \_ идентификаторов свойств конечной точки службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) для обслуживания Ws-MetadataExchange запросов по определенному адресу.</span><span class="sxs-lookup"><span data-stu-id="81258-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="81258-114">Указание метаданных и имен службы на узле службы</span><span class="sxs-lookup"><span data-stu-id="81258-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="81258-115">Первым шагом является указание документов метаданных на узле службы.</span><span class="sxs-lookup"><span data-stu-id="81258-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="81258-116">Для этого необходимо собрать отдельные документы в виде массива \_ строк WS XML \_ \* .</span><span class="sxs-lookup"><span data-stu-id="81258-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="81258-117">Эти строки могут быть XML-схемой, WSDL или WS-Policy документом.</span><span class="sxs-lookup"><span data-stu-id="81258-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="81258-118">Это указывается с помощью свойства [**\_ \_ \_ метаданных свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="81258-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="81258-119">При необходимости приложение может также указать имя службы и пространство имен как часть [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span><span class="sxs-lookup"><span data-stu-id="81258-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="81258-120">Если в документе метаданных не указан элемент службы для данного имени службы, то модель службы создаст элемент службы с соответствующими портами WSDL для службы.</span><span class="sxs-lookup"><span data-stu-id="81258-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="81258-121">Обратите внимание, что для документов не выполняется проверка отдельных документов метаданных.</span><span class="sxs-lookup"><span data-stu-id="81258-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="81258-122">Приложение проверяет содержимое документов и гарантирует, что все пути импорта являются относительно определенными.</span><span class="sxs-lookup"><span data-stu-id="81258-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="81258-123">Указанное пространство имен используется для нахождение документа, в котором элемент службы будет добавлен узлом службы.</span><span class="sxs-lookup"><span data-stu-id="81258-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="81258-124">Добавление элемента службы в документ WSDL</span><span class="sxs-lookup"><span data-stu-id="81258-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="81258-125">Узел службы предоставляет приложению средство для добавления элемента службы от его имени, если он еще не указан.</span><span class="sxs-lookup"><span data-stu-id="81258-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="81258-126">Чтобы обеспечить такое поведение, приложение должно указать поля Серивценаме и Сервиценс в структуре [**\_ \_ метаданных службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) .</span><span class="sxs-lookup"><span data-stu-id="81258-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="81258-127">Если serviceName и Сервиценс равны **null** , в документ WSDL не добавляется элемент Service.</span><span class="sxs-lookup"><span data-stu-id="81258-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="81258-128">Оба они используются для указания документа, в котором будет добавлен serviceElement.</span><span class="sxs-lookup"><span data-stu-id="81258-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="81258-129">Если [**свойство \_ \_ \_ метаданных свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) не указано, метаданные ексханже не будут выполняться на узле службы.</span><span class="sxs-lookup"><span data-stu-id="81258-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="81258-130">Указание порта в \_ конечной точке службы WS \_</span><span class="sxs-lookup"><span data-stu-id="81258-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="81258-131">Чтобы [**\_ \_ Конечная точка службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) была доступна в качестве порта внутри элемента Service в документе WSDL, приложение должно указать свойство метаданных для [**\_ \_ \_ свойства \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .</span><span class="sxs-lookup"><span data-stu-id="81258-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="81258-132">Предполагается, что ссылка на имя привязки и пространство имен существует в документах, указанных на узле службы как часть \_ \_ метаданных свойства службы WS \_ .</span><span class="sxs-lookup"><span data-stu-id="81258-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="81258-133">Среда выполнения не проверяет это от имени приложения.</span><span class="sxs-lookup"><span data-stu-id="81258-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="81258-134">Включение обслуживания WS-MetadataExchange в \_ \_ конечной точке службы WS</span><span class="sxs-lookup"><span data-stu-id="81258-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="81258-135">Чтобы обслуживать запросы WS-MetadataExchange, на узле службы должна быть включена хотя бы одна конечная точка для обслуживания запросов WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="81258-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="81258-136">Для этого необходимо задать соответствующую версию для WS-MetadataExchange в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="81258-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="81258-137">Включение обслуживания HTTP GET в \_ \_ конечной точке службы WS</span><span class="sxs-lookup"><span data-stu-id="81258-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="81258-138">Чтобы Сервицехттп запросы GET, на узле службы должна быть включена хотя бы одна конечная точка для обслуживания запросов WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="81258-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="81258-139">Для этого необходимо задать соответствующую версию для WS-MetadataExchange в [**\_ \_ конечной точке службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="81258-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="81258-140">Указание суффикса URL-адреса для запросов Ws-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="81258-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="81258-141">Приложение может при необходимости включить прием запросов только для WS-MetadataExchange по определенному пути.</span><span class="sxs-lookup"><span data-stu-id="81258-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="81258-142">Это делается путем указания суффикса для заданной \_ \_ конечной точки службы WS.</span><span class="sxs-lookup"><span data-stu-id="81258-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="81258-143">Этот суффикс объединяется "как есть" с фактическим URL-адресом \_ \_ конечной точки службы WS.</span><span class="sxs-lookup"><span data-stu-id="81258-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="81258-144">Объединенная строка используется в качестве соответствующего URL-адреса для полученного заголовка "to".</span><span class="sxs-lookup"><span data-stu-id="81258-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="81258-145">Следующие элементы API относятся к службе метаданных.</span><span class="sxs-lookup"><span data-stu-id="81258-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="81258-146">Перечисление</span><span class="sxs-lookup"><span data-stu-id="81258-146">Enumeration</span></span>                                                       | <span data-ttu-id="81258-147">Описание</span><span class="sxs-lookup"><span data-stu-id="81258-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="81258-148">**\_тип обмена метаданными WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81258-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="81258-149">Включает или отключает WS-MetadataExchange и HTTP GET для обслуживания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81258-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="81258-150">Структура</span><span class="sxs-lookup"><span data-stu-id="81258-150">Structure</span></span>                                                               | <span data-ttu-id="81258-151">Описание</span><span class="sxs-lookup"><span data-stu-id="81258-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="81258-152">**\_ \_ метаданные конечной точки службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="81258-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="81258-153">Представляет элемент порта для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81258-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="81258-154">**\_метаданные службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="81258-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="81258-155">Указывает массив документов метаданных службы.</span><span class="sxs-lookup"><span data-stu-id="81258-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="81258-156">**\_ \_ документ МЕТАДАННЫХ службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="81258-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="81258-157">Указывает отдельные документы, составляющие метаданные службы.</span><span class="sxs-lookup"><span data-stu-id="81258-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




