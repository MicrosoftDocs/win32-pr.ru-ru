---
title: Значения ошибок регистрации MDM (Мдмрегистратион. h)
description: Следующие значения ошибок связаны с регистрацией MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548989"
---
# <a name="mdm-registration-error-values"></a><span data-ttu-id="5f714-103">Значения ошибок регистрации MDM</span><span class="sxs-lookup"><span data-stu-id="5f714-103">MDM registration error values</span></span>

<span data-ttu-id="5f714-104">Следующие значения ошибок связаны с регистрацией MDM.</span><span class="sxs-lookup"><span data-stu-id="5f714-104">The following error values are with MDM registration.</span></span>

<dl> <dt>

<span data-ttu-id="5f714-105"><span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**\_несоответствие типов данных E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-105"><span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-106">0x8007065d</span><span class="sxs-lookup"><span data-stu-id="5f714-106">0x8007065d</span></span>
</dt> <dt>



<span data-ttu-id="5f714-107">Тип данных не соответствует ожидаемому типу данных.</span><span class="sxs-lookup"><span data-stu-id="5f714-107">The datatype does not match the expected datatype.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-108"><span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_ \_ \_ \_ Ошибка формата сообщения устройства мрегистер E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-108"><span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER\_E\_DEVICE\_MESSAGE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-109">0x80190001</span><span class="sxs-lookup"><span data-stu-id="5f714-109">0x80190001</span></span>
</dt> <dt>



<span data-ttu-id="5f714-110">Недопустимая схема, ошибка формата сообщения от сервера.</span><span class="sxs-lookup"><span data-stu-id="5f714-110">Invalid Schema, Message Format Error from server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-111"><span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_ \_ \_ \_ Ошибка формата сообщения устройства менролл E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-111"><span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**MENROLL\_E\_DEVICE\_MESSAGE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-112">0x80180001</span><span class="sxs-lookup"><span data-stu-id="5f714-112">0x80180001</span></span>
</dt> <dt>



<span data-ttu-id="5f714-113">Недопустимая схема, ошибка формата сообщения от сервера.</span><span class="sxs-lookup"><span data-stu-id="5f714-113">Invalid Schema , Message Format Error from server.</span></span>

<span data-ttu-id="5f714-114">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-114">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-115"><span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**\_ \_ \_ Ошибка проверки подлинности устройства мрегистер E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-115"><span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER\_E\_DEVICE\_AUTHENTICATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-116">0x80190002</span><span class="sxs-lookup"><span data-stu-id="5f714-116">0x80190002</span></span>
</dt> <dt>



<span data-ttu-id="5f714-117">Серверу не удалось проверить подлинность пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f714-117">Server failed to authenticate the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-118"><span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**\_ \_ \_ Ошибка проверки подлинности устройства менролл E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-118"><span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**MENROLL\_E\_DEVICE\_AUTHENTICATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-119">0x80180002</span><span class="sxs-lookup"><span data-stu-id="5f714-119">0x80180002</span></span>
</dt> <dt>



<span data-ttu-id="5f714-120">Серверу не удалось проверить подлинность пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f714-120">Server failed to authenticate the user.</span></span>

<span data-ttu-id="5f714-121">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-121">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-122"><span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_ \_ \_ Ошибка авторизации устройства мрегистер \_ E**</span><span class="sxs-lookup"><span data-stu-id="5f714-122"><span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MREGISTER\_E\_DEVICE\_AUTHORIZATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-123">0x80190003</span><span class="sxs-lookup"><span data-stu-id="5f714-123">0x80190003</span></span>
</dt> <dt>



<span data-ttu-id="5f714-124">У пользователя нет права на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="5f714-124">The user is not authorized to enroll.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-125"><span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_ \_ \_ Ошибка авторизации устройства менролл \_ E**</span><span class="sxs-lookup"><span data-stu-id="5f714-125"><span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**MENROLL\_E\_DEVICE\_AUTHORIZATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-126">0x80180003</span><span class="sxs-lookup"><span data-stu-id="5f714-126">0x80180003</span></span>
</dt> <dt>



<span data-ttu-id="5f714-127">У пользователя нет права на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="5f714-127">The user is not authorized to enroll.</span></span>

<span data-ttu-id="5f714-128">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-128">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-129"><span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**\_ \_ Ошибка цертифкатерекуест для устройства мрегистер E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-129"><span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER\_E\_DEVICE\_CERTIFCATEREQUEST\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-130">0x80190004</span><span class="sxs-lookup"><span data-stu-id="5f714-130">0x80190004</span></span>
</dt> <dt>



