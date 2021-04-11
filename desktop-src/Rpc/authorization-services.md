---
title: Службы авторизации
description: Служба авторизации — это метод, который SSP использует для авторизации доступа к удаленной процедуре. SSP могут предоставлять более одной службы авторизации. Однако они обычно выбирают один из них по умолчанию.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068284"
---
# <a name="authorization-services"></a><span data-ttu-id="84708-105">Службы авторизации</span><span class="sxs-lookup"><span data-stu-id="84708-105">Authorization Services</span></span>

<span data-ttu-id="84708-106">Служба авторизации — это метод, который SSP использует для авторизации доступа к удаленной процедуре.</span><span class="sxs-lookup"><span data-stu-id="84708-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="84708-107">SSP могут предоставлять более одной службы авторизации.</span><span class="sxs-lookup"><span data-stu-id="84708-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="84708-108">Однако они обычно выбирают один из них по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84708-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="84708-109">Приложение может использовать метод авторизации по умолчанию для текущего поставщика общих служб или указать его.</span><span class="sxs-lookup"><span data-stu-id="84708-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="84708-110">В настоящее время Microsoft RPC поддерживает два метода авторизации.</span><span class="sxs-lookup"><span data-stu-id="84708-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="84708-111">Один — для предоставления серверу авторизации на основе имени клиентской программы.</span><span class="sxs-lookup"><span data-stu-id="84708-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="84708-112">Другой — для сравнения учетных данных проверки подлинности клиента с списком управления доступом (ACL) сервера.</span><span class="sxs-lookup"><span data-stu-id="84708-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="84708-113">Список служб авторизации см. в разделе [константы службы авторизации](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="84708-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="84708-114">Рекомендуется, чтобы разработчики использовали RPC \_ C \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="84708-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




