---
title: Последовательность вызовов API метода туннеля
description: Сведения о последовательности вызовов API для методов туннелирования. См. Обзор и Просмотр дополнительных доступных ресурсов.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339300"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="ebacc-104">Последовательность вызовов API метода туннеля</span><span class="sxs-lookup"><span data-stu-id="ebacc-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="ebacc-105">В этом разделе рассматривается последовательность вызовов API для методов туннелирования.</span><span class="sxs-lookup"><span data-stu-id="ebacc-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="ebacc-106">Обзор последовательности вызовов метода туннеля</span><span class="sxs-lookup"><span data-stu-id="ebacc-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="ebacc-107">Когда запрашивающая сторона получает запрос на удостоверение пользователя и данные пользователя, обычно возникает следующий поток вызова API.</span><span class="sxs-lookup"><span data-stu-id="ebacc-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="ebacc-108">Запрашивающий объект вызывает Еафостпирпроцессрецеиведпаккет в EapHost для обработки пакета, полученного от средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ebacc-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="ebacc-109">После обработки этого пакета EAPHost определяет его как пакет Идентитирекуест и вызывает [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) в методе Tunnel, чтобы получить удостоверение пользователя, используемое для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ebacc-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="ebacc-110">Если методу туннелирования необходимо получить удостоверение пользователя из внутреннего метода, он вызывает [**еафостпиржетидентити**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) для внутреннего метода EAPHost, который, в свою очередь, вызывает [**еаппиржетидентити**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) во внутреннем методе.</span><span class="sxs-lookup"><span data-stu-id="ebacc-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="ebacc-111">Взаимодействие пользователя с потоком вызовов API методов туннелирования</span><span class="sxs-lookup"><span data-stu-id="ebacc-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="ebacc-112">В некоторых случаях, когда удостоверение недоступно или пользователь должен предоставить дополнительные сведения, метод EAP выдает диалоговое окно пользовательского интерфейса на вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="ebacc-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="ebacc-113">В таких случаях для получения сведений непосредственно от пользователя обычно используется последовательность вызовов.</span><span class="sxs-lookup"><span data-stu-id="ebacc-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="ebacc-114">Метод EAP туннеля возвращает код действия для вызова пользовательского интерфейса в EapHost.</span><span class="sxs-lookup"><span data-stu-id="ebacc-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="ebacc-115">Запрашивающий объект вызывает [**еафостпиржетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)для получения сведений о текущем контексте пользовательского интерфейса для диалогового окна пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ebacc-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="ebacc-116">Затем запрашивающий метод вызывает [ **еафостпиринвокеинтерактивеуи.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="ebacc-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="ebacc-117">Эта функция использует сведения о контексте пользовательского интерфейса для вызова интерактивного пользовательского интерфейса, который используется для получения учетных данных от пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebacc-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="ebacc-118">Процесс пользовательского интерфейса загружает Eappcfg.dll и получает указатели на Еаппиринвокеинтерактивеуи и Еаппирфримемори.</span><span class="sxs-lookup"><span data-stu-id="ebacc-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="ebacc-119">Процесс пользовательского интерфейса обычно собирает пользовательский интерфейс или обрабатывает интерактивный пользовательский интерфейс и отделен от процесса запрашивающего устройства.</span><span class="sxs-lookup"><span data-stu-id="ebacc-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="ebacc-120">Разделение этих двух процессов не является требованием EAPHost, но это имеет преимущество, позволяя процессу пользовательского интерфейса взаимодействовать с рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="ebacc-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="ebacc-121">EapHost вызывает [**еаппиринвокеидентитюи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) в методе Tunnel для получения сведений об удостоверении пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebacc-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="ebacc-122">Чтобы получить удостоверение пользователя из внутреннего метода, метод туннеля вызывает [**еафостпиринвокеидентитюи**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) для внутренней EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ebacc-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="ebacc-123">Внутренняя метод EAPHost вызывает [**еаппиринвокеидентитюи**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) для внутреннего метода для вызова пользовательского интерфейса удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebacc-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="ebacc-124">[**Еафостпирсетуиконтекст**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) предоставляет новые или обновленные сведения о контексте пользовательского интерфейса для однорангового метода EAP, загруженного в EAPHost после создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ebacc-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="ebacc-125">На следующей схеме объясняется последовательность вызовов API для методов туннелирования.</span><span class="sxs-lookup"><span data-stu-id="ebacc-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![последовательность вызовов API методов туннеля](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="ebacc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ebacc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebacc-128">Последовательность вызовов EAPHost</span><span class="sxs-lookup"><span data-stu-id="ebacc-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="ebacc-129">Последовательность вызовов API-интерфейса для запрашивающих сторон</span><span class="sxs-lookup"><span data-stu-id="ebacc-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="ebacc-130">Справочник по API для запрашивающей сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="ebacc-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




