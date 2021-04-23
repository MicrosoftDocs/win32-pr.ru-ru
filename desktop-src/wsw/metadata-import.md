---
title: Импорт метаданных
description: ВВСАПИ включает элементы API, которые можно использовать для обработки WSDL и политики из конечной точки с целью извлечения сведений, которые можно использовать для связи с конечной точкой.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Веб-службы импорта метаданных для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797394"
---
# <a name="metadata-import"></a><span data-ttu-id="1619d-106">Импорт метаданных</span><span class="sxs-lookup"><span data-stu-id="1619d-106">Metadata Import</span></span>

<span data-ttu-id="1619d-107">ВВСАПИ включает элементы API, которые можно использовать для обработки WSDL и политики из конечной точки с целью извлечения сведений, которые можно использовать для связи с конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="1619d-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="1619d-108">Эти API обычно используются, когда протокол связи, поддерживаемый конечной точкой, еще не известен.</span><span class="sxs-lookup"><span data-stu-id="1619d-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="1619d-109">Для обработки метаданных используйте следующую последовательность:</span><span class="sxs-lookup"><span data-stu-id="1619d-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="1619d-110">сведения о том, как утверждения WSDL и WS-Policy соответствуют API, см. в разделе [Сопоставление метаданных](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="1619d-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="1619d-111">Безопасность</span><span class="sxs-lookup"><span data-stu-id="1619d-111">Security</span></span>

