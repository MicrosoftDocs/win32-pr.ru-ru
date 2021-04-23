---
title: Общие часто задаваемые вопросы
description: Ознакомьтесь с ответами на часто задаваемые вопросы об API-интерфейсах EAPHost, например "Каково время существования проверки подлинности?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "105710407"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="27ead-103">Общие часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="27ead-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="27ead-104">В следующем разделе приведены ответы на часто задаваемые вопросы об API-интерфейсах EAPHost.</span><span class="sxs-lookup"><span data-stu-id="27ead-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="27ead-105">Общие часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="27ead-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27ead-106">Вопрос</span><span class="sxs-lookup"><span data-stu-id="27ead-106">Question</span></span></th>
<th><span data-ttu-id="27ead-107">Ответ</span><span class="sxs-lookup"><span data-stu-id="27ead-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ead-108">Что такое запрашивающее сторона?</span><span class="sxs-lookup"><span data-stu-id="27ead-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="27ead-109">Запрашивающая сторона — это сущность для проверки подлинности с помощью EAPHost.</span><span class="sxs-lookup"><span data-stu-id="27ead-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="27ead-110">Типичные отправителей запросов: клиенты [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , 802,3 клиентов и служба маршрутизации и удаленного доступа (RRAS), клиенты "точка — точка" (PPP).</span><span class="sxs-lookup"><span data-stu-id="27ead-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-111">Что такое одноранговый узел?</span><span class="sxs-lookup"><span data-stu-id="27ead-111">What is a peer?</span></span></td>
<td><span data-ttu-id="27ead-112">Одноранговая сторона является клиентской частью проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="27ead-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-113">Как одноранговый узел отличается от запрашивающего?</span><span class="sxs-lookup"><span data-stu-id="27ead-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="27ead-114">Запрашивающий объект переносит пакеты, в то время как одноранговый узел — нет.</span><span class="sxs-lookup"><span data-stu-id="27ead-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="27ead-115">Тем не менее, термины «одноранговый» и «клиент» в основном являются синонимами.</span><span class="sxs-lookup"><span data-stu-id="27ead-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-116">Что такое средство проверки подлинности?</span><span class="sxs-lookup"><span data-stu-id="27ead-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="27ead-117">Средство проверки подлинности — это беспроводная точка доступа, сервер сетевого доступа (NAS) или устройство сетевого доступа (NAD), которое проверяет подлинность запрашивающей стороной.</span><span class="sxs-lookup"><span data-stu-id="27ead-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="27ead-118">Средство проверки подлинности также называется сервером EAP.</span><span class="sxs-lookup"><span data-stu-id="27ead-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-119">Каково время существования проверки подлинности?</span><span class="sxs-lookup"><span data-stu-id="27ead-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="27ead-120">Время существования одного сеанса проверки подлинности на стороне клиента — это все, что происходит между вызовами функций [<strong>еафостпирбегинсессион</strong>] (/превиаус-версионс/Виндовс/десктоп/АПИ/еаппапис/НФ-еаппапис-еафостпирбегинсессион) и [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession).</span><span class="sxs-lookup"><span data-stu-id="27ead-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="27ead-121">Время существования на стороне средства проверки подлинности — это все, что происходит между функциями [<strong>еаппирбегинсессион</strong>] (/превиаус-версионс/Виндовс/десктоп/АПИ/еапмесодпирапис/НФ-еапмесодпирапис-еаппирбегинсессион) и [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</span><span class="sxs-lookup"><span data-stu-id="27ead-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-122">Что такое большой двоичный объект?</span><span class="sxs-lookup"><span data-stu-id="27ead-122">What is a BLOB?</span></span> <span data-ttu-id="27ead-123">Почему я преобразовывать двоичный BLOB-объект конфигурации (Binary) в XML?</span><span class="sxs-lookup"><span data-stu-id="27ead-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="27ead-124">Большой двоичный объект является большим двоичным объектом.</span><span class="sxs-lookup"><span data-stu-id="27ead-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="27ead-125">XML имеет несколько преимуществ по сравнению с двоичным BLOB-объектом конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27ead-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="27ead-126">Данные конфигурации, хранящиеся в формате XML, доступны для чтения, редактирования и кросс-платформенных платформ.</span><span class="sxs-lookup"><span data-stu-id="27ead-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-127">Когда я преобразовывать сохраненный большой двоичный объект XML обратно в двоичный BLOB-объект?</span><span class="sxs-lookup"><span data-stu-id="27ead-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="27ead-128">Можно сохранить двоичный BLOB-объект или двоичный объект XML, но перед использованием интерфейсов API времени выполнения необходимо всегда преобразовывать большой двоичный объект XML обратно в двоичный BLOB-объект. API-интерфейсы времени выполнения не могут принимать XML-каталоги.</span><span class="sxs-lookup"><span data-stu-id="27ead-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-129">Что такое собственные методы?</span><span class="sxs-lookup"><span data-stu-id="27ead-129">What are native methods?</span></span></td>
<td><span data-ttu-id="27ead-130">Собственные методы EAP используют новый API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="27ead-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-131">Что такое устаревшие методы?</span><span class="sxs-lookup"><span data-stu-id="27ead-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="27ead-132">Устаревшие методы EAP определяются в [справочнике по протоколу расширенной проверки подлинности](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span><span class="sxs-lookup"><span data-stu-id="27ead-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="27ead-133">Устаревшие методы EAP доступны для использования в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27ead-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="27ead-134">Эти методы могут быть недоступны для использования в последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="27ead-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-135">В чем разница между устаревшими и собственными методами?</span><span class="sxs-lookup"><span data-stu-id="27ead-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="27ead-136">Собственные API-интерфейсы проще и имеют меньше функций.</span><span class="sxs-lookup"><span data-stu-id="27ead-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="27ead-137">Все новые методы EAP должны быть написаны с помощью API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="27ead-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-138">Что такое &quot; Групповая политика &quot; ?</span><span class="sxs-lookup"><span data-stu-id="27ead-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="27ead-139">Описание групповой политики см. в разделе [Групповая политика Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="27ead-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-140">Могут ли функции EAPHost переопределить политику конфигурации, заданную групповой политикой?</span><span class="sxs-lookup"><span data-stu-id="27ead-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="27ead-141">Нет, никогда.</span><span class="sxs-lookup"><span data-stu-id="27ead-141">No, never.</span></span> <span data-ttu-id="27ead-142">Если групповая политика используется, параметры групповой политики всегда будут переопределять параметры конфигурации EAPHost.</span><span class="sxs-lookup"><span data-stu-id="27ead-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-143">Что такое единый вход (SSO)?</span><span class="sxs-lookup"><span data-stu-id="27ead-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="27ead-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) — это механизм проверки подлинности уровня 2.</span><span class="sxs-lookup"><span data-stu-id="27ead-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="27ead-145">В зависимости от конфигурации единого входа SSO позволяет пользователям проходить проверку подлинности в сети с помощью [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) до или сразу после входа в систему Windows.</span><span class="sxs-lookup"><span data-stu-id="27ead-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="27ead-146">Единый вход может быть настроен на использование учетных данных Windows для проверки подлинности сети (в этом случае пользователи вводят свои учетные данные только один раз) или используют разные учетные данные для проверки подлинности Windows и сети.</span><span class="sxs-lookup"><span data-stu-id="27ead-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="27ead-147">Дополнительные сведения см. в разделе [единый вход и PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="27ead-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-148">Что такое поставщик предварительных прав доступа (PLAP)</span><span class="sxs-lookup"><span data-stu-id="27ead-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="27ead-149">Дополнительные сведения см. в разделе [единый вход и PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="27ead-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-150">Что такое защищенный протокол PEAP?</span><span class="sxs-lookup"><span data-stu-id="27ead-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="27ead-151">Дополнительные сведения см. в разделе протокол [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) и [Протокол расширенной проверки подлинности](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span><span class="sxs-lookup"><span data-stu-id="27ead-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-152">Как PEAP работает с возобновлением сеанса и повторной проверкой подлинности?</span><span class="sxs-lookup"><span data-stu-id="27ead-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="27ead-153">Возобновление сеанса и повторная проверка подлинности обычно происходит при роуминге в беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="27ead-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="27ead-154">API защиты данных Windows (DPAPI) предоставляет способ защиты и привязки данных для пользователя и, при необходимости, сеанса входа в систему.</span><span class="sxs-lookup"><span data-stu-id="27ead-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="27ead-155">Вызывающий объект предоставляет [<strong>криптпротектмемори</strong>] (/Виндовс/десктоп/АПИ/дпапи/НФ-дпапи-криптпротектмемори) незашифрованный буфер, а DPAPI шифрует память на месте.</span><span class="sxs-lookup"><span data-stu-id="27ead-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="27ead-156">Позже вызывающий объект может передать зашифрованный буфер в [<strong>криптунпротектмемори</strong>] (/Виндовс/десктоп/АПИ/дпапи/НФ-дпапи-криптунпротектмемори), а DPAPI будет расшифровывать память снова на месте.</span><span class="sxs-lookup"><span data-stu-id="27ead-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="27ead-157">Дополнительные сведения см. в разделе [расширение внутреннего приложения TLS (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) и [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="27ead-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-158">Что такое безопасность уровня EAP-Transport (EAP-TLS)?</span><span class="sxs-lookup"><span data-stu-id="27ead-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="27ead-159">EAP-TLS — это протокол клиент-сервер, в котором для клиента и сервера обычно используются отдельные профили сертификатов. Дополнительные сведения см. в стандарте [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="27ead-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-160">Разделы справки реализовать изменение пароля с помощью API локального центра безопасности (LSA)?</span><span class="sxs-lookup"><span data-stu-id="27ead-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="27ead-161">Используйте функцию [<strong>LsaCallAuthenticationPackage</strong>] (/Виндовс/десктоп/АПИ/нтсекапи/НФ-нтсекапи-лсакаллаусентикатионпаккаже) для реализации изменения пароля.</span><span class="sxs-lookup"><span data-stu-id="27ead-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-162">Зачем нужно включать трассировку в EAPHost?</span><span class="sxs-lookup"><span data-stu-id="27ead-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="27ead-163">Журналы трассировки содержат отладочную информацию (доступна только на английском языке), которая может помочь разработчикам и партнерам корпорации Майкрософт в поиске основных причин возникновения проблем с процессом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27ead-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="27ead-164">Дополнительные сведения см. в разделе [Включение трассировки](enabling-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="27ead-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-165">Почему я получаю код ошибки, NTE_BAD_KEY_STATE (0x8009000BL) при использовании [криптографического](/windows/desktop/SecCrypto/cryptography-portal) API для входа в систему обмена данными EAP-TLS?</span><span class="sxs-lookup"><span data-stu-id="27ead-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="27ead-166">В файле Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) определен как &quot; ключ, недопустимый для использования в указанном состоянии &quot; .</span><span class="sxs-lookup"><span data-stu-id="27ead-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="27ead-167">Эта ошибка обычно возвращается в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="27ead-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="27ead-168">При попытке экспорта BLOB-объекта закрытого ключа, который не является экспортируемым</span><span class="sxs-lookup"><span data-stu-id="27ead-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="27ead-169">При неудачной попытке создать хэш-маркер функции псевдо-Random (PRF) с помощью [<strong>CryptCreateHash</strong>] (/Виндовс/десктоп/АПИ/винкрипт/НФ-винкрипт-крипткреатехаш)</span><span class="sxs-lookup"><span data-stu-id="27ead-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="27ead-170">Дополнительные сведения см. [в разделе Завершение сообщений в протоколе TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="27ead-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27ead-171">Что такое функция псевдо-Random (PRF)?</span><span class="sxs-lookup"><span data-stu-id="27ead-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="27ead-172">Функция, которая принимает ключ, метку и начальное значение в качестве входных данных, а затем выдает выходные данные произвольной длины.</span><span class="sxs-lookup"><span data-stu-id="27ead-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="27ead-173">Дополнительные сведения см. [в разделе Завершение сообщений в протоколе TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="27ead-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ead-174">Как привязать EAPHost к сетевым адаптерам?</span><span class="sxs-lookup"><span data-stu-id="27ead-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="27ead-175">EAPHost позволяет выполнять несколько отправителей запросов одновременно, и каждый запрашивающий способ может быть привязан к нескольким сетевым адаптерам.</span><span class="sxs-lookup"><span data-stu-id="27ead-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="27ead-176">EAPHost отправителей запросов обеспечивают привязку к сетевым слоям и пропускают процесс проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27ead-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="27ead-177">Отправителей запросов содержат конфигурацию проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27ead-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="27ead-178">Отправителей запросов также сохраняет состояние и обеспечивает последующую безопасность подключения.</span><span class="sxs-lookup"><span data-stu-id="27ead-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="27ead-179">Так как EAPHost не привязывается напрямую к какому-либо сетевому механизму, возможно расширение для обращений.</span><span class="sxs-lookup"><span data-stu-id="27ead-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="27ead-180">См. также</span><span class="sxs-lookup"><span data-stu-id="27ead-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ead-181">Вопросы и ответы по обращению EAPHost</span><span class="sxs-lookup"><span data-stu-id="27ead-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="27ead-182">Вопросы и ответы по методу EAPHost</span><span class="sxs-lookup"><span data-stu-id="27ead-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="27ead-183">Вопросы и ответы по разработке EAPHost</span><span class="sxs-lookup"><span data-stu-id="27ead-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

