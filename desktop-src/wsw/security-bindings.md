---
title: Привязки безопасности
description: Привязка безопасности — это спецификация маркера безопасности, которая указывает среде выполнения, как получить и использовать маркер безопасности для обеспечения безопасности канала.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Веб-службы привязки безопасности для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134795"
---
# <a name="security-bindings"></a><span data-ttu-id="4d1f4-106">Привязки безопасности</span><span class="sxs-lookup"><span data-stu-id="4d1f4-106">Security Bindings</span></span>

<span data-ttu-id="4d1f4-107">Привязка безопасности — это спецификация маркера безопасности, которая указывает среде выполнения, как получить и использовать маркер безопасности для обеспечения безопасности канала.</span><span class="sxs-lookup"><span data-stu-id="4d1f4-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="4d1f4-108">Маркер безопасности содержит сведения, подтверждающие право доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="4d1f4-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="4d1f4-109">Он также может иметь связанный криптографический ключ для выполнения подписей и шифрования.</span><span class="sxs-lookup"><span data-stu-id="4d1f4-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="4d1f4-110">Каждая привязка безопасности содержит собственную коллекцию дополнительных [параметров привязки безопасности](security-binding-settings.md) , область действия которой определяется маркером безопасности, который он определяет.</span><span class="sxs-lookup"><span data-stu-id="4d1f4-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="4d1f4-111">Он также содержит [учетные данные безопасности](security-credentials.md), представляющие доказательства безопасности (например, имя пользователя и пароли или сертификаты), необходимые для создания маркеров безопасности.</span><span class="sxs-lookup"><span data-stu-id="4d1f4-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="4d1f4-112">Следующие обратные вызовы являются частью привязки безопасности:</span><span class="sxs-lookup"><span data-stu-id="4d1f4-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="4d1f4-113">**\_ \_ \_ обратный вызов функции WS Validate SAML**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="4d1f4-114">Следующие перечисления являются частью привязки безопасности:</span><span class="sxs-lookup"><span data-stu-id="4d1f4-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="4d1f4-115">**\_ \_ Использование безопасности сообщений \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="4d1f4-116">**\_ \_ тип аутентификации WS \_ SAML**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="4d1f4-117">**\_ \_ тип привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="4d1f4-118">**\_ \_ \_ тип маркера ключа безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="4d1f4-119">Следующие функции являются частью привязки безопасности:</span><span class="sxs-lookup"><span data-stu-id="4d1f4-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="4d1f4-120">**вскреатексмлсекурититокен**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="4d1f4-121">**всфрисекурититокен**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="4d1f4-122">Следующие структуры являются частью привязки безопасности:</span><span class="sxs-lookup"><span data-stu-id="4d1f4-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="4d1f4-123">**\_ \_ маркер асимметричного \_ \_ ключа безопасности \_ WS CAPI**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="4d1f4-124">**\_ \_ \_ \_ Проверка подлинности SAML с подписью сертификата WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="4d1f4-125">**\_ \_ \_ Привязка безопасности для проверки подлинности заголовка WS \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="4d1f4-126">**\_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos \_ апрек**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="4d1f4-127">**\_ \_ \_ \_ Привязка безопасности транспорта WS помощью канала NamedPipe \_ SSPI**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="4d1f4-128">**\_ \_ маркер асимметричного \_ \_ ключа безопасности \_ WS NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="4d1f4-129">**\_ \_ маркер симметричного \_ \_ ключа безопасности \_ (необработанный) WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="4d1f4-130">**\_ \_ удостоверение WS SAML Authenticator**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="4d1f4-131">**\_ \_ \_ Привязка безопасности сообщения SAML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="4d1f4-132">**\_Привязка безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="4d1f4-133">**\_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="4d1f4-134">**\_ \_ маркер ключа безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="4d1f4-135">**\_ \_ \_ Привязка безопасности транспорта WS \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="4d1f4-136">**\_ \_ \_ \_ Привязка безопасности транспорта WS TCP \_ SSPI**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="4d1f4-137">**\_ \_ \_ Привязка безопасности сообщений имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="4d1f4-138">**\_ \_ \_ \_ Привязка безопасности сообщений для токена WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="4d1f4-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