<span data-ttu-id="1619d-112">Скачанные метаданные — это так же хорошо, как адрес, используемый для его скачивания.</span><span class="sxs-lookup"><span data-stu-id="1619d-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="1619d-113">Приложение должно обеспечить доверие к адресу.</span><span class="sxs-lookup"><span data-stu-id="1619d-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="1619d-114">Кроме того, приложение должно обеспечить использование протокола безопасности для загрузки документов метаданных, которые не допускают фальсификации с помощью метаданных.</span><span class="sxs-lookup"><span data-stu-id="1619d-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="1619d-115">Приложение должно проверять адреса служб, предоставляемых метаданными.</span><span class="sxs-lookup"><span data-stu-id="1619d-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="1619d-116">По умолчанию среда выполнения гарантирует, что имя узла службы совпадает с исходным URL-адресом, используемым для загрузки метаданных, но приложение может захотеть выполнить дополнительные проверки.</span><span class="sxs-lookup"><span data-stu-id="1619d-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="1619d-117">Приложение может отключить проверку имени узла, перезаписав свойство [**метаданных WS \_ \_ проверить имя \_ \_ узла \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) .</span><span class="sxs-lookup"><span data-stu-id="1619d-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="1619d-118">Если проверка имени узла, выполненная по умолчанию, отключена, приложение должно защищать себя от документов метаданных, содержащих адрес службы, от другой стороны, которая не доверяет каким-либо другим способом.</span><span class="sxs-lookup"><span data-stu-id="1619d-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="1619d-119">По умолчанию максимальный объем памяти, используемый средой выполнения метаданных для десериализации и обработки метаданных, составляет 256 КБ, а максимальное число документов, которое можно добавить, — 32.</span><span class="sxs-lookup"><span data-stu-id="1619d-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="1619d-120">Эти значения по умолчанию могут быть перезаписаны в свойствах [**\_ \_ \_ \_ запрошенного \_ размера кучи свойств метаданных**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) и свойств **\_ метаданных \_ \_ \_ WS** .</span><span class="sxs-lookup"><span data-stu-id="1619d-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="1619d-121">Эти границы предназначены для ограничения объема загружаемых файлов и ограничивают объем выделяемой памяти для накопления метаданных.</span><span class="sxs-lookup"><span data-stu-id="1619d-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="1619d-122">Увеличение этих значений может привести к чрезмерному потреблению памяти, использованию ЦП или пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="1619d-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="1619d-123">Обратите внимание, что из-за расширения строк словаря в двоичном формате небольшое сообщение может привести к значительному объему десериализованной формы, поэтому использование небольших сообщений для ограничения выделения памяти метаданных недостаточно при использовании двоичного формата.</span><span class="sxs-lookup"><span data-stu-id="1619d-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="1619d-124">По умолчанию максимальное количество альтернативных политик — 32, хотя оно может быть перезаписано свойством " [**\_ \_ \_ Максимальное \_ альтернативное свойство политики WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) ".</span><span class="sxs-lookup"><span data-stu-id="1619d-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="1619d-125">Если приложение просматривает каждую альтернативу в поисках совпадения, может потребоваться выполнить поиск во всех вариантах, прежде чем искать соответствие.</span><span class="sxs-lookup"><span data-stu-id="1619d-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="1619d-126">Увеличение максимального числа альтернатив может привести к чрезмерному использованию ЦП.</span><span class="sxs-lookup"><span data-stu-id="1619d-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="1619d-127">Следующие перечисления являются частью импорта метаданных:</span><span class="sxs-lookup"><span data-stu-id="1619d-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="1619d-128">**\_ \_ идентификатор свойства метаданных \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="1619d-129">**\_состояние МЕТАДАННЫХ \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="1619d-130">**\_ \_ тип расширения политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="1619d-131">**\_ \_ идентификатор свойства политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="1619d-132">**\_состояние политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="1619d-133">**\_ \_ \_ тип ограничения привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="1619d-134">В импорт метаданных входят следующие функции:</span><span class="sxs-lookup"><span data-stu-id="1619d-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="1619d-135">**вскреатеметадата**</span><span class="sxs-lookup"><span data-stu-id="1619d-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="1619d-136">**всфриметадата**</span><span class="sxs-lookup"><span data-stu-id="1619d-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="1619d-137">**всжетметадатаендпоинтс**</span><span class="sxs-lookup"><span data-stu-id="1619d-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="1619d-138">**всжетметадатапроперти**</span><span class="sxs-lookup"><span data-stu-id="1619d-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="1619d-139">**всжетмиссингметадатадокументаддресс**</span><span class="sxs-lookup"><span data-stu-id="1619d-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="1619d-140">**всжетполициалтернативекаунт**</span><span class="sxs-lookup"><span data-stu-id="1619d-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="1619d-141">**всжетполиципроперти**</span><span class="sxs-lookup"><span data-stu-id="1619d-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="1619d-142">**всматчполициалтернативе**</span><span class="sxs-lookup"><span data-stu-id="1619d-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="1619d-143">**всреадметадата**</span><span class="sxs-lookup"><span data-stu-id="1619d-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="1619d-144">**всресетметадата**</span><span class="sxs-lookup"><span data-stu-id="1619d-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="1619d-145">В импорт метаданных входят следующие дескрипторы:</span><span class="sxs-lookup"><span data-stu-id="1619d-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="1619d-146">\_метаданные WS</span><span class="sxs-lookup"><span data-stu-id="1619d-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="1619d-147">\_политика WS</span><span class="sxs-lookup"><span data-stu-id="1619d-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="1619d-148">В импорт метаданных входят следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="1619d-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="1619d-149">**\_ \_ \_ \_ ограничение привязки безопасности сообщений сертификата \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="1619d-150">**\_ \_ ограничение свойства канала \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="1619d-151">**\_расширение политики конечных точек WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1619d-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="1619d-152">**\_ \_ \_ \_ \_ ограничение привязки безопасности проверки подлинности заголовка WS HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1619d-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="1619d-153">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений \_ о выданных маркерах WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="1619d-154">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений WS Kerberos \_ апрек**</span><span class="sxs-lookup"><span data-stu-id="1619d-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="1619d-155">**\_ \_ Конечная точка метаданных WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="1619d-156">**\_ \_ конечные точки метаданных WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="1619d-157">**\_свойство МЕТАДАННЫХ \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="1619d-158">**\_ограничения политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="1619d-159">**\_расширение политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="1619d-160">**\_Свойства политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="1619d-161">**\_свойство политики \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="1619d-162">**\_ \_ \_ ограничение свойства токена \_ безопасности \_ WS Request**</span><span class="sxs-lookup"><span data-stu-id="1619d-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="1619d-163">**\_ \_ ограничение привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="1619d-164">**\_ \_ \_ ограничение свойства привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="1619d-165">**\_ограничения безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="1619d-166">**\_ \_ \_ \_ \_ ограничение привязки безопасности сообщений контекста \_ безопасности WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="1619d-167">**\_ \_ ограничение свойства безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="1619d-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="1619d-168">**\_ \_ \_ \_ ограничение привязки безопасности транспорта WS SSL \_**</span><span class="sxs-lookup"><span data-stu-id="1619d-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="1619d-169">**\_ \_ \_ \_ \_ ограничение привязки безопасности транспорта WS TCP \_ SSPI**</span><span class="sxs-lookup"><span data-stu-id="1619d-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="1619d-170">**\_ \_ \_ \_ ограничение привязки безопасности сообщений имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="1619d-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