<span data-ttu-id="5f714-131">У пользователя нет разрешений на шаблон сертификата, или центр сертификации недоступен.</span><span class="sxs-lookup"><span data-stu-id="5f714-131">The user has no permission for the certificate template or the certificate authority is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-132"><span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**\_ \_ Ошибка цертифкатерекуест для устройства менролл E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-132"><span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL\_E\_DEVICE\_CERTIFCATEREQUEST\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-133">0x80180004</span><span class="sxs-lookup"><span data-stu-id="5f714-133">0x80180004</span></span>
</dt> <dt>



<span data-ttu-id="5f714-134">У пользователя нет разрешений на шаблон сертификата, или центр сертификации недоступен.</span><span class="sxs-lookup"><span data-stu-id="5f714-134">The user has no permission for the certificate template or the certificate authority is unreachable.</span></span>

<span data-ttu-id="5f714-135">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-135">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-136"><span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**\_ \_ Ошибка конфигмгрсервер для устройства мрегистер E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-136"><span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER\_E\_DEVICE\_CONFIGMGRSERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-137">0x80190005</span><span class="sxs-lookup"><span data-stu-id="5f714-137">0x80190005</span></span>
</dt> <dt>



<span data-ttu-id="5f714-138">Произошел сбой на сервере управления, например ошибка доступа к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f714-138">There was a failure at the management server, such as a database access error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-139"><span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_ \_ Ошибка конфигмгрсервер для устройства менролл E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-139"><span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL\_E\_DEVICE\_CONFIGMGRSERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-140">0x80180005</span><span class="sxs-lookup"><span data-stu-id="5f714-140">0x80180005</span></span>
</dt> <dt>



<span data-ttu-id="5f714-141">Произошел сбой на сервере управления, например ошибка доступа к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f714-141">There was a failure at the management server, such as a database access error.</span></span>

<span data-ttu-id="5f714-142">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-142">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-143"><span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**\_ \_ Ошибка интерналсервице для устройства мрегистер E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-143"><span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER\_E\_DEVICE\_INTERNALSERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-144">0x80190006</span><span class="sxs-lookup"><span data-stu-id="5f714-144">0x80190006</span></span>
</dt> <dt>



<span data-ttu-id="5f714-145">На сервере возникло необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="5f714-145">There was an unhandled exception on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-146"><span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**\_ \_ Ошибка интерналсервице для устройства менролл E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-146"><span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL\_E\_DEVICE\_INTERNALSERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-147">0x80180006</span><span class="sxs-lookup"><span data-stu-id="5f714-147">0x80180006</span></span>
</dt> <dt>



<span data-ttu-id="5f714-148">На сервере возникло необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="5f714-148">There was an unhandled exception on the server.</span></span>

<span data-ttu-id="5f714-149">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-149">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-150"><span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**\_ \_ Ошибка инвалидсекурити для устройства мрегистер E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-150"><span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER\_E\_DEVICE\_INVALIDSECURITY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-151">0x80190007</span><span class="sxs-lookup"><span data-stu-id="5f714-151">0x80190007</span></span>
</dt> <dt>



<span data-ttu-id="5f714-152">На сервере возникло необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="5f714-152">There was an unhandled exception on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-153"><span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**\_ \_ Ошибка инвалидсекурити для устройства менролл E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-153"><span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL\_E\_DEVICE\_INVALIDSECURITY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-154">0x80180007</span><span class="sxs-lookup"><span data-stu-id="5f714-154">0x80180007</span></span>
</dt> <dt>



<span data-ttu-id="5f714-155">На сервере возникло необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="5f714-155">There was an unhandled exception on the server.</span></span>

<span data-ttu-id="5f714-156">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-156">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-157"><span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ \_ неизвестная \_ ошибка устройства мрегистер E**</span><span class="sxs-lookup"><span data-stu-id="5f714-157"><span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**MREGISTER\_E\_DEVICE\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-158">0x80190008</span><span class="sxs-lookup"><span data-stu-id="5f714-158">0x80190008</span></span>
</dt> <dt>



<span data-ttu-id="5f714-159">Неизвестная ошибка сервера.</span><span class="sxs-lookup"><span data-stu-id="5f714-159">Unknown server error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-160"><span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ \_ неизвестная \_ ошибка устройства менролл E**</span><span class="sxs-lookup"><span data-stu-id="5f714-160"><span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**MENROLL\_E\_DEVICE\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-161">0x80180008</span><span class="sxs-lookup"><span data-stu-id="5f714-161">0x80180008</span></span>
</dt> <dt>



