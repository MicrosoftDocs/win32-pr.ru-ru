---
description: Описание кодов ошибок 9000-11999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Коды системных ошибок (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807433"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="9cadb-103">Коды системных ошибок (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="9cadb-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="9cadb-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cadb-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="9cadb-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="9cadb-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 9000 – 11999).</span><span class="sxs-lookup"><span data-stu-id="9cadb-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="9cadb-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="9cadb-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="9cadb-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="9cadb-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="9cadb-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**\_Ошибка DNS \_ Ошибка \_ формата \_ ркоде**</span><span class="sxs-lookup"><span data-stu-id="9cadb-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="9cadb-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-111">DNS-серверу не удалось интерпретировать формат.</span><span class="sxs-lookup"><span data-stu-id="9cadb-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**\_Ошибка DNS \_ \_ при ркоде сервера \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-113">9002 (0x232A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-114">Ошибка DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="9cadb-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**Ошибка DNS ошибка \_ \_ \_ имени \_ ркоде**</span><span class="sxs-lookup"><span data-stu-id="9cadb-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-116">9003 (0x232B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-117">DNS-имя не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_Ошибка DNS \_ ркоде \_ не \_ реализована**</span><span class="sxs-lookup"><span data-stu-id="9cadb-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-119">9004 (0x232C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-120">DNS-запрос не поддерживается сервером имен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_Ошибка DNS \_ ркоде \_ отклонена**</span><span class="sxs-lookup"><span data-stu-id="9cadb-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-122">9005 (0x232D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-123">Операция DNS отклонена.</span><span class="sxs-lookup"><span data-stu-id="9cadb-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_Ошибка DNS \_ ркоде \_ иксдомаин**</span><span class="sxs-lookup"><span data-stu-id="9cadb-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-125">9006 (0x232E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-126">Существует несуществующее DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="9cadb-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_Ошибка DNS \_ ркоде \_ иксррсет**</span><span class="sxs-lookup"><span data-stu-id="9cadb-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-128">9007 (0x232F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-129">Существует набор DNS RR, который не должен существовать.</span><span class="sxs-lookup"><span data-stu-id="9cadb-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_Ошибка DNS \_ ркоде \_ нксррсет**</span><span class="sxs-lookup"><span data-stu-id="9cadb-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="9cadb-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-132">Набор RR DNS, который должен существовать, не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_Ошибка DNS \_ ркоде \_ нотаус**</span><span class="sxs-lookup"><span data-stu-id="9cadb-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="9cadb-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-135">DNS-сервер не является полномочным для зоны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_Ошибка DNS \_ ркоде \_ нотзоне**</span><span class="sxs-lookup"><span data-stu-id="9cadb-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="9cadb-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-138">DNS-имя в обновлении или prereq не входит в зону.</span><span class="sxs-lookup"><span data-stu-id="9cadb-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_Ошибка DNS \_ ркоде \_ бадсиг**</span><span class="sxs-lookup"><span data-stu-id="9cadb-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="9cadb-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-141">Не удалось проверить подпись DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_Ошибка DNS \_ ркоде \_ бадкэй**</span><span class="sxs-lookup"><span data-stu-id="9cadb-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="9cadb-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-144">Неверный ключ DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_Ошибка DNS \_ ркоде \_ бадтиме**</span><span class="sxs-lookup"><span data-stu-id="9cadb-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-146">9018 (0x233A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-147">Срок действия подписи DNS истек.</span><span class="sxs-lookup"><span data-stu-id="9cadb-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**\_ \_ требуется КЭЙМАСТЕР ошибка \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-149">9101 (0x238D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-150">Эту операцию могут выполнять только DNS-сервер, выступающий в качестве основного для зоны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_ \_ \_ \_ в \_ подписанной \_ зоне не разрешена ошибка DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-152">9102 (0x238E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-153">Эта операция запрещена для зоны, которая подписана или имеет ключи подписывания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Ошибка DNS \_ NSEC3 \_ несовместима \_ с \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="9cadb-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-155">9103 (0x238F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-156">NSEC3 несовместим с алгоритмом RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="9cadb-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="9cadb-157">Выберите другой алгоритм или используйте NSEC.</span><span class="sxs-lookup"><span data-stu-id="9cadb-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="9cadb-158">Это значение также называлось " **Ошибка DNS". \_ \_ недопустимые \_ \_ Параметры NSEC3**</span><span class="sxs-lookup"><span data-stu-id="9cadb-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_Ошибка DNS \_ - \_ недостаточно \_ \_ \_ дескрипторов ключей подписывания**</span><span class="sxs-lookup"><span data-stu-id="9cadb-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="9cadb-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-161">В зоне недостаточно ключей подписывания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="9cadb-162">Должен существовать хотя бы один ключ подписывания ключа (KSK) и хотя бы один ключ подписывания зоны (ZSK).</span><span class="sxs-lookup"><span data-stu-id="9cadb-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_ \_ неподдерживаемый алгоритм DNS-ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="9cadb-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-165">Указанный алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9cadb-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**Ошибка DNS- \_ \_ Недопустимый \_ \_ Размер ключа**</span><span class="sxs-lookup"><span data-stu-id="9cadb-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="9cadb-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-168">Указанный размер ключа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9cadb-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_ \_ ключ подписывания ошибки DNS \_ \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="9cadb-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="9cadb-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-171">Один или несколько ключей подписывания для зоны недоступны для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="9cadb-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="9cadb-172">Подписывание зоны не будет работать до устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cadb-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_KSP об ошибках DNS не \_ \_ \_ \_ поддерживает \_ защиту**</span><span class="sxs-lookup"><span data-stu-id="9cadb-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="9cadb-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-175">Указанный поставщик хранилища ключей не поддерживает DPAPI + + Data Protection.</span><span class="sxs-lookup"><span data-stu-id="9cadb-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="9cadb-176">Подписывание зоны не будет работать до устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cadb-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**Ошибка DNS, \_ \_ непредвиденная ошибка \_ \_ защиты данных \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="9cadb-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-179">Обнаружена непредвиденная ошибка DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="9cadb-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="9cadb-180">Подписывание зоны не будет работать до устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cadb-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**\_Ошибка DNS \_ непредвиденная \_ \_ Ошибка CNG**</span><span class="sxs-lookup"><span data-stu-id="9cadb-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="9cadb-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-183">Обнаружена непредвиденная ошибка шифрования.</span><span class="sxs-lookup"><span data-stu-id="9cadb-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="9cadb-184">Подписывание зоны может не работать, пока эта ошибка не будет устранена.</span><span class="sxs-lookup"><span data-stu-id="9cadb-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**Ошибка DNS — \_ \_ неизвестная \_ \_ версия параметра подписи \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="9cadb-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-187">DNS-сервер обнаружил ключ подписывания неизвестной версии.</span><span class="sxs-lookup"><span data-stu-id="9cadb-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="9cadb-188">Подписывание зоны не будет работать до устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cadb-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP ошибок \_ DNS \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="9cadb-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="9cadb-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-191">Указанный поставщик службы ключей не может быть открыт DNS-сервером.</span><span class="sxs-lookup"><span data-stu-id="9cadb-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_Ошибка DNS \_ слишком \_ много \_ скдс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="9cadb-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-194">DNS-сервер не может принимать дополнительные ключи подписывания с указанным алгоритмом и значением флага KSK для этой зоны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**Ошибка DNS. \_ \_ Недопустимый \_ \_ период переключения**</span><span class="sxs-lookup"><span data-stu-id="9cadb-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-196">9114 (0x239A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-197">Указан недопустимый период переключения.</span><span class="sxs-lookup"><span data-stu-id="9cadb-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**\_Ошибка DNS \_ недопустимое \_ \_ смещение начального переключения \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-199">9115 (0x239B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-200">Указано недопустимое начальное смещение смены ключа.</span><span class="sxs-lookup"><span data-stu-id="9cadb-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ \_ идет смена \_ состояния ошибки DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-202">9116 (0x239C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-203">Указанный ключ подписывания уже находится в процессе последовательного перебора ключей.</span><span class="sxs-lookup"><span data-stu-id="9cadb-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_ \_ \_ отсутствует ключ резервного режима ожидания \_ \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-205">9117 (0x239D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-206">Указанный ключ подписывания не имеет резервного ключа для отмены.</span><span class="sxs-lookup"><span data-stu-id="9cadb-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_Ошибка DNS \_ не \_ разрешена \_ для \_ ZSK**</span><span class="sxs-lookup"><span data-stu-id="9cadb-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-208">9118 (0x239E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-209">Эта операция запрещена для ключа подписывания зоны (ZSK).</span><span class="sxs-lookup"><span data-stu-id="9cadb-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_Ошибка DNS \_ не \_ разрешена \_ для \_ активного \_ SKD**</span><span class="sxs-lookup"><span data-stu-id="9cadb-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-211">9119 (0x239F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-212">Эта операция запрещена для активного ключа подписывания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_Смена ошибок \_ DNS \_ уже \_ поставлена в очередь**</span><span class="sxs-lookup"><span data-stu-id="9cadb-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-214">9120 (0x23A0)</span><span class="sxs-lookup"><span data-stu-id="9cadb-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-215">Указанный ключ подписывания уже помещен в очередь для продолжения.</span><span class="sxs-lookup"><span data-stu-id="9cadb-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_Ошибка DNS \_ не \_ разрешена \_ в \_ неподписанной \_ зоне**</span><span class="sxs-lookup"><span data-stu-id="9cadb-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-217">9121 (0x23A1)</span><span class="sxs-lookup"><span data-stu-id="9cadb-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-218">Эта операция запрещена для неподписанной зоны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_Ошибка DNS при \_ неправильном \_ кэймастер**</span><span class="sxs-lookup"><span data-stu-id="9cadb-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-220">9122 (0x23A2)</span><span class="sxs-lookup"><span data-stu-id="9cadb-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-221">Не удалось выполнить эту операцию, так как DNS-сервер, указанный в качестве текущего мастера ключей для этой зоны, отключен или неправильно настроен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="9cadb-222">Устраните проблему в текущем мастере ключей для этой зоны или используйте другой DNS-сервер для присвоения роли мастера ключей.</span><span class="sxs-lookup"><span data-stu-id="9cadb-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**\_Ошибка DNS \_ . \_ \_ срок действия \_ подписи недопустим**</span><span class="sxs-lookup"><span data-stu-id="9cadb-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-224">9123 (0x23A3)</span><span class="sxs-lookup"><span data-stu-id="9cadb-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-225">Указанный период действия подписи недопустим.</span><span class="sxs-lookup"><span data-stu-id="9cadb-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Ошибка DNS при \_ недопустимом \_ \_ числе итераций NSEC3 \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-227">9124 (0x23A4)</span><span class="sxs-lookup"><span data-stu-id="9cadb-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-228">Указанное число итераций NSEC3 выше, чем разрешено минимальной длиной ключа, используемой в зоне.</span><span class="sxs-lookup"><span data-stu-id="9cadb-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**\_Ошибка DNS \_ DNSSEC \_ \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="9cadb-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-230">9125 (0x23A5)</span><span class="sxs-lookup"><span data-stu-id="9cadb-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-231">Не удалось выполнить эту операцию, так как DNS-сервер настроен с отключенными функциями DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="9cadb-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="9cadb-232">Включите DNSSEC на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="9cadb-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ Недопустимый \_ XML-код ошибки DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-234">9126 (0x23A6)</span><span class="sxs-lookup"><span data-stu-id="9cadb-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-235">Не удалось выполнить эту операцию, так как полученный XML-поток пуст или является синтаксически недопустимым.</span><span class="sxs-lookup"><span data-stu-id="9cadb-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**Ошибка DNS — \_ \_ нет \_ допустимых \_ \_ якорей доверия**</span><span class="sxs-lookup"><span data-stu-id="9cadb-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-237">9127 (0x23A7)</span><span class="sxs-lookup"><span data-stu-id="9cadb-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-238">Эта операция завершена, но не были добавлены якоря доверия, так как все полученные якоря доверия были недопустимыми, не поддерживаются, истек срок действия или не станут действительными менее чем за 30 дней.</span><span class="sxs-lookup"><span data-stu-id="9cadb-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_не удается \_ прокрутить смену ошибок \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-240">9128 (0x23A8)</span><span class="sxs-lookup"><span data-stu-id="9cadb-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-241">Указанный ключ подписывания не ожидает обновления родительского DS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_Ошибка DNS \_ при \_ \_ конфликте имен NSEC3**</span><span class="sxs-lookup"><span data-stu-id="9cadb-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-243">9129 (0x23A9)</span><span class="sxs-lookup"><span data-stu-id="9cadb-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-244">При подписывании NSEC3 обнаружен конфликт хэша.</span><span class="sxs-lookup"><span data-stu-id="9cadb-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="9cadb-245">Укажите другую пользовательскую соль или используйте соль, сгенерированную случайным образом, и повторите попытку подписи зоны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Ошибка DNS \_ NSEC \_ несовместима \_ с \_ NSEC3 \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="9cadb-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-247">9130 (0x23AA)</span><span class="sxs-lookup"><span data-stu-id="9cadb-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-248">NSEC не совместима с алгоритмом NSEC3-RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="9cadb-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="9cadb-249">Выберите другой алгоритм или используйте NSEC3.</span><span class="sxs-lookup"><span data-stu-id="9cadb-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_сведения об DNS \_ нет \_ записей**</span><span class="sxs-lookup"><span data-stu-id="9cadb-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-251">9501 (0x251D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-252">Для данного запроса записей в DNS не найдено.</span><span class="sxs-lookup"><span data-stu-id="9cadb-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**Ошибка DNS — \_ \_ неправильный \_ пакет**</span><span class="sxs-lookup"><span data-stu-id="9cadb-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-254">9502 (0x251E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-255">Неверный пакет DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**Ошибка DNS — \_ \_ нет \_ пакета**</span><span class="sxs-lookup"><span data-stu-id="9cadb-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-257">9503 (0x251F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-258">Нет пакета DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_Ошибка DNS \_ ркоде**</span><span class="sxs-lookup"><span data-stu-id="9cadb-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="9cadb-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-261">Ошибка DNS, проверьте ркоде.</span><span class="sxs-lookup"><span data-stu-id="9cadb-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**\_Ошибка DNS при \_ небезопасном \_ пакете**</span><span class="sxs-lookup"><span data-stu-id="9cadb-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="9cadb-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-264">Незащищенный пакет DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_ \_ Ожидание запроса DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="9cadb-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-267">Запрос DNS-запроса ожидает выполнения.</span><span class="sxs-lookup"><span data-stu-id="9cadb-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**Ошибка DNS — \_ \_ Недопустимый \_ тип**</span><span class="sxs-lookup"><span data-stu-id="9cadb-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-269">9551 (0x254F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-270">Недопустимый тип DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_Ошибка DNS при \_ неправильном \_ IP- \_ адресе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="9cadb-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-273">Недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9cadb-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**Ошибка DNS — \_ \_ недопустимое \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="9cadb-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="9cadb-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-276">Недопустимое свойство.</span><span class="sxs-lookup"><span data-stu-id="9cadb-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**Ошибка DNS повторите попытку \_ \_ \_ \_ позже**</span><span class="sxs-lookup"><span data-stu-id="9cadb-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="9cadb-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-279">Повторите операцию DNS позже.</span><span class="sxs-lookup"><span data-stu-id="9cadb-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_Ошибка DNS \_ не является \_ уникальной**</span><span class="sxs-lookup"><span data-stu-id="9cadb-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="9cadb-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-282">Запись для заданного имени и типа не является уникальной.</span><span class="sxs-lookup"><span data-stu-id="9cadb-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**Ошибка DNS, \_ \_ не относящаяся к \_ \_ имени RFC**</span><span class="sxs-lookup"><span data-stu-id="9cadb-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="9cadb-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-285">DNS-имя не соответствует спецификациям RFC.</span><span class="sxs-lookup"><span data-stu-id="9cadb-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_ \_ полное доменное имя состояния DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="9cadb-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-288">DNS-имя — это полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="9cadb-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**состояние DNS — \_ \_ точечное \_ имя**</span><span class="sxs-lookup"><span data-stu-id="9cadb-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="9cadb-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-291">DNS-имя имеет несколько точек (с несколькими метками).</span><span class="sxs-lookup"><span data-stu-id="9cadb-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_ \_ \_ имя одной части \_ состояния DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="9cadb-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-294">DNS-имя — это однокомпонентное имя.</span><span class="sxs-lookup"><span data-stu-id="9cadb-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_Ошибка DNS \_ недопустимое \_ имя \_ char**</span><span class="sxs-lookup"><span data-stu-id="9cadb-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="9cadb-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-297">DNS-имя содержит недопустимый символ.</span><span class="sxs-lookup"><span data-stu-id="9cadb-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ числовое имя ошибки DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="9cadb-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-300">DNS-имя является полностью числовым.</span><span class="sxs-lookup"><span data-stu-id="9cadb-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_Ошибка DNS \_ не \_ разрешена \_ на \_ корневом \_ сервере**</span><span class="sxs-lookup"><span data-stu-id="9cadb-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-302">9562 (0x255A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-303">Запрошенная операция запрещена на корневом сервере DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_ \_ \_ \_ в делегировании не разрешена ошибка \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-305">9563 (0x255B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-306">Не удалось создать запись, так как эта часть пространства имен DNS делегирована другому серверу.</span><span class="sxs-lookup"><span data-stu-id="9cadb-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_Ошибка DNS \_ не удается \_ найти \_ корневые \_ ссылки**</span><span class="sxs-lookup"><span data-stu-id="9cadb-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-308">9564 (0x255C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-309">DNS-серверу не удалось найти набор корневых ссылок.</span><span class="sxs-lookup"><span data-stu-id="9cadb-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_Ошибка DNS при \_ несоответствии \_ корневых \_ ссылок**</span><span class="sxs-lookup"><span data-stu-id="9cadb-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-311">9565 (0x255D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-312">DNS-сервер обнаружил корневые ссылки, но они не были согласованы во всех адаптерах.</span><span class="sxs-lookup"><span data-stu-id="9cadb-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_Ошибка DNS \_ \_ \_ слишком \_ малое значение DWORD**</span><span class="sxs-lookup"><span data-stu-id="9cadb-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-314">9566 (0x255E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-315">Указанное значение слишком мало для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="9cadb-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_Ошибка DNS \_ \_ \_ слишком большая величина DWORD \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-317">9567 (0x255F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-318">Указанное значение слишком велико для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="9cadb-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ Фоновая загрузка ошибок DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="9cadb-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-321">Эта операция запрещена, пока DNS-сервер загружает зоны в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9cadb-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="9cadb-322">Повторите попытку позже.</span><span class="sxs-lookup"><span data-stu-id="9cadb-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_Ошибка DNS \_ не \_ разрешена \_ на \_ RODC**</span><span class="sxs-lookup"><span data-stu-id="9cadb-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="9cadb-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-325">Запрошенная операция запрещена для DNS-сервера, работающего на контроллере домена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9cadb-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_ \_ \_ \_ в Dname не разрешена ошибка DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="9cadb-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-328">Под записью DNAME не может быть данных.</span><span class="sxs-lookup"><span data-stu-id="9cadb-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_ \_ требуется делегирование ошибок DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="9cadb-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-331">Для этой операции требуется делегирование учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9cadb-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_Ошибка DNS при \_ неверной \_ \_ таблице политики**</span><span class="sxs-lookup"><span data-stu-id="9cadb-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="9cadb-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-334">Таблица политики разрешения имен повреждена.</span><span class="sxs-lookup"><span data-stu-id="9cadb-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="9cadb-335">Разрешение DNS завершится сбоем, пока оно не будет устранено.</span><span class="sxs-lookup"><span data-stu-id="9cadb-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="9cadb-336">Обратитесь к сетевому администратору.</span><span class="sxs-lookup"><span data-stu-id="9cadb-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_зона ошибок \_ DNS \_ \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="9cadb-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-339">Зона DNS не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**Ошибка DNS — \_ \_ нет \_ \_ сведений о зоне**</span><span class="sxs-lookup"><span data-stu-id="9cadb-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="9cadb-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-342">Сведения о зоне DNS недоступны.</span><span class="sxs-lookup"><span data-stu-id="9cadb-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_Ошибка DNS \_ при \_ \_ выполнении операции с зоной**</span><span class="sxs-lookup"><span data-stu-id="9cadb-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="9cadb-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-345">Недопустимая операция для зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_ \_ \_ Ошибка конфигурации зоны ошибок \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="9cadb-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-348">Недопустимая конфигурация зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**\_зона ошибок \_ DNS \_ \_ не имеет \_ \_ записи SOA**</span><span class="sxs-lookup"><span data-stu-id="9cadb-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="9cadb-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-351">В зоне DNS отсутствует начальная запись зоны (SOA).</span><span class="sxs-lookup"><span data-stu-id="9cadb-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**в \_ \_ зоне ошибок \_ DNS \_ нет \_ \_ записей NS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="9cadb-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-354">В зоне DNS нет записи сервера имен (NS).</span><span class="sxs-lookup"><span data-stu-id="9cadb-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_зона ошибок \_ DNS \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="9cadb-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="9cadb-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-357">Зона DNS заблокирована.</span><span class="sxs-lookup"><span data-stu-id="9cadb-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ не удалось создать зону ошибок DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="9cadb-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-360">Не удалось создать зону DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**\_зона ошибок \_ DNS \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="9cadb-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-363">Зона DNS уже существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**автозона "ошибка DNS" \_ \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-365">9610 (0x258A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-366">Автоматическая зона DNS уже существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**Ошибка DNS — \_ \_ Недопустимый \_ \_ тип зоны**</span><span class="sxs-lookup"><span data-stu-id="9cadb-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-368">9611 (0x258B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-369">Недопустимый тип зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**во \_ вторичной ошибке DNS \_ \_ требуется \_ главный \_ IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="9cadb-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-371">9612 (0x258C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-372">Для дополнительной зоны DNS требуется главный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9cadb-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_зона ошибок \_ DNS \_ не является \_ вторичной**</span><span class="sxs-lookup"><span data-stu-id="9cadb-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-374">9613 (0x258D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-375">Зона DNS не является вторичной.</span><span class="sxs-lookup"><span data-stu-id="9cadb-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**\_при ошибке DNS \_ требуются \_ Дополнительные \_ адреса**</span><span class="sxs-lookup"><span data-stu-id="9cadb-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-377">9614 (0x258E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-378">Требуется дополнительный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9cadb-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_Ошибка DNS \_ \_ при инициализации \_ WINS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-380">9615 (0x258F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-381">Сбой инициализации WINS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**\_Ошибка DNS при \_ необходимости \_ WINS- \_ серверов**</span><span class="sxs-lookup"><span data-stu-id="9cadb-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="9cadb-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-384">Требуются WINS-серверы.</span><span class="sxs-lookup"><span data-stu-id="9cadb-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_Ошибка DNS \_ \_ при инициализации \_ NBSTAT**</span><span class="sxs-lookup"><span data-stu-id="9cadb-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="9cadb-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-387">Не удалось вызвать инициализацию NBTSTAT.</span><span class="sxs-lookup"><span data-stu-id="9cadb-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_Ошибка DNS \_ при \_ удалении \_ SOA**</span><span class="sxs-lookup"><span data-stu-id="9cadb-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="9cadb-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-390">Недопустимое удаление начальной записи зоны (SOA).</span><span class="sxs-lookup"><span data-stu-id="9cadb-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**\_ \_ сервер пересылки ошибок DNS \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="9cadb-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-393">Для этого имени уже существует условная зона перенаправления.</span><span class="sxs-lookup"><span data-stu-id="9cadb-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**для \_ зоны ошибок DNS \_ \_ требуется \_ главный \_ IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="9cadb-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="9cadb-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-396">Для этой зоны необходимо настроить один или несколько IP-адресов главного DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="9cadb-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**\_зона ошибок \_ DNS \_ \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="9cadb-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="9cadb-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-399">Невозможно выполнить операцию, так как эта зона выключена.</span><span class="sxs-lookup"><span data-stu-id="9cadb-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_зона ошибок \_ DNS \_ заблокирована \_ для \_ подписывания**</span><span class="sxs-lookup"><span data-stu-id="9cadb-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="9cadb-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-402">Невозможно выполнить эту операцию, так как зона подписана в данный момент.</span><span class="sxs-lookup"><span data-stu-id="9cadb-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="9cadb-403">Повторите попытку позже.</span><span class="sxs-lookup"><span data-stu-id="9cadb-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**для \_ основной ошибки DNS \_ \_ требуется \_ файл данных**</span><span class="sxs-lookup"><span data-stu-id="9cadb-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-405">9651 (0x25B3)</span><span class="sxs-lookup"><span data-stu-id="9cadb-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-406">Основной зоне DNS требуется файл данных.</span><span class="sxs-lookup"><span data-stu-id="9cadb-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_Ошибка DNS при \_ недопустимом \_ \_ имени файла**</span><span class="sxs-lookup"><span data-stu-id="9cadb-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-408">9652 (0x25B4)</span><span class="sxs-lookup"><span data-stu-id="9cadb-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-409">Недопустимое имя файла в зоне DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_Ошибка \_ \_ при открытии файла ошибок \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-411">9653 (0x25B5)</span><span class="sxs-lookup"><span data-stu-id="9cadb-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-412">Не удалось открыть файл для зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_ \_ \_ сбой обратной записи в файл ошибок DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-414">9654 (0x25B6)</span><span class="sxs-lookup"><span data-stu-id="9cadb-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-415">Не удалось записать файл в зону DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**\_ \_ \_ синтаксический анализ файла ошибок DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-417">9655 (0x25B7)</span><span class="sxs-lookup"><span data-stu-id="9cadb-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-418">Ошибка при чтении файла подзоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_запись об ошибке DNS \_ \_ \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-420">9701 (0x25E5)</span><span class="sxs-lookup"><span data-stu-id="9cadb-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-421">Запись DNS не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_ \_ Формат записи ошибок \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-423">9702 (0x25E6)</span><span class="sxs-lookup"><span data-stu-id="9cadb-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-424">Ошибка формата записи DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ не удалось создать узел ошибки DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-426">9703 (0x25E7)</span><span class="sxs-lookup"><span data-stu-id="9cadb-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-427">Сбой создания узла в DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**Ошибка DNS — \_ \_ неизвестный \_ \_ тип записи**</span><span class="sxs-lookup"><span data-stu-id="9cadb-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-429">9704 (0x25E8)</span><span class="sxs-lookup"><span data-stu-id="9cadb-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-430">Неизвестный тип записи DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**\_ \_ \_ истекло время ожидания записи об ошибке DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-432">9705 (0x25E9)</span><span class="sxs-lookup"><span data-stu-id="9cadb-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-433">Истекло время ожидания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_имя ошибки \_ DNS \_ не \_ в \_ зоне**</span><span class="sxs-lookup"><span data-stu-id="9cadb-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-435">9706 (0x25EA)</span><span class="sxs-lookup"><span data-stu-id="9cadb-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-436">Имя не входит в зону DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_Ошибка DNS \_ \_ циклическая запись CNAME**</span><span class="sxs-lookup"><span data-stu-id="9cadb-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-438">9707 (0x25EB)</span><span class="sxs-lookup"><span data-stu-id="9cadb-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-439">Обнаружен цикл CNAME.</span><span class="sxs-lookup"><span data-stu-id="9cadb-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**\_узел ошибки \_ DNS \_ — \_ запись CNAME**</span><span class="sxs-lookup"><span data-stu-id="9cadb-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-441">9708 (0x25EC)</span><span class="sxs-lookup"><span data-stu-id="9cadb-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-442">Узел является записью CNAME DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_Ошибка DNS \_ при \_ конфликте CNAME**</span><span class="sxs-lookup"><span data-stu-id="9cadb-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-444">9709 (0x25ED)</span><span class="sxs-lookup"><span data-stu-id="9cadb-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-445">Запись CNAME уже существует для указанного имени.</span><span class="sxs-lookup"><span data-stu-id="9cadb-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_запись ошибок \_ DNS \_ только \_ в \_ \_ корне зоны**</span><span class="sxs-lookup"><span data-stu-id="9cadb-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-447">9710 (0x25EE)</span><span class="sxs-lookup"><span data-stu-id="9cadb-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-448">Запись только в корне зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**\_запись об ошибке DNS \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-450">9711 (0x25EF)</span><span class="sxs-lookup"><span data-stu-id="9cadb-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-451">Запись DNS уже существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ Дополнительные данные об ОШИБКАх DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-453">9712 (0x25F0)</span><span class="sxs-lookup"><span data-stu-id="9cadb-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-454">Ошибка данных дополнительной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**Ошибка DNS — \_ \_ нет \_ данных о создании \_ кэша \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-456">9713 (0x25F1)</span><span class="sxs-lookup"><span data-stu-id="9cadb-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-457">Не удалось создать данные кэша DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_имя ошибки \_ DNS \_ \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-459">9714 (0x25F2)</span><span class="sxs-lookup"><span data-stu-id="9cadb-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-460">DNS-имя не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_предупреждение DNS \_ \_ при создании \_ ошибки PTR**</span><span class="sxs-lookup"><span data-stu-id="9cadb-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-462">9715 (0x25F3)</span><span class="sxs-lookup"><span data-stu-id="9cadb-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-463">Не удалось создать запись указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="9cadb-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS-предупреждение о том, что \_ \_ домен не \_ удален**</span><span class="sxs-lookup"><span data-stu-id="9cadb-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-465">9716 (0x25F4)</span><span class="sxs-lookup"><span data-stu-id="9cadb-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-466">Домен DNS был удален.</span><span class="sxs-lookup"><span data-stu-id="9cadb-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_ \_ недоступная Служба каталогов DS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-468">9717 (0x25F5)</span><span class="sxs-lookup"><span data-stu-id="9cadb-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-469">Служба каталогов недоступна.</span><span class="sxs-lookup"><span data-stu-id="9cadb-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**\_зона DS с ошибками DNS \_ \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-471">9718 (0x25F6)</span><span class="sxs-lookup"><span data-stu-id="9cadb-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-472">Зона DNS уже существует в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_Ошибка DNS \_ нет \_ бутфиле \_ , \_ Если \_ зона DS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-474">9719 (0x25F7)</span><span class="sxs-lookup"><span data-stu-id="9cadb-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-475">DNS-сервер не создает или не считывает файл загрузки для зоны DNS, интегрированной со службой каталогов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**\_узел ошибки \_ DNS \_ — \_ Dname**</span><span class="sxs-lookup"><span data-stu-id="9cadb-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-477">9720 (0x25F8)</span><span class="sxs-lookup"><span data-stu-id="9cadb-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-478">Узел — это запись DNS DNAME.</span><span class="sxs-lookup"><span data-stu-id="9cadb-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_конфликт Dname с ошибками DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-480">9721 (0x25F9)</span><span class="sxs-lookup"><span data-stu-id="9cadb-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-481">Запись DNAME уже существует для данного имени.</span><span class="sxs-lookup"><span data-stu-id="9cadb-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_ \_ цикл псевдонима ошибок DNS \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-483">9722 (0x25FA)</span><span class="sxs-lookup"><span data-stu-id="9cadb-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-484">Обнаружена петля псевдонимов с записями CNAME или DNAME.</span><span class="sxs-lookup"><span data-stu-id="9cadb-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_сведения DNS \_ AXFR \_ завершены**</span><span class="sxs-lookup"><span data-stu-id="9cadb-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="9cadb-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-487">Завершение DNS AXFR (зонная отправка).</span><span class="sxs-lookup"><span data-stu-id="9cadb-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_Ошибка DNS \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="9cadb-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="9cadb-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-490">Сбой при переносе зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**\_сведения о DNS \_ добавлены \_ Локальная \_ Служба WINS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="9cadb-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-493">Добавлен локальный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="9cadb-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_ \_ требуется продолжить состояние \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="9cadb-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-496">Вызов безопасного обновления должен продолжать запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="9cadb-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_Ошибка DNS \_ отсутствует \_ TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9cadb-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-498">9851 (0x267B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-499">Сетевой протокол TCP/IP не установлен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**Ошибка DNS — \_ \_ нет \_ DNS- \_ серверов**</span><span class="sxs-lookup"><span data-stu-id="9cadb-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-501">9852 (0x267C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-502">Нет DNS-серверов, настроенных для локальной системы.</span><span class="sxs-lookup"><span data-stu-id="9cadb-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_ \_ точка распространения ошибок \_ DNS \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-504">9901 (0x26AD)</span><span class="sxs-lookup"><span data-stu-id="9cadb-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-505">Указанный раздел каталога не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**\_точка распространения с ошибкой DNS \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="9cadb-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-507">9902 (0x26AE)</span><span class="sxs-lookup"><span data-stu-id="9cadb-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-508">Указанный раздел каталога уже существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_ \_ точка распространения ошибок DNS \_ не \_ прикреплена**</span><span class="sxs-lookup"><span data-stu-id="9cadb-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-510">9903 (0x26AF)</span><span class="sxs-lookup"><span data-stu-id="9cadb-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-511">Этот DNS-сервер не прикреплен к указанному разделу каталога.</span><span class="sxs-lookup"><span data-stu-id="9cadb-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_ \_ точка распространения ошибок DNS \_ уже \_ прикреплена**</span><span class="sxs-lookup"><span data-stu-id="9cadb-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-513">9904 (0x26B0)</span><span class="sxs-lookup"><span data-stu-id="9cadb-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-514">Этот DNS-сервер уже прикреплен к указанному разделу каталога.</span><span class="sxs-lookup"><span data-stu-id="9cadb-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_Ошибка " \_ точка распространения DNS \_ \_ недоступна"**</span><span class="sxs-lookup"><span data-stu-id="9cadb-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-516">9905 (0x26B1)</span><span class="sxs-lookup"><span data-stu-id="9cadb-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-517">Раздел каталога недоступен в данный момент.</span><span class="sxs-lookup"><span data-stu-id="9cadb-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="9cadb-518">Подождите несколько минут и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="9cadb-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**Ошибка DNS при возникновении ошибки \_ \_ DP \_ FSMO \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-520">9906 (0x26B2)</span><span class="sxs-lookup"><span data-stu-id="9cadb-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-521">Не удалось выполнить операцию, так как не удалось связаться с ролью FSMO хозяина именования доменов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="9cadb-522">Контроллер домена, на котором находится роль FSMO хозяина именования доменов, не работает или не может обслуживать запрос либо не работает под Windows Server 2003 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9cadb-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="9cadb-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="9cadb-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-525">Операция блокировки была прервана вызовом Всаканцелблоккингкалл.</span><span class="sxs-lookup"><span data-stu-id="9cadb-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**всаебадф**</span><span class="sxs-lookup"><span data-stu-id="9cadb-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="9cadb-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-528">Указан недопустимый файловый обработчик.</span><span class="sxs-lookup"><span data-stu-id="9cadb-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**всаеакцес**</span><span class="sxs-lookup"><span data-stu-id="9cadb-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-530">10013 (0x271D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-531">Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="9cadb-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**всаефаулт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-533">10014 (0x271E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-534">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="9cadb-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="9cadb-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="9cadb-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-537">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="9cadb-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**всаемфиле**</span><span class="sxs-lookup"><span data-stu-id="9cadb-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="9cadb-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-540">Слишком много открытых сокетов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**всаеваулдблокк**</span><span class="sxs-lookup"><span data-stu-id="9cadb-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="9cadb-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-543">Не удалось немедленно завершить операцию неблокирующего сокета.</span><span class="sxs-lookup"><span data-stu-id="9cadb-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="9cadb-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-546">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="9cadb-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**всаеалреади**</span><span class="sxs-lookup"><span data-stu-id="9cadb-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="9cadb-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-549">Была предпринята попытка выполнить операцию на неблокируемом сокете, на котором уже выполнялась операция.</span><span class="sxs-lookup"><span data-stu-id="9cadb-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="9cadb-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="9cadb-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-552">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="9cadb-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**всаедестаддррек**</span><span class="sxs-lookup"><span data-stu-id="9cadb-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="9cadb-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-555">В операции на сокете пропущен требуемый адрес.</span><span class="sxs-lookup"><span data-stu-id="9cadb-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**всаемсгсизе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="9cadb-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-558">Сообщение, отправленное на сокет датаграммы, превысило размер внутреннего буфера сообщений или другое ограничение сети, или буфер, используемый для получения датаграммы, меньше, чем сама датаграмма.</span><span class="sxs-lookup"><span data-stu-id="9cadb-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**всаепрототипе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="9cadb-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-561">В вызове функции сокета указан протокол, не поддерживающий семантику запрошенного типа сокета.</span><span class="sxs-lookup"><span data-stu-id="9cadb-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-563">10042 (0x273A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-564">В вызове жетсоккопт или сетсоккопт был указан неизвестный, недопустимый или неподдерживаемый параметр или уровень.</span><span class="sxs-lookup"><span data-stu-id="9cadb-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**всаепротоносуппорт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-566">10043 (0x273B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-567">Запрошенный протокол не был настроен в системе или для него не существует реализации.</span><span class="sxs-lookup"><span data-stu-id="9cadb-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**всаесокктносуппорт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-569">10044 (0x273C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-570">Указанный тип сокета не поддерживается в данном семействе адресов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="9cadb-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-572">10045 (0x273D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-573">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="9cadb-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**всаепфносуппорт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-575">10046 (0x273E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-576">Семейство протоколов не было настроено в системе или не существует реализации для него.</span><span class="sxs-lookup"><span data-stu-id="9cadb-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**всаеафносуппорт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-578">10047 (0x273F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-579">Использован адрес, несовместимый с запрошенным протоколом.</span><span class="sxs-lookup"><span data-stu-id="9cadb-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**всаеаддринусе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="9cadb-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-582">обычно разрешено только одно использование каждого адреса сокета (протокол/сетевой адрес/порт).</span><span class="sxs-lookup"><span data-stu-id="9cadb-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**всаеаддрнотаваил**</span><span class="sxs-lookup"><span data-stu-id="9cadb-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="9cadb-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-585">Запрошенный адрес недопустим в своем контексте.</span><span class="sxs-lookup"><span data-stu-id="9cadb-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**всаенетдовн**</span><span class="sxs-lookup"><span data-stu-id="9cadb-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="9cadb-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-588">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="9cadb-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**всаенетунреач**</span><span class="sxs-lookup"><span data-stu-id="9cadb-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="9cadb-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-591">Операция сокета была предпринята к недостижимой сети.</span><span class="sxs-lookup"><span data-stu-id="9cadb-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**всаенетресет**</span><span class="sxs-lookup"><span data-stu-id="9cadb-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="9cadb-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-594">Соединение разорвано из-за того, что операция проверки активности обнаруживает сбой во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9cadb-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**всаеконнабортед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="9cadb-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-597">Установленное подключение прервано программой на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="9cadb-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**всаеконнресет**</span><span class="sxs-lookup"><span data-stu-id="9cadb-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="9cadb-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-600">существующее соединение было принудительно завершено удаленным узлом.</span><span class="sxs-lookup"><span data-stu-id="9cadb-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**всаенобуфс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="9cadb-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-603">Не удалось выполнить операцию с сокетом, так как в системе недостаточно места в буфере или из-за переполнения очереди.</span><span class="sxs-lookup"><span data-stu-id="9cadb-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**всаеисконн**</span><span class="sxs-lookup"><span data-stu-id="9cadb-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="9cadb-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-606">Запрос на подключение был сделан на уже подключенном сокете.</span><span class="sxs-lookup"><span data-stu-id="9cadb-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**всаенотконн**</span><span class="sxs-lookup"><span data-stu-id="9cadb-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="9cadb-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-609">Запрос на отправку или получение данных отклонен, так как сокет не подключен и (при отправке по сокету датаграмм через вызов sendto) не указан адрес.</span><span class="sxs-lookup"><span data-stu-id="9cadb-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**всаешутдовн**</span><span class="sxs-lookup"><span data-stu-id="9cadb-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-611">10058 (0x274A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-612">Запрос на отправку или получение данных запрещен, так как сокет уже завершил работу в этом направлении по предыдущему запросу на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9cadb-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**всаетуманирефс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-614">10059 (0x274B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-615">Слишком много ссылок на некоторый объект ядра.</span><span class="sxs-lookup"><span data-stu-id="9cadb-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**всаетимедаут**</span><span class="sxs-lookup"><span data-stu-id="9cadb-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-617">10060 (0x274C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-618">Попытка подключения не удалась, так как подключенная сторона не ответила должным образом по истечении определенного периода времени или не удалось установить соединение, так как не удалось ответить подключенному узлу.</span><span class="sxs-lookup"><span data-stu-id="9cadb-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**всаеконнрефусед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-620">10061 (0x274D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-621">Не удалось установить подключение, так как целевой компьютер отказался от него.</span><span class="sxs-lookup"><span data-stu-id="9cadb-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**всаелуп**</span><span class="sxs-lookup"><span data-stu-id="9cadb-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-623">10062 (0x274E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-624">Не удается преобразовать имя.</span><span class="sxs-lookup"><span data-stu-id="9cadb-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**всаенаметулонг**</span><span class="sxs-lookup"><span data-stu-id="9cadb-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-626">10063 (0x274F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-627">Имя компонента или имя слишком длинное.</span><span class="sxs-lookup"><span data-stu-id="9cadb-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**всаехостдовн**</span><span class="sxs-lookup"><span data-stu-id="9cadb-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="9cadb-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-630">Сбой операции сокета, так как целевой узел не работает.</span><span class="sxs-lookup"><span data-stu-id="9cadb-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**всаехостунреач**</span><span class="sxs-lookup"><span data-stu-id="9cadb-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="9cadb-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-633">Сделана попытка выполнить операцию на сокете для недоступного хоста.</span><span class="sxs-lookup"><span data-stu-id="9cadb-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**всаенотемпти**</span><span class="sxs-lookup"><span data-stu-id="9cadb-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="9cadb-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-636">Невозможно удалить каталог, который не является пустым.</span><span class="sxs-lookup"><span data-stu-id="9cadb-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**всаепроклим**</span><span class="sxs-lookup"><span data-stu-id="9cadb-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="9cadb-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-639">Реализация сокетов Windows может иметь ограничение на количество приложений, которые могут использовать его одновременно.</span><span class="sxs-lookup"><span data-stu-id="9cadb-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**всаеусерс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="9cadb-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-642">Квота исчерпана.</span><span class="sxs-lookup"><span data-stu-id="9cadb-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**всаедкуот**</span><span class="sxs-lookup"><span data-stu-id="9cadb-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="9cadb-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-645">Дисковая квота исчерпана.</span><span class="sxs-lookup"><span data-stu-id="9cadb-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**всаестале**</span><span class="sxs-lookup"><span data-stu-id="9cadb-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="9cadb-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-648">Ссылка на файл больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="9cadb-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**всаеремоте**</span><span class="sxs-lookup"><span data-stu-id="9cadb-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="9cadb-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-651">Элемент не доступен локально.</span><span class="sxs-lookup"><span data-stu-id="9cadb-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**всасиснотреади**</span><span class="sxs-lookup"><span data-stu-id="9cadb-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-653">10091 (0x276B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-654">В настоящее время сбой WSAStartup не может работать, так как базовая система, используемая для предоставления сетевых служб, в данный момент недоступна.</span><span class="sxs-lookup"><span data-stu-id="9cadb-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**всавернотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-656">10092 (0x276C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-657">Запрошенная версия сокетов Windows не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9cadb-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**всанотинитиалисед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-659">10093 (0x276D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-660">Либо приложение не вызвало сбой WSAStartup, либо сбой сбой WSAStartup.</span><span class="sxs-lookup"><span data-stu-id="9cadb-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**всаедискон**</span><span class="sxs-lookup"><span data-stu-id="9cadb-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="9cadb-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-663">Возвращается функцией Всарекв или Всареквфром, чтобы указать, что удаленная сторона инициировала корректное завершение работы.</span><span class="sxs-lookup"><span data-stu-id="9cadb-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**всаеноморе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="9cadb-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-666">Всалукупсервиценекст не может вернуть дополнительные результаты.</span><span class="sxs-lookup"><span data-stu-id="9cadb-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**всаеканцеллед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="9cadb-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-669">Вызов Всалукупсервицеенд был выполнен во время обработки этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9cadb-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="9cadb-670">Вызов отменен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**всаеинвалидпроктабле**</span><span class="sxs-lookup"><span data-stu-id="9cadb-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="9cadb-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-673">Недопустимая таблица вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="9cadb-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**всаеинвалидпровидер**</span><span class="sxs-lookup"><span data-stu-id="9cadb-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="9cadb-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-676">Запрошенный поставщик услуг недопустим.</span><span class="sxs-lookup"><span data-stu-id="9cadb-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**всаепровидерфаилединит**</span><span class="sxs-lookup"><span data-stu-id="9cadb-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-678">10106 (0x277A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-679">Не удалось загрузить или инициализировать запрошенного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="9cadb-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**всасискаллфаилуре**</span><span class="sxs-lookup"><span data-stu-id="9cadb-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-681">10107 (0x277B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-682">Сбой системного вызова.</span><span class="sxs-lookup"><span data-stu-id="9cadb-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**ВСАСЕРВИЦЕ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="9cadb-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-684">10108 (0x277C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-685">Такая служба неизвестна.</span><span class="sxs-lookup"><span data-stu-id="9cadb-685">No such service is known.</span></span> <span data-ttu-id="9cadb-686">Не удается найти службу в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**ВСАТИПЕ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="9cadb-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-688">10109 (0x277D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-689">Указанный класс не найден.</span><span class="sxs-lookup"><span data-stu-id="9cadb-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ больше \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-691">10110 (0x277E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-692">Всалукупсервиценекст не может вернуть дополнительные результаты.</span><span class="sxs-lookup"><span data-stu-id="9cadb-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ отменено**</span><span class="sxs-lookup"><span data-stu-id="9cadb-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-694">10111 (0x277F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-695">Вызов Всалукупсервицеенд был выполнен во время обработки этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9cadb-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="9cadb-696">Вызов отменен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**всаерефусед**</span><span class="sxs-lookup"><span data-stu-id="9cadb-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="9cadb-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-699">Запрос к базе данных не выполнен из-за того, что он был активно отклонен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**ВСАХОСТ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="9cadb-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-701">11001 (0x2AF9)</span><span class="sxs-lookup"><span data-stu-id="9cadb-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-702">Такой узел не существует.</span><span class="sxs-lookup"><span data-stu-id="9cadb-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**ВСАТРИ \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-704">11002 (0x2AFA)</span><span class="sxs-lookup"><span data-stu-id="9cadb-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-705">Обычно это временная ошибка при разрешении имени узла, и она означает, что локальный сервер не получил ответа от заслуживающего доверия сервера.</span><span class="sxs-lookup"><span data-stu-id="9cadb-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_Восстановление всано**</span><span class="sxs-lookup"><span data-stu-id="9cadb-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-707">11003 (0x2AFB)</span><span class="sxs-lookup"><span data-stu-id="9cadb-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-708">Во время поиска базы данных произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="9cadb-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_данные всано**</span><span class="sxs-lookup"><span data-stu-id="9cadb-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-710">11004 (0x2AFC)</span><span class="sxs-lookup"><span data-stu-id="9cadb-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-711">Запрошенное имя допустимо, но данные запрошенного типа не найдены.</span><span class="sxs-lookup"><span data-stu-id="9cadb-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_получатели качества обслуживания WSA \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-713">11005 (0x2AFD)</span><span class="sxs-lookup"><span data-stu-id="9cadb-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-714">Получен по меньшей мере один резерв.</span><span class="sxs-lookup"><span data-stu-id="9cadb-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_отправители качества обслуживания WSA \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-716">11006 (0x2AFE)</span><span class="sxs-lookup"><span data-stu-id="9cadb-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-717">Получен по крайней мере один путь.</span><span class="sxs-lookup"><span data-stu-id="9cadb-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ качество обслуживания \_ нет \_ отправителей**</span><span class="sxs-lookup"><span data-stu-id="9cadb-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-719">11007 (0x2AFF)</span><span class="sxs-lookup"><span data-stu-id="9cadb-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-720">Отправители отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9cadb-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA \_ качество обслуживания \_ нет \_ получателей**</span><span class="sxs-lookup"><span data-stu-id="9cadb-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-722">11008 (0x2B00)</span><span class="sxs-lookup"><span data-stu-id="9cadb-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-723">Нет получателей.</span><span class="sxs-lookup"><span data-stu-id="9cadb-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_запрос на качество обслуживания WSA \_ \_ подтвержден**</span><span class="sxs-lookup"><span data-stu-id="9cadb-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-725">11009 (0x2B01)</span><span class="sxs-lookup"><span data-stu-id="9cadb-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-726">Резервирование подтверждено.</span><span class="sxs-lookup"><span data-stu-id="9cadb-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_ \_ Ошибка при допуске обслуживания WSA \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-728">11010 (0x2B02)</span><span class="sxs-lookup"><span data-stu-id="9cadb-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-729">Ошибка из-за нехватки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cadb-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_Ошибка политики качества обслуживания WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-731">11011 (0x2B03)</span><span class="sxs-lookup"><span data-stu-id="9cadb-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-732">Отклонено по соображениям администрирования — неверные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="9cadb-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ неверный стиль качества обслуживания WSA \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-734">11012 (0x2B04)</span><span class="sxs-lookup"><span data-stu-id="9cadb-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-735">Неизвестный или конфликтующий стиль.</span><span class="sxs-lookup"><span data-stu-id="9cadb-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_Недопустимый объект качества обслуживания WSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-737">11013 (0x2B05)</span><span class="sxs-lookup"><span data-stu-id="9cadb-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-738">Проблема с некоторой частью буфера филтерспек или провидерспеЦифик в целом.</span><span class="sxs-lookup"><span data-stu-id="9cadb-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_ \_ \_ Ошибка Ctrl трафик качества обслуживания WSA \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-740">11014 (0x2B06)</span><span class="sxs-lookup"><span data-stu-id="9cadb-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-741">Проблема с некоторой частью фловспек.</span><span class="sxs-lookup"><span data-stu-id="9cadb-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ Общая ошибка WSA \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="9cadb-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-743">11015 (0x2B07)</span><span class="sxs-lookup"><span data-stu-id="9cadb-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-744">Общая ошибка QOS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ качество обслуживания \_ есервицетипе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-746">11016 (0x2B08)</span><span class="sxs-lookup"><span data-stu-id="9cadb-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-747">В фловспек найден недопустимый или Нераспознанный тип службы.</span><span class="sxs-lookup"><span data-stu-id="9cadb-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA \_ качество обслуживания \_ ефловспек**</span><span class="sxs-lookup"><span data-stu-id="9cadb-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-749">11017 (0x2B09)</span><span class="sxs-lookup"><span data-stu-id="9cadb-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-750">В структуре QOS обнаружена недопустимая или нераспознанная фловспек.</span><span class="sxs-lookup"><span data-stu-id="9cadb-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ качество обслуживания \_ епровспекбуф**</span><span class="sxs-lookup"><span data-stu-id="9cadb-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-752">11018 (0x2B0A)</span><span class="sxs-lookup"><span data-stu-id="9cadb-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-753">Недопустимый буфер, зависящий от поставщика QOS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ качество обслуживания \_ ефилтерстиле**</span><span class="sxs-lookup"><span data-stu-id="9cadb-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-755">11019 (0x2B0B)</span><span class="sxs-lookup"><span data-stu-id="9cadb-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-756">Использован недопустимый стиль фильтра качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA \_ качество обслуживания \_ ефилтертипе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-758">11020 (0x2B0C)</span><span class="sxs-lookup"><span data-stu-id="9cadb-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-759">Использован недопустимый тип фильтра качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA \_ качество обслуживания \_ ефилтеркаунт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-761">11021 (0x2B0D)</span><span class="sxs-lookup"><span data-stu-id="9cadb-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-762">В ФЛОВДЕСКРИПТОР указано неверное число Филтерспекс качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA \_ качество обслуживания \_ еобжленгс**</span><span class="sxs-lookup"><span data-stu-id="9cadb-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-764">11022 (0x2B0E)</span><span class="sxs-lookup"><span data-stu-id="9cadb-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-765">В буфере, зависящем от поставщика QOS, был указан объект с недопустимым полем Обжектленгс.</span><span class="sxs-lookup"><span data-stu-id="9cadb-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA \_ качество обслуживания \_ ефловкаунт**</span><span class="sxs-lookup"><span data-stu-id="9cadb-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-767">11023 (0x2B0F)</span><span class="sxs-lookup"><span data-stu-id="9cadb-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-768">В структуре QOS задано неверное число дескрипторов потока.</span><span class="sxs-lookup"><span data-stu-id="9cadb-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ качество обслуживания \_ еунковнпсобж**</span><span class="sxs-lookup"><span data-stu-id="9cadb-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-770">11024 (0x2B10)</span><span class="sxs-lookup"><span data-stu-id="9cadb-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-771">В буфере, зависящем от поставщика QOS, обнаружен нераспознанный объект.</span><span class="sxs-lookup"><span data-stu-id="9cadb-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ качество обслуживания \_ еполициобж**</span><span class="sxs-lookup"><span data-stu-id="9cadb-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-773">11025 (0x2B11)</span><span class="sxs-lookup"><span data-stu-id="9cadb-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-774">В буфере, зависящем от поставщика QOS, обнаружен недопустимый объект политики.</span><span class="sxs-lookup"><span data-stu-id="9cadb-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ качество обслуживания \_ ефловдеск**</span><span class="sxs-lookup"><span data-stu-id="9cadb-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-776">11026 (0x2B12)</span><span class="sxs-lookup"><span data-stu-id="9cadb-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-777">В списке дескрипторов потока обнаружен недопустимый дескриптор потока качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9cadb-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ качество обслуживания \_ епсфловспек**</span><span class="sxs-lookup"><span data-stu-id="9cadb-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-779">11027 (0x2B13)</span><span class="sxs-lookup"><span data-stu-id="9cadb-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-780">В буфере, заданном для поставщика QOS, обнаружено недопустимое или непротиворечивое фловспек.</span><span class="sxs-lookup"><span data-stu-id="9cadb-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ качество обслуживания \_ епсфилтерспек**</span><span class="sxs-lookup"><span data-stu-id="9cadb-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-782">11028 (0x2B14)</span><span class="sxs-lookup"><span data-stu-id="9cadb-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-783">В буфере, зависящем от поставщика QOS, обнаружен недопустимый ФИЛТЕРСПЕК.</span><span class="sxs-lookup"><span data-stu-id="9cadb-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ качество обслуживания \_ есдмодеобж**</span><span class="sxs-lookup"><span data-stu-id="9cadb-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-785">11029 (0x2B15)</span><span class="sxs-lookup"><span data-stu-id="9cadb-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-786">В буфере, заданном поставщиком QOS, обнаружен недопустимый объект режима удаления фигуры.</span><span class="sxs-lookup"><span data-stu-id="9cadb-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ качество обслуживания \_ ешаператеобж**</span><span class="sxs-lookup"><span data-stu-id="9cadb-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-788">11030 (0x2B16)</span><span class="sxs-lookup"><span data-stu-id="9cadb-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-789">В буфере, зависящем от поставщика QOS, обнаружен недопустимый объект частоты формирования.</span><span class="sxs-lookup"><span data-stu-id="9cadb-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA \_ качество обслуживания \_ зарезервировано \_ петипе**</span><span class="sxs-lookup"><span data-stu-id="9cadb-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-791">11031 (0x2B17)</span><span class="sxs-lookup"><span data-stu-id="9cadb-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-792">Зарезервированный элемент политики обнаружен в буфере, зависящем от поставщика QOS.</span><span class="sxs-lookup"><span data-stu-id="9cadb-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ не найден безопасный узел \_ WSA**</span><span class="sxs-lookup"><span data-stu-id="9cadb-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-794">11032 (0x2B18)</span><span class="sxs-lookup"><span data-stu-id="9cadb-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-795">Такой узел не известен безопасно.</span><span class="sxs-lookup"><span data-stu-id="9cadb-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cadb-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_ \_ \_ Ошибка политики имен IP WSA IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="9cadb-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cadb-797">11033 (0x2B19)</span><span class="sxs-lookup"><span data-stu-id="9cadb-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="9cadb-798">Не удалось добавить политику IPSEC на основе имен.</span><span class="sxs-lookup"><span data-stu-id="9cadb-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="9cadb-799">Требования</span><span class="sxs-lookup"><span data-stu-id="9cadb-799">Requirements</span></span>



| <span data-ttu-id="9cadb-800">Требование</span><span class="sxs-lookup"><span data-stu-id="9cadb-800">Requirement</span></span> | <span data-ttu-id="9cadb-801">Значение</span><span class="sxs-lookup"><span data-stu-id="9cadb-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cadb-802">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cadb-802">Minimum supported client</span></span><br/> | <span data-ttu-id="9cadb-803">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9cadb-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9cadb-804">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cadb-804">Minimum supported server</span></span><br/> | <span data-ttu-id="9cadb-805">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cadb-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cadb-806">Header</span><span class="sxs-lookup"><span data-stu-id="9cadb-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cadb-807"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cadb-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cadb-808">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cadb-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cadb-809">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="9cadb-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




