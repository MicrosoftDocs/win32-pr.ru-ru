---
title: Перечисление членов в группе
description: Члены группы хранятся в атрибуте с несколькими значениями, называемом Member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Перечисление членов в группе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133686"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="e2642-104">Перечисление членов в группе</span><span class="sxs-lookup"><span data-stu-id="e2642-104">Enumerating Members in a Group</span></span>

<span data-ttu-id="e2642-105">Члены группы хранятся в атрибуте с несколькими значениями, называемом **member**.</span><span class="sxs-lookup"><span data-stu-id="e2642-105">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="e2642-106">Для групп с небольшим и средним членством используйте метод [**иадсграуп. members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) , чтобы получить указатель на объект [**иадсмемберс**](/windows/desktop/api/iads/nn-iads-iadsmembers) , содержащий список всех элементов.</span><span class="sxs-lookup"><span data-stu-id="e2642-106">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="e2642-107">Затем используйте [**иадсмемберс:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) , чтобы получить объект перечислителя, который можно использовать для перечисления элементов.</span><span class="sxs-lookup"><span data-stu-id="e2642-107">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="e2642-108">Если ожидаемое членство в группе будет составлять 1000 или более членов, используйте для извлечения пользователей по одному диапазону за раз.</span><span class="sxs-lookup"><span data-stu-id="e2642-108">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="e2642-109">Дополнительные сведения об использовании различных компонентов для перечисления элементов см. в разделе [Перечисление групп, содержащих много элементов](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="e2642-109">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 