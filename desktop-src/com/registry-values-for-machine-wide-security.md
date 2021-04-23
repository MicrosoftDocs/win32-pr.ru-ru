---
title: Параметры реестра для System-Wide безопасности
description: Параметры реестра для System-Wide безопасности
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986337"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="7449a-103">Параметры реестра для System-Wide безопасности</span><span class="sxs-lookup"><span data-stu-id="7449a-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="7449a-104">Не рекомендуется изменять параметры безопасности на уровне системы, так как это повлияет на все серверные приложения COM, которые не устанавливают собственную систему безопасности на уровне процесса и могут препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="7449a-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="7449a-105">Если вы изменяете параметры безопасности на уровне системы, чтобы они влияли на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="7449a-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="7449a-106">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="7449a-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="7449a-107">Определенные значения в реестре используются для определения параметров безопасности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7449a-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7449a-108">Для изменения этих параметров безопасности по умолчанию для компьютера можно использовать Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="7449a-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="7449a-109">Пошаговые инструкции, описывающие использование Dcomcnfg.exe для этой цели, см. в разделе [настройка System-Wide безопасности с помощью DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="7449a-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="7449a-110">Другой способ изменения параметров по умолчанию для всей системы заключается в непосредственном управлении значениями реестра.</span><span class="sxs-lookup"><span data-stu-id="7449a-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="7449a-111">Однако только администраторы и система имеют полный доступ к части реестра, содержащей параметры безопасности вызова по умолчанию для всей системы.</span><span class="sxs-lookup"><span data-stu-id="7449a-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="7449a-112">Все остальные пользователи имеют доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7449a-112">All other users have read-access only.</span></span>

<span data-ttu-id="7449a-113">Ниже приведены именованные значения, влияющие на параметры безопасности на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="7449a-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="7449a-114">дефаултлаунчпермиссион</span><span class="sxs-lookup"><span data-stu-id="7449a-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="7449a-115">дефаултакцесспермиссион</span><span class="sxs-lookup"><span data-stu-id="7449a-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="7449a-116">легациаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="7449a-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="7449a-117">легациимперсонатионлевел</span><span class="sxs-lookup"><span data-stu-id="7449a-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="7449a-118">легацисекуререференцес</span><span class="sxs-lookup"><span data-stu-id="7449a-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="7449a-119">српруннингобжектчеккс</span><span class="sxs-lookup"><span data-stu-id="7449a-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="7449a-120">српактиватеасактиваторчеккс</span><span class="sxs-lookup"><span data-stu-id="7449a-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="7449a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7449a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7449a-122">Настройка безопасности Process-Wide</span><span class="sxs-lookup"><span data-stu-id="7449a-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




