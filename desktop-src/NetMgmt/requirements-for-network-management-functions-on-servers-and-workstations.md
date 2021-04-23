---
title: Требования к функциям управления сетью на серверах и рабочих станциях
description: При вызове одной из функций управления сетью, перечисленных в этом разделе на сервере или рабочей станции, разные требования к доступу применяются к информационным запросам и обновлениям информации.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890992"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="8cff1-103">Требования к функциям управления сетью на серверах и рабочих станциях</span><span class="sxs-lookup"><span data-stu-id="8cff1-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="8cff1-104">При вызове одной из функций управления сетью, перечисленных в этом разделе на сервере или рабочей станции, разные требования к доступу применяются к информационным запросам и обновлениям информации.</span><span class="sxs-lookup"><span data-stu-id="8cff1-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="8cff1-105">Запросы</span><span class="sxs-lookup"><span data-stu-id="8cff1-105">Queries</span></span>

<span data-ttu-id="8cff1-106">При вызове одной из следующих функций для выполнения запроса на сервере или рабочей станции по умолчанию все прошедшие проверку пользователи могут считывать и перечислять данные.</span><span class="sxs-lookup"><span data-stu-id="8cff1-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="8cff1-107">[**Нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**нетграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**нетграупжетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="8cff1-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="8cff1-108">[**Нетлокалграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**нетлокалграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**нетлокалграупжетмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="8cff1-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="8cff1-109">**неткуеридисплайинформатион**</span><span class="sxs-lookup"><span data-stu-id="8cff1-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="8cff1-110">[**Нетсессионжетинфо**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (только уровни 1 и 2)</span><span class="sxs-lookup"><span data-stu-id="8cff1-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="8cff1-111">[**Нетшаринум**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (только уровни 2 и 502)</span><span class="sxs-lookup"><span data-stu-id="8cff1-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="8cff1-112">[**Нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**нетусержетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**нетусержетлокалграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**нетусермодалсжет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="8cff1-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="8cff1-113">[**Нетвкстажетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **нетвкстаусеренум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="8cff1-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="8cff1-114">Ниже приведены дополнительные сведения об анонимном доступе при чтении и перечислении информации.</span><span class="sxs-lookup"><span data-stu-id="8cff1-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="8cff1-115">**Windows Server 2003 и Windows XP:** Анонимный доступ к информации возможен, если параметр политики Еверйонеинклудесанонимаус разрешает анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="8cff1-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="8cff1-116">**Windows 2000:** Анонимный доступ к защищаемым объектам возможен, если параметр политики RestrictAnonymous разрешает анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="8cff1-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="8cff1-117">Можно ограничить анонимный доступ, задав для следующего раздела реестра значение 1.</span><span class="sxs-lookup"><span data-stu-id="8cff1-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="8cff1-118">**HKey \_ Локальный \_ компьютер \\ система \\ CurrentControlSet \\ Управление \\ LSA** \\ **RestrictAnonymous** = 1</span><span class="sxs-lookup"><span data-stu-id="8cff1-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="8cff1-119">Дополнительные сведения см. в следующей статье базы знаний Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="8cff1-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="8cff1-120">Идентификатор статьи: [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="8cff1-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="8cff1-121">TITLE: использование значения реестра RestrictAnonymous.</span><span class="sxs-lookup"><span data-stu-id="8cff1-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="8cff1-122">Обновления</span><span class="sxs-lookup"><span data-stu-id="8cff1-122">Updates</span></span>

<span data-ttu-id="8cff1-123">По умолчанию данные могут записывать только администраторы и опытные пользователи.</span><span class="sxs-lookup"><span data-stu-id="8cff1-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="8cff1-124">Дополнительные сведения об управлении доступом к защищаемым объектам см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control), [права](/windows/desktop/SecAuthZ/privileges)доступа и [защищаемые объекты](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="8cff1-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="8cff1-125">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="8cff1-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 