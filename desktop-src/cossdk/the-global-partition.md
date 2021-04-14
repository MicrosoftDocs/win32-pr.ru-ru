---
description: Глобальный раздел
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: Глобальный раздел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496650"
---
# <a name="the-global-partition"></a><span data-ttu-id="593af-103">Глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="593af-103">The Global Partition</span></span>

<span data-ttu-id="593af-104">В дополнение к определенным администратором секциям и наборам разделов на каждом компьютере имеется специальный раздел, называемый *глобальным разделом*.</span><span class="sxs-lookup"><span data-stu-id="593af-104">In addition to administrator-defined partitions and partition sets, there is a special partition on each computer called a *global partition*.</span></span> <span data-ttu-id="593af-105">Глобальный раздел создается автоматически при установке COM+.</span><span class="sxs-lookup"><span data-stu-id="593af-105">A global partition is automatically created when COM+ is installed.</span></span> <span data-ttu-id="593af-106">Глобальный раздел предназначен для размещения приложений на уровне системы, которые должны быть доступны всем пользователям на сервере или в домене.</span><span class="sxs-lookup"><span data-stu-id="593af-106">The global partition is designed to contain system-wide applications that need to be accessible to all users on a server or in the domain.</span></span> <span data-ttu-id="593af-107">Установка приложения в глобальный раздел устраняет необходимость установки копии приложения в набор разделов каждого отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="593af-107">Installing an application into the global partition removes the need to install a copy of the application into each individual user's partition set.</span></span>

<span data-ttu-id="593af-108">Если набор разделов пользователя не включает определенное приложение, к которому пытается получить доступ пользователь, но это приложение устанавливается в глобальном разделе, приложение активируется из глобального раздела.</span><span class="sxs-lookup"><span data-stu-id="593af-108">If a user's partition set does not include a specific application that the user is attempting to access, but that application is installed in the global partition, the application is activated from the global partition.</span></span> <span data-ttu-id="593af-109">Однако в этом случае все компоненты приложения, установленные в глобальном разделе, должны быть помечены как открытые, а не закрытые компоненты.</span><span class="sxs-lookup"><span data-stu-id="593af-109">In this case, however, all components of the application installed in the global partition must be marked as public, not private, components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="593af-110">См. также</span><span class="sxs-lookup"><span data-stu-id="593af-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="593af-111">Секции по умолчанию</span><span class="sxs-lookup"><span data-stu-id="593af-111">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="593af-112">Локальные секции</span><span class="sxs-lookup"><span data-stu-id="593af-112">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="593af-113">Свойства секции</span><span class="sxs-lookup"><span data-stu-id="593af-113">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="593af-114">Секции и Active Directory</span><span class="sxs-lookup"><span data-stu-id="593af-114">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> </dl>

 

 



