---
title: Связанные с EAP константы и сведения об ошибках (Еафостеррор. h)
description: Отдельные группы констант, связанных с EAP и данными, общие для всех технологий API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071714"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="53663-103">Константы, относящиеся к EAP и сведения об ошибках</span><span class="sxs-lookup"><span data-stu-id="53663-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="53663-104">Отдельные группы констант, связанных с EAP и данными, общие для всех технологий API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="53663-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="53663-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**\_сначала EAP E с \_ EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="53663-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="53663-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="53663-107">Определяет границу отчетов об ошибках; Любая ошибка, связанная с EAPHost, будет вызвана между **EAP \_ e \_ EAPHost \_ First** и **\_ \_ \_ последней EAP e EAPHost**.</span><span class="sxs-lookup"><span data-stu-id="53663-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**Последнее время в EAP \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53663-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="53663-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-110">Определяет границу отчетов об ошибках; Любая ошибка, связанная с EAPHost, будет вызвана между **EAP \_ e \_ EAPHost \_ First** и **\_ \_ \_ последней EAP e EAPHost**.</span><span class="sxs-lookup"><span data-stu-id="53663-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**сначала требуется протокол EAP \_ I \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53663-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="53663-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="53663-113">Определяет границу информационных отчетов; все события, связанные с EAPHost, будут регистрироваться между **EAP \_ i \_ EAPHost \_ First** и с **EAP \_ i \_ EAPHost \_ последней**.</span><span class="sxs-lookup"><span data-stu-id="53663-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**\_ \_ \_ Дата последнего протокола EAP I**</span><span class="sxs-lookup"><span data-stu-id="53663-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="53663-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-116">Определяет границу информационных отчетов; все события, связанные с EAPHost, будут регистрироваться между **EAP \_ i \_ EAPHost \_ First** и с **EAP \_ i \_ EAPHost \_ последней**.</span><span class="sxs-lookup"><span data-stu-id="53663-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_ \_ хранилище сертификатов EAP \_ E \_ недоступно**</span><span class="sxs-lookup"><span data-stu-id="53663-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="53663-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="53663-119">Ни средство проверки подлинности, ни одноранговые узлы не могут получить доступ к хранилищу сертификатов.</span><span class="sxs-lookup"><span data-stu-id="53663-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ не установлен метод метода EAPHOST EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="53663-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="53663-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="53663-122">Запрошенный метод EAP не установлен.</span><span class="sxs-lookup"><span data-stu-id="53663-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_ \_ \_ \_ \_ Сброс узла метода \_ EAP E EAPHOST сторонних**</span><span class="sxs-lookup"><span data-stu-id="53663-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="53663-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="53663-125">Узел стороннего метода не отвечает и перезапускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="53663-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ еапкек \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="53663-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="53663-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="53663-128">EAPHost не удается связаться с [клиентом принудительного применения карантина](/windows/desktop/NAP/nap-client-architecture) EAP (Кек) на клиенте с поддержкой [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="53663-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_ \_ \_ неизвестное удостоверение "EAP E EAPHOST" \_**</span><span class="sxs-lookup"><span data-stu-id="53663-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="53663-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="53663-131">EAPHost возвращает эту ошибку, если проверка подлинности после отправки удостоверения одноранговой сети завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="53663-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_ \_ Ошибка проверки подлинности EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="53663-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="53663-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="53663-134">EAPHost возвращает эту ошибку при сбое проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="53663-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ сбой СОГЛАСОВАНия EAP \_ с EAP**</span><span class="sxs-lookup"><span data-stu-id="53663-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="53663-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="53663-137">EAPHost регистрирует это информационное событие, если клиент и сервер не настроены с совместимыми типами EAP.</span><span class="sxs-lookup"><span data-stu-id="53663-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ Недопустимый пакет метода \_ EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="53663-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="53663-140">Метод EAP получил пакет EAP, который не может быть обработан.</span><span class="sxs-lookup"><span data-stu-id="53663-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="53663-141">Другое имя для **\_ метода EAP E в \_ \_ методе EAPHOST \_ \_** — недопустимый пакет **\_ метода EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="53663-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ \_ Удаленный \_ Недопустимый \_ пакет для EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="53663-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="53663-144">EAPHost получил пакет, который не может быть обработан.</span><span class="sxs-lookup"><span data-stu-id="53663-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="53663-145">Другое имя для **EAP \_ E \_ EAPHOST \_ Remote \_ Недопустимый \_ пакет** — **\_ Недопустимый \_ пакет EAP**.</span><span class="sxs-lookup"><span data-stu-id="53663-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ \_ неправильный формат XML EAP E EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="53663-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="53663-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="53663-148">Сбой проверки схемы конфигурации EAPHost.</span><span class="sxs-lookup"><span data-stu-id="53663-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**\_ \_ Конфигурация метода EAP \_ E \_ \_ не \_ поддерживает \_ единый вход**</span><span class="sxs-lookup"><span data-stu-id="53663-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="53663-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="53663-151">Windows 7 или более поздней версии: метод EAP не поддерживает единый вход (SSO) для указанной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="53663-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_операция с методом протокола EAPHOST EAP E \_ \_ \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="53663-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="53663-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="53663-154">EAPHost возвращает эту ошибку, если настроенный метод EAP не поддерживает запрошенную операцию (вызов процедуры).</span><span class="sxs-lookup"><span data-stu-id="53663-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_Пользователь EAP \_ E \_ First**</span><span class="sxs-lookup"><span data-stu-id="53663-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="53663-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="53663-157">Определяет границу отчетов об ошибках; любое сообщение об ошибке, связанное с пользователем, будет происходить между **\_ пользователем EAP e \_ \_ First** и **\_ \_ \_ последним пользователем EAP e**.</span><span class="sxs-lookup"><span data-stu-id="53663-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**время \_ \_ последнего пользователя \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="53663-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="53663-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-160">Определяет границу отчетов об ошибках; любое сообщение об ошибке, связанное с пользователем, будет происходить между **\_ пользователем EAP e \_ \_ First** и **\_ \_ \_ последним пользователем EAP e**.</span><span class="sxs-lookup"><span data-stu-id="53663-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**\_ \_ \_ ПРЕДВАРИТЕЛЬный Пользователь EAP**</span><span class="sxs-lookup"><span data-stu-id="53663-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="53663-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="53663-163">Определяет границу информационных отчетов; регистрация в журнале событий, связанных с EAP, будет осуществляться между **пользователем с EAP \_ i \_ \_ первым** и **\_ \_ \_ последним пользователем EAP i**.</span><span class="sxs-lookup"><span data-stu-id="53663-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ последний пользователь EAP \_**</span><span class="sxs-lookup"><span data-stu-id="53663-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="53663-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-166">Определяет границу информационных отчетов; регистрация в журнале событий, связанных с EAP, будет осуществляться между **пользователем с EAP \_ i \_ \_ первым** и **\_ \_ \_ последним пользователем EAP i**.</span><span class="sxs-lookup"><span data-stu-id="53663-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_сертификат EAP \_ E \_ user \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="53663-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="53663-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="53663-169">EAPHost не удалось найти сертификат пользователя для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="53663-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ \_ Недопустимый сертификат \_ пользователя EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="53663-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="53663-172">Сертификат пользователя для проверки подлинности не имеет правильного набора расширенного использования ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="53663-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**\_ \_ \_ срок действия сертификата пользователя EAP E \_ истек**</span><span class="sxs-lookup"><span data-stu-id="53663-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="53663-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="53663-175">В EAPhost обнаружен сертификат пользователя с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="53663-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ \_ отозванный сертификат пользователя EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="53663-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="53663-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="53663-178">Сертификат пользователя, используемый для проверки подлинности, был отозван.</span><span class="sxs-lookup"><span data-stu-id="53663-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_ \_ \_ \_ другая ошибка EAP E user \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="53663-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="53663-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="53663-181">В сертификате пользователя, используемом для проверки подлинности, произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="53663-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ сертификат пользователя EAP \_ E \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="53663-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="53663-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="53663-184">Средство проверки подлинности отклонило сертификат пользователя.</span><span class="sxs-lookup"><span data-stu-id="53663-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ \_ другая ошибка УЧЕТной записи пользователя EAP \_**</span><span class="sxs-lookup"><span data-stu-id="53663-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="53663-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="53663-187">Ошибка EAP была получена после обмена удостоверениями, что указывает на вероятность проблемы с учетной записью пользователя, выполняющего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="53663-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ \_ учетные данные пользователя EAP E \_ отклонены**</span><span class="sxs-lookup"><span data-stu-id="53663-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="53663-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="53663-190">Средство проверки подлинности отклонило учетные данные пользователя для аутентификации.</span><span class="sxs-lookup"><span data-stu-id="53663-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_пароль EAP \_ E \_ имя \_ пользователя \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="53663-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="53663-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="53663-193">Windows 7 или более поздней версии: проверка подлинности не удалась.</span><span class="sxs-lookup"><span data-stu-id="53663-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="53663-194">Средство проверки подлинности отклонило учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="53663-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ без \_ считывателя смарт- \_ карт \_**</span><span class="sxs-lookup"><span data-stu-id="53663-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="53663-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="53663-197">Windows 7 или более поздней версии: устройство чтения смарт-карт не найдено.</span><span class="sxs-lookup"><span data-stu-id="53663-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_ \_ Сначала сервер EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="53663-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="53663-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="53663-200">Определяет границу отчетов об ошибках; Любая ошибка, связанная с сервером, возникает между сервером **EAP \_ e \_ \_ First** и **\_ сервером EAP e \_ \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="53663-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_Сервер EAP \_ E \_ Last**</span><span class="sxs-lookup"><span data-stu-id="53663-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="53663-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-203">Определяет границу отчетов об ошибках; Любая ошибка, связанная с сервером, возникает между сервером **EAP \_ e \_ \_ First** и **\_ сервером EAP e \_ \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="53663-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ сертификат сервера EAP \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="53663-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="53663-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="53663-206">EAPHost не удалось найти сертификат сервера для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="53663-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ \_ Недопустимый сертификат \_ сервера EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="53663-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="53663-209">Сертификат сервера, который пользователь выполняет для проверки подлинности, не имеет правильного набора расширенного использования ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="53663-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_ \_ \_ \_ истек срок действия сертификата сервера EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="53663-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="53663-212">В EAPhost обнаружен сертификат сервера с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="53663-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ сертификат сервера EAP \_ E \_ отозван**</span><span class="sxs-lookup"><span data-stu-id="53663-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="53663-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="53663-215">Сертификат сервера, используемый для проверки подлинности, был отозван.</span><span class="sxs-lookup"><span data-stu-id="53663-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ другая \_ Ошибка сертификата сервера EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="53663-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="53663-218">В сертификате сервера произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="53663-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ сначала пользователь EAP E \_ root \_ CERT \_**</span><span class="sxs-lookup"><span data-stu-id="53663-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="53663-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="53663-221">Определяет границу отчетов об ошибках; Любая ошибка, связанная с корневым сертификатом пользователя, будет находиться между **\_ \_ \_ \_ \_ первым** и корневым сертификатом пользователя **EAP \_ \_ \_ \_ \_** e.</span><span class="sxs-lookup"><span data-stu-id="53663-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ корневой сертификат пользователя EAP E — \_ \_ \_ последний**</span><span class="sxs-lookup"><span data-stu-id="53663-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="53663-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-224">Определяет границу отчетов об ошибках; Любая ошибка, связанная с корневым сертификатом пользователя, будет находиться между **\_ \_ \_ \_ \_ первым** и корневым сертификатом пользователя **EAP \_ \_ \_ \_ \_** e.</span><span class="sxs-lookup"><span data-stu-id="53663-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ корневой сертификат пользователя EAP E \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="53663-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="53663-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="53663-227">EAPHost не удалось найти сертификат в доверенном корневом хранилище сертификатов для проверки сертификата пользователя.</span><span class="sxs-lookup"><span data-stu-id="53663-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ \_ недопустимый корневой \_ сертификат пользователя \_ EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="53663-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="53663-230">Не удалось выполнить проверку подлинности, так как корневой сертификат, используемый для этой сети, недопустим.</span><span class="sxs-lookup"><span data-stu-id="53663-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_ \_ \_ срок действия корневого сертификата пользователя EAP E \_ \_ истек**</span><span class="sxs-lookup"><span data-stu-id="53663-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="53663-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="53663-233">Истек срок действия доверенного корневого сертификата, необходимого для проверки сертификата пользователя.</span><span class="sxs-lookup"><span data-stu-id="53663-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ \_ сначала следует корневой \_ сертификат сервера EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="53663-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="53663-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="53663-236">Определяет границу отчетов об ошибках; все ошибки, связанные с корневым сертификатом сервера, происходят сначала между **\_ \_ \_ корневым \_ \_ сертификатом EAP e Server** и **\_ \_ \_ корневым \_ сертификатом \_ EAP e Server**.</span><span class="sxs-lookup"><span data-stu-id="53663-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ последний корневой \_ сертификат сервера EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="53663-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="53663-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="53663-239">Определяет границу отчетов об ошибках; все ошибки, связанные с корневым сертификатом сервера, происходят сначала между **\_ \_ \_ корневым \_ \_ сертификатом EAP e Server** и **\_ \_ \_ корневым \_ сертификатом \_ EAP e Server**.</span><span class="sxs-lookup"><span data-stu-id="53663-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ корневой сертификат сервера EAP E \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="53663-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="53663-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="53663-242">EAPHost не удалось найти корневой сертификат в доверенном корневом хранилище сертификатов для проверки сертификации сервера.</span><span class="sxs-lookup"><span data-stu-id="53663-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ \_ недопустимый корневой \_ сертификат сервера \_ EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="53663-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="53663-245">Не удалось выполнить проверку подлинности, так как сертификат сервера, необходимый для этой сети на компьютере сервера, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="53663-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53663-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ \_ требуется имя корневого \_ сертификата \_ сервера \_ EAP E**</span><span class="sxs-lookup"><span data-stu-id="53663-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53663-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="53663-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="53663-248">Не удалось выполнить проверку подлинности, так как для сертификата на сервере не указано имя сервера.</span><span class="sxs-lookup"><span data-stu-id="53663-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53663-249">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53663-249">Remarks</span></span>

