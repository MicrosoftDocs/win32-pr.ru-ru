---
description: Описание кодов ошибок 12000-1599, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Коды системных ошибок (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496245"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="8dd90-103">Коды системных ошибок (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="8dd90-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="8dd90-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="8dd90-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="8dd90-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 12000 – 15999).</span><span class="sxs-lookup"><span data-stu-id="8dd90-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="8dd90-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="8dd90-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="8dd90-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="8dd90-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="8dd90-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Ошибка при \_ \_Интернет \** _</span><span class="sxs-lookup"><span data-stu-id="8dd90-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-110">12000-12175 (0x2EE0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-111">См. [коды ошибок Интернета](../wininet/wininet-errors.md) и WinInet. h.</span><span class="sxs-lookup"><span data-stu-id="8dd90-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *Ошибка \_ \_ Политика QM \_ IPSec \_ существует*\*</span><span class="sxs-lookup"><span data-stu-id="8dd90-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-113">13000 (0x32C8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-114">Указанная политика быстрого режима уже существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена политика QM IPSec.**</span><span class="sxs-lookup"><span data-stu-id="8dd90-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-116">13001 (0x32C9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-117">Указанная политика быстрого режима не найдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании политики QM \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-119">13002 (0x32CA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-120">Указанная политика быстрого режима используется.</span><span class="sxs-lookup"><span data-stu-id="8dd90-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**Ошибка \_ Политика протокола IPsec \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-122">13003 (0x32CB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-123">Указанная политика основного режима уже существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена политика mm для IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-125">13004 (0x32CC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-126">Указанная политика основного режима не найдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**Ошибка \_ \_ \_ \_ при \_ использовании политики протокола IPsec mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-128">13005 (0x32CD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-129">Указанная политика основного режима используется.</span><span class="sxs-lookup"><span data-stu-id="8dd90-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**Ошибка \_ фильтр протокола IPsec \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-131">13006 (0x32CE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-132">Указанный фильтр основного режима уже существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не найден фильтр IPSec \_ mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-134">13007 (0x32CF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-135">Указанный фильтр основного режима не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**Ошибка \_ \_ Фильтр транспорта \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-137">13008 (0x32D0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-138">Указанный фильтр транспортного режима уже существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена фильтр транспорта IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-140">13009 (0x32D1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-141">Указанный фильтр транспортного режима не существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**Ошибка \_ \_ \_ проверки подлинности IPsec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-143">13010 (0x32D2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-144">Указанный список проверки подлинности в основном режиме существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**Ошибка \_ \_ \_ \_ не найдена проверка подлинности IPsec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-146">13011 (0x32D3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-147">Указанный список проверки подлинности в основном режиме не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании проверки подлинности IPsec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-149">13012 (0x32D4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-150">Используется указанный список проверки подлинности в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="8dd90-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**Ошибка \_ IPSec \_ по умолчанию \_ \_ \_ не \_ найдена политика mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-152">13013 (0x32D5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-153">Указанная политика основного режима по умолчанию не найдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**Ошибка \_ IPSec \_ по умолчанию \_ \_ \_ не найдена проверка подлинности mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-155">13014 (0x32D6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-156">Указанный список проверки подлинности основного режима по умолчанию не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**Ошибка \_ IPSec \_ Default \_ QM \_ политика \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-158">13015 (0x32D7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-159">Указанная политика быстрого режима по умолчанию не найдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**Ошибка \_ \_ Фильтр туннеля \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-161">13016 (0x32D8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-162">Указанный фильтр режима туннелирования существует.</span><span class="sxs-lookup"><span data-stu-id="8dd90-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена фильтр туннеля IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-164">13017 (0x32D9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-165">Указанный фильтр туннельного режима не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-167">13018 (0x32DA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-168">Фильтр основного режима ожидает удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра транспорта \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-170">13019 (0x32DB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-171">Фильтр транспорта ожидает удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления фильтра туннеля \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-173">13020 (0x32DC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-174">Фильтр туннеля ожидает удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления политики IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-176">13021 (0x32DD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-177">Политика основного режима ожидает удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**Ошибка \_ \_ \_ проверки подлинности при \_ ожидании \_ удаления с IPSec mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-179">13022 (0x32DE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-180">Идет удаление пакета проверки подлинности основного режима.</span><span class="sxs-lookup"><span data-stu-id="8dd90-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**Ошибка \_ при \_ \_ \_ ожидании удаления политики IPSec QM \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-182">13023 (0x32DF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-183">Политика быстрого режима ожидает удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**предупреждение \_ об \_ \_ очистке политики IPSec mm \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-185">13024 (0x32E0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-186">Политика основного режима успешно добавлена, но некоторые из запрошенных предложений не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8dd90-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**предупреждение \_ об \_ \_ очистке политики IPSec QM \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-188">13025 (0x32E1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-189">Политика быстрого режима успешно добавлена, но некоторые из запрошенных предложений не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8dd90-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**Ошибка \_ при \_ \_ \_ \_ начале состояния "сбой IPSec IKE"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-191">13800 (0x35E8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-192">Ошибка \_ при \_ \_ \_ \_ начале состояния "сбой IPSec IKE"</span><span class="sxs-lookup"><span data-stu-id="8dd90-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**Ошибка \_ \_ \_ проверки подлинности IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-194">13801 (0x35E9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-195">Учетные данные проверки подлинности IKE недопустимы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**Ошибка при сбое в IPSec для ошибки \_ \_ IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-197">13802 (0x35EA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-198">Атрибуты безопасности IKE недопустимы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**Ошибка \_ \_ \_ ожидания согласования IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-200">13803 (0x35EB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-201">Выполняется согласование IKE.</span><span class="sxs-lookup"><span data-stu-id="8dd90-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**Ошибка \_ при \_ \_ общей \_ обработке \_ IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-203">13804 (0x35EC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-204">Общая ошибка обработки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**Ошибка при истечении \_ \_ \_ времени \_ ожидания IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-206">13805 (0x35ED)</span><span class="sxs-lookup"><span data-stu-id="8dd90-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-207">Истекло время ожидания согласования.</span><span class="sxs-lookup"><span data-stu-id="8dd90-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ сертификата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-209">13806 (0x35EE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-210">IKE не удалось найти допустимый сертификат компьютера.</span><span class="sxs-lookup"><span data-stu-id="8dd90-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="8dd90-211">Обратитесь к администратору безопасности сети, чтобы установить действительный сертификат в соответствующем хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**Ошибка \_ при \_ \_ удалении SA IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-213">13807 (0x35EF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-214">SA IKE удалено одноранговым узлом перед завершением установки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**Ошибка при установке \_ IPSec \_ IKE \_ SA \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-216">13808 (0x35F0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-217">SA IKE удалено до завершения установки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**Ошибка при \_ получении из протокола IPsec \_ IKE \_ mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-219">13809 (0x35F1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-220">Слишком длинный запрос на согласование в очереди.</span><span class="sxs-lookup"><span data-stu-id="8dd90-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ получения запроса \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-222">13810 (0x35F2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-223">Слишком длинный запрос на согласование в очереди.</span><span class="sxs-lookup"><span data-stu-id="8dd90-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**Ошибка \_ при \_ \_ \_ отброшении очереди IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-225">13811 (0x35F3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-226">Слишком длинный запрос на согласование в очереди.</span><span class="sxs-lookup"><span data-stu-id="8dd90-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**Ошибка \_ при \_ \_ отбрасывания очереди IKE IPSec \_ \_ No \_ mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-228">13812 (0x35F4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-229">Слишком длинный запрос на согласование в очереди.</span><span class="sxs-lookup"><span data-stu-id="8dd90-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**Ошибка \_ при \_ \_ отбрасывания IPSec IKE \_ без \_ ответа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-231">13813 (0x35F5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-232">Нет ответа от однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="8dd90-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**Ошибка \_ \_ \_ \_ отложенной \_ отбрасывания IKE с ошибкой IPSec mm**</span><span class="sxs-lookup"><span data-stu-id="8dd90-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-234">13814 (0x35F6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-235">Согласование заняло слишком много времени.</span><span class="sxs-lookup"><span data-stu-id="8dd90-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ delaying \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-237">13815 (0x35F7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-238">Согласование заняло слишком много времени.</span><span class="sxs-lookup"><span data-stu-id="8dd90-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**Ошибка \_ \_ IKE IPSec \_ об ошибке**</span><span class="sxs-lookup"><span data-stu-id="8dd90-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-240">13816 (0x35F8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-241">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**Ошибка \_ IPSec \_ IKE \_ CRL \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-243">13817 (0x35F9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-244">Проверка отзыва сертификата не пройдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимое \_ \_ Использование ключа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-246">13818 (0x35FA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-247">Недопустимое использование ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="8dd90-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ \_ тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-249">13819 (0x35FB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-250">Недопустимый тип сертификата.</span><span class="sxs-lookup"><span data-stu-id="8dd90-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ закрытого \_ ключа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-252">13820 (0x35FC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-253">Сбой согласования IKE, так как используемый сертификат компьютера не имеет закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="8dd90-254">Для сертификатов IPsec требуется закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="8dd90-255">Обратитесь к администратору безопасности сети, чтобы заменить сертификат с закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="8dd90-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**Ошибка \_ \_ \_ одновременного \_ смены ключей IPsec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-257">13821 (0x35FD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-258">Обнаружены одновременные Переключи.</span><span class="sxs-lookup"><span data-stu-id="8dd90-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**Ошибка \_ IPSec \_ \_ Сбой IKE DH \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-260">13822 (0x35FE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-261">Сбой в Diffie-Hellmanных вычислениях.</span><span class="sxs-lookup"><span data-stu-id="8dd90-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**Ошибка \_ \_ \_ \_ \_ не распознана критическая \_ нагрузка IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-263">13823 (0x35FF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-264">Не знает, как обрабатывать критически важные полезные данные.</span><span class="sxs-lookup"><span data-stu-id="8dd90-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**Ошибка \_ \_ \_ неправильного \_ заголовка IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="8dd90-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-267">Недопустимый заголовок.</span><span class="sxs-lookup"><span data-stu-id="8dd90-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ политики**</span><span class="sxs-lookup"><span data-stu-id="8dd90-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="8dd90-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-270">Политика не настроена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**Ошибка \_ \_ \_ недопустимой подписи IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="8dd90-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-273">Не удалось проверить подпись.</span><span class="sxs-lookup"><span data-stu-id="8dd90-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**Ошибка \_ IPSec \_ IKE \_ Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="8dd90-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-276">Не удалось выполнить проверку подлинности с помощью Kerberos.</span><span class="sxs-lookup"><span data-stu-id="8dd90-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ открытого \_ ключа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="8dd90-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-279">У сертификата узла нет открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**Ошибка \_ протокола IPsec \_ IKE для \_ процесса \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="8dd90-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-282">Ошибка при обработке полезных данных ошибки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**Ошибка \_ IPSec \_ процесса IKE об ошибке \_ \_ \_ SA**</span><span class="sxs-lookup"><span data-stu-id="8dd90-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="8dd90-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-285">Ошибка обработки полезных данных SA.</span><span class="sxs-lookup"><span data-stu-id="8dd90-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**Ошибка сообщения об ошибке \_ \_ процесса IKE при IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="8dd90-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-288">Ошибка обработки полезных данных предложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ Process \_ Err \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="8dd90-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-291">Ошибка обработки полезных данных преобразования.</span><span class="sxs-lookup"><span data-stu-id="8dd90-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**Ошибка \_ ошибки \_ IKE при \_ обработке протокола \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="8dd90-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-294">Ошибка обработки полезных данных.</span><span class="sxs-lookup"><span data-stu-id="8dd90-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**Ошибка \_ с \_ \_ \_ идентификатором Err процесса IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-296">13834 (0x360A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-297">Ошибка при обработке полезных данных идентификатора.</span><span class="sxs-lookup"><span data-stu-id="8dd90-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**Ошибка \_ при \_ \_ работе с \_ \_ сертификатом сообщения Err IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-299">13835 (0x360B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-300">Ошибка обработки полезных данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="8dd90-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**Ошибка \_ IPSec \_ процесс IKE, запрос \_ \_ \_ сертификата Err \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-302">13836 (0x360C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-303">Ошибка обработки полезных данных запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="8dd90-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**Ошибка при проверке погрешности \_ протокола IPsec \_ IKE \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-305">13837 (0x360D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-306">Ошибка при обработке полезных данных хэша.</span><span class="sxs-lookup"><span data-stu-id="8dd90-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-308">13838 (0x360E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-309">Ошибка при обработке полезных данных сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**Ошибка сообщения об ошибке для \_ \_ процесса IKE IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-311">13839 (0x360F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-312">Ошибка обработки полезных данных nonce.</span><span class="sxs-lookup"><span data-stu-id="8dd90-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**Ошибка \_ при \_ \_ \_ \_ уведомлении об ошибке процесса IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="8dd90-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-315">Ошибка обработки полезных данных уведомления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**Ошибка \_ при \_ \_ удалении IKE \_ процесса \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="8dd90-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-318">Ошибка при обработке полезных данных удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**Ошибка \_ \_ \_ поставщика Err для процесса IKE \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="8dd90-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-321">Ошибка обработки полезных данных VendorId.</span><span class="sxs-lookup"><span data-stu-id="8dd90-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ полезная нагрузка**</span><span class="sxs-lookup"><span data-stu-id="8dd90-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="8dd90-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-324">Получены недопустимые полезные данные.</span><span class="sxs-lookup"><span data-stu-id="8dd90-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**Ошибка \_ IPSec \_ IKE \_ Load \_ \_ Software SA**</span><span class="sxs-lookup"><span data-stu-id="8dd90-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="8dd90-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-327">Мягкое SA загружено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**Ошибка \_ при \_ \_ \_ \_ отключении мягкого SA IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="8dd90-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-330">Мягкое SA разорвано.</span><span class="sxs-lookup"><span data-stu-id="8dd90-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**Ошибка \_ \_ \_ неправильного \_ файла cookie IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="8dd90-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-333">Получен недопустимый файл cookie.</span><span class="sxs-lookup"><span data-stu-id="8dd90-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**Ошибка \_ IPSec \_ IKE \_ без \_ однорангового \_ сертификата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="8dd90-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-336">Узлу не удалось отправить действительный сертификат компьютера.</span><span class="sxs-lookup"><span data-stu-id="8dd90-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**Ошибка \_ \_ \_ при сбое однорангового \_ списка отзыва сертификатов IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="8dd90-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-339">Сбой проверки отзыва сертификата узла.</span><span class="sxs-lookup"><span data-stu-id="8dd90-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**Ошибка \_ при \_ \_ изменении политики \_ IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="8dd90-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-342">Новая политика не прошла проверку SAs, сформированной с помощью старой политики.</span><span class="sxs-lookup"><span data-stu-id="8dd90-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**Ошибка \_ IPSec \_ IKE \_ No \_ mm, \_ Политика**</span><span class="sxs-lookup"><span data-stu-id="8dd90-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-344">13850 (0x361A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-345">Нет доступной политики IKE основного режима.</span><span class="sxs-lookup"><span data-stu-id="8dd90-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**Ошибка \_ IPSec \_ IKE \_ ноткбприв**</span><span class="sxs-lookup"><span data-stu-id="8dd90-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-347">13851 (0x361B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-348">Не удалось включить привилегии TCB.</span><span class="sxs-lookup"><span data-stu-id="8dd90-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**Ошибка \_ IPSec \_ IKE \_ секлоадфаил**</span><span class="sxs-lookup"><span data-stu-id="8dd90-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-350">13852 (0x361C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-351">Не удалось загрузить SECURITY.DLL.</span><span class="sxs-lookup"><span data-stu-id="8dd90-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**Ошибка \_ IPSec \_ IKE \_ фаилсспинит**</span><span class="sxs-lookup"><span data-stu-id="8dd90-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-353">13853 (0x361D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-354">Не удалось получить адрес диспетчеризации таблицы функции безопасности от SSPI.</span><span class="sxs-lookup"><span data-stu-id="8dd90-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**Ошибка \_ IPSec \_ IKE \_ фаилкуериссп**</span><span class="sxs-lookup"><span data-stu-id="8dd90-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-356">13854 (0x361E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-357">Не удалось запросить пакет Kerberos для получения максимального размера токена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**Ошибка \_ IPSec \_ IKE \_ срваккфаил**</span><span class="sxs-lookup"><span data-stu-id="8dd90-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-359">13855 (0x361F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-360">Не удалось получить учетные данные сервера Kerberos для \_ службы IKE/Error IPSec \_ .</span><span class="sxs-lookup"><span data-stu-id="8dd90-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="8dd90-361">Проверка подлинности Kerberos не будет работать.</span><span class="sxs-lookup"><span data-stu-id="8dd90-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="8dd90-362">Наиболее вероятной причиной этого является отсутствие членства в домене.</span><span class="sxs-lookup"><span data-stu-id="8dd90-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="8dd90-363">Это нормально, если компьютер входит в рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="8dd90-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**Ошибка \_ IPSec \_ IKE \_ срвкуерикред**</span><span class="sxs-lookup"><span data-stu-id="8dd90-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="8dd90-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-366">Не удалось определить имя участника SSPI для \_ службы IKE/Error IPSec \_ ([**куерикредентиалсаттрибутес**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span><span class="sxs-lookup"><span data-stu-id="8dd90-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**Ошибка \_ IPSec \_ IKE \_ жетспифаил**</span><span class="sxs-lookup"><span data-stu-id="8dd90-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="8dd90-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-369">Не удалось получить новый SPI для входящего SA из драйвера IPsec.</span><span class="sxs-lookup"><span data-stu-id="8dd90-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="8dd90-370">Наиболее распространенной причиной этого является то, что драйвер не имеет нужного фильтра.</span><span class="sxs-lookup"><span data-stu-id="8dd90-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="8dd90-371">Проверьте политику, чтобы проверить фильтры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**Ошибка \_ \_ \_ неверного \_ фильтра IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="8dd90-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-374">Данный фильтр недопустим.</span><span class="sxs-lookup"><span data-stu-id="8dd90-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**Ошибка \_ \_ \_ нехватки \_ памяти IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="8dd90-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-377">Ошибка выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="8dd90-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**Ошибка \_ IPSec \_ IKE \_ \_ \_ не удалось добавить ключ обновления \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="8dd90-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-380">Не удалось добавить сопоставление безопасности в драйвер IPsec.</span><span class="sxs-lookup"><span data-stu-id="8dd90-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="8dd90-381">Наиболее распространенной причиной этого является то, что согласование IKE заняло слишком много времени.</span><span class="sxs-lookup"><span data-stu-id="8dd90-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="8dd90-382">Если проблема будет повторяться, уменьшите нагрузку на неисправный компьютер.</span><span class="sxs-lookup"><span data-stu-id="8dd90-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Политика**</span><span class="sxs-lookup"><span data-stu-id="8dd90-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-384">13861 (0x3625)</span><span class="sxs-lookup"><span data-stu-id="8dd90-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-385">Недопустимая политика.</span><span class="sxs-lookup"><span data-stu-id="8dd90-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**Ошибка \_ IPSec \_ IKE \_ Unknown \_ ДОИ**</span><span class="sxs-lookup"><span data-stu-id="8dd90-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="8dd90-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-388">Недопустимый ДОИ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**Ошибка \_ \_ \_ неправильной \_ ситуации IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="8dd90-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-391">Недопустимая ситуация.</span><span class="sxs-lookup"><span data-stu-id="8dd90-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**Ошибка \_ IPSec \_ IKE \_ DH- \_ сбой**</span><span class="sxs-lookup"><span data-stu-id="8dd90-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="8dd90-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-394">Сбой Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8dd90-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Группа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="8dd90-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-397">Недопустимая группа Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8dd90-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**Ошибка \_ \_ шифрования IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-399">13866 (0x362A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-400">Ошибка при шифровании полезных данных.</span><span class="sxs-lookup"><span data-stu-id="8dd90-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**Ошибка \_ \_ \_ расшифровки IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-402">13867 (0x362B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-403">Ошибка при расшифровке полезных данных.</span><span class="sxs-lookup"><span data-stu-id="8dd90-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**Ошибка \_ \_ \_ соответствия политике IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-405">13868 (0x362C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-406">Ошибка соответствия политики.</span><span class="sxs-lookup"><span data-stu-id="8dd90-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**Ошибка \_ \_ \_ неподдерживаемого идентификатора IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-408">13869 (0x362D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-409">Неподдерживаемый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8dd90-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**Ошибка \_ \_ \_ неверного \_ хэша IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-411">13870 (0x362E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-412">Проверка хэша не пройдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**Ошибка \_ \_ IKE IPSec \_ -Недопустимый \_ алгоритм хэширования \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-414">13871 (0x362F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-415">Недопустимый хэш-алгоритм.</span><span class="sxs-lookup"><span data-stu-id="8dd90-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**Ошибка \_ IPSec \_ IKE \_ -Недопустимый \_ \_ Размер хэша**</span><span class="sxs-lookup"><span data-stu-id="8dd90-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="8dd90-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-418">Недопустимый размер хэша.</span><span class="sxs-lookup"><span data-stu-id="8dd90-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ \_ алгоритм шифрования**</span><span class="sxs-lookup"><span data-stu-id="8dd90-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="8dd90-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-421">Недопустимый алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="8dd90-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ алгоритм проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="8dd90-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-424">Недопустимый алгоритм проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8dd90-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**Ошибка \_ \_ \_ неправильной \_ подписи IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="8dd90-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-427">Недопустимая подпись сертификата.</span><span class="sxs-lookup"><span data-stu-id="8dd90-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**Ошибка \_ \_ \_ при загрузке IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="8dd90-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-430">Сбой загрузки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**Ошибка \_ IPSec \_ IKE \_ RPC \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="8dd90-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="8dd90-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-433">Удалено через вызов RPC.</span><span class="sxs-lookup"><span data-stu-id="8dd90-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**Ошибка \_ при \_ \_ \_ переинициализации IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="8dd90-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-436">Временное состояние, созданное для выполнения повторной инициализации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="8dd90-437">Это не реальный сбой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимое \_ \_ уведомление о времени существования респондента \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="8dd90-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-440">Значение времени существования, полученное в поле уведомления о времени жизни респондента, ниже минимально настроенного значения Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8dd90-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="8dd90-441">Исправьте политику на одноранговом компьютере.</span><span class="sxs-lookup"><span data-stu-id="8dd90-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ Основная \_ версия**</span><span class="sxs-lookup"><span data-stu-id="8dd90-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="8dd90-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-444">Получателю не удается управлять версией IKE, указанной в заголовке.</span><span class="sxs-lookup"><span data-stu-id="8dd90-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимый \_ сертификат \_ кэйлен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="8dd90-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-447">Длина ключа в сертификате слишком мала для настроенных требований безопасности.</span><span class="sxs-lookup"><span data-stu-id="8dd90-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**\_ \_ \_ предел IKE mm \_ , ошибка IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-449">13882 (0x363A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-450">Превышено максимальное число установленных одноранговых сопоставлений MM SAs.</span><span class="sxs-lookup"><span data-stu-id="8dd90-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**Ошибка \_ при \_ \_ отключенном согласовании IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-452">13883 (0x363B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-453">IKE получила политику, которая отключает согласование.</span><span class="sxs-lookup"><span data-stu-id="8dd90-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="8dd90-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-455">13884 (0x363C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-456">Достигнуто максимальное ограничение быстрого режима для основного режима.</span><span class="sxs-lookup"><span data-stu-id="8dd90-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="8dd90-457">Будет запущен новый основной режим.</span><span class="sxs-lookup"><span data-stu-id="8dd90-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**Ошибка \_ \_ IKE \_ mm с \_ истекшим сроком действия**</span><span class="sxs-lookup"><span data-stu-id="8dd90-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-459">13885 (0x363D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-460">Срок жизни SA основного режима истек, или узел отправил удаление в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="8dd90-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**Ошибка \_ \_ \_ предполагается, что одноранговый mm IKE не является \_ \_ \_ допустимым**</span><span class="sxs-lookup"><span data-stu-id="8dd90-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-462">13886 (0x363E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-463">Предполагается, что SA основного режима недопустимо, так как одноранговый узел перестал отвечать.</span><span class="sxs-lookup"><span data-stu-id="8dd90-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**Ошибка \_ при \_ \_ \_ \_ несоответствии политики цепочки сертификатов IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-465">13887 (0x363F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-466">Сертификат не цепочка доверенного корня в политике IPsec.</span><span class="sxs-lookup"><span data-stu-id="8dd90-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**Ошибка \_ \_ \_ непредусмотренного \_ идентификатора сообщения IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="8dd90-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-469">Получен непредвиденный идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**Ошибка \_ IPSec \_ IKE \_ недопустимые \_ полезные данные проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="8dd90-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-472">Получены недопустимые предложения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8dd90-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**Ошибка \_ при \_ \_ \_ отправке куки-файла cookie IKE DOS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="8dd90-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-475">Отправлен файл cookie DoS на уведомление инициатора.</span><span class="sxs-lookup"><span data-stu-id="8dd90-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**Ошибка \_ при \_ \_ завершении работы IPsec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="8dd90-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-478">Служба IKE завершает работу.</span><span class="sxs-lookup"><span data-stu-id="8dd90-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**Ошибка \_ \_ \_ \_ при проверке подлинности IPsec IKE КГА \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="8dd90-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-481">Не удалось проверить привязку между адресом КГА и сертификатом.</span><span class="sxs-lookup"><span data-stu-id="8dd90-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**Ошибка \_ при \_ обработке протокола IPsec IKE \_ \_ \_ натоа**</span><span class="sxs-lookup"><span data-stu-id="8dd90-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="8dd90-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-484">Ошибка при обработке полезных данных Натоа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**Ошибка \_ IPSec \_ IKE \_ Недопустимая \_ mm \_ для \_ QM**</span><span class="sxs-lookup"><span data-stu-id="8dd90-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="8dd90-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-487">Параметры основного режима недопустимы для этого быстрого режима.</span><span class="sxs-lookup"><span data-stu-id="8dd90-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**Ошибка \_ IPSec \_ IKE \_ QM \_ срок действия истек**</span><span class="sxs-lookup"><span data-stu-id="8dd90-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="8dd90-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-490">Срок действия SA быстрого режима истек для драйвера IPsec.</span><span class="sxs-lookup"><span data-stu-id="8dd90-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**Ошибка \_ \_ IKE " \_ слишком \_ много \_ фильтров IPsec"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="8dd90-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-493">Обнаружено слишком много динамически добавляемых фильтров IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="8dd90-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**Ошибка \_ при \_ \_ \_ \_ истечении состояния "сбой IPSec IKE"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="8dd90-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-496">Ошибка \_ при \_ \_ \_ \_ истечении состояния "сбой IPSec IKE"</span><span class="sxs-lookup"><span data-stu-id="8dd90-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**Ошибка \_ IPSec \_ IKE \_ Kill \_ фиктивный \_ \_ туннель NAP**</span><span class="sxs-lookup"><span data-stu-id="8dd90-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-498">13898 (0x364A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-499">Повторная проверка подлинности NAP прошла удачно, и необходимо удалить фиктивный туннель IKEv2 для NAP.</span><span class="sxs-lookup"><span data-stu-id="8dd90-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**Ошибка \_ \_ \_ \_ \_ при назначении внутреннего IP-адреса IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-501">13899 (0x364B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-502">Ошибка при назначении внутреннего IP-адреса инициатору в туннельном режиме.</span><span class="sxs-lookup"><span data-stu-id="8dd90-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**Ошибка \_ IPSec \_ IKE \_ не \_ требуется \_ полезных данных CP \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-504">13900 (0x364C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-505">Требуется отсутствие полезных данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**Ошибка \_ при \_ \_ \_ согласовании олицетворения модуля \_ ключей \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-507">13901 (0x364D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-508">Выполняется согласование в качестве участника безопасности, который выдал подключение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**Ошибка \_ при \_ \_ ПОДАВЛЕНии сосуществования IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-510">13902 (0x364E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-511">SA удалено из-за отключения проверки сосуществования в IKEv1/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="8dd90-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**Ошибка \_ IPSec \_ IKE \_ рателимит \_ DROP**</span><span class="sxs-lookup"><span data-stu-id="8dd90-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-513">13903 (0x364F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-514">Входящий запрос SA был удален из-за ограничения скорости однорангового IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**Ошибка \_ IPSec \_ IKE \_ \_ \_ не поддерживает \_ мобике**</span><span class="sxs-lookup"><span data-stu-id="8dd90-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="8dd90-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-517">Одноранговый узел не поддерживает МОБИКЕ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**Ошибка \_ \_ \_ при проверке IPSec IKE \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="8dd90-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-520">Установка SA не разрешена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности \_ при сбое авторизации в IPSec IKE**</span><span class="sxs-lookup"><span data-stu-id="8dd90-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="8dd90-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-523">Установка SA не разрешена, так как не существует достаточно строгих учетных данных на основе PKINIT.</span><span class="sxs-lookup"><span data-stu-id="8dd90-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**Ошибка \_ \_ авторизации IKE IPSec при \_ \_ \_ \_ необязательной \_ повторной попытке**</span><span class="sxs-lookup"><span data-stu-id="8dd90-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="8dd90-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-526">Установка SA не разрешена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-526">SA establishment is not authorized.</span></span> <span data-ttu-id="8dd90-527">Может потребоваться ввести обновленные или другие учетные данные, например смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="8dd90-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности \_ при проверке \_ \_ согласованности IPSec IKE и цертмап**</span><span class="sxs-lookup"><span data-stu-id="8dd90-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="8dd90-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-530">Установка SA не разрешена, так как не существует достаточно строгих учетных данных на основе PKINIT.</span><span class="sxs-lookup"><span data-stu-id="8dd90-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="8dd90-531">Это может быть связано со сбоем сопоставления сертификатов и учетных записей для сопоставления безопасности.</span><span class="sxs-lookup"><span data-stu-id="8dd90-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**Ошибка \_ при \_ \_ \_ \_ расширенном завершении сообщения IKE о состоянии \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="8dd90-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-534">Ошибка \_ при \_ \_ \_ \_ расширенном завершении сообщения IKE о состоянии \_ IPSec</span><span class="sxs-lookup"><span data-stu-id="8dd90-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**Ошибка \_ IPSec \_ Bad \_ SPI**</span><span class="sxs-lookup"><span data-stu-id="8dd90-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="8dd90-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-537">Индекс SPI в пакете не соответствует действительному сопоставлению безопасности IPsec.</span><span class="sxs-lookup"><span data-stu-id="8dd90-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**Ошибка \_ \_ \_ времени существования SA IPsec \_ истекло**</span><span class="sxs-lookup"><span data-stu-id="8dd90-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="8dd90-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-540">Пакет был получен на сопоставление безопасности IPsec, срок действия которого истек.</span><span class="sxs-lookup"><span data-stu-id="8dd90-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**Ошибка \_ IPSec с \_ неверным \_ SA**</span><span class="sxs-lookup"><span data-stu-id="8dd90-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="8dd90-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-543">Пакет был получен на сопоставление безопасности IPsec, которое не соответствует характеристикам пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**Ошибка \_ \_ \_ при проверке воспроизведения IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="8dd90-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-546">Сбой при проверке воспроизведения порядкового номера пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**Ошибка \_ \_ недопустимого \_ пакета IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-548">13914 (0x365A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-549">Недопустимый заголовок или трейлер IPsec в пакете.</span><span class="sxs-lookup"><span data-stu-id="8dd90-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**Ошибка \_ \_ \_ при проверке целостности \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-551">13915 (0x365B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-552">Проверка целостности IPsec не пройдена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**Ошибка \_ при \_ \_ отбрасывания открытого текста IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-554">13916 (0x365C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-555">IPsec отбросил пакет с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="8dd90-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**Ошибка \_ при \_ \_ отбрасывания брандмауэра проверки подлинности IPsec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-557">13917 (0x365D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-558">IPsec отбросил входящий пакет ESP в режиме прошедшего проверку подлинности брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8dd90-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="8dd90-559">Это немягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="8dd90-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**Ошибка \_ \_ сброса регулирования IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-561">13918 (0x365E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-562">IPsec отбросил пакет из-за регулирования DoS.</span><span class="sxs-lookup"><span data-stu-id="8dd90-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**Ошибка \_ в \_ \_ блоке досп IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="8dd90-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-565">Защита с помощью IPsec DoS соответствует явному правилу блокировки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**Ошибка \_ IPSec \_ досп \_ получения \_ многоадресной рассылки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="8dd90-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-568">Протокол IPsec DoS Protection получил пакет многоадресной рассылки, зависящий от IPsec, что запрещено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**Ошибка \_ IPSec \_ досп \_ Недопустимый \_ пакет**</span><span class="sxs-lookup"><span data-stu-id="8dd90-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="8dd90-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-571">IPsec DoS Protection получил неправильно отформатированный пакет.</span><span class="sxs-lookup"><span data-stu-id="8dd90-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**Ошибка \_ \_ \_ \_ при поиске состояния досп \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="8dd90-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="8dd90-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-574">Защите от вирусов IPsec не удалось найти состояние.</span><span class="sxs-lookup"><span data-stu-id="8dd90-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**Ошибка \_ при \_ \_ вводе максимального числа записей IPSec досп \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="8dd90-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-577">Защите от вирусов IPsec не удалось создать состояние, так как достигнуто максимально допустимое число записей в политике.</span><span class="sxs-lookup"><span data-stu-id="8dd90-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**Ошибка \_ IPSec \_ досп \_ кэймод \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-579">13930 (0x366A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-580">Защита от вирусов IPsec получила пакет согласования IPsec для модуля создания ключей, который не разрешен политикой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**Ошибка \_ IPSec \_ досп \_ не \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-582">13931 (0x366B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-583">Защита от вирусов в ОС DoS не включена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**Ошибка \_ IPSec \_ досп \_ Max \_ для \_ \_ \_ очередей IP рателимит**</span><span class="sxs-lookup"><span data-stu-id="8dd90-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-585">13932 (0x366C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-586">Защите от вирусов IPsec не удалось создать очередь за внутренний предел скорости IP-адресов, так как достигнуто максимальное число очередей, разрешенных политикой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена раздел SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-588">14000 (0x36B0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-589">Запрошенный раздел отсутствует в контексте активации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**Ошибка \_ SxS не \_ удается \_ Gen \_ акткткс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-591">14001 (0x36B1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-592">Не удалось запустить приложение, так как его Параллельная конфигурация неверна.</span><span class="sxs-lookup"><span data-stu-id="8dd90-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="8dd90-593">Дополнительные сведения см. в журнале событий приложений или с помощью средства командной строки sxstrace.exe.</span><span class="sxs-lookup"><span data-stu-id="8dd90-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**Ошибка \_ SxS, \_ Недопустимый \_ \_ Формат актктксдата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-595">14002 (0x36B2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-596">Недопустимый формат данных привязки приложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена сборка SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-598">14003 (0x36B3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-599">Сборка, на которую указывает ссылка, не установлена в системе.</span><span class="sxs-lookup"><span data-stu-id="8dd90-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**Ошибка \_ \_ формата манифеста SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-601">14004 (0x36B4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-602">Файл манифеста не начинается с требуемого тега и сведений о форматировании.</span><span class="sxs-lookup"><span data-stu-id="8dd90-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**Ошибка \_ \_ \_ при синтаксическом анализе манифеста SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-604">14005 (0x36B5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-605">Файл манифеста содержит одну или несколько синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="8dd90-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**Ошибка \_ \_ \_ отключения контекста активации \_ SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-607">14006 (0x36B6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-608">Приложение попыталось активировать отключенный контекст активации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена ключ SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-610">14007 (0x36B7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-611">Запрошенный ключ поиска не найден ни в одном из активных контекстов активации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**Ошибка \_ при \_ \_ конфликте версий SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-613">14008 (0x36B8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-614">Версия компонента, необходимая для приложения, конфликтует с другой версией компонента, которая уже активна.</span><span class="sxs-lookup"><span data-stu-id="8dd90-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**Ошибка \_ SxS \_ . \_ неправильный \_ тип раздела**</span><span class="sxs-lookup"><span data-stu-id="8dd90-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-616">14009 (0x36B9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-617">Раздел контекста активации запрошенного типа не соответствует используемому API запроса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**Ошибка \_ при \_ \_ отключении запросов потока SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-619">14010 (0x36BA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-620">Нехватка системных ресурсов требует отключения изолированной активации для текущего потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**Ошибка \_ \_ \_ по умолчанию для процесса SxS \_ уже \_ задана**</span><span class="sxs-lookup"><span data-stu-id="8dd90-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-622">14011 (0x36BB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-623">Не удалось задать контекст активации по умолчанию для процесса, так как уже задан контекст активации по умолчанию процесса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**Ошибка \_ \_ неизвестной \_ группы кодирования SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-625">14012 (0x36BC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-626">Указанный идентификатор группы кодировок не распознан.</span><span class="sxs-lookup"><span data-stu-id="8dd90-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**Ошибка \_ \_ неизвестной \_ кодировки SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-628">14013 (0x36BD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-629">Запрошенная кодировка не распознана.</span><span class="sxs-lookup"><span data-stu-id="8dd90-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**Ошибка \_ SxS. \_ Недопустимый \_ \_ URI пространства имен XML \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-631">14014 (0x36BE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-632">Манифест содержит ссылку на недопустимый URI.</span><span class="sxs-lookup"><span data-stu-id="8dd90-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**Ошибка \_ \_ \_ \_ \_ не установлена зависимость корневого манифеста SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-634">14015 (0x36BF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-635">Манифест приложения содержит ссылку на зависимую сборку, которая не установлена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**Ошибка \_ при \_ \_ \_ \_ \_ установке зависимости конечного манифеста SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-637">14016 (0x36C0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-638">Манифест для сборки, используемой приложением, имеет ссылку на зависимую сборку, которая не установлена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**Ошибка \_ SxS. \_ Недопустимый \_ \_ атрибут удостоверения сборки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-640">14017 (0x36C1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-641">Манифест содержит недопустимый атрибут для удостоверения сборки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**Ошибка \_ \_ манифеста \_ SxS \_ отсутствует \_ необходимое \_ пространство имен по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="8dd90-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-643">14018 (0x36C2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-644">В манифесте отсутствует требуемая спецификация пространства имен по умолчанию для элемента Assembly.</span><span class="sxs-lookup"><span data-stu-id="8dd90-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**Ошибка \_ \_ манифеста SxS. \_ недопустимое \_ требуемое \_ пространство имен по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-646">14019 (0x36C3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-647">Манифест имеет пространство имен по умолчанию, указанное в элементе Assembly, но его значение не равно "urn: schemas-microsoft-com: ASM. v1".</span><span class="sxs-lookup"><span data-stu-id="8dd90-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**Ошибка \_ при \_ \_ \_ перекрестном пути частного манифеста SxS \_ \_ с \_ точкой повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-649">14020 (0x36C4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-650">Проверенный частный манифест превысил путь с неподдерживаемой точкой повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ имя библиотеки DLL \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-652">14021 (0x36C5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-653">Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют файлы с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="8dd90-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ \_ имя виндовкласс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-655">14022 (0x36C6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-656">Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют классы окон с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="8dd90-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**Ошибка \_ при \_ дублировании CLSID для SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-658">14023 (0x36C7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-659">Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют одинаковые идентификаторы CLSID COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="8dd90-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**Ошибка \_ при \_ дублировании \_ идентификатора SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-661">14024 (0x36C8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-662">Два или более компонентов, на которые напрямую или косвенно ссылается манифест приложения, имеют прокси-серверы для одного и того же интерфейса COM идентификаторов IID.</span><span class="sxs-lookup"><span data-stu-id="8dd90-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**Ошибка \_ SxS \_ дублирует \_ тлбид**</span><span class="sxs-lookup"><span data-stu-id="8dd90-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-664">14025 (0x36C9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-665">Два или более компонентов, на которые непосредственно или косвенно ссылается манифест приложения, имеют одинаковые Тлбидс библиотеки типов COM.</span><span class="sxs-lookup"><span data-stu-id="8dd90-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**Ошибка \_ при \_ дублировании \_ идентификатора SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-667">14026 (0x36CA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-668">Два или более компонента, непосредственно или косвенно упоминаемые в манифесте приложения, имеют одинаковые идентификаторы ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="8dd90-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**Ошибка \_ SxS. \_ повторяющееся \_ \_ имя сборки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-670">14027 (0x36CB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-671">Два или более компонента, непосредственно или косвенно упоминаемые в манифесте приложения, являются разными версиями одного и того же компонента, что не разрешено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии хэша файла SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-673">14028 (0x36CC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-674">Файл компонента не соответствует сведениям проверки, присутствующим в манифесте компонента.</span><span class="sxs-lookup"><span data-stu-id="8dd90-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**Ошибка \_ при \_ анализе политики SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-676">14029 (0x36CD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-677">Манифест политики содержит одну или несколько синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="8dd90-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингкуоте**</span><span class="sxs-lookup"><span data-stu-id="8dd90-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-679">14030 (0x36CE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-680">Ошибка анализа манифеста: ожидался строковый литерал, но не найдена открывающая кавычка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**Ошибка \_ SxS \_ XML \_ E \_ комментсинтакс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-682">14031 (0x36CF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-683">Ошибка анализа манифеста: в комментарии использован неверный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="8dd90-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадстартнамечар**</span><span class="sxs-lookup"><span data-stu-id="8dd90-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-685">14032 (0x36D0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-686">Ошибка анализа манифеста: имя было запущено с недопустимым символом.</span><span class="sxs-lookup"><span data-stu-id="8dd90-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**Ошибка \_ SxS \_ XML \_ E \_ баднамечар**</span><span class="sxs-lookup"><span data-stu-id="8dd90-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-688">14033 (0x36D1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-689">Ошибка анализа манифеста: имя содержит недопустимый символ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадчаринстринг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-691">14034 (0x36D2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-692">Ошибка анализа манифеста: строковый литерал содержал недопустимый символ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**Ошибка \_ SxS \_ XML \_ E \_ ксмлдеклсинтакс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-694">14035 (0x36D3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-695">Ошибка анализа манифеста: недопустимый синтаксис объявления XML.</span><span class="sxs-lookup"><span data-stu-id="8dd90-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадчардата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-697">14036 (0x36D4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-698">Ошибка анализа манифеста: в текстовом содержимом обнаружен недопустимый символ.</span><span class="sxs-lookup"><span data-stu-id="8dd90-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингвхитеспаце**</span><span class="sxs-lookup"><span data-stu-id="8dd90-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-700">14037 (0x36D5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-701">Ошибка анализа манифеста: отсутствует обязательный пробел.</span><span class="sxs-lookup"><span data-stu-id="8dd90-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**Ошибка \_ SxS \_ XML \_ E \_ експектингтаженд**</span><span class="sxs-lookup"><span data-stu-id="8dd90-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-703">14038 (0x36D6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-704">Ошибка анализа манифеста: ожидался символ ">".</span><span class="sxs-lookup"><span data-stu-id="8dd90-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингсемиколон**</span><span class="sxs-lookup"><span data-stu-id="8dd90-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-706">14039 (0x36D7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-707">Ошибка анализа манифеста: ожидался символ точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**Ошибка \_ SxS \_ XML \_ E \_ унбаланцедпарен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-709">14040 (0x36D8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-710">Ошибка анализа манифеста: непарные круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**Ошибка \_ SxS \_ XML \_ E \_ интерналеррор**</span><span class="sxs-lookup"><span data-stu-id="8dd90-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-712">14041 (0x36D9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-713">Ошибка анализа манифеста: Внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ непредвиденный \_ пробел**</span><span class="sxs-lookup"><span data-stu-id="8dd90-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-715">14042 (0x36DA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-716">Ошибка анализа манифеста: пробелы в этом месте не разрешены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**Ошибка \_ \_ \_ \_ неполной кодировки SxS XML E \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-718">14043 (0x36DB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-719">Ошибка анализа манифеста: достигнут конец файла в недопустимом состоянии для текущей кодировки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**Ошибка \_ SxS \_ XML \_ E \_ отсутствует \_ скобка**</span><span class="sxs-lookup"><span data-stu-id="8dd90-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-721">14044 (0x36DC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-722">Ошибка анализа манифеста: отсутствует круглая скобка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**Ошибка \_ SxS \_ XML \_ E \_ експектингклосекуоте**</span><span class="sxs-lookup"><span data-stu-id="8dd90-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-724">14045 (0x36DD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-725">Ошибка анализа манифеста: отсутствует одинарная или двойная закрывающая кавычка ( \\ "или \\ ").</span><span class="sxs-lookup"><span data-stu-id="8dd90-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**Ошибка \_ SxS \_ XML \_ E \_ несколько \_ двоеточий**</span><span class="sxs-lookup"><span data-stu-id="8dd90-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-727">14046 (0x36DE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-728">Ошибка анализа манифеста: в имени не допускается несколько двоеточий.</span><span class="sxs-lookup"><span data-stu-id="8dd90-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**Ошибка \_ SxS \_ XML \_ E \_ недопустимое \_ десятичное число**</span><span class="sxs-lookup"><span data-stu-id="8dd90-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-730">14047 (0x36DF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-731">Ошибка анализа манифеста: недопустимый символ для десятичной цифры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**Ошибка \_ SxS \_ XML \_ E \_ недопустимое \_ шестнадцатеричное представление**</span><span class="sxs-lookup"><span data-stu-id="8dd90-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-733">14048 (0x36E0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-734">Ошибка анализа манифеста: недопустимый символ для шестнадцатеричной цифры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимая \_ кодировка Юникод**</span><span class="sxs-lookup"><span data-stu-id="8dd90-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-736">14049 (0x36E1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-737">Ошибка анализа манифеста: недопустимое значение символа Юникода для этой платформы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**Ошибка \_ SxS \_ XML \_ E \_ вхитеспацеоркуестионмарк**</span><span class="sxs-lookup"><span data-stu-id="8dd90-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-739">14050 (0x36E2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-740">Ошибка анализа манифеста: ожидается пробел или "?".</span><span class="sxs-lookup"><span data-stu-id="8dd90-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унекспектедендтаг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-742">14051 (0x36E3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-743">Ошибка анализа манифеста: в этом месте не ожидался конечный тег.</span><span class="sxs-lookup"><span data-stu-id="8dd90-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседтаг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-745">14052 (0x36E4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-746">Ошибка анализа манифеста: следующие теги не закрыты: %1.</span><span class="sxs-lookup"><span data-stu-id="8dd90-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**Ошибка \_ SxS \_ XML \_ E \_ дупликатеаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="8dd90-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-748">14053 (0x36E5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-749">Ошибка анализа манифеста: дублирующийся атрибут.</span><span class="sxs-lookup"><span data-stu-id="8dd90-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**Ошибка \_ SxS \_ XML \_ E \_ мултиплерутс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-751">14054 (0x36E6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-752">Ошибка анализа манифеста: в XML-документе допускается только один элемент верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8dd90-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалидатрутлевел**</span><span class="sxs-lookup"><span data-stu-id="8dd90-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-754">14055 (0x36E7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-755">Ошибка анализа манифеста: недопустимо на верхнем уровне документа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадксмлдекл**</span><span class="sxs-lookup"><span data-stu-id="8dd90-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-757">14056 (0x36E8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-758">Ошибка анализа манифеста: недопустимое объявление XML.</span><span class="sxs-lookup"><span data-stu-id="8dd90-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссингрут**</span><span class="sxs-lookup"><span data-stu-id="8dd90-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-760">14057 (0x36E9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-761">Ошибка анализа манифеста: XML-документ должен иметь элемент верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8dd90-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**Ошибка \_ SxS \_ XML \_ E \_ унекспектедеоф**</span><span class="sxs-lookup"><span data-stu-id="8dd90-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-763">14058 (0x36EA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-764">Ошибка анализа манифеста: непредвиденный конец файла.</span><span class="sxs-lookup"><span data-stu-id="8dd90-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадперефинсубсет**</span><span class="sxs-lookup"><span data-stu-id="8dd90-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-766">14059 (0x36EB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-767">Ошибка анализа манифеста: нельзя использовать сущности параметров внутри объявлений разметки во внутреннем подмножестве.</span><span class="sxs-lookup"><span data-stu-id="8dd90-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседстарттаг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-769">14060 (0x36EC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-770">Ошибка анализа манифеста: элемент не закрыт.</span><span class="sxs-lookup"><span data-stu-id="8dd90-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседендтаг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-772">14061 (0x36ED)</span><span class="sxs-lookup"><span data-stu-id="8dd90-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-773">Ошибка анализа манифеста: в элементе End отсутствовал символ ">".</span><span class="sxs-lookup"><span data-stu-id="8dd90-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседстринг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-775">14062 (0x36EE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-776">Ошибка анализа манифеста: строковый литерал не закрыт.</span><span class="sxs-lookup"><span data-stu-id="8dd90-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседкоммент**</span><span class="sxs-lookup"><span data-stu-id="8dd90-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-778">14063 (0x36EF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-779">Ошибка анализа манифеста: комментарий не закрыт.</span><span class="sxs-lookup"><span data-stu-id="8dd90-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседдекл**</span><span class="sxs-lookup"><span data-stu-id="8dd90-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-781">14064 (0x36F0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-782">Ошибка анализа манифеста: объявление не закрыто.</span><span class="sxs-lookup"><span data-stu-id="8dd90-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**Ошибка \_ SxS \_ XML \_ E \_ унклоседкдата**</span><span class="sxs-lookup"><span data-stu-id="8dd90-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-784">14065 (0x36F1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-785">Ошибка анализа манифеста: раздел CDATA не закрыт.</span><span class="sxs-lookup"><span data-stu-id="8dd90-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**Ошибка \_ SxS \_ XML \_ E \_ ресерведнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="8dd90-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-787">14066 (0x36F2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-788">Ошибка анализа манифеста: префикс пространства имен не может начинаться с зарезервированной строки "XML".</span><span class="sxs-lookup"><span data-stu-id="8dd90-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалиденкодинг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-790">14067 (0x36F3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-791">Ошибка анализа манифеста: система не поддерживает указанную кодировку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**Ошибка \_ SxS \_ XML \_ E \_ инвалидсвитч**</span><span class="sxs-lookup"><span data-stu-id="8dd90-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-793">14068 (0x36F4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-794">Ошибка анализа манифеста: переключение с текущей кодировки на указанную не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8dd90-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**Ошибка \_ SxS \_ XML \_ E \_ бадксмлкасе**</span><span class="sxs-lookup"><span data-stu-id="8dd90-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-796">14069 (0x36F5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-797">Ошибка анализа манифеста: имя "XML" зарезервировано и должно быть указано в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="8dd90-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимый \_ автономный**</span><span class="sxs-lookup"><span data-stu-id="8dd90-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-799">14070 (0x36F6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-800">Ошибка анализа манифеста: Изолированный атрибут должен иметь значение "Yes" или "No".</span><span class="sxs-lookup"><span data-stu-id="8dd90-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**Ошибка \_ SxS \_ XML \_ E \_ непредвиденная \_ Автономная**</span><span class="sxs-lookup"><span data-stu-id="8dd90-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-802">14071 (0x36F7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-803">Ошибка анализа манифеста: Автономный атрибут не может использоваться во внешних сущностях.</span><span class="sxs-lookup"><span data-stu-id="8dd90-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**Ошибка \_ SxS \_ XML \_ E \_ Недопустимая \_ версия**</span><span class="sxs-lookup"><span data-stu-id="8dd90-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-805">14072 (0x36F8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-806">Ошибка анализа манифеста: недопустимый номер версии.</span><span class="sxs-lookup"><span data-stu-id="8dd90-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**Ошибка \_ SxS \_ XML \_ E \_ миссинжекуалс**</span><span class="sxs-lookup"><span data-stu-id="8dd90-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-808">14073 (0x36F9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-809">Ошибка анализа манифеста: отсутствует знак равенства между атрибутом и значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="8dd90-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**Ошибка \_ \_ \_ при восстановлении защиты SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-811">14074 (0x36FA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-812">Ошибка защиты сборки: не удалось восстановить указанную сборку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**Ошибка \_ \_ открытого ключа защиты SxS, \_ \_ \_ слишком \_ короткий**</span><span class="sxs-lookup"><span data-stu-id="8dd90-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-814">14075 (0x36FB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-815">Ошибка защиты сборки: открытый ключ для сборки слишком короткий, чтобы быть разрешенным.</span><span class="sxs-lookup"><span data-stu-id="8dd90-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**Ошибка \_ \_ \_ \_ \_ Недопустимый каталог защиты SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-817">14076 (0x36FC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-818">Ошибка защиты сборки: Каталог для сборки является недопустимым или не соответствует манифесту сборки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**Ошибка \_ \_ переводимого значения HRESULT при непреобразовании SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-820">14077 (0x36FD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-821">Не удалось преобразовать значение HRESULT в соответствующий код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="8dd90-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**Ошибка \_ в \_ \_ файле каталога \_ защиты \_ SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-823">14078 (0x36FE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-824">Ошибка защиты сборки: отсутствует каталог для сборки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**Ошибка \_ SxS \_ . \_ отсутствует \_ атрибут удостоверения сборки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-826">14079 (0x36FF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-827">В указанном удостоверении сборки отсутствует один или несколько атрибутов, которые должны присутствовать в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="8dd90-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ \_ имя атрибута \_ удостоверения сборки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="8dd90-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-830">Предоставленное удостоверение сборки имеет одно или несколько имен атрибутов, содержащих символы, запрещенные в именах XML.</span><span class="sxs-lookup"><span data-stu-id="8dd90-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**Ошибка \_ \_ сборки SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="8dd90-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-833">Не удалось найти сборку, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**Ошибка \_ SxS, \_ поврежденный \_ \_ стек активации**</span><span class="sxs-lookup"><span data-stu-id="8dd90-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="8dd90-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-836">Стек активации контекста активации для выполняющегося потока поврежден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**Ошибка \_ при \_ повреждении SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="8dd90-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-839">Метаданные изоляции приложения для этого процесса или потока были повреждены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**Ошибка \_ при \_ ранних \_ деактивации SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="8dd90-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-842">Деактивируемый контекст активации не является самой последней активацией.</span><span class="sxs-lookup"><span data-stu-id="8dd90-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**Ошибка \_ \_ неправильной \_ деактивации SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="8dd90-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-845">Деактивируемый контекст активации неактивен для текущего потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**Ошибка \_ при \_ множественной \_ деактивации SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="8dd90-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-848">Деактивируемый контекст активации уже деактивирован.</span><span class="sxs-lookup"><span data-stu-id="8dd90-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**Ошибка \_ при \_ \_ завершении завершения процесса SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="8dd90-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-851">Компонент, используемый средством изоляции, запросил завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="8dd90-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**Ошибка \_ \_ \_ контекста активации выпуска \_ SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="8dd90-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-854">Компонент режима ядра освобождает ссылку на контекст активации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**Ошибка \_ SxS \_ . \_ \_ контекст активации по умолчанию для системы \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="8dd90-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-857">Не удалось создать контекст активации системной сборки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dd90-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ значение атрибута Identity \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-859">14090 (0x370A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-860">Значение атрибута в удостоверении находится за пределами допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dd90-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**Ошибка \_ SxS \_ недопустимое \_ \_ имя атрибута удостоверения \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-862">14091 (0x370B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-863">Имя атрибута в удостоверении находится за пределами допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dd90-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**Ошибка \_ \_ \_ дублирования атрибута удостоверения SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-865">14092 (0x370C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-866">Удостоверение содержит два определения для одного и того же атрибута.</span><span class="sxs-lookup"><span data-stu-id="8dd90-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**Ошибка \_ \_ \_ синтаксического анализа удостоверения SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-868">14093 (0x370D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-869">Строка удостоверения имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="8dd90-869">The identity string is malformed.</span></span> <span data-ttu-id="8dd90-870">Это может быть вызвано завершающей запятой, более чем двумя неименованными атрибутами, отсутствием имени атрибута или отсутствующим значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="8dd90-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**Ошибка при \_ оформлении \_ строки подстановки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-872">14094 (0x370E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-873">Строка, содержащая локализованное подставляемое содержимое, имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="8dd90-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="8dd90-874">За символом доллара ($) следует не левая круглая скобка или другой знак доллара, либо правая скобки подстановки не найдены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**Ошибка \_ SxS \_ . \_ неправильный \_ токен открытого ключа \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-876">14095 (0x370F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-877">Токен открытого ключа не соответствует указанному открытому ключу.</span><span class="sxs-lookup"><span data-stu-id="8dd90-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**Ошибка при \_ НЕсопоставленной \_ строке подстановки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="8dd90-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-880">Строка подстановки не имеет сопоставления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**Ошибка \_ " \_ Сборка SxS \_ не \_ заблокирована"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-882">14097 (0x3711)</span><span class="sxs-lookup"><span data-stu-id="8dd90-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-883">Перед выполнением запроса компонент должен быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="8dd90-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**Ошибка \_ при \_ \_ повреждении хранилища компонентов SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="8dd90-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-886">Хранилище компонентов повреждено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**Ошибка \_ расширенного \_ установщика ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="8dd90-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-889">Сбой расширенного установщика во время установки или обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8dd90-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**Ошибка \_ при \_ несоответствии кодировки XML \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="8dd90-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-892">Кодировка символов в объявлении XML не соответствует кодировке, используемой в документе.</span><span class="sxs-lookup"><span data-stu-id="8dd90-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**Ошибка \_ \_ идентичности манифеста SxS, \_ \_ \_ но \_ содержимое \_ отличается**</span><span class="sxs-lookup"><span data-stu-id="8dd90-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="8dd90-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-895">Удостоверения манифестов идентичны, но их содержимое отличается.</span><span class="sxs-lookup"><span data-stu-id="8dd90-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ОШИБКИ \_ , \_ отличные от удостоверений SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="8dd90-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-898">Идентификаторы компонентов различаются.</span><span class="sxs-lookup"><span data-stu-id="8dd90-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**Ошибка \_ \_ сборки SxS \_ \_ не является \_ \_ развертыванием**</span><span class="sxs-lookup"><span data-stu-id="8dd90-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="8dd90-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-901">Сборка не является развертыванием.</span><span class="sxs-lookup"><span data-stu-id="8dd90-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**Ошибка \_ SxS. \_ файл \_ не является \_ частью \_ \_ сборки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="8dd90-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-904">Файл не является частью сборки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**Ошибка \_ \_ \_ слишком большой манифест \_ SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="8dd90-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-907">Размер манифеста превышает максимально допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**Ошибка \_ \_ \_ не \_ зарегистрирована параметр SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-909">14106 (0x371A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-910">Параметр не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="8dd90-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**Ошибка \_ \_ \_ неполной закрытия транзакции SxS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-912">14107 (0x371B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-913">Отсутствует один или несколько обязательных элементов транзакции.</span><span class="sxs-lookup"><span data-stu-id="8dd90-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**Ошибка \_ \_ \_ при выполнении установщика примитива SMI \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-915">14108 (0x371C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-916">Сбой установщика примитива SMI во время установки или обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8dd90-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**Ошибка \_ \_ \_ при выполнении универсальной команды**</span><span class="sxs-lookup"><span data-stu-id="8dd90-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-918">14109 (0x371D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-919">Исполняемый файл универсальной команды вернул результат, который указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**Ошибка \_ при \_ \_ отсутствии хэша \_ файла SxS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-921">14110 (0x371E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-922">В манифесте компонента отсутствуют сведения о проверке файлов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Ошибка \_ evt \_ недопустимого \_ \_ пути канала**</span><span class="sxs-lookup"><span data-stu-id="8dd90-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-924">15000 (0x3A98)</span><span class="sxs-lookup"><span data-stu-id="8dd90-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-925">Указан недопустимый путь к каналу.</span><span class="sxs-lookup"><span data-stu-id="8dd90-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Ошибка \_ \_ недопустимого \_ запроса evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-927">15001 (0x3A99)</span><span class="sxs-lookup"><span data-stu-id="8dd90-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-928">Указан недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="8dd90-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Ошибка \_ \_ \_ \_ не найдены метаданные издателя \_ evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-930">15002 (0x3A9A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-931">Не удается найти метаданные издателя в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="8dd90-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ шаблон событий Error \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-933">15003 (0x3A9B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-934">Не удается найти шаблон для определения события в ресурсе (ошибка = %1).</span><span class="sxs-lookup"><span data-stu-id="8dd90-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**Ошибка \_ evt \_ недопустимое \_ \_ имя издателя**</span><span class="sxs-lookup"><span data-stu-id="8dd90-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-936">15004 (0x3A9C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-937">Указано недопустимое имя издателя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Ошибка \_ evt " \_ недопустимые \_ \_ данные события"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-939">15005 (0x3A9D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-940">Данные события, создаваемые издателем, несовместимы с определением шаблона события в манифесте издателя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_канал ошибки \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-942">15007 (0x3A9F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-943">Не удалось найти указанный канал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-943">The specified channel could not be found.</span></span> <span data-ttu-id="8dd90-944">Проверьте конфигурацию канала.</span><span class="sxs-lookup"><span data-stu-id="8dd90-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**Ошибка \_ evt \_ неправильно сформированный \_ XML- \_ текст**</span><span class="sxs-lookup"><span data-stu-id="8dd90-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-946">15008 (0x3AA0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-947">Указанный XML-текст имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="8dd90-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="8dd90-948">Дополнительные сведения см. в разделе Расширенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8dd90-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Ошибка \_ при \_ подписке evt \_ на \_ прямой \_ канал**</span><span class="sxs-lookup"><span data-stu-id="8dd90-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-950">15009 (0x3AA1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-951">Вызывающая сторона пытается подписываться на прямой канал, что недопустимо.</span><span class="sxs-lookup"><span data-stu-id="8dd90-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="8dd90-952">События прямого канала переходят непосредственно в файл журнала и не могут быть подписаны на.</span><span class="sxs-lookup"><span data-stu-id="8dd90-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Ошибка \_ \_ конфигурации evt \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-954">15010 (0x3AA2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-955">Ошибка конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**\_ \_ \_ неактуальный результат \_ запроса "ошибка evt"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-957">15011 (0x3AA3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-958">Результат запроса устарел или недопустим.</span><span class="sxs-lookup"><span data-stu-id="8dd90-958">The query result is stale / invalid.</span></span> <span data-ttu-id="8dd90-959">Это может быть вызвано очисткой или перебором журнала после создания результата запроса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="8dd90-960">Пользователи должны решить этот код, отпустив объект результата запроса и повторно выполнив запрос.</span><span class="sxs-lookup"><span data-stu-id="8dd90-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ошибочное \_ \_ \_ значение результата \_ запроса \_ "ошибка evt"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-962">15012 (0x3AA4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-963">Результат запроса в настоящее время находится в недопустимой позиции.</span><span class="sxs-lookup"><span data-stu-id="8dd90-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Ошибка \_ EVT, \_ не \_ проверяющая \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="8dd90-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-965">15013 (0x3AA5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-966">Зарегистрированный MSXML не поддерживает проверку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Ошибка \_ evt \_ Filter \_ алреадископед**</span><span class="sxs-lookup"><span data-stu-id="8dd90-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-968">15014 (0x3AA6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-969">За выражением может следовать только изменение операции Scope только в том случае, если оно является набором узлов и еще не является частью другого изменения области действия.</span><span class="sxs-lookup"><span data-stu-id="8dd90-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Ошибка \_ evt \_ Filter \_ нотелтсет**</span><span class="sxs-lookup"><span data-stu-id="8dd90-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-971">15015 (0x3AA7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-972">Невозможно выполнить шаг с термином, который не представляет набор элементов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Ошибка \_ evt \_ Filter \_ инварг**</span><span class="sxs-lookup"><span data-stu-id="8dd90-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-974">15016 (0x3AA8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-975">Аргументы левой стороны к бинарным операторам должны быть либо атрибутами, либо узлами, либо переменными и аргументами правой части должны быть константы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Ошибка \_ evt \_ Filter \_ инвтест**</span><span class="sxs-lookup"><span data-stu-id="8dd90-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-977">15017 (0x3AA9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-978">Операция шага должна затрагивать либо проверку узла, либо, в случае предиката, алгебраические выражение, по которому будет проверяться каждый узел в наборе узлов, идентифицируемом предшествующим набором узлов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**Ошибка \_ evt \_ Filter \_ инвтипе**</span><span class="sxs-lookup"><span data-stu-id="8dd90-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-980">15018 (0x3AAA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-981">Этот тип данных в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8dd90-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Ошибка \_ evt \_ Filter \_ парсирр**</span><span class="sxs-lookup"><span data-stu-id="8dd90-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-983">15019 (0x3AAB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-984">Синтаксическая ошибка в позиции %1! d!.</span><span class="sxs-lookup"><span data-stu-id="8dd90-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Ошибка \_ evt \_ Filter \_ унсуппортедоп**</span><span class="sxs-lookup"><span data-stu-id="8dd90-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-986">15020 (0x3AAC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-987">Этот оператор не поддерживается этой реализацией фильтра.</span><span class="sxs-lookup"><span data-stu-id="8dd90-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Ошибка \_ evt \_ Filter \_ унекспектедтокен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-989">15021 (0x3AAD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-990">Обнаружена непредвиденная лексема.</span><span class="sxs-lookup"><span data-stu-id="8dd90-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Ошибка \_ evt \_ недопустимой \_ операции \_ через \_ включенный \_ прямой \_ канал**</span><span class="sxs-lookup"><span data-stu-id="8dd90-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-992">15022 (0x3AAE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-993">Запрошенная операция не может быть выполнена через включенный прямой канал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="8dd90-994">Прежде чем выполнять запрошенную операцию, необходимо отключить канал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства канала \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-996">15023 (0x3AAF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-997">Свойство канала %1! s!</span><span class="sxs-lookup"><span data-stu-id="8dd90-997">Channel property %1!s!</span></span> <span data-ttu-id="8dd90-998">содержит недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-998">contains invalid value.</span></span> <span data-ttu-id="8dd90-999">Значение имеет недопустимый тип, находится вне допустимого диапазона, не может быть обновлено или не поддерживается этим типом канала.</span><span class="sxs-lookup"><span data-stu-id="8dd90-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства издателя \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1001">15024 (0x3AB0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1002">Свойство издателя %1! s!</span><span class="sxs-lookup"><span data-stu-id="8dd90-1002">Publisher property %1!s!</span></span> <span data-ttu-id="8dd90-1003">содержит недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1003">contains invalid value.</span></span> <span data-ttu-id="8dd90-1004">Значение имеет недопустимый тип, находится вне допустимого диапазона, не может быть обновлено или не поддерживается издателем этого типа.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**Ошибка \_ при \_ \_ активации канала \_ evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1006">15025 (0x3AB1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1007">Не удается активировать канал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**\_ \_ \_ слишком \_ сложный фильтр evt ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1009">15026 (0x3AB2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1010">Выражение XPath превысило поддерживаемую сложность.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="8dd90-1011">Симплифи его или разделите его на два или более простых выражения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**сообщение с ошибкой \_ evt \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1013">15027 (0x3AB3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1014">ресурс сообщения существует, но сообщение не найдено в строке или таблице сообщений.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ идентификатор сообщения ошибки \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1016">15028 (0x3AB4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1017">Не удалось найти идентификатор сообщения для требуемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Ошибка \_ EVT, \_ неразрешенное \_ значение \_ INSERT**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1019">15029 (0x3AB5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1020">Не удалось найти строку подстановки для индекса вставки (%1).</span><span class="sxs-lookup"><span data-stu-id="8dd90-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Ошибка \_ EVT, \_ неразрешенная \_ \_ Вставка параметра**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1022">15030 (0x3AB6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1023">Не удалось найти строку описания для ссылки на параметр (%1).</span><span class="sxs-lookup"><span data-stu-id="8dd90-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_ \_ \_ достигнуто максимальное число вставок \_ ошибок evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1025">15031 (0x3AB7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1026">Достигнуто максимальное число замен.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_Определение события "ошибка evt" \_ \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1028">15032 (0x3AB8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1029">Не удалось найти определение события для идентификатора события (%1).</span><span class="sxs-lookup"><span data-stu-id="8dd90-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ не удалось найти языковой стандарт сообщений \_ с ошибкой evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1031">15033 (0x3AB9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1032">Не указан ресурс, зависящий от языкового стандарта для требуемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**\_ \_ \_ слишком \_ старая версия evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1034">15034 (0x3ABA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1035">Ресурс слишком старый, чтобы быть совместимым.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**\_ \_ \_ слишком \_ Новая версия ошибки evt**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1037">15035 (0x3ABB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1038">Ресурс слишком новый для совместимости.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Ошибка \_ evt \_ не \_ удается \_ открыть \_ канал \_ запроса**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1040">15036 (0x3ABC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1041">Канал по индексу %1! d!</span><span class="sxs-lookup"><span data-stu-id="8dd90-1041">The channel at index %1!d!</span></span> <span data-ttu-id="8dd90-1042">не удается открыть запрос.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Ошибка \_ " \_ Издатель evt \_ отключен"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1044">15037 (0x3ABD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1045">Издатель отключен, и его ресурс недоступен.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="8dd90-1046">Обычно это происходит, когда издатель находится в процессе удаления или обновления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ОШИБОЧный \_ \_ Фильтр evt \_ за пределами \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1048">15038 (0x3ABE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1049">Попытка создать числовой тип, который находится за пределами допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**Ошибка \_ \_ \_ не удается активировать подписку EC \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1051">15080 (0x3AE8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1052">Не удается активировать подписку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**Ошибка \_ EC — \_ Журнал \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1054">15081 (0x3AE9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1055">Журнал подписки находится в отключенном состоянии и не может использоваться для перенаправления событий в.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="8dd90-1056">Прежде чем активировать подписку, необходимо включить журнал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**Ошибка \_ EC \_ цикличное \_ перенаправление**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1058">15082 (0x3AEA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1059">При пересылке событий с локального компьютера на себя, запрос подписки не может содержать целевой журнал подписки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**Ошибка \_ EC \_ кредсторе \_ Full**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1061">15083 (0x3AEB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1062">Хранилище учетных данных, используемое для сохранения учетных данных, заполнено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**Ошибка \_ EC \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1064">15084 (0x3AEC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1065">Учетные данные, используемые этой подпиской, невозможно найти в хранилище учетных данных.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**Ошибка \_ EC \_ нет \_ активного \_ канала**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1067">15085 (0x3AED)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1068">Для запроса не найден активный канал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**файл MUI с ОШИБКАми \_ \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1070">15100 (0x3AFC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1071">Загрузчику ресурсов не удалось найти файл MUI.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**Ошибка \_ \_ недопустимого \_ файла MUI**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1073">15101 (0x3AFD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1074">Загрузчику ресурсов не удалось загрузить MUI-файл, так как файл не прошел проверку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**Ошибка \_ MUI \_ Недопустимая \_ \_ Конфигурация RC**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1076">15102 (0x3AFE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1077">Манифест RC поврежден с данными мусора или неподдерживаемой версией, или отсутствует обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**Ошибка \_ MUI \_ недопустимое \_ имя локали \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1079">15103 (0x3AFF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1080">Манифест версии-КАНДИДАТа имеет недопустимое имя языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**Ошибка \_ MUI \_ недопустимое \_ \_ имя ултиматефаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1082">15104 (0x3B00)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1083">Манифест версии-КАНДИДАТа имеет недопустимое имя ултиматефаллбакк.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**файл MUI с ОШИБКАми \_ \_ \_ не \_ загружен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1085">15105 (0x3B01)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1086">Кэш загрузчика ресурсов не загрузил запись MUI.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_ \_ Перечисление \_ пользовательских ресурсов ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1088">15106 (0x3B02)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1089">Пользователь остановил перечисление ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**Ошибка \_ многоязыкового интерфейса пользователя \_ интлсеттингс \_ уиланг \_ не \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1091">15107 (0x3B03)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1092">Не удалось установить язык пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**Ошибка \_ многоязыкового интерфейса пользователя \_ интлсеттингс \_ недопустимое \_ имя локали \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1094">15108 (0x3B04)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1095">Не удалось установить языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**Ошибка \_ управления записями сообщений \_ среды выполнения \_ без \_ по умолчанию \_ или \_ нейтрального \_ ресурса**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1097">15110 (0x3B06)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1098">Ресурс не имеет значения по умолчанию или нейтрального.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**Ошибка \_ управления записями сообщений \_ Недопустимая \_ файлу priconfig**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1100">15111 (0x3B07)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1101">Недопустимый файл конфигурации PRI.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ \_ Тип файла**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1103">15112 (0x3B08)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1104">Недопустимый тип файла.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**Ошибка \_ управления записями сообщений \_ неизвестный \_ квалификатор**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1106">15113 (0x3B09)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1107">Неизвестный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**Ошибка \_ управления записями сообщений \_ недопустимое \_ значение квалификатора \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1109">15114 (0x3B0A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1110">Недопустимое значение квалификатора.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**Ошибка \_ управления записями сообщений \_ нет \_ кандидатов**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1112">15115 (0x3B0B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1113">Кандидатов не найдены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**Ошибка \_ управления записями сообщений \_ нет \_ совпадения \_ или \_ кандидата по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1115">15116 (0x3B0C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1116">Ресаурцемап или Намедресаурце имеет элемент, который не имеет по умолчанию или нейтрального ресурса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии типа ресурса управления записями сообщений \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1118">15117 (0x3B0D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1119">Недопустимый тип Ресаурцекандидате.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**Ошибка \_ управления записями сообщений \_ дублирование \_ \_ имени схемы**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1121">15118 (0x3B0E)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1122">Повторяющаяся схема ресурса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**Ошибка \_ управления записями сообщений \_ повторяющаяся \_ запись**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1124">15119 (0x3B0F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1125">Повторяющаяся запись.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ \_ идентификатор ресурса**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1127">15120 (0x3B10)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1128">Недопустимый идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**Ошибка \_ управления записями сообщений \_ путь к файлу \_ слишком \_ длинный**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1130">15121 (0x3B11)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1131">Слишком длинный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**Ошибка \_ управления записями сообщений \_ неподдерживаемый \_ \_ тип каталога**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1133">15122 (0x3B12)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1134">Неподдерживаемый тип каталога.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ PRI \_ файл**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1136">15126 (0x3B16)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1137">Недопустимый PRI файл.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**Ошибка \_ управления записями сообщений. \_ именованный \_ ресурс \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1139">15127 (0x3B17)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1140">Намедресаурце не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**Ошибка \_ управления записями сообщений \_ . \_ не \_ удалось найти карту**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1142">15135 (0x3B1F)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1143">Ресаурцемап не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**Ошибка \_ управления записями сообщений \_ неподдерживаемый \_ \_ Тип профиля**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1145">15136 (0x3B20)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1146">Неподдерживаемый тип профиля MRT.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**Ошибка \_ управления записями сообщений \_ Недопустимый \_ оператор квалификатора \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1148">15137 (0x3B21)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1149">Недопустимый оператор квалификатора.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**Ошибка \_ управления записями сообщений \_ \_ значение квалификатора неопределенности \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1151">15138 (0x3B22)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1152">Не удалось определить значение квалификатора, или значение квалификатора не задано.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**Ошибка \_ управления записями сообщений. \_ Автослияние \_ включено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1154">15139 (0x3B23)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1155">Автослияние включено в PRI-файле.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**Ошибка \_ управления записями сообщений \_ слишком \_ много \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1157">15140 (0x3B24)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1158">Для пакета определено слишком много ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**Ошибка \_ MCA. \_ Недопустимая \_ \_ строка возможностей**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1160">15200 (0x3B60)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1161">Монитор вернул строку возможностей DDC/CI, которая не соответствует спецификации доступа. Bus 3,0, DDC/CI 1,1 или MCCS 2 Revision 1.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**Ошибка \_ MCA, \_ Недопустимая \_ \_ версия**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1163">15201 (0x3B61)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1164">Код версии-0xDF (версия-перечислитель монитора) вернул недопустимое значение версии.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**\_монитор ошибок \_ MCA \_ нарушает \_ \_ спецификацию MCCS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1166">15202 (0x3B62)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1167">Монитор не соответствует спецификации MCCS, которую он требует для поддержки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии версии MCA MCCS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1169">15203 (0x3B63)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1170">Версия MCCS в \_ функции MCCS ver монитора не соответствует версии MCCS, которую монитор сообщает при использовании кода версии-0xDF.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**Ошибка \_ MCA \_ неподдерживаемая \_ \_ версия MCCS**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1172">15204 (0x3B64)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1173">API конфигурации монитора работает только с мониторами, которые поддерживают спецификацию MCCS 1,0, спецификация MCCS 2,0 или MCCS 2,0 редакции 1.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**\_ \_ Внутренняя ошибка MCA \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1175">15205 (0x3B65)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1176">Произошла внутренняя ошибка API настройки монитора.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**Ошибка \_ MCA \_ возвратила недопустимый \_ \_ тип технологии \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1178">15206 (0x3B66)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1179">Монитор вернул недопустимый тип технологии мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="8dd90-1180">Примеры типов технологий мониторинга: CRT, плазменный и ЖК-монитор (TFT).</span><span class="sxs-lookup"><span data-stu-id="8dd90-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="8dd90-1181">Эта ошибка означает, что монитор нарушил спецификацию MCCS 2,0 или MCCS 2,0 Revision 1.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**Ошибка \_ при \_ неподдерживаемой \_ цветовой \_ температуре MCA**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1183">15207 (0x3B67)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1184">Вызывающий объект [**сетмониторколортемпературе**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) указал цветовую температуру, которую текущий монитор не поддерживал.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="8dd90-1185">Эта ошибка означает, что монитор нарушил спецификацию MCCS 2,0 или MCCS 2,0 Revision 1.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**Ошибка \_ неоднозначных \_ системных \_ устройств**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1187">15250 (0x3B92)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1188">Не удается определить запрошенное системное устройство из-за нескольких неразличимых устройств, которые могут соответствовать критериям идентификации.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_системное устройство с ошибками \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1190">15299 (0x3BC3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1191">Не удается найти запрошенное системное устройство.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_хэш ошибок \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1193">15300 (0x3BC4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1194">Создание хэша для указанной версии хэша и типа хэша не включено на сервере.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_хэш ошибки \_ отсутствует \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1196">15301 (0x3BC5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1197">Хэш, запрошенный с сервера, недоступен или больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**Ошибка \_ \_ \_ \_ не зарегистрирована вторичный поставщик IC \_ .**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1199">15321 (0x3BD9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1200">Экземпляр дополнительного контроллера прерываний, управляющий указанным прерыванием, не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**Ошибка \_ \_ \_ недопустимых сведений о клиенте GPIO \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1202">15322 (0x3BDA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1203">Недопустимые сведения, предоставленные драйвером GPIO Client.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**Ошибка \_ " \_ версия GPIO \_ не \_ поддерживается"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1205">15323 (0x3BDB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1206">Версия, указанная драйвером GPIO Client, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**Ошибка \_ GPIO — \_ Недопустимый \_ \_ Пакет регистрации**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1208">15324 (0x3BDC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1209">Недопустимый регистрационный пакет, предоставленный драйвером GPIO Client.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**Ошибка \_ GPIO. \_ операция \_ запрещена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1211">15325 (0x3BDD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1212">Запрошенная операция не поддерживается для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**Ошибка \_ GPIO \_ несовместимого \_ \_ режима подключения**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1214">15326 (0x3BDE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1215">Запрошенный режим подключения конфликтует с существующим режимом на одном или нескольких указанных ПИН-кодах.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**Ошибка \_ " \_ прерывание GPIO уже снято с \_ \_ маски"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1217">15327 (0x3BDF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1218">Прерывание, запрошенное для снятия маски, не замаскировано.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**Ошибка \_ не может \_ Переключить \_ RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1220">15400 (0x3C28)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1221">Не удается успешно завершить запрошенный параметр уровня выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**Ошибка \_ недопустимого \_ \_ параметра RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1223">15401 (0x3C29)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1224">Служба имеет недопустимый параметр уровня выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="8dd90-1225">Уровень выполнения для службы не должен быть выше уровня выполнения зависимых служб.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**Ошибка \_ RUNLEVEL \_ \_ время ожидания переключения**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1227">15402 (0x3C2A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1228">Не удается успешно выполнить запрошенный параметр уровня выполнения, так как одна или несколько служб не будут перезапущены или перезагружены в течение указанного времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**Ошибка \_ RUNLEVEL \_ \_ время ожидания агента коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1230">15403 (0x3C2B)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1231">Агент переключения уровня выполнения не ответил в течение указанного времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**Ошибка \_ \_ \_ при выполнении переключения \_ RUNLEVEL**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1233">15404 (0x3C2C)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1234">В настоящее время выполняется переключение уровня выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_ \_ сбой при \_ автозапуске служб ошибок**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1236">15405 (0x3C2D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1237">Не удалось запустить одну или несколько служб на этапе запуска службы коммутатора уровня выполнения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**Ошибка \_ при \_ \_ ожидании завершения задачи com \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1239">15501 (0x3C8D)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1240">Запрос на остановку задачи не может быть выполнен немедленно, так как для выполнения задачи требуется больше времени для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**Ошибка \_ \_ при установке открытого \_ пакета \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1242">15600 (0x3CF0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1243">Не удалось открыть пакет.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**Ошибка при \_ установке \_ пакета \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1245">15601 (0x3CF1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1246">Пакет не найден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**Ошибка при \_ установке \_ недопустимого \_ пакета**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1248">15602 (0x3CF2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1249">Недопустимые данные пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**Ошибка \_ \_ при установке разрешения \_ зависимости \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1251">15603 (0x3CF3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1252">Сбой пакета обновлений, зависимости или проверки конфликтов.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**Ошибка при \_ установке \_ нехватки места на \_ \_ диске \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1254">15604 (0x3CF4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1255">На компьютере недостаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="8dd90-1256">Освободите место и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**Ошибка \_ \_ при установке сетевого \_ сбоя**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1258">15605 (0x3CF5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1259">При скачивании продукта возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**Ошибка \_ \_ при регистрации \_ установки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1261">15606 (0x3CF6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1262">Не удалось зарегистрировать пакет.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**Ошибка \_ при отмене \_ регистрации установки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1264">15607 (0x3CF7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1265">Не удалось отменить регистрацию пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**Ошибка при \_ установке \_ "Отмена"**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1267">15608 (0x3CF8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1268">Пользователь отменил запрос на установку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**Ошибка \_ \_ при установке**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1270">15609 (0x3CF9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1271">Сбой установки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1271">Install failed.</span></span> <span data-ttu-id="8dd90-1272">Обратитесь к поставщику программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**Ошибка \_ \_ при удалении**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1274">15610 (0x3CFA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1275">Сбой удаления.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1275">Removal failed.</span></span> <span data-ttu-id="8dd90-1276">Обратитесь к поставщику программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**\_пакет ошибок \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1278">15611 (0x3CFB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1279">Указанный пакет уже установлен, и переустановка пакета была заблокирована.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="8dd90-1280">Дополнительные сведения см. в журнале событий AppXDeployment-Server.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**Ошибка \_ требует \_ исправления**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1282">15612 (0x3CFC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1283">Не удается запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1283">The application cannot be started.</span></span> <span data-ttu-id="8dd90-1284">Попробуйте переустановить приложение, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**Ошибка \_ \_ при установке необходимого компонента \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1286">15613 (0x3CFD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1287">Не удалось удовлетворить необходимым требованиям для установки.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**\_ \_ репозиторий пакета ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1289">15614 (0x3CFE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1290">Репозиторий пакетов поврежден.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**Ошибка \_ \_ при установке \_ сбоя политики**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1292">15615 (0x3CFF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1293">Для установки этого приложения требуется либо лицензия разработчика Windows, либо система, поддерживающая загрузку неопубликованных приложений.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**Ошибка \_ при \_ обновлении пакета**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1295">15616 (0x3D00)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1296">Невозможно запустить приложение, так как оно сейчас обновляется.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_развертывание ошибок \_ заблокировано \_ \_ политикой**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1298">15617 (0x3D01)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1299">Операция развертывания пакета заблокирована политикой.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="8dd90-1300">Обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_используемые пакеты \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1302">15618 (0x3D02)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1303">Не удалось установить пакет, так как ресурсы, которые он изменяет, сейчас используются.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**\_файл восстановления \_ ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1305">15619 (0x3D03)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1306">Не удалось восстановить пакет, так как необходимые данные для восстановления повреждены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**Ошибка \_ недопустимой \_ промежуточной \_ подписи**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1308">15620 (0x3D04)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1309">Сигнатура недопустима.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1309">The signature is invalid.</span></span> <span data-ttu-id="8dd90-1310">Для регистрации в режиме разработчика AppxSignature. p7x и AppxBlockMap.xml должны быть допустимыми или отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**Ошибка \_ \_ при удалении \_ существующего \_ хранилища \_ APPLICATIONDATA**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1312">15621 (0x3D05)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1313">Произошла ошибка при удалении ранее существующих данных приложения пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**Ошибка \_ при \_ установке \_ понижения уровня пакета**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1315">15622 (0x3D06)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1316">Не удалось установить пакет, поскольку уже установлена более поздняя версия этого пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**\_система ошибок \_ требует \_ исправления**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1318">15623 (0x3D07)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1319">Обнаружена ошибка в системном двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="8dd90-1320">Попробуйте обновить компьютер, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**Ошибка \_ \_ проверки целостности APPX в \_ \_ CLR \_ Ngen**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1322">15624 (0x3D08)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1323">В системе обнаружен поврежденный двоичный файл среды CLR NGEN.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_ \_ поврежден файл устойчивости к ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1325">15625 (0x3D09)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1326">Не удалось возобновить операцию, так как необходимые данные для восстановления повреждены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**Ошибка \_ при \_ установке \_ службы брандмауэра \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1328">15626 (0x3D0A)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1329">Не удалось установить пакет, так как служба брандмауэра Windows не запущена.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="8dd90-1330">Включите службу брандмауэра Windows и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_Ошибка APPMODEL \_ без \_ пакета**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1332">15700 (0x3D54)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1333">Процесс не имеет удостоверения пакета.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Среда выполнения пакета с ошибками APPMODEL \_ \_ \_ повреждена**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1335">15701 (0x3D55)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1336">Сведения о среде выполнения пакета повреждены.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_ \_ удостоверение пакета ошибок APPMODEL \_ \_ повреждено**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1338">15702 (0x3D56)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1339">Удостоверение пакета повреждено.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**\_Ошибка APPMODEL \_ нет \_ приложения**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1341">15703 (0x3D57)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1342">Процесс не имеет удостоверения приложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**Ошибка \_ \_ \_ хранилища при загрузке \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1344">15800 (0x3DB8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1345">Не удалось загрузить хранилище состояний.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ \_ сбой при получении версии \_ состояния ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1347">15801 (0x3DB9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1348">Не удалось получить версию состояния для приложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**Ошибка \_ \_ при установке \_ версии состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1350">15802 (0x3DBA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1351">Не удалось задать версию состояния для приложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**Ошибка \_ \_ структурированного \_ сброса состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1353">15803 (0x3DBB)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1354">Не удалось сбросить структурированное состояние приложения.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**Ошибка \_ \_ при открытии \_ контейнера состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1356">15804 (0x3DBC)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1357">Диспетчеру состояний не удалось открыть контейнер.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**Ошибка \_ \_ при создании \_ контейнера состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1359">15805 (0x3DBD)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1360">Диспетчеру состояний не удалось создать контейнер.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**Ошибка \_ \_ при удалении \_ контейнера состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1362">15806 (0x3DBE)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1363">Диспетчеру состояний не удалось удалить контейнер.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_ \_ \_ Сбой настройки чтения состояния \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1365">15807 (0x3DBF)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1366">Диспетчеру состояний не удалось прочитать параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ \_ Сбой настройки записи состояния \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1368">15808 (0x3DC0)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1369">Диспетчеру состояний не удалось записать параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**Ошибка \_ \_ при удалении \_ параметра состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1371">15809 (0x3DC1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1372">Диспетчеру состояний не удалось удалить параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_ \_ \_ сбой параметра запроса состояния \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1374">15810 (0x3DC2)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1375">Диспетчеру состояний не удалось запросить параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**Ошибка \_ \_ при чтении \_ параметра "составное состояние \_ " \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1377">15811 (0x3DC3)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1378">Диспетчеру состояний не удалось считать составной параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**Ошибка \_ \_ при создании \_ составного \_ параметра записи состояния \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1380">15812 (0x3DC4)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1381">Диспетчеру состояний не удалось записать составной параметр.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**\_ \_ не удалось перечислить \_ контейнер состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1383">15813 (0x3DC5)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1384">Диспетчеру состояний не удалось перечислить контейнеры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ не удалось перечислить \_ Параметры состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1386">15814 (0x3DC6)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1387">Диспетчеру состояний не удалось перечислить параметры.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ Превышено ограничение на размер \_ значения \_ составного параметра состояния ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1389">15815 (0x3DC7)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1390">Размер значения составного параметра диспетчера состояний превысил установленное ограничение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ превышен предел размера значения параметра \_ состояния ошибки**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1392">15816 (0x3DC8)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1393">Размер значения параметра диспетчера состояний превысил установленное ограничение.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_ \_ \_ \_ \_ превышен предельный размер имени параметра состояния ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1395">15817 (0x3DC9)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1396">Длина имени параметра диспетчера состояний превысила предел.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_ \_ \_ \_ Превышено ограничение на размер имени \_ контейнера \_ состояний ошибок**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1398">15818 (0x3DCA)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1399">Длина имени контейнера диспетчера состояний превысила предел.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8dd90-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**\_API ошибок \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="8dd90-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd90-1401">15841 (0x3DE1)</span><span class="sxs-lookup"><span data-stu-id="8dd90-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="8dd90-1402">Этот API нельзя использовать в контексте типа приложения вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="8dd90-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dd90-1403">Требования</span><span class="sxs-lookup"><span data-stu-id="8dd90-1403">Requirements</span></span>



| <span data-ttu-id="8dd90-1404">Требование</span><span class="sxs-lookup"><span data-stu-id="8dd90-1404">Requirement</span></span> | <span data-ttu-id="8dd90-1405">Значение</span><span class="sxs-lookup"><span data-stu-id="8dd90-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd90-1406">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dd90-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd90-1407">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8dd90-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8dd90-1408">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dd90-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd90-1409">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8dd90-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dd90-1410">Header</span><span class="sxs-lookup"><span data-stu-id="8dd90-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dd90-1411"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dd90-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dd90-1412">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dd90-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd90-1413">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="8dd90-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
