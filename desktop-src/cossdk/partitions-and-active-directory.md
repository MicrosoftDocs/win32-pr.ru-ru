---
description: Помимо секций, содержащих одно или несколько приложений, COM+ также включает наборы разделов, содержащие одну или несколько секций.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Секции и Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673123"
---
# <a name="partitions-and-active-directory"></a><span data-ttu-id="312bf-103">Секции и Active Directory</span><span class="sxs-lookup"><span data-stu-id="312bf-103">Partitions and Active Directory</span></span>

<span data-ttu-id="312bf-104">Помимо секций, содержащих одно или несколько приложений, COM+ также включает *наборы разделов*, содержащие одну или несколько секций.</span><span class="sxs-lookup"><span data-stu-id="312bf-104">In addition to partitions, which contain one or more applications, COM+ also includes *partition sets*, which contain one or more partitions.</span></span> <span data-ttu-id="312bf-105">Наборы разделов, созданные в Active Directory, позволяют пользователям домена получать доступ к приложениям COM+ во всем домене.</span><span class="sxs-lookup"><span data-stu-id="312bf-105">Created in Active Directory, partition sets allow users in a domain to access COM+ applications throughout the domain.</span></span> <span data-ttu-id="312bf-106">Во время создания каждый конкретный пользователь или подразделение (OU) назначается или сопоставляется с набором разделов.</span><span class="sxs-lookup"><span data-stu-id="312bf-106">During creation, each specific user or organizational unit (OU) is assigned, or mapped, to a partition set.</span></span>

<span data-ttu-id="312bf-107">Один пользователь или подразделение могут обращаться к нескольким разделам и их приложениям, так как между удостоверением пользователя или подразделением и набором секций существует корреляция "один к одному".</span><span class="sxs-lookup"><span data-stu-id="312bf-107">A single user or OU can access multiple partitions and their applications because there is a one-to-one correlation between a user identity or OU and a partition set.</span></span> <span data-ttu-id="312bf-108">Без набора разделов пользователю или подразделению потребуется несколько удостоверений пользователей для доступа к приложениям в разных разделах.</span><span class="sxs-lookup"><span data-stu-id="312bf-108">Without a partition set, a user or OU would need multiple user identities to access applications in different partitions.</span></span>

<span data-ttu-id="312bf-109">Чтобы сделать приложения COM+ доступными для пользователей домена, администратор должен выполнить задачи на контроллере домена, где Active Directory находится на сервере, на котором установлено приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="312bf-109">To make COM+ applications available to domain users, an administrator must perform tasks both on the domain controller where Active Directory resides and on the server where the COM+ application is installed.</span></span>

## <a name="on-the-domain-controller"></a><span data-ttu-id="312bf-110">На контроллере домена</span><span class="sxs-lookup"><span data-stu-id="312bf-110">On the Domain Controller</span></span>

<span data-ttu-id="312bf-111">Администратор сначала создает раздел в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="312bf-111">The administrator first creates a partition within Active Directory.</span></span> <span data-ttu-id="312bf-112">Создание раздела COM+ выполняется либо с помощью средства администрирования Active Directory пользователи и компьютеры, либо программно с помощью интерфейса Active Directory Services (ADSI).</span><span class="sxs-lookup"><span data-stu-id="312bf-112">Creating a COM+ partition is done either through the use of the Active Directory Users and Computers administrative tool or programmatically by using the Active Directory Services Interface (ADSI).</span></span>

<span data-ttu-id="312bf-113">После создания секции в Active Directory администратор создает набор разделов.</span><span class="sxs-lookup"><span data-stu-id="312bf-113">After the partition has been created within Active Directory, the administrator then creates a partition set.</span></span> <span data-ttu-id="312bf-114">При создании набора разделов администратор определяет разделы, входящие в этот набор.</span><span class="sxs-lookup"><span data-stu-id="312bf-114">In creating a partition set, the administrator defines the partitions that are included in that set.</span></span> <span data-ttu-id="312bf-115">Создание набора разделов COM+ выполняется либо с помощью средства администрирования Active Directory пользователи и компьютеры, либо программно с помощью интерфейса Active Directory Services (ADSI).</span><span class="sxs-lookup"><span data-stu-id="312bf-115">Creating a COM+ partition set is done either through the use of the Active Directory Users and Computers administrative tool or programmatically by using the Active Directory Services Interface (ADSI).</span></span>

<span data-ttu-id="312bf-116">Наконец, администратор сопоставляет пользователей домена или подразделения с только что созданным набором разделов.</span><span class="sxs-lookup"><span data-stu-id="312bf-116">Finally, the administrator maps domain users or organizational units (OUs) to the newly created partition set.</span></span> <span data-ttu-id="312bf-117">Это делается путем отображения страницы **свойств** пользователя, доступа к вкладке « **наборы разделов COM+** » и выбора набора разделов из списка.</span><span class="sxs-lookup"><span data-stu-id="312bf-117">This is done by displaying a user's **Properties** page, accessing the **COM+ Partition Sets** tab, and selecting a partition set from the list box.</span></span>

## <a name="on-the-com-application-server"></a><span data-ttu-id="312bf-118">На сервере приложений COM+</span><span class="sxs-lookup"><span data-stu-id="312bf-118">On the COM+ Application Server</span></span>

