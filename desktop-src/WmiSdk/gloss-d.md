---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080894"
---
# <a name="d-wmi"></a><span data-ttu-id="085ea-103">D (WMI)</span><span class="sxs-lookup"><span data-stu-id="085ea-103">D (WMI)</span></span>

<span data-ttu-id="085ea-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="085ea-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="085ea-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**</span><span class="sxs-lookup"><span data-stu-id="085ea-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**datetime**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-106">См. раздел [*DateTime CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="085ea-106">See [*CIM datetime*](gloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="085ea-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**Несвязанный поставщик**</span><span class="sxs-lookup"><span data-stu-id="085ea-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**decoupled provider**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-108">Поставщик, который выполняется в отдельном от WMI процессе.</span><span class="sxs-lookup"><span data-stu-id="085ea-108">A provider hosted in a separate process from WMI.</span></span> <span data-ttu-id="085ea-109">Для инструментирования приложения рекомендуется использовать несвязанные поставщики, так как поставщик может управлять собственным временем существования, а не запускать каждый раз, когда пользователь обращается к поставщику через WMI.</span><span class="sxs-lookup"><span data-stu-id="085ea-109">Decoupled providers are the recommended way to instrument an application, because the provider can control its own lifetime instead of being started each time a user accesses the provider through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="085ea-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**прямой доступ**</span><span class="sxs-lookup"><span data-stu-id="085ea-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direct access**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-111">Способ доступа к свойствам и методам, предоставляемым WMI в скрипте, как если бы они были свойствами автоматизации и методами [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="085ea-111">A way to access properties and methods supplied by WMI in a script as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="085ea-112">Непосредственный доступ: `VolumeName = MyDisk.Properties_("VolumeName")`</span><span class="sxs-lookup"><span data-stu-id="085ea-112">Nondirect access: `VolumeName = MyDisk.Properties_("VolumeName")`</span></span>

<span data-ttu-id="085ea-113">Прямой доступ: `VolumeName = MyDisk.VolumeName`</span><span class="sxs-lookup"><span data-stu-id="085ea-113">Direct access: `VolumeName = MyDisk.VolumeName`</span></span>

</dd> <dt>

<span data-ttu-id="085ea-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Распределенное управление задачей Force (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="085ea-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-115">Международная организация стандартов, которая работает с основными поставщиками технологий, включая Майкрософт, для разработки, внедрения и унификации стандартов управления и инициатив для настольных, корпоративных и Интернет сред.</span><span class="sxs-lookup"><span data-stu-id="085ea-115">An international standards organization that works with key technology vendors, including Microsoft, to lead the development, adoption, and unification of management standards and initiatives for desktop, enterprise, and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="085ea-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span><span class="sxs-lookup"><span data-stu-id="085ea-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-117">См. раздел *распределенное управление Task Force (DMTF)*.</span><span class="sxs-lookup"><span data-stu-id="085ea-117">See *Distributed Management Task Force (DMTF)*.</span></span>

</dd> <dt>

<span data-ttu-id="085ea-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**динамический класс**</span><span class="sxs-lookup"><span data-stu-id="085ea-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamic class**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-119">Класс CIM, определение которого предоставляется [*поставщиком*](gloss-p.md) во время выполнения по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="085ea-119">A CIM class whose definition is supplied by a [*provider*](gloss-p.md) at run time, as required.</span></span> <span data-ttu-id="085ea-120">Динамические классы представляют [*управляемые объекты*](gloss-m.md) , зависящие от поставщика, и не хранятся в [*репозитории CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="085ea-120">Dynamic classes represent provider-specific [*managed objects*](gloss-m.md) and are not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="085ea-121">Динамические классы поддерживают только *динамические экземпляры*.</span><span class="sxs-lookup"><span data-stu-id="085ea-121">Dynamic classes support only *dynamic instances*.</span></span>

</dd> <dt>

<span data-ttu-id="085ea-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**динамический экземпляр**</span><span class="sxs-lookup"><span data-stu-id="085ea-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamic instance**</span></span>
</dt> <dd>

<span data-ttu-id="085ea-123">Экземпляр класса CIM, предоставляемый [*поставщиком*](gloss-p.md) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="085ea-123">An instance of a CIM class that is supplied by a [*provider*](gloss-p.md) when required.</span></span> <span data-ttu-id="085ea-124">Он не хранится в [*репозитории CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="085ea-124">It is not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="085ea-125">Динамические экземпляры могут быть предоставлены либо для статических, либо для динамических классов.</span><span class="sxs-lookup"><span data-stu-id="085ea-125">Dynamic instances can be provided for either static or dynamic classes.</span></span> <span data-ttu-id="085ea-126">Динамически поддерживающие экземпляры класса позволяют поставщику предоставлять значения [*свойств*](gloss-p.md) , сопоставляемые в минуту.</span><span class="sxs-lookup"><span data-stu-id="085ea-126">Dynamically supporting instances of a class enables a provider to supply up-to-the-minute [*property*](gloss-p.md) values.</span></span>

</dd> </dl>

 

 



