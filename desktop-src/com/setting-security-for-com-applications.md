---
title: Настройка безопасности для приложений COM
description: Настройка безопасности для приложений COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889255"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="65d04-103">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="65d04-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="65d04-104">Существует несколько способов помочь в управлении безопасностью приложений.</span><span class="sxs-lookup"><span data-stu-id="65d04-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="65d04-105">Можно изменить параметры безопасности компьютера по умолчанию, используемые всеми приложениями на компьютере, которые не предоставляют собственные значения безопасности.</span><span class="sxs-lookup"><span data-stu-id="65d04-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="65d04-106">Для конкретного процесса можно настроить безопасность с помощью Dcomcnfg.exe или путем вызова [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="65d04-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="65d04-107">Можно также программно управлять параметрами безопасности на уровне прокси интерфейса.</span><span class="sxs-lookup"><span data-stu-id="65d04-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="65d04-108">В следующих разделах приводятся процедуры, объясняющие, как настроить безопасность:</span><span class="sxs-lookup"><span data-stu-id="65d04-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="65d04-109">Изменение параметров безопасности компьютера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="65d04-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="65d04-110">Настройка безопасности Process-Wide</span><span class="sxs-lookup"><span data-stu-id="65d04-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="65d04-111">Настройка безопасности на уровне прокси-сервера интерфейса</span><span class="sxs-lookup"><span data-stu-id="65d04-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="65d04-112">См. также</span><span class="sxs-lookup"><span data-stu-id="65d04-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d04-113">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="65d04-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




