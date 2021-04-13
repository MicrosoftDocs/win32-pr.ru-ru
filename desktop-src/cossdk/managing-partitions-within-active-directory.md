---
description: В качестве альтернативы управлению Active Directory разделами с помощью средства администрирования Active Directory пользователей и компьютеров можно управлять разделами COM+ программным путем с помощью набора объектов COM+ в Active Directory системном интерфейсе (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Управление секциями в Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539284"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="880ac-103">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="880ac-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="880ac-104">В качестве альтернативы управлению Active Directory разделами с помощью средства администрирования Active Directory пользователей и компьютеров можно управлять разделами COM+ программным путем с помощью набора объектов COM+ в Active Directory системном интерфейсе (ADSI).</span><span class="sxs-lookup"><span data-stu-id="880ac-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="880ac-105">Независимо от методики администрирования, выбранной для управления разделами COM+, существует общая последовательность действий, которые должны выполнять администраторы.</span><span class="sxs-lookup"><span data-stu-id="880ac-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="880ac-106">Создайте новые разделы COM+ в Active Directory для своего домена.</span><span class="sxs-lookup"><span data-stu-id="880ac-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="880ac-107">Создайте наборы разделов COM+ в Active Directory и сопоставьте их с созданными разделами COM+.</span><span class="sxs-lookup"><span data-stu-id="880ac-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="880ac-108">Настройте разделы Active Directory на локальном компьютере с помощью соответствующего объекта COM+.</span><span class="sxs-lookup"><span data-stu-id="880ac-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="880ac-109">При настройке раздела Active Directory на локальном компьютере в папке этого раздела автоматически создается папка **приложений COM+** .</span><span class="sxs-lookup"><span data-stu-id="880ac-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="880ac-110">Установите приложения COM+ в соответствующих разделах COM+.</span><span class="sxs-lookup"><span data-stu-id="880ac-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="880ac-111">Все предыдущие шаги можно выполнить программно, используя набор Active Directory интерфейсов, называемых ADSI.</span><span class="sxs-lookup"><span data-stu-id="880ac-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="880ac-112">Ниже перечислены объекты, доступные для управления секциями, доступными в ADSI.</span><span class="sxs-lookup"><span data-stu-id="880ac-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="880ac-113">\_имя УСЕРПАРТИТИОНСЕТЛИНК \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="880ac-114">\_имя ПАРТИТИОНЛИНК \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="880ac-115">\_имя ObjectID \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="880ac-116">\_имя ДЕФАУЛТПАРТИТИОНЛИНК \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="880ac-117">\_имя УСЕРЛИНК \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="880ac-118">\_имя подраздела DS \_</span><span class="sxs-lookup"><span data-stu-id="880ac-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="880ac-119">\_имя раздела \_ DS</span><span class="sxs-lookup"><span data-stu-id="880ac-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="880ac-120">Сведения о создании разделов COM+ и управлении ими с помощью Active Directory пользователи и компьютеры и средства администрирования служб компонентов см. в справке в Интернете, доступной в рамках каждого средства.</span><span class="sxs-lookup"><span data-stu-id="880ac-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="880ac-121">См. также</span><span class="sxs-lookup"><span data-stu-id="880ac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="880ac-122">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="880ac-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="880ac-123">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="880ac-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="880ac-124">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="880ac-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="880ac-125">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="880ac-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="880ac-126">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="880ac-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



