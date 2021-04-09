---
title: Вложение в смешанном режиме
description: В этом разделе перечислены ограничения групп безопасности в домене смешанного режима.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Вложение в смешанном режиме AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887636"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="74897-104">Вложение в смешанном режиме</span><span class="sxs-lookup"><span data-stu-id="74897-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="74897-105">В этом разделе перечислены ограничения групп безопасности в домене смешанного режима.</span><span class="sxs-lookup"><span data-stu-id="74897-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="74897-106">Группы безопасности в домене в смешанном режиме имеют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="74897-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="74897-107">Универсальные группы нельзя создавать в доменах в смешанном режиме, так как универсальная область поддерживается только в доменах Windows 2000 в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="74897-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="74897-108">Глобальная группа может содержать учетные записи из того же домена, к которому принадлежит группа.</span><span class="sxs-lookup"><span data-stu-id="74897-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="74897-109">Глобальная группа не может содержать универсальные группы, любые глобальные группы или учетные записи из другого домена.</span><span class="sxs-lookup"><span data-stu-id="74897-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="74897-110">Локальная группа домена может содержать глобальные группы и учетные записи из любого домена или леса.</span><span class="sxs-lookup"><span data-stu-id="74897-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="74897-111">Локальная группа домена не может содержать другие локальные группы домена.</span><span class="sxs-lookup"><span data-stu-id="74897-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="74897-112">Имейте в виду, что группы распространения могут быть вложены в соответствии с правилами вложенности в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="74897-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




