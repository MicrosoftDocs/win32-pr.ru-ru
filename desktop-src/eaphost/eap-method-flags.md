---
title: Флаги методов EAP (Еаптипес. h)
description: Флаги методов EAP используются в запрашивающей стороне, средствах проверки подлинности и одноранговых функциях для указания поведения сеанса проверки подлинности EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488913"
---
# <a name="eap-method-flags"></a><span data-ttu-id="4e98b-103">Флаги методов EAP</span><span class="sxs-lookup"><span data-stu-id="4e98b-103">EAP Method Flags</span></span>

<span data-ttu-id="4e98b-104">Флаги методов EAP используются в запрашивающей стороне, средствах проверки подлинности и одноранговых функциях для указания поведения сеанса проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="4e98b-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="4e98b-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Reserved1 флаг \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4e98b-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-107">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-107">Do not use.</span></span> <span data-ttu-id="4e98b-108">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**Флаг EAP, \_ \_ не \_ Интерактивный**</span><span class="sxs-lookup"><span data-stu-id="4e98b-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4e98b-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-111">Не отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4e98b-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_Вход с флагом EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4e98b-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4e98b-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-114">Данные пользователя получены из входа в Windows.</span><span class="sxs-lookup"><span data-stu-id="4e98b-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_ \_ Предварительный просмотр ФЛАГа EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4e98b-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-117">Показать пользовательский интерфейс учетных данных перед проверкой подлинности, даже если имеются кэшированные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="4e98b-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**Протокол EAP \_ ФЛАГ \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="4e98b-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e98b-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-120">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-120">Do not use.</span></span> <span data-ttu-id="4e98b-121">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_ \_ Проверка подлинности компьютера с ФЛАГом EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4e98b-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="4e98b-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-124">Использовать проверку подлинности на уровне компьютера; Если этот флаг не задан, то используется проверка подлинности на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e98b-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**Флаг EAP, \_ показывающий \_ гостевой \_ доступ**</span><span class="sxs-lookup"><span data-stu-id="4e98b-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4e98b-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="4e98b-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-127">Указывает запрос на предоставление гостевого доступа.</span><span class="sxs-lookup"><span data-stu-id="4e98b-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Reserved3 флаг \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="4e98b-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="4e98b-130">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-130">Do not use.</span></span> <span data-ttu-id="4e98b-131">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**Протокол EAP \_ ФЛАГ \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="4e98b-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="4e98b-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="4e98b-134">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-134">Do not use.</span></span> <span data-ttu-id="4e98b-135">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_флаг EAP \_ возобновляется \_ из \_ режима гибернации**</span><span class="sxs-lookup"><span data-stu-id="4e98b-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="4e98b-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-138">Указывает, что это первый вызов после возобновления активности компьютера с периода гибернации.</span><span class="sxs-lookup"><span data-stu-id="4e98b-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**Протокол EAP \_ ФЛАГ \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="4e98b-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="4e98b-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="4e98b-141">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-141">Do not use.</span></span> <span data-ttu-id="4e98b-142">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Reserved6 флаг \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="4e98b-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-145">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-145">Do not use.</span></span> <span data-ttu-id="4e98b-146">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ полная \_ Проверка ПОдлинности EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="4e98b-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-149">Указывает, что методы туннеля должны выполнять полную проверку подлинности вместо сокращенной версии, например [защищенное быстрое повторное подключение EAP (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4e98b-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**\_ \_ предпочтительные \_ \_ учетные данные для флага EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="4e98b-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-152">Указывает, что учетные данные, передаваемые в [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) , являются предпочтительными для всех других форм получения учетных данных, даже если данные конфигурации, переданные в текущую функцию, запрашивают другой режим получения учетных данных.</span><span class="sxs-lookup"><span data-stu-id="4e98b-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="4e98b-153">Этот флаг используется только [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="4e98b-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Reserved7 флаг \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="4e98b-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-156">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-156">Do not use.</span></span> <span data-ttu-id="4e98b-157">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_ \_ \_ изменение состояния работоспособности однорангового флага EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e98b-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="4e98b-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-160">Указывает, что причиной повторной проверки подлинности является обратный вызов [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP). NAP инициировала сеанс проверки подлинности, так как изменилось состояние работоспособности.</span><span class="sxs-lookup"><span data-stu-id="4e98b-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="4e98b-161">Этот флаг должен отправляться, только если эта функция вызывается обратным вызовом [*нотификатионхандлер*](/previous-versions/windows/desktop/api) , связанным с NAP, предоставленным предыдущим вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="4e98b-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_Пользовательский интерфейс флага EAP \_ скрывать \_**</span><span class="sxs-lookup"><span data-stu-id="4e98b-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="4e98b-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-164">Продолжайте проверку подлинности с помощью доступной информации.</span><span class="sxs-lookup"><span data-stu-id="4e98b-164">Continue authentication with available information.</span></span> <span data-ttu-id="4e98b-165">Если проверка подлинности не может быть продолжена, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4e98b-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_флаг EAP \_ Предварительный \_ Вход**</span><span class="sxs-lookup"><span data-stu-id="4e98b-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="4e98b-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-168">Указывает, что EAPHost должен обеспечивать единый вход (SSO).</span><span class="sxs-lookup"><span data-stu-id="4e98b-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="4e98b-169">Дополнительные сведения см. в разделе [единый вход и PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="4e98b-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_ \_ Проверка подлинности пользователя с ФЛАГом EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4e98b-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="4e98b-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-172">Указывает проверку подлинности на уровне пользователя для устаревших методов, которые не могут установить **\_ флаг EAP \_ \_ Проверка подлинности компьютера**.</span><span class="sxs-lookup"><span data-stu-id="4e98b-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_флаг EAP \_ CONFG \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4e98b-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="4e98b-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="4e98b-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-175">Указывает, что конфигурацию можно просмотреть, но не обновить.</span><span class="sxs-lookup"><span data-stu-id="4e98b-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e98b-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Reserved8 флаг \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="4e98b-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e98b-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="4e98b-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="4e98b-178">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="4e98b-178">Do not use.</span></span> <span data-ttu-id="4e98b-179">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="4e98b-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e98b-180">Требования</span><span class="sxs-lookup"><span data-stu-id="4e98b-180">Requirements</span></span>



| <span data-ttu-id="4e98b-181">Требование</span><span class="sxs-lookup"><span data-stu-id="4e98b-181">Requirement</span></span> | <span data-ttu-id="4e98b-182">Значение</span><span class="sxs-lookup"><span data-stu-id="4e98b-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e98b-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e98b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4e98b-184">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e98b-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e98b-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e98b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4e98b-186">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e98b-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e98b-187">Header</span><span class="sxs-lookup"><span data-stu-id="4e98b-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e98b-188"><dt>Еаптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e98b-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e98b-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e98b-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e98b-190">Общие константы EAPHost</span><span class="sxs-lookup"><span data-stu-id="4e98b-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

