---
title: Изменение параметров безопасности компьютера по умолчанию
description: Изменение параметров безопасности компьютера по умолчанию
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410591"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="77427-103">Изменение параметров безопасности компьютера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="77427-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="77427-104">Не рекомендуется изменять параметры безопасности на уровне системы, так как это повлияет на все серверные приложения COM, которые не устанавливают собственную систему безопасности на уровне процесса и могут препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="77427-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="77427-105">Если вы изменяете параметры безопасности на уровне системы, чтобы они влияли на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="77427-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="77427-106">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="77427-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="77427-107">Определенные значения в реестре определяют параметры безопасности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="77427-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="77427-108">Эти параметры можно изменить с помощью Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="77427-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="77427-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="77427-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="77427-110">Параметры реестра для System-Wide безопасности</span><span class="sxs-lookup"><span data-stu-id="77427-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="77427-111">Настройка безопасности System-Wide с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="77427-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="77427-112">См. также</span><span class="sxs-lookup"><span data-stu-id="77427-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77427-113">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="77427-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="77427-114">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="77427-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