<span data-ttu-id="5f714-162">Неизвестная ошибка сервера.</span><span class="sxs-lookup"><span data-stu-id="5f714-162">Unknown server error.</span></span>

<span data-ttu-id="5f714-163">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-163">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-164"><span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**\_ \_ выполняется регистрация мрегистер \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-164"><span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MREGISTER\_E\_REGISTRATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-165">0x80190009</span><span class="sxs-lookup"><span data-stu-id="5f714-165">0x80190009</span></span>
</dt> <dt>



<span data-ttu-id="5f714-166">В настоящее время выполняется другая операция регистрации.</span><span class="sxs-lookup"><span data-stu-id="5f714-166">Another enrollment operation is currently underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-167"><span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_ \_ идет регистрация менролл E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-167"><span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**MENROLL\_E\_ENROLLMENT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-168">0x80180009</span><span class="sxs-lookup"><span data-stu-id="5f714-168">0x80180009</span></span>
</dt> <dt>



<span data-ttu-id="5f714-169">В настоящее время выполняется другая операция регистрации.</span><span class="sxs-lookup"><span data-stu-id="5f714-169">Another enrollment operation is currently underway.</span></span>

<span data-ttu-id="5f714-170">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-170">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-171"><span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**\_устройство мрегистер \_ E \_ уже \_ зарегистрировано**</span><span class="sxs-lookup"><span data-stu-id="5f714-171"><span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER\_E\_DEVICE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-172">0x8019000A</span><span class="sxs-lookup"><span data-stu-id="5f714-172">0x8019000A</span></span>
</dt> <dt>



<span data-ttu-id="5f714-173">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="5f714-173">No longer used.</span></span>

<span data-ttu-id="5f714-174">**Windows 8.1:** Устройство уже зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="5f714-174">**Windows 8.1:** The device is already enrolled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-175"><span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**\_устройство менролл \_ E \_ уже \_ зарегистрировано**</span><span class="sxs-lookup"><span data-stu-id="5f714-175"><span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**MENROLL\_E\_DEVICE\_ALREADY\_ENROLLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-176">0x8018000A</span><span class="sxs-lookup"><span data-stu-id="5f714-176">0x8018000A</span></span>
</dt> <dt>



<span data-ttu-id="5f714-177">Устройство уже зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="5f714-177">The device is already enrolled.</span></span>

<span data-ttu-id="5f714-178">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-178">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-179"><span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_устройство мрегистер \_ E \_ не \_ зарегистрировано**</span><span class="sxs-lookup"><span data-stu-id="5f714-179"><span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER\_E\_DEVICE\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-180">0x8019000B</span><span class="sxs-lookup"><span data-stu-id="5f714-180">0x8019000B</span></span>
</dt> <dt>



<span data-ttu-id="5f714-181">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="5f714-181">No longer used.</span></span>

<span data-ttu-id="5f714-182">**Windows 8.1:** Устройство не зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="5f714-182">**Windows 8.1:** The device is not enrolled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-183"><span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**\_устройство менролл \_ E \_ не \_ зарегистрировано**</span><span class="sxs-lookup"><span data-stu-id="5f714-183"><span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**MENROLL\_E\_DEVICE\_NOT\_ENROLLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-184">0x8018000B</span><span class="sxs-lookup"><span data-stu-id="5f714-184">0x8018000B</span></span>
</dt> <dt>



<span data-ttu-id="5f714-185">Устройство не зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="5f714-185">The device is not enrolled.</span></span>

<span data-ttu-id="5f714-186">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-186">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-187"><span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**\_Перенаправление \_ обнаружения мрегистер E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-187"><span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER\_E\_DISCOVERY\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-188">0x8019000C</span><span class="sxs-lookup"><span data-stu-id="5f714-188">0x8019000C</span></span>
</dt> <dt>



<span data-ttu-id="5f714-189">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="5f714-189">No longer used.</span></span>

<span data-ttu-id="5f714-190">**Windows 8.1:** Требуется перенаправление.</span><span class="sxs-lookup"><span data-stu-id="5f714-190">**Windows 8.1:** Redirection is needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-191"><span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**МРЕГИСТЕР \_ E \_ устройство \_ не \_ \_ зарегистрировано \_ Ошибка AD**</span><span class="sxs-lookup"><span data-stu-id="5f714-191"><span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER\_E\_DEVICE\_NOT\_AD\_REGISTERED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-192">0x8019000D</span><span class="sxs-lookup"><span data-stu-id="5f714-192">0x8019000D</span></span>
</dt> <dt>



