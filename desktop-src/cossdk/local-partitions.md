---
description: Локальные секции
ms.assetid: 629c4915-00b8-46da-b52a-2d274056eb6c
title: Локальные секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f1a8524b0ebada203d6b42ac7b6cae000f5a51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673119"
---
# <a name="local-partitions"></a><span data-ttu-id="4cda4-103">Локальные секции</span><span class="sxs-lookup"><span data-stu-id="4cda4-103">Local Partitions</span></span>

<span data-ttu-id="4cda4-104">Один из способов использования секций — локально на сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="4cda4-104">One way that partitions can be used is locally on an application server.</span></span> <span data-ttu-id="4cda4-105">В этом сценарии администратор может создать раздел с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="4cda4-105">In this scenario, an administrator can create a partition using the Component Services administrative tool.</span></span> <span data-ttu-id="4cda4-106">Секции, реализованные локально, а не в Active Directory, доступны только локальным пользователям, а не пользователям на других компьютерах в домене.</span><span class="sxs-lookup"><span data-stu-id="4cda4-106">Partitions implemented locally and not within Active Directory are accessible to local users only, not to users on other computers in the domain.</span></span> <span data-ttu-id="4cda4-107">После создания секции и установки в нее приложения COM+ администратор может назначить этот раздел как раздел по умолчанию для одного или нескольких пользователей на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="4cda4-107">After a partition is created and a COM+ application is installed into it, the administrator can assign that partition as a default partition for one or more users on that server.</span></span> <span data-ttu-id="4cda4-108">Для назначения пользователю раздела по умолчанию администратор может использовать средство администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="4cda4-108">To assign a default partition to a user, the administrator can use the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cda4-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4cda4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cda4-110">Секции по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4cda4-110">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="4cda4-111">Свойства секции</span><span class="sxs-lookup"><span data-stu-id="4cda4-111">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="4cda4-112">Секции и Active Directory</span><span class="sxs-lookup"><span data-stu-id="4cda4-112">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="4cda4-113">Глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="4cda4-113">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



