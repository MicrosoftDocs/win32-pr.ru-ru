---
title: Перечисление членов в группе
description: Дополнительные сведения о перечислении членов в группе Azure Active Directory. Члены группы хранятся в атрибуте с несколькими значениями, называемом Member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Перечисление членов в группе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407427"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="e6865-105">Перечисление членов в группе</span><span class="sxs-lookup"><span data-stu-id="e6865-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="e6865-106">Члены группы хранятся в атрибуте с несколькими значениями, называемом **member**.</span><span class="sxs-lookup"><span data-stu-id="e6865-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="e6865-107">Для групп с небольшим и средним членством используйте метод [**иадсграуп. members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) , чтобы получить указатель на объект [**иадсмемберс**](/windows/desktop/api/iads/nn-iads-iadsmembers) , содержащий список всех элементов.</span><span class="sxs-lookup"><span data-stu-id="e6865-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="e6865-108">Затем используйте [**иадсмемберс:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) , чтобы получить объект перечислителя, который можно использовать для перечисления элементов.</span><span class="sxs-lookup"><span data-stu-id="e6865-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="e6865-109">Если ожидаемое членство в группе будет составлять 1000 или более членов, используйте для извлечения пользователей по одному диапазону за раз.</span><span class="sxs-lookup"><span data-stu-id="e6865-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="e6865-110">Дополнительные сведения об использовании различных компонентов для перечисления элементов см. в разделе [Перечисление групп, содержащих много элементов](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="e6865-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 