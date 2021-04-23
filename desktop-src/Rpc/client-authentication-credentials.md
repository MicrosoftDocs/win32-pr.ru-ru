---
title: Учетные данные проверки подлинности клиента
description: Каждый прошедший проверку подлинности клиент должен предоставить серверу учетные данные для проверки подлинности.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068551"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="0adf6-103">Учетные данные проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="0adf6-103">Client Authentication Credentials</span></span>

<span data-ttu-id="0adf6-104">Каждый прошедший проверку подлинности клиент должен предоставить серверу учетные данные для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0adf6-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="0adf6-105">В разделе RPC клиент хранит свои учетные данные для проверки подлинности в привязке между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0adf6-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="0adf6-106">Для этого клиент вызывает [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) или [**рпкбиндингсетаусинфоекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span><span class="sxs-lookup"><span data-stu-id="0adf6-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="0adf6-107">Существует два типа учетных данных — неявные и явные:</span><span class="sxs-lookup"><span data-stu-id="0adf6-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="0adf6-108">Явные учетные данные существуют, когда клиент предоставляет имя пользователя, пароль и домен.</span><span class="sxs-lookup"><span data-stu-id="0adf6-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="0adf6-109">Неявные учетные данные существуют, когда клиент использует учетные данные из потока или маркера процесса, вызывающего функции **рпкбиндингсетаусинфо** или **рпкбиндингсетаусинфоекс** .</span><span class="sxs-lookup"><span data-stu-id="0adf6-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="0adf6-110">Клиенты должны отключаться от предоставления явных учетных данных, поскольку хранение, обработка и извлечение пароля пользователя может вызвать уязвимость в распределенной системе, если используются явные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0adf6-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="0adf6-111">Чтобы использовать неявные учетные данные, клиент вызывает **рпкбиндингсетаусинфо**(*ex*).</span><span class="sxs-lookup"><span data-stu-id="0adf6-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="0adf6-112">Система безопасности и RPC получают учетные данные из потока или маркера процесса для использования в сеансе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0adf6-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="0adf6-113">Если клиент использует явные учетные данные, Пятый параметр этих двух функций имеет тип [**\_ \_ \_ маркера идентификации RPC auth**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="0adf6-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="0adf6-114">Это гибкий тип, который является указателем на структуру данных.</span><span class="sxs-lookup"><span data-stu-id="0adf6-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="0adf6-115">Содержимое структуры данных может различаться для каждой службы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0adf6-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="0adf6-116">В настоящее время SSP, поддерживаемые RPC, потребовали, чтобы ваш **\_ \_ \_ обработчик удостоверений проверки подлинности RPC** настроил, чтобы он указывал на структуру [**\_ \_ \_ удостоверений WinNT auth в секунду**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="0adf6-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="0adf6-117">Структура **\_ удостоверения для \_ проверки \_ подлинности в секунду (в секундах** ) содержит поля для имени пользователя, домена и пароля.</span><span class="sxs-lookup"><span data-stu-id="0adf6-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




