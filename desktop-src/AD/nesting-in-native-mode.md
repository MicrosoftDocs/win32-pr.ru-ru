---
title: Вложенность в собственном режиме
description: В следующем списке описывается, что может содержаться в группе, существующей в домене в основном режиме.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Вложение в собственный режим AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887635"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="be0a5-104">Вложенность в собственном режиме</span><span class="sxs-lookup"><span data-stu-id="be0a5-104">Nesting in Native Mode</span></span>

<span data-ttu-id="be0a5-105">В следующем списке описывается, что может содержаться в группе, существующей в домене в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="be0a5-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="be0a5-106">Этот же список также применяется к группам распространения в доменах в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="be0a5-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="be0a5-107">Область группы определяет эти правила включения.</span><span class="sxs-lookup"><span data-stu-id="be0a5-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="be0a5-108">Универсальная группа может содержать другие универсальные группы, глобальные группы и учетные записи из любого домена в лесу, в котором находится эта универсальная группа.</span><span class="sxs-lookup"><span data-stu-id="be0a5-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="be0a5-109">Глобальная группа может содержать другие глобальные группы и учетные записи из того же домена, к которому принадлежит группа.</span><span class="sxs-lookup"><span data-stu-id="be0a5-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="be0a5-110">Глобальная группа не может содержать универсальные группы или любые глобальные группы или учетные записи из другого домена.</span><span class="sxs-lookup"><span data-stu-id="be0a5-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="be0a5-111">Локальная группа домена может содержать универсальные группы, глобальные группы и учетные записи из любого домена или леса.</span><span class="sxs-lookup"><span data-stu-id="be0a5-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="be0a5-112">Локальная группа домена также может содержать другие локальные группы домена из того же домена, к которому принадлежит эта группа.</span><span class="sxs-lookup"><span data-stu-id="be0a5-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="be0a5-113">Локальная группа домена не может содержать другие локальные группы домена из любого другого домена или леса.</span><span class="sxs-lookup"><span data-stu-id="be0a5-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