<span data-ttu-id="5f714-193">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="5f714-193">No longer used.</span></span>

<span data-ttu-id="5f714-194">**Windows 8.1:** Устройство не зарегистрировано в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f714-194">**Windows 8.1:** The device is not registered with Active Directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-195"><span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**\_ \_ \_ \_ \_ Недопустимая дата сертификата обнаружения менролл E в секунду \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-195"><span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL\_E\_DISCOVERY\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-196">0x8018000D</span><span class="sxs-lookup"><span data-stu-id="5f714-196">0x8018000D</span></span>
</dt> <dt>



<span data-ttu-id="5f714-197">Во время обнаружения недопустимая дата сертификата в секунду.</span><span class="sxs-lookup"><span data-stu-id="5f714-197">During discovery the sec cert date was invalid.</span></span>

<span data-ttu-id="5f714-198">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-198">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-199"><span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**\_ \_ сбой обнаружения мрегистер \_ E**</span><span class="sxs-lookup"><span data-stu-id="5f714-199"><span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MREGISTER\_E\_DISCOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-200">0x8019000E</span><span class="sxs-lookup"><span data-stu-id="5f714-200">0x8019000E</span></span>
</dt> <dt>



<span data-ttu-id="5f714-201">Больше не используется.</span><span class="sxs-lookup"><span data-stu-id="5f714-201">No longer used.</span></span>

<span data-ttu-id="5f714-202">**Windows 8.1:** Сбой обнаружения; требуется перенаправление.</span><span class="sxs-lookup"><span data-stu-id="5f714-202">**Windows 8.1:** Discovery failed; redirection is needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-203"><span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_ \_ требуется пароль менролл \_ E**</span><span class="sxs-lookup"><span data-stu-id="5f714-203"><span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL\_E\_PASSWORD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-204">0x8018000E</span><span class="sxs-lookup"><span data-stu-id="5f714-204">0x8018000E</span></span>
</dt> <dt>



<span data-ttu-id="5f714-205">Требуется пароль, но он не был указан.</span><span class="sxs-lookup"><span data-stu-id="5f714-205">A password is needed, but was not supplied.</span></span>

<span data-ttu-id="5f714-206">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-206">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-207"><span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**МЕНРОЛЛ \_ E \_ , \_ Ошибка wab**</span><span class="sxs-lookup"><span data-stu-id="5f714-207"><span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**MENROLL\_E\_WAB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-208">0x8018000F</span><span class="sxs-lookup"><span data-stu-id="5f714-208">0x8018000F</span></span>
</dt> <dt>



<span data-ttu-id="5f714-209">Во время регистрации WAB произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5f714-209">An error occurred during WAB enrollment.</span></span>

<span data-ttu-id="5f714-210">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-210">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-211"><span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**\_Подключение менролл E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-211"><span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL\_E\_CONNECTIVITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-212">0x80180010</span><span class="sxs-lookup"><span data-stu-id="5f714-212">0x80180010</span></span>
</dt> <dt>



<span data-ttu-id="5f714-213">Произошла сетевая ошибка, например DNS или время ожидания сети.</span><span class="sxs-lookup"><span data-stu-id="5f714-213">A network error occurred, such as DNS or a network timeout.</span></span>

<span data-ttu-id="5f714-214">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-214">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-215"><span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**\_Регистрация менролл \_ \_ приостановлена**</span><span class="sxs-lookup"><span data-stu-id="5f714-215"><span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**MENROLL\_S\_ENROLLMENT\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-216">0x00180011</span><span class="sxs-lookup"><span data-stu-id="5f714-216">0x00180011</span></span>
</dt> <dt>



<span data-ttu-id="5f714-217">Регистрация приостановлена.</span><span class="sxs-lookup"><span data-stu-id="5f714-217">Enrollment was suspended.</span></span> <span data-ttu-id="5f714-218">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f714-218">No longer supported.</span></span>

<span data-ttu-id="5f714-219">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-219">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-220"><span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**МЕНРОЛЛ \_ E \_ инвалидсслцерт**</span><span class="sxs-lookup"><span data-stu-id="5f714-220"><span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL\_E\_INVALIDSSLCERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-221">0x80180012</span><span class="sxs-lookup"><span data-stu-id="5f714-221">0x80180012</span></span>
</dt> <dt>



<span data-ttu-id="5f714-222">Недопустимый SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="5f714-222">The SSL cert was not valid.</span></span>

