---
title: Изменение области или типа группы
description: В этом разделе показано, как изменить область или тип группы в доменах в собственном режиме.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- группы AD, изменение области или типа группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772743"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="b3675-104">Изменение области или типа группы</span><span class="sxs-lookup"><span data-stu-id="b3675-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="b3675-105">Изменение области или типа группы запрещено в доменах в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="b3675-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="b3675-106">Однако в доменах в основном режиме разрешены следующие преобразования:</span><span class="sxs-lookup"><span data-stu-id="b3675-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="b3675-107">Глобальная группа в универсальную группу: это разрешено, только если глобальная группа не является членом другой глобальной группы.</span><span class="sxs-lookup"><span data-stu-id="b3675-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="b3675-108">Локальная группа домена в универсальную группу. преобразуемая локальная группа домена не может содержать другую локальную группу домена.</span><span class="sxs-lookup"><span data-stu-id="b3675-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="b3675-109">Универсальная группа для глобальной или локальной группы домена. для преобразования в глобальную группу преобразуемая универсальная группа не может содержать пользователей или глобальные группы из другого домена.</span><span class="sxs-lookup"><span data-stu-id="b3675-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="b3675-110">Для преобразования в локальную группу домена преобразуемая универсальная группа не может быть членом любой универсальной группы или локальной группы домена из другого домена.</span><span class="sxs-lookup"><span data-stu-id="b3675-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="b3675-111">В собственном режиме тип группы можно свободно преобразовать между группами безопасности и группами распространения.</span><span class="sxs-lookup"><span data-stu-id="b3675-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="b3675-112">Имейте в виду, что если группа используется для настройки контроля доступа, изменение области или типа может повлиять на записи управления доступом (ACE), содержащие эту группу.</span><span class="sxs-lookup"><span data-stu-id="b3675-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="b3675-113">Система безопасности будет игнорировать ACE, содержащие группы, которые не являются группами безопасности.</span><span class="sxs-lookup"><span data-stu-id="b3675-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




