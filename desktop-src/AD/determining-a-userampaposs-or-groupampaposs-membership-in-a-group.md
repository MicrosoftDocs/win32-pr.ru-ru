---
title: Определение членства пользователя или группы в группе
description: Метод Иадсграуп. GetObject можно использовать для определения того, является ли объект членом группы.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Определение членства пользователя или группы в группе AD
- группы AD, определение членства пользователя или группы в группе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069783"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="79d4a-105">Определение членства пользователя или группы в группе</span><span class="sxs-lookup"><span data-stu-id="79d4a-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="79d4a-106">Метод [**иадсграуп.**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) GetObject можно использовать для определения того, является ли объект членом группы.</span><span class="sxs-lookup"><span data-stu-id="79d4a-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="79d4a-107">Этот метод возвращает **значение true** , если указанный объект является прямым членом группы, то есть свойство элемента группы содержит указанный объект.</span><span class="sxs-lookup"><span data-stu-id="79d4a-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="79d4a-108">Группа может содержать другие группы.</span><span class="sxs-lookup"><span data-stu-id="79d4a-108">A group can contain other groups.</span></span> <span data-ttu-id="79d4a-109">Метод [**иадсграуп. DataMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) не рекурсивно проверяет членов групп в своем свойстве элемента, группирует в этих группах и т. д.</span><span class="sxs-lookup"><span data-stu-id="79d4a-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="79d4a-110">Для рекурсивной проверки того, что объект является членом группы, перечислите группы в свойстве Member, проверьте члены этих групп, чтобы определить, является ли объект членом, и если эти группы содержат другие группы, проверьте их члены и т. д.</span><span class="sxs-lookup"><span data-stu-id="79d4a-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="79d4a-111">Поскольку группы могут быть вложенными, членство в группе может иметь циклы.</span><span class="sxs-lookup"><span data-stu-id="79d4a-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="79d4a-112">Любой скрипт, который перечисляет несколько групп, должен обеспечить выполнение внутреннего списка групп для завершения рекурсии, если группа уже была открыта.</span><span class="sxs-lookup"><span data-stu-id="79d4a-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 