<span data-ttu-id="5f714-223">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-223">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-224"><span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**МЕНРОЛЛ \_ E \_ DEVICECAPREACHED**</span><span class="sxs-lookup"><span data-stu-id="5f714-224"><span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL\_E\_DEVICECAPREACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-225">0x80180013</span><span class="sxs-lookup"><span data-stu-id="5f714-225">0x80180013</span></span>
</dt> <dt>



<span data-ttu-id="5f714-226">Пользователь уже зарегистрировал слишком много устройств.</span><span class="sxs-lookup"><span data-stu-id="5f714-226">The user has already enrolled too many devices.</span></span> <span data-ttu-id="5f714-227">Удалите или отменяйте регистрацию старых, чтобы устранить эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="5f714-227">Delete or unenroll old ones to fix this error.</span></span> <span data-ttu-id="5f714-228">Обратите внимание, что пользователь может устранить эту ошибку без помощи администратора.</span><span class="sxs-lookup"><span data-stu-id="5f714-228">Note that the user can resolve this error without admin assistance.</span></span>

<span data-ttu-id="5f714-229">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-229">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-230"><span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**МЕНРОЛЛ \_ E \_ девиценотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="5f714-230"><span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL\_E\_DEVICENOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-231">кодом 0x80180014</span><span class="sxs-lookup"><span data-stu-id="5f714-231">0x80180014</span></span>
</dt> <dt>



<span data-ttu-id="5f714-232">Определенная платформа (например, Windows) или версия не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f714-232">A specific platform (e.g. Windows) or version is not supported.</span></span> <span data-ttu-id="5f714-233">Общее исправление этой ошибки — обновление устройства.</span><span class="sxs-lookup"><span data-stu-id="5f714-233">The general fix for this error is to upgrade the device.</span></span>

<span data-ttu-id="5f714-234">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-234">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-235"><span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**МЕНРОЛЛ \_ E \_ NOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="5f714-235"><span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL\_E\_NOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-236">0x80180015</span><span class="sxs-lookup"><span data-stu-id="5f714-236">0x80180015</span></span>
</dt> <dt>



<span data-ttu-id="5f714-237">Обычно управление мобильными устройствами не поддерживается для этого устройства — пользователь может вызвать администратора, но маловероятно, чтобы устранить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="5f714-237">Mobile device management is generally not supported for this device - the user may call the admin, but will be unlikely to resolve this issue.</span></span>

<span data-ttu-id="5f714-238">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-238">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-239"><span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**МРЕГИСТЕР \_ E \_ нотелигиблеторенев**</span><span class="sxs-lookup"><span data-stu-id="5f714-239"><span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER\_E\_NOTELIGIBLETORENEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-240">0x80180016</span><span class="sxs-lookup"><span data-stu-id="5f714-240">0x80180016</span></span>
</dt> <dt>



<span data-ttu-id="5f714-241">Устройство пытается продлить, но сервер отклонил запрос.</span><span class="sxs-lookup"><span data-stu-id="5f714-241">The device is attempting to renew, but the server rejected the request.</span></span> <span data-ttu-id="5f714-242">Проверка времени на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5f714-242">Check time on device.</span></span> <span data-ttu-id="5f714-243">Пользователь может устранить эту ошибку путем повторной регистрации.</span><span class="sxs-lookup"><span data-stu-id="5f714-243">The user may be able to resolve this error by re-enrolling.</span></span>

<span data-ttu-id="5f714-244">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-244">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-245"><span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**МЕНРОЛЛ \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-245"><span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL\_E\_INMAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-246">0x80180017</span><span class="sxs-lookup"><span data-stu-id="5f714-246">0x80180017</span></span>
</dt> <dt>



<span data-ttu-id="5f714-247">Учетная запись находится в состоянии обслуживания; Повторите попытку позже.</span><span class="sxs-lookup"><span data-stu-id="5f714-247">Account is in maintenance; retry later.</span></span> <span data-ttu-id="5f714-248">Пользователь может повторить попытку позже.</span><span class="sxs-lookup"><span data-stu-id="5f714-248">The user can retry later.</span></span> <span data-ttu-id="5f714-249">Однако пользователь может выбрать вызов администратора для определения расписания обслуживания.</span><span class="sxs-lookup"><span data-stu-id="5f714-249">However, the user may choose to call the admin to determine the maintenance schedule.</span></span>

<span data-ttu-id="5f714-250">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-250">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-251"><span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**МЕНРОЛЛ \_ E \_ усерлиценсе**</span><span class="sxs-lookup"><span data-stu-id="5f714-251"><span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL\_E\_USERLICENSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-252">0x80180018</span><span class="sxs-lookup"><span data-stu-id="5f714-252">0x80180018</span></span>
</dt> <dt>



