---
title: Реализация поддержки NAP для методов EAP
description: Узнайте, как реализовать поддержку NAP для запрашивающего устройства EAPHost. См. разделы, посвященные защите доступа к версии EAPHost, и просмотрите дополнительные доступные ресурсы.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104070893"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="d12ba-104">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="d12ba-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="d12ba-105">В этом разделе объясняется, как реализовать NAP для запрашивающего устройства EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d12ba-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="d12ba-106">В Windows Vista и Windows Server 2008 клиент принудительной защиты доступа к сети (NAP EC) доступен для подключений с проверкой подлинности [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d12ba-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="d12ba-107">Реализация защиты доступа к сети (NAP)</span><span class="sxs-lookup"><span data-stu-id="d12ba-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="d12ba-108">Для поддержки NAP в качестве запрашивающего объекта EAPHost реализуется функция обратного вызова, соответствующая прототипу обратного вызова [**нотификатионхандлер**](/previous-versions/windows/desktop/api) , и при вызове [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)необходимо предоставить указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d12ba-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="d12ba-109">Функция обратного вызова принимает два параметра.</span><span class="sxs-lookup"><span data-stu-id="d12ba-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="d12ba-110">Идентификатор GUID, однозначно определяющий интерфейс, связанный с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="d12ba-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="d12ba-111">Указатель типа VOID на непрозрачную структуру данных, предоставляемую вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="d12ba-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="d12ba-112">Функция EAPHost вызывает предоставленную через вызывающую сторона функцию обратного вызова с уникальным идентификатором GUID интерфейса и указателем VOID при изменении состояния карантина компьютера.</span><span class="sxs-lookup"><span data-stu-id="d12ba-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="d12ba-113">Когда EAPHost вызывает функцию обратного вызова, предоставленную вызывающим объектом, он реагирует на то, что логическое сетевое подключение, определяемое указателем GUID/VOID интерфейса, и снова начинает проверку подлинности с помощью **еафостпирбегинсессион**.</span><span class="sxs-lookup"><span data-stu-id="d12ba-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="d12ba-114">EAPHost может вызвать функцию обратного вызова, предоставленную через вызывающий объект, в любое время: до, во время активной проверки подлинности или после завершения проверки подлинности (после вызова [**еафостпирендсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) , но не до вызова [**еафостпирклеарконнектион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ).</span><span class="sxs-lookup"><span data-stu-id="d12ba-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="d12ba-115">Он должен всегда отвечать на запросы путем разрыва подключения логической сети и повторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d12ba-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="d12ba-116">Если вызывающий объект завершает работу или не получает уведомления об изменениях состояния изоляции, он должен вызвать [**еафостпирклеарконнектион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) и указать соответствующий GUID интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d12ba-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="d12ba-117">Если необходимо определить изоляцию логического сетевого подключения, он может получить эту информацию из **еафостпирмесодресулт. исолатионстате** , когда [**Еафостпирмесодресулт**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) получен из [**еафостпиржетресулт**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span><span class="sxs-lookup"><span data-stu-id="d12ba-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="d12ba-118">Сведения о NAP, связанные с EAPHost</span><span class="sxs-lookup"><span data-stu-id="d12ba-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="d12ba-119">Сведения о NAP, связанные с API EAPHost, см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="d12ba-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="d12ba-120">**\_тип атрибута \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="d12ba-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="d12ba-121">**\_ошибка EAP**</span><span class="sxs-lookup"><span data-stu-id="d12ba-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="d12ba-122">Часто задаваемые вопросы о запрашивающем сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="d12ba-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="d12ba-123">**Свойства метода EAP**</span><span class="sxs-lookup"><span data-stu-id="d12ba-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="d12ba-124">**еафостпирбегинсессион**</span><span class="sxs-lookup"><span data-stu-id="d12ba-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="d12ba-125">**Константы, относящиеся к EAP и сведения об ошибках**</span><span class="sxs-lookup"><span data-stu-id="d12ba-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="d12ba-126">**\_состояние изоляции**</span><span class="sxs-lookup"><span data-stu-id="d12ba-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="d12ba-127">**нотификатионхандлер**</span><span class="sxs-lookup"><span data-stu-id="d12ba-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="d12ba-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d12ba-128">Additional Resources</span></span>


-   <span data-ttu-id="d12ba-129">Список ресурсов NAP см. в разделе [Защита доступа к сети](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="d12ba-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="d12ba-130">Сведения о состоянии работоспособности см. в разделе сообщения о состоянии [работоспособности защиты доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="d12ba-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="d12ba-131">Веб-страницу и блог группы "Корпоративная сеть" см. в разделе [Защита доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="d12ba-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="d12ba-132">Сведения об API NAP см. в разделе [Защита доступа к сети](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="d12ba-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="d12ba-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d12ba-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d12ba-134">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="d12ba-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="d12ba-135">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="d12ba-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="d12ba-136">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="d12ba-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="d12ba-137">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="d12ba-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d12ba-138">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="d12ba-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 