---
title: Настройки привязки безопасности
description: Параметры привязки безопасности управляют способом получения или использования маркера безопасности.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Параметры привязки безопасности веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797269"
---
# <a name="security-binding-settings"></a><span data-ttu-id="edea4-106">Настройки привязки безопасности</span><span class="sxs-lookup"><span data-stu-id="edea4-106">Security Binding Settings</span></span>

<span data-ttu-id="edea4-107">Параметры привязки безопасности управляют способом получения или использования маркера безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-107">Security binding settings control the way a security token is obtained or used.</span></span> <span data-ttu-id="edea4-108">Они представлены в виде коллекции пар "свойство-значение" с ключами свойств, определенными в [**\_ \_ \_ свойстве**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)"перечисление WS Security Binding".</span><span class="sxs-lookup"><span data-stu-id="edea4-108">They are represented as a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property).</span></span> <span data-ttu-id="edea4-109">Каждое свойство в коллекции имеет разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="edea4-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="edea4-110">В результате можно определить и использовать описание безопасности без указания каких-либо параметров привязки безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-110">As a result, it is possible to define and use a security description without specifying any of the security binding settings.</span></span>


<span data-ttu-id="edea4-111">Сведения о параметрах безопасности для всего канала с помощью свойств, ключи которых определяются перечислением [**\_ \_ \_ идентификаторов свойств безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) , см. в разделе [Параметры канала безопасности](security-channel-settings.md).</span><span class="sxs-lookup"><span data-stu-id="edea4-111">For information on channel-wide security settings, with properties whose keys are defined by the [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) enumeration, see[Security Channel Settings](security-channel-settings.md).</span></span>

<span data-ttu-id="edea4-112">Следующие элементы API используются с параметрами привязки безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-112">The following API elements are used with security binding settings.</span></span>

| <span data-ttu-id="edea4-113">Перечисление</span><span class="sxs-lookup"><span data-stu-id="edea4-113">Enumeration</span></span>                                                                          | <span data-ttu-id="edea4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="edea4-114">Description</span></span>                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edea4-115">**\_сбой сертификата \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-115">**WS\_CERT\_FAILURE**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | <span data-ttu-id="edea4-116">Определяет ошибки, связанные с проверкой сертификата.</span><span class="sxs-lookup"><span data-stu-id="edea4-116">Defines failures related to certificate validation.</span></span>                                                                                                               |
| <span data-ttu-id="edea4-117">[**\_ \_ \_ Схема проверки подлинности заголовка WS HTTP \_**](https://technet.microsoft.com/windows/dd401907(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="edea4-117">[**WS\_HTTP\_HEADER\_AUTH\_SCHEME**](https://technet.microsoft.com/windows/dd401907(v=vs.60))</span></span>                 | <span data-ttu-id="edea4-118">Определяет параметры для выполнения проверки подлинности клиента с помощью заголовков проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="edea4-118">Defines the options for performing client authentication using HTTP authentication headers.</span></span>                                                                       |
| [<span data-ttu-id="edea4-119">**\_ \_ \_ целевой объект проверки подлинности заголовка HTTP WS \_**</span><span class="sxs-lookup"><span data-stu-id="edea4-119">**WS\_HTTP\_HEADER\_AUTH\_TARGET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | <span data-ttu-id="edea4-120">Определяет целевой объект для привязки безопасности для проверки подлинности HTTP-заголовка.</span><span class="sxs-lookup"><span data-stu-id="edea4-120">Defines the target for the HTTP header authentication security binding.</span></span>                                                                                           |
| [<span data-ttu-id="edea4-121">**\_ \_ \_ действие токена безопасности WS Request \_**</span><span class="sxs-lookup"><span data-stu-id="edea4-121">**WS\_REQUEST\_SECURITY\_TOKEN\_ACTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | <span data-ttu-id="edea4-122">Определяет, какой набор действий следует использовать при согласовании маркеров безопасности с помощью WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="edea4-122">Defines which set of actions to use when negotiating security tokens using WS-Trust.</span></span>                                                                              |
| [<span data-ttu-id="edea4-123">**\_ \_ имя набора алгоритмов безопасности WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="edea4-123">**WS\_SECURITY\_ALGORITHM\_SUITE\_NAME**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | <span data-ttu-id="edea4-124">Набор алгоритмов безопасности, используемых для таких задач, как подписывание и енкритинг.</span><span class="sxs-lookup"><span data-stu-id="edea4-124">A suite of security algorithms used for tasks such as signing and encryting.</span></span>                                                                                      |
| [<span data-ttu-id="edea4-125">**\_ \_ \_ идентификатор свойства привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-125">**WS\_SECURITY\_BINDING\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | <span data-ttu-id="edea4-126">Определяет свойства, используемые для указания параметров привязки безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-126">Identifies the properties used to specify security binding settings.</span></span>                                                                                              |
| [<span data-ttu-id="edea4-127">**\_ \_ \_ режим энтропии ключа безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-127">**WS\_SECURITY\_KEY\_ENTROPY\_MODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | <span data-ttu-id="edea4-128">Определяет, как случайное значение должно быть внесено в выданный ключ во время согласования маркера безопасности с помощью сообщений и смешанного режима безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-128">Defines how randomness should be contributed to the issued key during a security token negotiation done with message and mixed-mode security.</span></span>                     |
| [<span data-ttu-id="edea4-129">**\_ \_ тип ключа безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-129">**WS\_SECURITY\_KEY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | <span data-ttu-id="edea4-130">Тип ключа маркера безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-130">The key type of a security token.</span></span>                                                                                                                                 |
| [<span data-ttu-id="edea4-131">**\_ \_ \_ режим ссылки на токен безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="edea4-131">**WS\_SECURITY\_TOKEN\_REFERENCE\_MODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | <span data-ttu-id="edea4-132">механизм, используемый для ссылки на маркер безопасности из сигнатур, зашифрованные элементы и производные токены в контексте сообщений и привязок безопасности в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="edea4-132">the mechanism to use to refer to a security token from signatures, encrypted items and derived tokens in the context of message and mixed-mode security bindings.</span></span> |
| [<span data-ttu-id="edea4-133">**\_версия доверия \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-133">**WS\_TRUST\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | <span data-ttu-id="edea4-134">Определяет версию спецификации WS-Trust, используемую для обеспечения безопасности сообщений и смешанного режима безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-134">Defines the WS-Trust specification version to be used with message security and mixed-mode security.</span></span>                                                              |
| [<span data-ttu-id="edea4-135">**\_ \_ встроенный \_ пакет проверки подлинности WS Windows \_**</span><span class="sxs-lookup"><span data-stu-id="edea4-135">**WS\_WINDOWS\_INTEGRATED\_AUTH\_PACKAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | <span data-ttu-id="edea4-136">Определяет конкретный пакет SSP, используемый для встроенной проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="edea4-136">Defines the specific SSP package to be used for Windows Integrated Authentication.</span></span>                                                                                |



 



| <span data-ttu-id="edea4-137">Структура</span><span class="sxs-lookup"><span data-stu-id="edea4-137">Structure</span></span>                                                               | <span data-ttu-id="edea4-138">Описание</span><span class="sxs-lookup"><span data-stu-id="edea4-138">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="edea4-139">**\_ \_ свойство привязки безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="edea4-139">**WS\_SECURITY\_BINDING\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | <span data-ttu-id="edea4-140">Задает параметры привязки безопасности.</span><span class="sxs-lookup"><span data-stu-id="edea4-140">Specifies a security binding specific setting.</span></span> |



 

 

 




