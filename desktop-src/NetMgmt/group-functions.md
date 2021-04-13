---
title: Групповые функции
description: Глобальная группа содержит учетные записи пользователей из одного домена, сгруппированных с одной группой имен учетных записей.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413484"
---
# <a name="group-functions"></a><span data-ttu-id="44364-103">Групповые функции</span><span class="sxs-lookup"><span data-stu-id="44364-103">Group Functions</span></span>

<span data-ttu-id="44364-104">*Глобальная группа* содержит учетные записи пользователей из одного домена, сгруппированных с одной группой имен учетных записей.</span><span class="sxs-lookup"><span data-stu-id="44364-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="44364-105">Глобальная группа может содержать только членов (пользователей) из домена, в котором создана Глобальная группа; Он не может содержать локальные группы.</span><span class="sxs-lookup"><span data-stu-id="44364-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="44364-106">Глобальная группа доступна в собственном домене и в любом доверяющем домене.</span><span class="sxs-lookup"><span data-stu-id="44364-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="44364-107">Функции группы управления сетью управляют глобальными группами.</span><span class="sxs-lookup"><span data-stu-id="44364-107">The network management group functions control global groups.</span></span> <span data-ttu-id="44364-108">Групповые функции перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="44364-108">The group functions are listed following.</span></span>



| <span data-ttu-id="44364-109">Функция</span><span class="sxs-lookup"><span data-stu-id="44364-109">Function</span></span>                                     | <span data-ttu-id="44364-110">Описание</span><span class="sxs-lookup"><span data-stu-id="44364-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="44364-111">**нетграупадд**</span><span class="sxs-lookup"><span data-stu-id="44364-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="44364-112">Создает глобальную группу.</span><span class="sxs-lookup"><span data-stu-id="44364-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="44364-113">**нетграупаддусер**</span><span class="sxs-lookup"><span data-stu-id="44364-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="44364-114">Добавляет одного пользователя в существующую глобальную группу.</span><span class="sxs-lookup"><span data-stu-id="44364-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="44364-115">**нетграупдел**</span><span class="sxs-lookup"><span data-stu-id="44364-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="44364-116">Удаляет глобальную группу независимо от того, содержит ли группа какие-либо члены.</span><span class="sxs-lookup"><span data-stu-id="44364-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="44364-117">**нетграупделусер**</span><span class="sxs-lookup"><span data-stu-id="44364-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="44364-118">Удаляет одно имя пользователя из глобальной группы.</span><span class="sxs-lookup"><span data-stu-id="44364-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="44364-119">**нетграупенум**</span><span class="sxs-lookup"><span data-stu-id="44364-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="44364-120">Список всех глобальных групп на сервере.</span><span class="sxs-lookup"><span data-stu-id="44364-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="44364-121">**нетграупжетинфо**</span><span class="sxs-lookup"><span data-stu-id="44364-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="44364-122">Возвращает сведения о конкретной глобальной группе.</span><span class="sxs-lookup"><span data-stu-id="44364-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="44364-123">**нетграупжетусерс**</span><span class="sxs-lookup"><span data-stu-id="44364-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="44364-124">Список всех членов определенной глобальной группы.</span><span class="sxs-lookup"><span data-stu-id="44364-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="44364-125">**нетграупсетинфо**</span><span class="sxs-lookup"><span data-stu-id="44364-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="44364-126">Задает общие сведения о глобальной группе.</span><span class="sxs-lookup"><span data-stu-id="44364-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="44364-127">**нетграупсетусерс**</span><span class="sxs-lookup"><span data-stu-id="44364-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="44364-128">Назначает члены новой глобальной группе; заменяет члены существующей группы.</span><span class="sxs-lookup"><span data-stu-id="44364-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="44364-129">При вызове функции [**нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) для создания глобальной группы необходимо указать имя группы.</span><span class="sxs-lookup"><span data-stu-id="44364-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="44364-130">Изначально новая группа не имеет членов.</span><span class="sxs-lookup"><span data-stu-id="44364-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="44364-131">Учетные записи пользователей автоматически принадлежат к особым пользователям домена глобальной группы.</span><span class="sxs-lookup"><span data-stu-id="44364-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="44364-132">Членство в этой группе косвенно контролируется функциями [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)и [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="44364-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="44364-133">Сведения об учетной записи глобальной группы доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="44364-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="44364-134">**\_Сведения о группе \_ 0**</span><span class="sxs-lookup"><span data-stu-id="44364-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="44364-135">**\_Сведения о группе \_ 1**</span><span class="sxs-lookup"><span data-stu-id="44364-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="44364-136">**\_Сведения о группе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="44364-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="44364-137">**\_Сведения о группе \_ 3**</span><span class="sxs-lookup"><span data-stu-id="44364-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="44364-138">**\_Сведения о группе \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="44364-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="44364-139">**\_Сведения о группе \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="44364-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="44364-140">Уровни 1002 и 1005 допустимы только для функции [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .</span><span class="sxs-lookup"><span data-stu-id="44364-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="44364-141">Сведения о члене глобальной группы доступны на следующем уровне информации:</span><span class="sxs-lookup"><span data-stu-id="44364-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="44364-142">**\_Сведения о пользователях группы \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="44364-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="44364-143">Дополнительные сведения см. в разделе [функции локальной группы](local-group-functions.md)управления сетью.</span><span class="sxs-lookup"><span data-stu-id="44364-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="44364-144">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции группы управления сетью.</span><span class="sxs-lookup"><span data-stu-id="44364-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="44364-145">Дополнительные сведения см. в разделе [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="44364-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 