<span data-ttu-id="312bf-119">Администратор создает новый раздел, указывая то же имя секции и идентификатор раздела (GUID), что и для раздела, созданного в Active Directory на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="312bf-119">The administrator creates a new partition, specifying the same partition name and partition ID (GUID) as that of the partition that was created within Active Directory on the domain controller.</span></span> <span data-ttu-id="312bf-120">Это делается с помощью папки " **разделы COM+** " в средстве администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="312bf-120">This is done using the **COM+ Partitions** folder within the Component Services administrative tool.</span></span> <span data-ttu-id="312bf-121">Чтобы упростить эту задачу, средство "службы компонентов" позволяет администратору просматривать Active Directory, чтобы выбрать нужную секцию и ее идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="312bf-121">To simplify this task, the Component Services tool allows the administrator to browse Active Directory to select the desired partition and its GUID.</span></span>

<span data-ttu-id="312bf-122">При создании раздела домена на сервере приложений раздел по умолчанию пользователя станет разделом по умолчанию раздела, установленного в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="312bf-122">When the domain partition has been created on the application server, a user's default partition becomes the default partition of the partition set in the Active Directory.</span></span> <span data-ttu-id="312bf-123">Наконец, администратор может установить приложение COM+ в созданном разделе на сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="312bf-123">Finally, the administrator can install the COM+ application into the newly created partition on the application server.</span></span>

<span data-ttu-id="312bf-124">Дополнительные сведения об администрировании разделов для доступа пользователей домена см. в справке, связанной с средством администрирования Active Directory пользователи и компьютеры.</span><span class="sxs-lookup"><span data-stu-id="312bf-124">For more information about administering partitions for access by domain users, see the help associated with the Active Directory Users and Computers administrative tool.</span></span>

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a><span data-ttu-id="312bf-125">Сопоставление удостоверений пользователей и подразделений с наборами разделов</span><span class="sxs-lookup"><span data-stu-id="312bf-125">Mapping User Identities and OUs to Partition Sets</span></span>

<span data-ttu-id="312bf-126">Пользователи и подразделения могут быть сопоставлены с наборами секций.</span><span class="sxs-lookup"><span data-stu-id="312bf-126">Users and OUs can be mapped to a partition sets.</span></span> <span data-ttu-id="312bf-127">При сопоставлении подразделений с наборами разделов администратор может одновременно связать нескольких пользователей с набором секций, вместо того чтобы сопоставлять несколько удостоверений пользователей.</span><span class="sxs-lookup"><span data-stu-id="312bf-127">By mapping OUs to partition sets, an administrator can associate multiple users with a partition set at one time instead of having to map multiple user identities.</span></span> <span data-ttu-id="312bf-128">Одно удостоверение пользователя или подразделение можно сопоставить только с одним набором разделов.</span><span class="sxs-lookup"><span data-stu-id="312bf-128">A single user identity or OU can be mapped to one partition set only.</span></span> <span data-ttu-id="312bf-129">Как правило, Сопоставление удостоверений пользователей или подразделений с наборами секций выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="312bf-129">In general, mapping user identities or OUs to partition sets does the following:</span></span>

-   <span data-ttu-id="312bf-130">Гарантирует, что приложения будут доступны соответствующим пользователям в домене.</span><span class="sxs-lookup"><span data-stu-id="312bf-130">Ensures that applications are available to the appropriate users in the domain</span></span>
-   <span data-ttu-id="312bf-131">Помогает COM+ определить раздел, в котором находится приложение</span><span class="sxs-lookup"><span data-stu-id="312bf-131">Helps COM+ in determining the partition in which an application is located</span></span>
-   <span data-ttu-id="312bf-132">Устанавливает право пользователя на доступ к определенному приложению</span><span class="sxs-lookup"><span data-stu-id="312bf-132">Establishes a user's right to access a particular application</span></span>

<span data-ttu-id="312bf-133">Для связывания секций с наборами разделов в Active Directory и сопоставления пользователей и подразделений с этими наборами разделов администраторы используют средства администрирования Active Directory пользователи и компьютеры и службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="312bf-133">To associate partitions with partition sets within Active Directory and to map users and OUs to those partition sets, administrators use the Active Directory Users and Computers and Component Services administrative tools.</span></span> <span data-ttu-id="312bf-134">При создании секции в Active Directory администратору необходимо локально настроить этот раздел на компьютере, на котором должно быть установлено соответствующее приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="312bf-134">When a partition is created within Active Directory, an administrator needs to locally configure that partition on the computer where the relevant COM+ application is to be installed.</span></span> <span data-ttu-id="312bf-135">Эта локальная конфигурация секций, созданных в Active Directory, выполняется с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="312bf-135">This local configuration of partitions created within Active Directory is done through the Component Services administrative tool.</span></span>

<span data-ttu-id="312bf-136">Если удостоверение пользователя домена не сопоставлено с набором разделов, пользователю предоставляется доступ к подразделению пользователя, которое сопоставляется с секцией.</span><span class="sxs-lookup"><span data-stu-id="312bf-136">If a domain user identity is not mapped to a partition set, the user is granted access by the user's OU, which is mapped to the partition.</span></span> <span data-ttu-id="312bf-137">Если подразделение пользователя не сопоставлено с набором разделов, но следующее наибольшее подразделение в иерархии сопоставлено с этим набором разделов, пользователь может получить доступ к этой секции.</span><span class="sxs-lookup"><span data-stu-id="312bf-137">If the user's OU is not mapped to a partition set but the next highest OU in the hierarchy is mapped to that partition set, the user can access the partition.</span></span>

## <a name="related-topics"></a><span data-ttu-id="312bf-138">См. также</span><span class="sxs-lookup"><span data-stu-id="312bf-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312bf-139">Секции по умолчанию</span><span class="sxs-lookup"><span data-stu-id="312bf-139">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="312bf-140">Локальные секции</span><span class="sxs-lookup"><span data-stu-id="312bf-140">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="312bf-141">Свойства секции</span><span class="sxs-lookup"><span data-stu-id="312bf-141">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="312bf-142">Глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="312bf-142">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



