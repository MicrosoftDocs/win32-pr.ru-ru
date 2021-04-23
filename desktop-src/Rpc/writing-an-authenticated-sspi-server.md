---
title: Написание сервера SSPI с проверкой подлинности
description: Прежде чем клиентские и серверные программы могли пройти проверку подлинности, сервер должен зарегистрировать сведения для проверки подлинности.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Удаленный вызов процедур RPC, задачи, написание сервера SSPI с проверкой подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067925"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="514f0-104">Написание сервера SSPI с проверкой подлинности</span><span class="sxs-lookup"><span data-stu-id="514f0-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="514f0-105">Прежде чем клиентские и серверные программы могли пройти проверку подлинности, сервер должен зарегистрировать сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="514f0-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="514f0-106">В частности, сервер должен зарегистрировать имя участника и указать используемую службу проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="514f0-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="514f0-107">Дополнительные сведения об именах участников см. в разделе [имена участников](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="514f0-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="514f0-108">Дополнительные сведения о службах аутентификации см. в разделе [службы проверки подлинности](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="514f0-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="514f0-109">Чтобы зарегистрировать сведения для проверки подлинности, серверы вызывают функцию [**рпксерверрегистераусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="514f0-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="514f0-110">Передайте указатель на имя участника в качестве значения первого параметра.</span><span class="sxs-lookup"><span data-stu-id="514f0-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="514f0-111">Задайте для второго параметра значение константы, указывающее службу проверки подлинности, которую будет использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="514f0-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="514f0-112">Описание служб проверки подлинности см. в разделе [константы службы проверки подлинности](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="514f0-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="514f0-113">Сервер также может передать адрес функции приобретения ключа в качестве значения третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="514f0-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="514f0-114">См. [раздел функции приобретения ключей](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="514f0-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="514f0-115">Чтобы использовать функцию приобретения ключа по умолчанию для выбранной службы проверки подлинности, установите для третьего параметра **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="514f0-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="514f0-116">Последний параметр функции [**рпксерверрегистераусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) — это данные указателя для передачи в функцию приобретения ключа, если вы предоставляете функцию приобретения ключа.</span><span class="sxs-lookup"><span data-stu-id="514f0-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="514f0-117">Вызов **рпксерверрегистераусинфо** показан в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="514f0-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="514f0-118">Кроме того, сервер может предоставить библиотеку времени выполнения RPC с помощью функции авторизации.</span><span class="sxs-lookup"><span data-stu-id="514f0-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="514f0-119">Чтобы задать функцию авторизации, вызовите функцию [**рпкмгмтсетаусоризатионфн**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .</span><span class="sxs-lookup"><span data-stu-id="514f0-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="514f0-120">Серверная часть распределенного приложения может вызывать функцию [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) или [**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) для запроса к маркеру привязки сведений для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="514f0-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="514f0-121">Если сервер регистрируется в поставщике поддержки безопасности, клиентские вызовы с недействительными учетными данными не будут отправлены.</span><span class="sxs-lookup"><span data-stu-id="514f0-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="514f0-122">Однако вызовы без учетных данных будут отправлены.</span><span class="sxs-lookup"><span data-stu-id="514f0-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="514f0-123">Избежать этого можно тремя способами:</span><span class="sxs-lookup"><span data-stu-id="514f0-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="514f0-124">Зарегистрируйте интерфейс с помощью [**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), используя функцию обратного вызова безопасности. Это приведет к тому, что библиотека времени выполнения RPC автоматически отклонит непроверенные вызовы к этому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="514f0-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="514f0-125">Регистрация функции обратного вызова совместима с другими методами проверки учетных данных доступа. Функция обратного вызова может вызывать функции [**рпЦимперсонатеклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**рпкжетаусоризатионконтекстфорклиент**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), [**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) или другие.</span><span class="sxs-lookup"><span data-stu-id="514f0-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="514f0-126">Однако эти функции не могут использовать переданные функции аргументы, так как они не обрабатываются в этот момент.</span><span class="sxs-lookup"><span data-stu-id="514f0-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="514f0-127">Регистрация интерфейса с помощью [**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) с функцией обратного вызова безопасности является наиболее часто рекомендуемым методом проверки учетных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="514f0-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="514f0-128">Вызовите [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , чтобы определить уровень безопасности, который использует клиент.</span><span class="sxs-lookup"><span data-stu-id="514f0-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="514f0-129">После этого заглушка может вернуть ошибку, если клиент не прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="514f0-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




