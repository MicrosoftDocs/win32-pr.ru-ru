---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691676"
---
# <a name="ntlmssp"></a><span data-ttu-id="dc26a-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="dc26a-103">NTLMSSP</span></span>

<span data-ttu-id="dc26a-104">Поставщик NTLMSSP, чей идентификатор службы проверки подлинности — RPC \_ C \_ AUTHN \_ WinNT, является поставщиком поддержки безопасности, доступным во всех версиях DCOM.</span><span class="sxs-lookup"><span data-stu-id="dc26a-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="dc26a-105">Для проверки подлинности используется протокол NTLM.</span><span class="sxs-lookup"><span data-stu-id="dc26a-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="dc26a-106">NTLM никогда не передает пароль пользователя на сервер во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="dc26a-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="dc26a-107">Поэтому сервер не может использовать пароль во время олицетворения для доступа к сетевым ресурсам, к которым у пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="dc26a-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="dc26a-108">Доступны только локальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dc26a-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="dc26a-109">NTLM работает как локально, так и на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="dc26a-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="dc26a-110">То есть, если клиент и сервер находятся на разных компьютерах, NTLM по-прежнему может убедиться, что клиент является им.</span><span class="sxs-lookup"><span data-stu-id="dc26a-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="dc26a-111">При использовании NTLM удостоверение клиента представляется именем домена, именем пользователя, паролем или токеном.</span><span class="sxs-lookup"><span data-stu-id="dc26a-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="dc26a-112">Когда сервер вызывает [**кокуериклиентбланкет**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), возвращаются доменное имя клиента и имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc26a-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="dc26a-113">Однако когда сервер вызывает [**коимперсонатеклиент**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), возвращается маркер клиента.</span><span class="sxs-lookup"><span data-stu-id="dc26a-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="dc26a-114">Если между клиентом и сервером нет отношений доверия и если у сервера есть локальная учетная запись с тем же именем и паролем, что и у клиента, то эта учетная запись будет использоваться для представления клиента.</span><span class="sxs-lookup"><span data-stu-id="dc26a-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="dc26a-115">NTLM поддерживает взаимную проверку подлинности между потоками и между процессами (только локально).</span><span class="sxs-lookup"><span data-stu-id="dc26a-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="dc26a-116">Если клиент указывает имя участника сервера в форме "пользователь домена" \\ при вызове [**иклиентсекурити:: сетбланкет**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), удостоверение сервера должно совпадать с именем участника, иначе вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dc26a-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="dc26a-117">Если клиент указывает **значение NULL**, удостоверение сервера не будет проверяться.</span><span class="sxs-lookup"><span data-stu-id="dc26a-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="dc26a-118">NTLM дополнительно поддерживает уровень олицетворения делегирования между потоками и между процессами (только локально).</span><span class="sxs-lookup"><span data-stu-id="dc26a-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc26a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dc26a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc26a-120">Пакеты безопасности и COM</span><span class="sxs-lookup"><span data-stu-id="dc26a-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 