---
description: Поставщик WMI для Hyper-V позволяет разработчикам и программистам быстро создавать собственные средства, служебные программы и усовершенствования для платформы виртуализации. Интерфейсы WMI могут управлять всеми аспектами служб Hyper-V.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: Сведения о поставщике WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663389"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="e2d99-104">Сведения о поставщике WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="e2d99-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="e2d99-105">Поставщик WMI для Hyper-V позволяет разработчикам и программистам быстро создавать собственные средства, служебные программы и усовершенствования для платформы виртуализации.</span><span class="sxs-lookup"><span data-stu-id="e2d99-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="e2d99-106">Интерфейсы WMI могут управлять всеми аспектами служб Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e2d99-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="e2d99-107">О Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="e2d99-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="e2d99-108">Microsoft Windows Server 2008 R2 Hyper-V позволяет системным администраторам консолидировать отдельные серверы оборудования на одном сервере под управлением Microsoft Windows Server 2008 R2 в качестве операционной системы узла.</span><span class="sxs-lookup"><span data-stu-id="e2d99-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="e2d99-109">Каждая из размещенных виртуальных машин выполняется в отдельной изолированной виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="e2d99-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="e2d99-110">Это позволяет администратору легко управлять, предоставлять и поддерживать большое количество виртуальных машин, одновременно уменьшая необходимость запуска нескольких аппаратных решений для использования различных продуктов и операционных систем.</span><span class="sxs-lookup"><span data-stu-id="e2d99-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="e2d99-111">Другое преимущество среды виртуальной машины — тестирование и поддержка.</span><span class="sxs-lookup"><span data-stu-id="e2d99-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="e2d99-112">Новые конфигурации сервера и системы можно развертывать и тестировать параллельно с существующей системой, не требуя дорогостоящего простоя на этапе развертывания.</span><span class="sxs-lookup"><span data-stu-id="e2d99-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="e2d99-113">Каждая виртуальная машина может быть настроена на использование различных конфигураций при работе на стандартной платформе для получения лучших результатов тестирования.</span><span class="sxs-lookup"><span data-stu-id="e2d99-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="e2d99-114">Благодаря поддержке более ранних операционных систем, одна из них может поддерживать и тестировать устаревшее оборудование, системы и приложения.</span><span class="sxs-lookup"><span data-stu-id="e2d99-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="e2d99-115">Поддержка моментальных снимков позволяет создать моментальный снимок состояния виртуальной машины, чтобы при необходимости можно было вернуться к предыдущему событию.</span><span class="sxs-lookup"><span data-stu-id="e2d99-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="e2d99-116">Hyper-V предоставляет многофункциональный интерфейс, позволяющий пользователю отслеживать среду виртуальной машины и управлять ей.</span><span class="sxs-lookup"><span data-stu-id="e2d99-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="e2d99-117">Большая часть Hyper-V может управляться с помощью поставщика WMI, что позволяет легко и, но без труда настраивать виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="e2d99-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="e2d99-118">Дополнительные сведения о том, что можно контролировать с помощью поставщика WMI, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e2d99-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="e2d99-119">Служба управления виртуальными системами</span><span class="sxs-lookup"><span data-stu-id="e2d99-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="e2d99-120">Сетевая служба</span><span class="sxs-lookup"><span data-stu-id="e2d99-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="e2d99-121">Служба управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="e2d99-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="e2d99-122">Новые возможности поставщика WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="e2d99-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



