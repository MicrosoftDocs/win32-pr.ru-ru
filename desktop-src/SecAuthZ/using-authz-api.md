---
description: API authz позволяет приложениям выполнять настраиваемые проверки доступа, обеспечивая более высокую производительность и более простую разработку, чем управление доступом низкого уровня.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Использование API-интерфейса authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349705"
---
# <a name="using-authz-api"></a><span data-ttu-id="fa4df-103">Использование API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="fa4df-103">Using Authz API</span></span>

<span data-ttu-id="fa4df-104">API authz позволяет приложениям выполнять настраиваемые проверки доступа, обеспечивая более высокую производительность и более простую разработку, чем [Управление доступом низкого уровня](low-level-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="fa4df-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="fa4df-105">API authz позволяет приложениям кэшировать проверки доступа для повышения производительности, запрашивать и изменять контексты клиентов, а также определять бизнес-правила, которые можно использовать для динамической оценки разрешений доступа.</span><span class="sxs-lookup"><span data-stu-id="fa4df-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa4df-106">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="fa4df-106">In This Section</span></span>



| <span data-ttu-id="fa4df-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="fa4df-107">Topic</span></span>                                                                             | <span data-ttu-id="fa4df-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fa4df-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa4df-109">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="fa4df-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="fa4df-110">Приложение должно создать контекст клиента, прежде чем он сможет использовать API-интерфейс authz для выполнения проверок доступа или аудита.</span><span class="sxs-lookup"><span data-stu-id="fa4df-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="fa4df-111">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="fa4df-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="fa4df-112">Приложения могут вызывать функцию [**аусзжетинформатионфромконтекст**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) для запроса сведений о существующем контексте клиента.</span><span class="sxs-lookup"><span data-stu-id="fa4df-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="fa4df-113">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="fa4df-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="fa4df-114">Приложение может добавлять [*идентификаторы безопасности*](/windows/desktop/SecGloss/s-gly) (SID) в существующий контекст клиента путем вызова функции [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="fa4df-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="fa4df-115">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="fa4df-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="fa4df-116">Приложения определяют, предоставлять ли доступ к защищаемым объектам, вызывая функцию [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="fa4df-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="fa4df-117">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="fa4df-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="fa4df-118">Когда приложение выполняет проверку доступа путем вызова функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , результаты проверки доступа могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="fa4df-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

