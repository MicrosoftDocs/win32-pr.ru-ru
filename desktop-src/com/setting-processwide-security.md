---
title: Настройка безопасности Process-Wide
description: Существует несколько способов установки безопасности на уровне процесса.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710175"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="94ccb-103">Настройка безопасности Process-Wide</span><span class="sxs-lookup"><span data-stu-id="94ccb-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="94ccb-104">Существует несколько способов установки безопасности на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="94ccb-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="94ccb-105">Первый способ заключается в том, что использование средства Dcomcnfg.exe проще, поскольку оно не требует программирования.</span><span class="sxs-lookup"><span data-stu-id="94ccb-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="94ccb-106">Второй способ предоставляет программисту больший контроль и требует вызова [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="94ccb-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="94ccb-107">Другой способ — задать безопасность на уровне процесса в реестре с помощью ключа [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="94ccb-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="94ccb-108">Дополнительные сведения об этих методах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="94ccb-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="94ccb-109">Настройка безопасности Process-Wide с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="94ccb-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="94ccb-110">Настройка безопасности Process-Wide с помощью CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="94ccb-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="94ccb-111">Настройка безопасности Process-Wide в реестре</span><span class="sxs-lookup"><span data-stu-id="94ccb-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="94ccb-112">См. также</span><span class="sxs-lookup"><span data-stu-id="94ccb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94ccb-113">Настройка безопасности на уровне прокси-сервера интерфейса</span><span class="sxs-lookup"><span data-stu-id="94ccb-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="94ccb-114">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="94ccb-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