<span data-ttu-id="5f714-253">Лицензия пользователя находится в неисправном состоянии, блокирующем регистрацию. пользователь должен будет вызвать администратор.</span><span class="sxs-lookup"><span data-stu-id="5f714-253">The license of user is in bad state blocking enrollment; the user will need to call the admin.</span></span>

<span data-ttu-id="5f714-254">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-254">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-255"><span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**МЕНРОЛЛ \_ E \_ енроллментдатаинвалид**</span><span class="sxs-lookup"><span data-stu-id="5f714-255"><span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL\_E\_ENROLLMENTDATAINVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-256">0x80180019</span><span class="sxs-lookup"><span data-stu-id="5f714-256">0x80180019</span></span>
</dt> <dt>



<span data-ttu-id="5f714-257">Сервер отклонил данные регистрации. возможно, сервер настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="5f714-257">The server rejected the Enrollment Data; the server may not be configured correctly.</span></span>

<span data-ttu-id="5f714-258">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-258">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-259"><span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**МЕНРОЛЛ \_ E \_ инсекурередирект**</span><span class="sxs-lookup"><span data-stu-id="5f714-259"><span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL\_E\_INSECUREREDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-260">0x8018001A</span><span class="sxs-lookup"><span data-stu-id="5f714-260">0x8018001A</span></span>
</dt> <dt>



<span data-ttu-id="5f714-261">Сервер запросил HTTP, а не HTTPS, но он не был принят.</span><span class="sxs-lookup"><span data-stu-id="5f714-261">The server requested HTTP rather than HTTPS but it was not accepted.</span></span>

<span data-ttu-id="5f714-262">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-262">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-263"><span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ неправильное \_ состояние платформы менролл E**</span><span class="sxs-lookup"><span data-stu-id="5f714-263"><span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**MENROLL\_E\_PLATFORM\_WRONG\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-264">0x8018001B</span><span class="sxs-lookup"><span data-stu-id="5f714-264">0x8018001B</span></span>
</dt> <dt>



<span data-ttu-id="5f714-265">Попытка выполнить недопустимую операцию, например повторная регистрация одного и того же устройства дважды или Отмена регистрации неизвестного устройства.</span><span class="sxs-lookup"><span data-stu-id="5f714-265">An invalid operation was attempted, such trying to enroll the same device twice or unenroll an unknown device.</span></span>

<span data-ttu-id="5f714-266">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-266">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-267"><span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**\_ \_ \_ Ошибка лицензии платформы менролл \_ E**</span><span class="sxs-lookup"><span data-stu-id="5f714-267"><span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**MENROLL\_E\_PLATFORM\_LICENSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-268">0x8018001C</span><span class="sxs-lookup"><span data-stu-id="5f714-268">0x8018001C</span></span>
</dt> <dt>



<span data-ttu-id="5f714-269">Версия Windows, установленная на клиенте, не поддерживает этот тип регистрации.</span><span class="sxs-lookup"><span data-stu-id="5f714-269">The version of Windows installed on the client does not support this enrollment type.</span></span>

<span data-ttu-id="5f714-270">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-270">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-271"><span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**\_ \_ \_ неизвестная \_ Ошибка платформы менролл E**</span><span class="sxs-lookup"><span data-stu-id="5f714-271"><span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**MENROLL\_E\_PLATFORM\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-272">0x8018001D</span><span class="sxs-lookup"><span data-stu-id="5f714-272">0x8018001D</span></span>
</dt> <dt>



<span data-ttu-id="5f714-273">На клиенте произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5f714-273">An unknown error occurred on the client.</span></span>

<span data-ttu-id="5f714-274">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-274">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-275"><span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ цертсторе**</span><span class="sxs-lookup"><span data-stu-id="5f714-275"><span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL\_E\_PROV\_CSP\_CERTSTORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-276">0x8018001E</span><span class="sxs-lookup"><span data-stu-id="5f714-276">0x8018001E</span></span>
</dt> <dt>



<span data-ttu-id="5f714-277">Сбой подготовки в CSP хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5f714-277">Provisioning failed in the certificate store CSP.</span></span>

<span data-ttu-id="5f714-278">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-278">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-279"><span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ W7**</span><span class="sxs-lookup"><span data-stu-id="5f714-279"><span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL\_E\_PROV\_CSP\_W7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-280">0x8018001F</span><span class="sxs-lookup"><span data-stu-id="5f714-280">0x8018001F</span></span>
</dt> <dt>



