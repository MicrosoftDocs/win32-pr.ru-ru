---
title: Обзор сценария с единым входом EAPHost
description: Содержит два сценария, демонстрирующих преимущества поддержки единого входа (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104133358"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="e303a-103">Обзор сценария с единым входом EAPHost</span><span class="sxs-lookup"><span data-stu-id="e303a-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="e303a-104">В следующем разделе содержатся два сценария, демонстрирующие преимущества одноразовых запросов с поддержкой единого входа.</span><span class="sxs-lookup"><span data-stu-id="e303a-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="e303a-105">О сценариях</span><span class="sxs-lookup"><span data-stu-id="e303a-105">About the Scenarios</span></span>

<span data-ttu-id="e303a-106">Единый вход предоставляет функциональные возможности для хранения дополнительных сведений об учетных данных пользователя, чем обычно хранится в пользовательском BLOB-объекте EAP.</span><span class="sxs-lookup"><span data-stu-id="e303a-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="e303a-107">В отличие от других процессов учетных данных, отправителей запросов с поддержкой единого входа может разрешать такие ситуации, как перемещение AP, и изменение пароля без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="e303a-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="e303a-108">Поведение кэширования для единого входа EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="e303a-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="e303a-109">Запрашивающая сторона может попытаться выполнить проверку подлинности сети с помощью метода EAP на основе смарт-карты, такого как протокол EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="e303a-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="e303a-110">В этом и подобных сценариях запрашивающая сторона получает от пользователя ПИН-код и получает сертификат пользователя для проверки подлинности сети, за которым следует вызов Винлогин на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e303a-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="e303a-111">После успешной проверки подлинности сторона кэширует большой двоичный объект пользователя и не сохраняет информацию о ПИН-коде пользователя.</span><span class="sxs-lookup"><span data-stu-id="e303a-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="e303a-112">Когда пользователь переходит в другое место, необходимо возобновить сеанс и повторно пройти проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="e303a-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="e303a-113">Так как сертификат не может быть сохранен при предварительном входе в систему, проверка подлинности пользователя завершится ошибкой, а запрашивающий объект запустит Пользовательский BLOB.</span><span class="sxs-lookup"><span data-stu-id="e303a-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="e303a-114">На этом этапе для получения сертификата пользователя из смарт-карты для сетевой проверки подлинности требуется ПИН пользователя.</span><span class="sxs-lookup"><span data-stu-id="e303a-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="e303a-115">Поскольку единый вход кэширует ПИН-код, сертификат может быть получен без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="e303a-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="e303a-116">Без единого входа EAP-TLS должен снова вызвать пользовательский интерфейс коллекции закрепления.</span><span class="sxs-lookup"><span data-stu-id="e303a-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="e303a-117">Пошаговый подход см. в разделе [режим кэширования ПИН-кода в режиме единого входа](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="e303a-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="e303a-118">Поведение при изменении пароля единого входа</span><span class="sxs-lookup"><span data-stu-id="e303a-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="e303a-119">Запрашивающий объект может попытаться выполнить проверку подлинности в сети с помощью метода EAP на основе пароля, например протокола проверки подлинности Microsoft Challenge версии 2,0 (MS-CHAPv2), настроенного для использования учетных данных Винлогин.</span><span class="sxs-lookup"><span data-stu-id="e303a-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="e303a-120">В этом сценарии запрашивающая сторона собирает учетные данные пользователя один раз и предоставляет им значение EAPHost для проверки подлинности сети.</span><span class="sxs-lookup"><span data-stu-id="e303a-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="e303a-121">После успешной проверки подлинности сети запрашивающий объект использует тот же набор учетных данных для Винлогин.</span><span class="sxs-lookup"><span data-stu-id="e303a-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="e303a-122">Однако, если учетные данные, такие как пароль пользователя, были изменены во время проверки подлинности сети без запрашивающего абонента, последующий вызов Винлогин приведет к сбою.</span><span class="sxs-lookup"><span data-stu-id="e303a-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="e303a-123">Единый вход оставляет новые учетные данные и позволяет успешно Винлогин без дополнительного вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="e303a-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="e303a-124">Пошаговый подход см. в разделе поведение при [изменении пароля единого входа](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="e303a-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e303a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e303a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e303a-126">Единый вход и PLAP</span><span class="sxs-lookup"><span data-stu-id="e303a-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




