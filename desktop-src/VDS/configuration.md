---
description: Обзор конфигурации
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Обзор конфигурации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991047"
---
# <a name="configuration-overview"></a><span data-ttu-id="02076-103">Обзор конфигурации</span><span class="sxs-lookup"><span data-stu-id="02076-103">Configuration Overview</span></span>

<span data-ttu-id="02076-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02076-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="02076-105">Если вы не знакомы с объектами, определенными службой VDS, см. раздел [объектная модель VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="02076-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="02076-106">Сложность конфигурации виртуального диска может варьироваться от простого в настройке.</span><span class="sxs-lookup"><span data-stu-id="02076-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="02076-107">Несамостоятельные, бесплатные и корпоративные виртуальные диски определяют три типичные перспективы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="02076-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="02076-108">Каждая Перспектива представляет несколько других требований:</span><span class="sxs-lookup"><span data-stu-id="02076-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="02076-109">Неработающие виртуальные диски не настраиваются, возможно, только Автоматизируйте секционирование и форматирование новых дисков или временно создает зеркальный том для переноса данных с одного диска на другой без простоев.</span><span class="sxs-lookup"><span data-stu-id="02076-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="02076-110">Такие диски хорошо подходят для ноутбуков и других систем с одним или несколькими дисками.</span><span class="sxs-lookup"><span data-stu-id="02076-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="02076-111">Виртуальные диски с бесплатной поддержкой — это хранилище, которое обеспечивает самостоятельную настройку, самостоятельное восстановление и доступность; использует чередующиеся тома и LUN для достижения лучшей производительности; для достижения лучшей доступности использует зеркальные тома и LUN. и используют пакеты, чтобы сделать режимы сбоя чистыми и содержащимися.</span><span class="sxs-lookup"><span data-stu-id="02076-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="02076-112">Этот уровень конфигурации идеально подходит при замене старых, небольших, медленных системных дисков новыми, большими и быстрыми дисками.</span><span class="sxs-lookup"><span data-stu-id="02076-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="02076-113">Он также идеально подходит для зеркального отображения данных с помощью автоматического резервирования — один запасной диск может защищать множество дисков.</span><span class="sxs-lookup"><span data-stu-id="02076-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="02076-114">Дополнительные сведения см. в разделе [горячее резервирование](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="02076-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="02076-115">Небольшие сети хранения данных зависят от гибкости и автоматизации, предлагаемых этим уровнем конфигурации, как и устройства сетевого подключения (NAS).</span><span class="sxs-lookup"><span data-stu-id="02076-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="02076-116">Свободные виртуальные диски упрощают задачу консолидации хранилища приложений (например, хранилище для SQL и Exchange) без объединения серверов.</span><span class="sxs-lookup"><span data-stu-id="02076-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="02076-117">Виртуальные диски предприятия содержат очень большие или сложные конфигурации предприятия с дополнительными требованиями для конкретного сайта или приложения.</span><span class="sxs-lookup"><span data-stu-id="02076-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="02076-118">Администраторы настраивайте подсистему хранения для одного приложения, которое может выполняться только редко, например ежемесячное задание пакетного отчета в системе транзакций, принимающей заказы.</span><span class="sxs-lookup"><span data-stu-id="02076-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="02076-119">Виртуальные диски предприятия должны масштабироваться, показывать активность подсистемы хранения в реальном времени и удовлетворять требованиям практических администраторов.</span><span class="sxs-lookup"><span data-stu-id="02076-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="02076-120">Дополнительные сведения о зеркалах, полосковых элементах и других параметрах конфигурации в службе VDS см. в разделе [Привязка томов и LUN](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="02076-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="02076-121">Расширенный способ настройки, называемый наложением, позволяет объединять конфигурации, связанные с существующими томами и LUN.</span><span class="sxs-lookup"><span data-stu-id="02076-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="02076-122">Дополнительные сведения см. в разделе [Настройка стека](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="02076-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02076-123">См. также</span><span class="sxs-lookup"><span data-stu-id="02076-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02076-124">Служба виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="02076-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="02076-125">Объектная модель VDS</span><span class="sxs-lookup"><span data-stu-id="02076-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="02076-126">Горячее резервирование</span><span class="sxs-lookup"><span data-stu-id="02076-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="02076-127">Привязка томов и устройств LUN</span><span class="sxs-lookup"><span data-stu-id="02076-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="02076-128">Настройка стека</span><span class="sxs-lookup"><span data-stu-id="02076-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