<span data-ttu-id="5f714-281">Сбой подготовки в W7/Дмакк CPP.</span><span class="sxs-lookup"><span data-stu-id="5f714-281">Provisioning failed in a W7/DMAcc CPP.</span></span>

<span data-ttu-id="5f714-282">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-282">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-283"><span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ DMCLIENT**</span><span class="sxs-lookup"><span data-stu-id="5f714-283"><span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL\_E\_PROV\_CSP\_DMCLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-284">0x80180020</span><span class="sxs-lookup"><span data-stu-id="5f714-284">0x80180020</span></span>
</dt> <dt>



<span data-ttu-id="5f714-285">Сбой подготовки в CSP клиента DM.</span><span class="sxs-lookup"><span data-stu-id="5f714-285">Provisioning failed in a DM client CSP.</span></span>

<span data-ttu-id="5f714-286">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-286">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-287"><span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ пфв**</span><span class="sxs-lookup"><span data-stu-id="5f714-287"><span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL\_E\_PROV\_CSP\_PFW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-288">0x80180021</span><span class="sxs-lookup"><span data-stu-id="5f714-288">0x80180021</span></span>
</dt> <dt>



<span data-ttu-id="5f714-289">Сбой подготовки в CSP для работы Passport for Network.</span><span class="sxs-lookup"><span data-stu-id="5f714-289">Provisioning failed in a Passport for Work CSP.</span></span>

<span data-ttu-id="5f714-290">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-290">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-291"><span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**МЕНРОЛЛ \_ E \_ Prov \_ . \_ Прочее**</span><span class="sxs-lookup"><span data-stu-id="5f714-291"><span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL\_E\_PROV\_CSP\_MISC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-292">0x80180022</span><span class="sxs-lookup"><span data-stu-id="5f714-292">0x80180022</span></span>
</dt> <dt>



<span data-ttu-id="5f714-293">Сбой подготовки в CSP, не указанном выше.</span><span class="sxs-lookup"><span data-stu-id="5f714-293">Provisioning failed in a CSP not listed above.</span></span>

<span data-ttu-id="5f714-294">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-294">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-295"><span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**Неизвестный МЕНРОЛЛ \_ E \_ Prov \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-295"><span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL\_E\_PROV\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-296">0x80180023</span><span class="sxs-lookup"><span data-stu-id="5f714-296">0x80180023</span></span>
</dt> <dt>



<span data-ttu-id="5f714-297">Сбой подготовки, но не указан конкретный CSP.</span><span class="sxs-lookup"><span data-stu-id="5f714-297">Provisioning failed, but a specific CSP is not indicated.</span></span>

<span data-ttu-id="5f714-298">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-298">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-299"><span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**МЕНРОЛЛ \_ E \_ Prov \_ сслцертнотфаунд**</span><span class="sxs-lookup"><span data-stu-id="5f714-299"><span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL\_E\_PROV\_SSLCERTNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-300">0x80180024</span><span class="sxs-lookup"><span data-stu-id="5f714-300">0x80180024</span></span>
</dt> <dt>



<span data-ttu-id="5f714-301">При попытке привязки открытого сертификата или закрытого ключа общедоступный сертификат не был найден: при попытке привязки открытого сертификата или закрытого ключа или при поиске полезных данных подготовки (возможно, нацеленных на неправильное хранилище).</span><span class="sxs-lookup"><span data-stu-id="5f714-301">When attempting to bind the public cert/private key, the public cert was not found either: when attempting to bind the public cert/private key, or when looking into provisioning payload (perhaps targeting the wrong store).</span></span>

<span data-ttu-id="5f714-302">**Windows 8.1:** Эта константа недоступна до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5f714-302">**Windows 8.1:** This constant is not available before Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-303"><span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ аппмгмт**</span><span class="sxs-lookup"><span data-stu-id="5f714-303"><span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL\_E\_PROV\_CSP\_APPMGMT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-304">0x80180025</span><span class="sxs-lookup"><span data-stu-id="5f714-304">0x80180025</span></span>
</dt> <dt>



<span data-ttu-id="5f714-305">Сбой подготовки в CSP Ентерприсеаппманажемент.</span><span class="sxs-lookup"><span data-stu-id="5f714-305">Provisioning failed in the EnterpriseAppManagement CSP.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-306">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-306">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-307"><span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**\_ \_ Управление устройством менролл \_ \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="5f714-307"><span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**MENROLL\_E\_DEVICE\_MANAGEMENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-308">0x80180026</span><span class="sxs-lookup"><span data-stu-id="5f714-308">0x80180026</span></span>
</dt> <dt>