<span data-ttu-id="53663-250">Существуют альтернативные имена для некоторых ошибок:</span><span class="sxs-lookup"><span data-stu-id="53663-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="53663-251">Другое имя для **\_ метода EAP E в \_ \_ методе EAPHOST \_ \_** — недопустимый пакет **\_ метода EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="53663-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="53663-252">Другое имя для **EAP \_ E \_ EAPHOST \_ Remote \_ Недопустимый \_ пакет** — **\_ Недопустимый \_ пакет EAP**.</span><span class="sxs-lookup"><span data-stu-id="53663-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="53663-253">Требования</span><span class="sxs-lookup"><span data-stu-id="53663-253">Requirements</span></span>



| <span data-ttu-id="53663-254">Требование</span><span class="sxs-lookup"><span data-stu-id="53663-254">Requirement</span></span> | <span data-ttu-id="53663-255">Значение</span><span class="sxs-lookup"><span data-stu-id="53663-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="53663-256">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53663-256">Minimum supported client</span></span><br/> | <span data-ttu-id="53663-257">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53663-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="53663-258">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53663-258">Minimum supported server</span></span><br/> | <span data-ttu-id="53663-259">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53663-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="53663-260">Header</span><span class="sxs-lookup"><span data-stu-id="53663-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="53663-261"><dt>Еафостеррор. h</dt></span><span class="sxs-lookup"><span data-stu-id="53663-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53663-262">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53663-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53663-263">Общие константы EAPHost</span><span class="sxs-lookup"><span data-stu-id="53663-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

