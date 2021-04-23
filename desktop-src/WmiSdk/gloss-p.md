---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999493"
---
# <a name="p-wmi"></a><span data-ttu-id="e4a1a-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="e4a1a-103">P (WMI)</span></span>

<span data-ttu-id="e4a1a-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e4a1a-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e4a1a-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**Счетчик производительности**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-106">Свойство в классе производительности, производное от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , в котором хранятся данные производительности.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**Объект производительности**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-108">Объект в библиотеке производительности, хранящий данные в счетчиках.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="e4a1a-109">Эти объекты отображаются в программе [*системного монитора*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a1a-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="e4a1a-110">Примерами являются объекты кэша и логические диски.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="e4a1a-111">При передаче в WMI процессом [*ADAP*](gloss-a.md) каждый объект превращается в два класса производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="e4a1a-112">Один класс, содержащий необработанные данные, является производным от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="e4a1a-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="e4a1a-113">Другой класс является производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) и содержит те же данные, которые отображаются в системном мониторе, как рассчитывается поставщиком счетчика обработанные.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**Постоянный потребитель**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-115">[*Потребитель событий*](gloss-e.md) , регистрация которого продолжается до тех пор, пока она не будет явно отменена.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="e4a1a-116">См. также [*временный потребитель*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="e4a1a-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**физический потребитель**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-118">COM-объект, реализованный [*поставщиком потребителей событий*](gloss-e.md) , который содержит [*приемник*](gloss-s.md) для получения уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**свойства**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-120">Пара имя/значение, описывающая единицу данных для класса.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="e4a1a-121">Значения свойств должны иметь допустимый [*MOF-файл типа данных (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a1a-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="e4a1a-122">См. также [*свойство Reference*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="e4a1a-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**поставщик свойств**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-124">COM-сервер, который поддерживает извлечение и изменение свойств WMI.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="e4a1a-125">Поставщики свойств реализуют интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .</span><span class="sxs-lookup"><span data-stu-id="e4a1a-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**поставщики**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-127">COM-сервер, который обменивается данными с управляемыми объектами для доступа к данным и уведомлениям о событиях, таким как реестр или SNMP-устройство.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="e4a1a-128">Поставщики перенаправляют эти данные в [*Диспетчер объектов CIM*](gloss-c.md) для интеграции и интерпретации.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="e4a1a-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**метод поставщика**</span><span class="sxs-lookup"><span data-stu-id="e4a1a-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="e4a1a-130">Метод, реализуемый *поставщиком* WMI.</span><span class="sxs-lookup"><span data-stu-id="e4a1a-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
