---
title: Безопасность активации
description: Безопасность активации
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488365"
---
# <a name="activation-security"></a><span data-ttu-id="6cab0-103">Безопасность активации</span><span class="sxs-lookup"><span data-stu-id="6cab0-103">Activation Security</span></span>

<span data-ttu-id="6cab0-104">Безопасность активации (также называемая безопасностью запуска) помогает контролировать, кто может запускать сервер.</span><span class="sxs-lookup"><span data-stu-id="6cab0-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="6cab0-105">Безопасность активации автоматически применяется диспетчером управления службами (SCM) определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6cab0-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="6cab0-106">После получения запроса от клиента на активацию объекта (как описано в разделе [вспомогательные функции создания экземпляра](instance-creation-helper-functions.md)), SCM проверяет запрос на соответствие сведениям о безопасности активации, хранящимся в реестре.</span><span class="sxs-lookup"><span data-stu-id="6cab0-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="6cab0-107">(Безопасность активации также проверяется на наличие активаций для одного компьютера.)</span><span class="sxs-lookup"><span data-stu-id="6cab0-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="6cab0-108">При определении удостоверения клиента активация проверяет флаг маскировки, установленный в вызове клиента в [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="6cab0-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="6cab0-109">Если установлен флаг маскировки (для динамической или статической маскировки), для определения удостоверения клиента используется токен потока, если он есть.</span><span class="sxs-lookup"><span data-stu-id="6cab0-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="6cab0-110">Если маскировка не задана, вместо токена потока используется токен процесса.</span><span class="sxs-lookup"><span data-stu-id="6cab0-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="6cab0-111">Дополнительные сведения о безопасности активации см. в разделе [**коаусинфо**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) и [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="6cab0-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cab0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6cab0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cab0-113">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="6cab0-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 