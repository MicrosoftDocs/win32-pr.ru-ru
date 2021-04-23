---
title: Константы ошибок NAP (WinError. h)
description: Следующие константы ошибок NAP определены в файле WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989151"
---
# <a name="nap-error-constants"></a><span data-ttu-id="b2fc5-103">Константы ошибок NAP</span><span class="sxs-lookup"><span data-stu-id="b2fc5-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="b2fc5-104">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2fc5-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b2fc5-105">Следующие константы ошибок NAP определены в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="b2fc5-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_ \_ Недопустимый \_ пакет NAP E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-107">\_HRESULT \_ TYPEDEF \_ (0x80270001L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-108">Недопустимый пакет [**состояния работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**\_ \_ отсутствует \_ состояние работоспособности NAP E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-110">\_HRESULT \_ TYPEDEF \_ (0x80270002L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-111">В пакете NAP отсутствовало [**состояние работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="b2fc5-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ \_ конфликтующий идентификатор NAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-113">\_HRESULT \_ TYPEDEF \_ (0x80270003L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-114">Идентификатор сущности конфликтует с уже зарегистрированным ИДЕНТИФИКАТОРом сущности.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**Защита доступа к сети \_ E \_ без \_ кэшированного \_ состояния работоспособности**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-116">\_HRESULT \_ TYPEDEF \_ (0x80270004L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-117">Отсутствует кэшированное [**состояние работоспособности**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="b2fc5-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**\_ \_ по-прежнему \_ привязанный к NAP E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-119">\_HRESULT \_ TYPEDEF \_ (0x80270005L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-120">Сущность все еще привязана к системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**Защита доступа к сети \_ E \_ не \_ зарегистрирована**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-122">\_HRESULT \_ TYPEDEF \_ (0x80270006L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-123">Сущность не зарегистрирована в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**Защита доступа к сети \_ E \_ не \_ инициализирована**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-125">\_HRESULT \_ TYPEDEF \_ (0x80270007L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-126">Сущность не инициализирована системой защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ \_ несовпадающий идентификатор NAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-128">\_HRESULT \_ TYPEDEF \_ (0x80270008L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-129">Идентификаторы корреляции в запросе [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) и ответе **SoH** не совпадают.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**Защита доступа к сети \_ E \_ не \_ ожидается**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-131">\_HRESULT \_ TYPEDEF \_ (0x80270009L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-132">Завершение было указано для запроса, который в настоящий момент не находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**Идентификатор защиты доступа к сети ( \_ E) \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-134">\_HRESULT \_ TYPEDEF \_ (0x8027000AL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-135">Идентификатор компонента NAP не найден.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**\_ \_ \_ слишком \_ маленький размер защиты доступа к сети (NAP)**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-137">\_HRESULT \_ TYPEDEF \_ (0x8027000BL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-138">Максимальный размер соединения слишком мал для пакета SoH.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_Служба NAP \_ E \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-140">\_HRESULT \_ TYPEDEF \_ (0x8027000CL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-141">Служба Напажент не запущена.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_сертификат NAP \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-143">\_HRESULT \_ TYPEDEF \_ (0x0027000DL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="b2fc5-144">Сертификат уже существует в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_ \_ отключена сущность NAP E \_**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-146">\_HRESULT \_ TYPEDEF \_ (0x8027000EL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-147">Сущность отключена в службе Напажент.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_ \_ \_ GROUPPOLICY \_ Ошибка Netsh для защиты доступа к сети**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-149">\_HRESULT \_ TYPEDEF \_ (0x8027000FL)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-150">Групповая политика не настроена.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**\_ \_ слишком \_ много вызовов NAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-152">\_HRESULT \_ TYPEDEF \_ (0x80270010L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-153">Слишком много одновременных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**Конфигурация средства защиты доступа к сети (NAP) \_ \_ \_ \_ существовала**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-155">\_HRESULT \_ TYPEDEF \_ (0x80270011L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-156">Конфигурация SHV уже существует.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="b2fc5-157">Поддерживается в Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ не \_ найдена Конфигурация NAP E SHV**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-159">\_HRESULT \_ TYPEDEF \_ (0x80270012L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-160">Конфигурация SHV не найдена.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="b2fc5-161">Поддерживается в Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2fc5-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_ \_ время ожидания SHV для защиты от NAP \_**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fc5-163">\_HRESULT \_ TYPEDEF \_ (0x80270013L)</span><span class="sxs-lookup"><span data-stu-id="b2fc5-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="b2fc5-164">Время ожидания SHV истекло в запросе.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="b2fc5-165">Поддерживается в Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2fc5-166">Требования</span><span class="sxs-lookup"><span data-stu-id="b2fc5-166">Requirements</span></span>



| <span data-ttu-id="b2fc5-167">Требование</span><span class="sxs-lookup"><span data-stu-id="b2fc5-167">Requirement</span></span> | <span data-ttu-id="b2fc5-168">Значение</span><span class="sxs-lookup"><span data-stu-id="b2fc5-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2fc5-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2fc5-169">Minimum supported client</span></span><br/> | <span data-ttu-id="b2fc5-170">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2fc5-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2fc5-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2fc5-171">Minimum supported server</span></span><br/> | <span data-ttu-id="b2fc5-172">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2fc5-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2fc5-173">Header</span><span class="sxs-lookup"><span data-stu-id="b2fc5-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2fc5-174"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2fc5-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2fc5-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2fc5-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2fc5-176">**Константы NAP**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





