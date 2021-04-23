---
title: Константы HTTP_AUTH_ENABLE_ (HTTP. h)
description: Определите схемы проверки подлинности, которые можно включить для группы URL-адресов.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492831"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="035a5-103">\_ \_ Константы включения проверки подлинности HTTP \_</span><span class="sxs-lookup"><span data-stu-id="035a5-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="035a5-104">Константы **HTTP \_ AUTH \_ позволяют** определить схемы проверки подлинности, которые можно включить для группы URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="035a5-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="035a5-105">Эти константы используются в структуре [**\_ \_ \_ сведений о проверке подлинности HTTP-сервера**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .</span><span class="sxs-lookup"><span data-stu-id="035a5-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="035a5-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_Проверка подлинности HTTP \_ Enable \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="035a5-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-107">Основная схема проверки подлинности включена.</span><span class="sxs-lookup"><span data-stu-id="035a5-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_дайджест включения проверки подлинности HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="035a5-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-109">Схема дайджест-проверки подлинности включена.</span><span class="sxs-lookup"><span data-stu-id="035a5-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_Проверка подлинности HTTP \_ Enable \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="035a5-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-111">Схема проверки подлинности Kerberos включена.</span><span class="sxs-lookup"><span data-stu-id="035a5-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_ \_ флаг ex HTTP \_ AUTH \_ Включение \_ \_ кэширования учетных данных Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="035a5-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-113">Кэширование учетных данных Kerberos включено.</span><span class="sxs-lookup"><span data-stu-id="035a5-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="035a5-114">**Windows Server 2003 и более того:** Недоступно.</span><span class="sxs-lookup"><span data-stu-id="035a5-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ запись \_ учетных данных с флагом HTTP auth ex**</span><span class="sxs-lookup"><span data-stu-id="035a5-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-116">API сервера HTTP захватывает удостоверение вызывающего объекта и использует его для проверки подлинности только для схем Negotiate и Kerberos.</span><span class="sxs-lookup"><span data-stu-id="035a5-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="035a5-117">**Windows Server 2003 и более того:** Недоступно.</span><span class="sxs-lookup"><span data-stu-id="035a5-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_Проверка подлинности HTTP \_ Enable \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="035a5-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-119">Схема проверки подлинности NTLM включена.</span><span class="sxs-lookup"><span data-stu-id="035a5-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_Проверка подлинности HTTP \_ включить \_ согласование**</span><span class="sxs-lookup"><span data-stu-id="035a5-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-121">Схема проверки подлинности Negotiate включена.</span><span class="sxs-lookup"><span data-stu-id="035a5-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="035a5-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_включить проверку подлинности HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="035a5-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="035a5-123">Все схемы проверки подлинности включены.</span><span class="sxs-lookup"><span data-stu-id="035a5-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="035a5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="035a5-124">Requirements</span></span>



| <span data-ttu-id="035a5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="035a5-125">Requirement</span></span> | <span data-ttu-id="035a5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="035a5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="035a5-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="035a5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="035a5-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="035a5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="035a5-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="035a5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="035a5-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="035a5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="035a5-131">Header</span><span class="sxs-lookup"><span data-stu-id="035a5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="035a5-132"><dt>HTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="035a5-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="035a5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="035a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="035a5-134">Константы API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="035a5-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="035a5-135">**\_ \_ сведения о проверке подлинности HTTP-сервера \_**</span><span class="sxs-lookup"><span data-stu-id="035a5-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="035a5-136">**хттпсетурлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="035a5-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="035a5-137">**хттпсетсерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="035a5-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="035a5-138">**хттпкуерюрлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="035a5-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="035a5-139">**хттпкуерисерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="035a5-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