<span data-ttu-id="5f714-309">Управление мобильными устройствами (MDM) было заблокировано, возможно, с помощью групповая политика или функции [**сетманажедекстерналли**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .</span><span class="sxs-lookup"><span data-stu-id="5f714-309">Mobile Device Management (MDM) was blocked, possibly by Group Policy or the [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) function.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-310">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-310">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-311"><span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**\_ \_ \_ сбой приватекэйкреатион цертполици \_ менролл**</span><span class="sxs-lookup"><span data-stu-id="5f714-311"><span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL\_E\_CERTPOLICY\_PRIVATEKEYCREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-312">0x80180027</span><span class="sxs-lookup"><span data-stu-id="5f714-312">0x80180027</span></span>
</dt> <dt>



<span data-ttu-id="5f714-313">Не удалось создать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="5f714-313">Failed to create the private key.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-314">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-314">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-315"><span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**МЕНРОЛЛ \_ E \_ цертаус \_ не \_ удалось \_ найти \_ сертификат**</span><span class="sxs-lookup"><span data-stu-id="5f714-315"><span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL\_E\_CERTAUTH\_FAILED\_TO\_FIND\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-316">0x80180028</span><span class="sxs-lookup"><span data-stu-id="5f714-316">0x80180028</span></span>
</dt> <dt>



<span data-ttu-id="5f714-317">Запрошена проверка подлинности сертификата, но не удалось найти сертификат для использования.</span><span class="sxs-lookup"><span data-stu-id="5f714-317">Certificate Authentication was requested, but failed find a certificate to use.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-318">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-318">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-319"><span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**МЕНРОЛЛ \_ е \_ пустое \_ сообщение**</span><span class="sxs-lookup"><span data-stu-id="5f714-319"><span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL\_E\_EMPTY\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-320">0x80180029</span><span class="sxs-lookup"><span data-stu-id="5f714-320">0x80180029</span></span>
</dt> <dt>



<span data-ttu-id="5f714-321">Сервер ответил HTTP 200, но сообщение было пустым.</span><span class="sxs-lookup"><span data-stu-id="5f714-321">The server responded with HTTP 200, but the message was empty.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-322">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-322">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-323"><span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**\_Отмена менролл \_ пользователем \_**</span><span class="sxs-lookup"><span data-stu-id="5f714-323"><span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL\_E\_USER\_CANCELED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-324">0x80180030</span><span class="sxs-lookup"><span data-stu-id="5f714-324">0x80180030</span></span>
</dt> <dt>



<span data-ttu-id="5f714-325">Пользователь отменил операцию.</span><span class="sxs-lookup"><span data-stu-id="5f714-325">The user canceled the operation.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-326">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-326">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f714-327"><span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**МЕНРОЛЛ \_ . \_ \_ не \_ настроено MDM**</span><span class="sxs-lookup"><span data-stu-id="5f714-327"><span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL\_E\_MDM\_NOT\_CONFIGURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f714-328">0x80180031</span><span class="sxs-lookup"><span data-stu-id="5f714-328">0x80180031</span></span>
</dt> <dt>



<span data-ttu-id="5f714-329">Управление мобильными устройствами (MDM) не настроено.</span><span class="sxs-lookup"><span data-stu-id="5f714-329">Mobile Device Management (MDM) is not configured.</span></span>

> [!Note]  
> <span data-ttu-id="5f714-330">Эта константа недоступна до Windows 10, версия 1709.</span><span class="sxs-lookup"><span data-stu-id="5f714-330">This constant is not available before Windows 10, version 1709.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f714-331">Требования</span><span class="sxs-lookup"><span data-stu-id="5f714-331">Requirements</span></span>

| <span data-ttu-id="5f714-332">Требование</span><span class="sxs-lookup"><span data-stu-id="5f714-332">Requirement</span></span> | <span data-ttu-id="5f714-333">Применение</span><span class="sxs-lookup"><span data-stu-id="5f714-333">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f714-334">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f714-334">Minimum supported client</span></span><br/> | <span data-ttu-id="5f714-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5f714-335">Windows 8.1</span></span><br/>                                                                       |
| <span data-ttu-id="5f714-336">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f714-336">Minimum supported server</span></span><br/> | <span data-ttu-id="5f714-337">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5f714-337">None supported</span></span><br/>                                                                    |
| <span data-ttu-id="5f714-338">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5f714-338">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f714-339"><dt>Мдмрегистратион. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f714-339"><dt>MDMRegistration.h</dt></span></span> </dl> |



 

 





