---
title: Учетная запись для безопасного доступа
description: Учетные данные безопасности — это часть доказательств, которой владеет взаимодействующая сторона, которая может использоваться для создания или получения маркера безопасности.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Веб-службы с учетными данными безопасности для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105700984"
---
# <a name="security-credentials"></a><span data-ttu-id="df0cc-106">Учетная запись для безопасного доступа</span><span class="sxs-lookup"><span data-stu-id="df0cc-106">Security Credentials</span></span>

<span data-ttu-id="df0cc-107">Учетные данные безопасности — это часть доказательств, которой владеет взаимодействующая сторона, которая может использоваться для создания или получения маркера безопасности.</span><span class="sxs-lookup"><span data-stu-id="df0cc-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="df0cc-108">Таким образом, учетные данные обычно длиннее, чем маркеры безопасности, и маркер безопасности можно просмотреть в виде манифеста среды выполнения учетных данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="df0cc-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="df0cc-109">Например, учетные данные включают сертификат компьютера (который можно преобразовать в маркер безопасности X. 509 во время выполнения) или пару имя пользователя и пароль для домена (который может использоваться для получения маркера безопасности Kerberos).</span><span class="sxs-lookup"><span data-stu-id="df0cc-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="df0cc-110">Учетные данные указываются как часть [привязок безопасности](security-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="df0cc-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="df0cc-111">Следующие элементы API используются с учетными данными безопасности.</span><span class="sxs-lookup"><span data-stu-id="df0cc-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="df0cc-112">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="df0cc-112">Callback</span></span>                                                                  | <span data-ttu-id="df0cc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="df0cc-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="df0cc-114">**\_ \_ обратный вызов сертификата WS Get \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="df0cc-115">Предоставляет сертификат для среды выполнения безопасности.</span><span class="sxs-lookup"><span data-stu-id="df0cc-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="df0cc-116">**\_ \_ обратный вызов проверки пароля WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="df0cc-117">Проверяет пару имя пользователя и пароль на стороне получателя.</span><span class="sxs-lookup"><span data-stu-id="df0cc-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="df0cc-118">Перечисление</span><span class="sxs-lookup"><span data-stu-id="df0cc-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="df0cc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="df0cc-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="df0cc-120">**\_ \_ тип учетных данных сертификата WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="df0cc-121">Тип учетных данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="df0cc-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="df0cc-122">**\_ \_ тип учетных данных имени пользователя WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="df0cc-123">Тип учетных данных имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="df0cc-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="df0cc-124">**\_ \_ \_ \_ тип учетных данных интегрированной проверки ПОдлинности Windows WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="df0cc-125">Тип учетных данных встроенной проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="df0cc-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="df0cc-126">Структура</span><span class="sxs-lookup"><span data-stu-id="df0cc-126">Structure</span></span>                                                                                                   | <span data-ttu-id="df0cc-127">Описание</span><span class="sxs-lookup"><span data-stu-id="df0cc-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df0cc-128">**\_ \_ учетные данные сертификата WS**</span><span class="sxs-lookup"><span data-stu-id="df0cc-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="df0cc-129">Абстрактный базовый тип для всех типов учетных данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="df0cc-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="df0cc-130">**\_пользовательские \_ \_ учетные данные сертификата**</span><span class="sxs-lookup"><span data-stu-id="df0cc-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="df0cc-131">Тип для указания учетных данных сертификата, которые должны предоставляться обратным вызовом к приложению.</span><span class="sxs-lookup"><span data-stu-id="df0cc-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="df0cc-132">**\_ \_ \_ \_ учетные данные встроенной проверки подлинности Windows по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="df0cc-133">Тип для предоставления учетных данных встроенной проверки подлинности Windows на основе текущего маркера потока.</span><span class="sxs-lookup"><span data-stu-id="df0cc-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="df0cc-134">**\_непрозрачные \_ \_ \_ учетные данные встроенной проверки подлинности WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="df0cc-135">Тип для предоставления учетных данных встроенной проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="df0cc-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="df0cc-136">**\_ \_ учетные данные имени пользователя для строки WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="df0cc-137">Тип для предоставления пары "имя пользователя-пароль" в виде строк.</span><span class="sxs-lookup"><span data-stu-id="df0cc-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="df0cc-138">**\_ \_ \_ \_ учетные данные интегрированной проверки подлинности Windows WS String \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="df0cc-139">Тип для предоставления учетных данных Windows в качестве имени пользователя, пароля и строк домена.</span><span class="sxs-lookup"><span data-stu-id="df0cc-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="df0cc-140">**WS \_ имя субъекта \_ \_ \_ учетные данные сертификата**</span><span class="sxs-lookup"><span data-stu-id="df0cc-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="df0cc-141">Тип для указания учетных данных сертификата с помощью имени субъекта сертификата, расположения хранилища и имени хранилища.</span><span class="sxs-lookup"><span data-stu-id="df0cc-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="df0cc-142">**\_ \_ учетные данные сертификата для отпечатка WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="df0cc-143">Тип для указания учетных данных сертификата с помощью отпечатка сертификата, расположения хранилища и имени хранилища.</span><span class="sxs-lookup"><span data-stu-id="df0cc-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="df0cc-144">**\_ \_ учетные данные имени пользователя WS**</span><span class="sxs-lookup"><span data-stu-id="df0cc-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="df0cc-145">Абстрактный базовый тип для всех учетных данных имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="df0cc-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="df0cc-146">**\_ \_ \_ учетные данные интегрированной проверки подлинности Windows WS \_**</span><span class="sxs-lookup"><span data-stu-id="df0cc-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="df0cc-147">Абстрактный базовый тип для всех типов учетных данных, используемых при встроенной проверке подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="df0cc-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




