---
title: Написание клиента с проверкой подлинности SSPI
description: Запись клиента SSPI с проверкой подлинности и удаленного вызова процедур (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Удаленный вызов процедур RPC, задачи, написание клиента SSPI с проверкой подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134262"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="ff990-104">Написание клиента с проверкой подлинности SSPI</span><span class="sxs-lookup"><span data-stu-id="ff990-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="ff990-105">Всем сеансам клиента или сервера RPC требуется привязка между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ff990-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="ff990-106">Чтобы добавить безопасность в клиентские и серверные приложения, программы должны использовать аутентифицированную привязку.</span><span class="sxs-lookup"><span data-stu-id="ff990-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="ff990-107">В этом разделе описывается процесс создания привязок с проверкой подлинности между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ff990-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="ff990-108">Создание дескрипторов привязки на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="ff990-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="ff990-109">Предоставление серверу учетных данных клиента</span><span class="sxs-lookup"><span data-stu-id="ff990-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="ff990-110">Дополнительные сведения см. в разделе [процедуры, используемые с большинством пакетов безопасности и протоколов](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="ff990-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="ff990-111">Создание дескрипторов привязки на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="ff990-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="ff990-112">Чтобы создать сеанс с проверкой подлинности в серверной программе, клиентские приложения должны предоставить сведения о проверке подлинности с помощью соответствующего маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="ff990-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="ff990-113">Чтобы настроить маркер привязки, прошедший проверку подлинности, клиенты вызывают функцию [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) или [**рпкбиндингсетаусинфоекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="ff990-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="ff990-114">Эти две функции практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="ff990-114">These two functions are nearly identical.</span></span> <span data-ttu-id="ff990-115">Единственное различие между ними заключается в том, что клиент может указать качество обслуживания с помощью функции **рпкбиндингсетаусинфоекс** .</span><span class="sxs-lookup"><span data-stu-id="ff990-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="ff990-116">В следующем фрагменте кода показано, как может выглядеть вызов [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="ff990-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



<span data-ttu-id="ff990-117">После успешного вызова клиентом функций [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) или [**рпкбиндингсетаусинфоекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) библиотека времени выполнения RPC автоматически проверяет подлинность всех вызовов RPC для привязки.</span><span class="sxs-lookup"><span data-stu-id="ff990-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="ff990-118">Уровень безопасности и проверки подлинности, который выбирает клиент, применяется только к этому маркеру привязки.</span><span class="sxs-lookup"><span data-stu-id="ff990-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="ff990-119">Дескрипторы контекста, производные от дескриптора привязки, будут использовать одни и те же сведения о безопасности, но последующие изменения в дескрипторе привязки не будут отражены в дескрипторах контекста.</span><span class="sxs-lookup"><span data-stu-id="ff990-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="ff990-120">Дополнительные сведения см. в разделе [дескрипторы контекста](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="ff990-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="ff990-121">Уровень проверки подлинности остается действительным до тех пор, пока клиент не выберет другой уровень или пока процесс не завершится.</span><span class="sxs-lookup"><span data-stu-id="ff990-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="ff990-122">Для большинства приложений изменение уровня безопасности не требуется.</span><span class="sxs-lookup"><span data-stu-id="ff990-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="ff990-123">Клиент может запросить любой маркер привязки, чтобы получить сведения об авторизации, вызвав [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) и передав ему маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="ff990-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="ff990-124">Предоставление серверу учетных данных клиента</span><span class="sxs-lookup"><span data-stu-id="ff990-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="ff990-125">Серверы используют сведения о привязке клиента для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="ff990-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="ff990-126">Клиенты всегда передают маркер привязки в качестве первого параметра удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="ff990-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="ff990-127">Однако серверы не могут использовать этот обработчик, если он не объявлен как первый параметр для удаленных процедур в IDL-файле или в файле конфигурации приложения сервера (ACF).</span><span class="sxs-lookup"><span data-stu-id="ff990-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="ff990-128">Можно выбрать список маркера привязки в IDL-файле, но это заставляет все клиенты объявлять и манипулировать маркером привязки, а не использовать автоматическую или неявную привязку.</span><span class="sxs-lookup"><span data-stu-id="ff990-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="ff990-129">Дополнительные сведения см. [в файлах IDL и ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff990-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="ff990-130">Другой способ — оставить дескрипторы привязки из IDL-файла и поместить **явный атрибут \_ Handle** в ACF сервера.</span><span class="sxs-lookup"><span data-stu-id="ff990-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="ff990-131">Таким образом клиент может использовать тип привязки, наиболее подходящий для приложения, в то время как сервер использует маркер привязки, как если бы он был объявлен явным образом.</span><span class="sxs-lookup"><span data-stu-id="ff990-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="ff990-132">Процесс извлечения учетных данных клиента из маркера привязки выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ff990-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="ff990-133">Клиенты RPC вызывают [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) и включают сведения о проверке подлинности в составе сведений о привязке, передаваемых серверу.</span><span class="sxs-lookup"><span data-stu-id="ff990-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="ff990-134">Как правило, сервер вызывает [**рпЦимперсонатеклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) , чтобы вести себя так, как если бы он был клиентом.</span><span class="sxs-lookup"><span data-stu-id="ff990-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="ff990-135">Если маркер привязки не прошел проверку подлинности, вызов завершается с помощью RPC \_ S \_ \_ \_ . контекст недоступен.</span><span class="sxs-lookup"><span data-stu-id="ff990-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="ff990-136">Чтобы получить имя пользователя клиента, вызовите [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) при олицетворении или в Windows XP или более поздних версиях Windows, вызовите [**рпкжетаусоризатионконтекстфорклиент**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , чтобы получить контекст авторизации, а затем используйте функции authz для получения имени.</span><span class="sxs-lookup"><span data-stu-id="ff990-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="ff990-137">Сервер, как правило, вызывает [**креатеприватеобжектсекурити**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) для создания объектов с помощью списков ACL.</span><span class="sxs-lookup"><span data-stu-id="ff990-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="ff990-138">После этого последующие проверки безопасности становятся автоматическими.</span><span class="sxs-lookup"><span data-stu-id="ff990-138">After this is accomplished, later security checks become automatic.</span></span>

 

 