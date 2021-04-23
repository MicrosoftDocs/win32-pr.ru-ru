---
title: Основы безопасности RPC
description: Для выполнения любого удаленного вызова процедуры все распределенные приложения должны создать привязку между клиентом и сервером.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889003"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="3fa78-103">Основы безопасности RPC</span><span class="sxs-lookup"><span data-stu-id="3fa78-103">RPC Security Essentials</span></span>

<span data-ttu-id="3fa78-104">Для выполнения любого удаленного вызова процедуры все распределенные приложения должны создать привязку между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="3fa78-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="3fa78-105">Дополнительные сведения о привязках см. в разделе [Binding and Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="3fa78-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="3fa78-106">Для завершения безопасного удаленного вызова процедур необходимо выполнить дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="3fa78-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="3fa78-107">Во-первых, сервер должен выбрать поставщика безопасности (служба проверки подлинности в терминологии DCE).</span><span class="sxs-lookup"><span data-stu-id="3fa78-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="3fa78-108">Затем он должен принять решение о механизме проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3fa78-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="3fa78-109">После этого клиент получает привязку к серверу и запрашивает безопасный удаленный вызов процедур из среды выполнения RPC и задает различные параметры безопасности, такие как поставщик безопасности, параметры качества обслуживания системы безопасности и т. д.</span><span class="sxs-lookup"><span data-stu-id="3fa78-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="3fa78-110">В этом разделе объясняются основные понятия и сведения, необходимые для использования функций RPC для создания клиента и сервера для распределенного приложения с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="3fa78-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="3fa78-111">Он состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="3fa78-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="3fa78-112">Имена участников</span><span class="sxs-lookup"><span data-stu-id="3fa78-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="3fa78-113">Уровни проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="3fa78-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="3fa78-114">Службы проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="3fa78-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="3fa78-115">Учетные данные проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="3fa78-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="3fa78-116">Службы авторизации</span><span class="sxs-lookup"><span data-stu-id="3fa78-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="3fa78-117">Качество обслуживания</span><span class="sxs-lookup"><span data-stu-id="3fa78-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="3fa78-118">Функции авторизации</span><span class="sxs-lookup"><span data-stu-id="3fa78-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="3fa78-119">Функции приобретения ключей</span><span class="sxs-lookup"><span data-stu-id="3fa78-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="3fa78-120">Олицетворение клиента</span><span class="sxs-lookup"><span data-stu-id="3fa78-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




