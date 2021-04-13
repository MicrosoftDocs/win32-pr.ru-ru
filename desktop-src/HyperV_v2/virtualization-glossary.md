---
description: Глоссарий терминов, используемых в документации по пакету SDK для виртуализации Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Глоссарий Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272074"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="08e8d-103">Глоссарий Hyper-V</span><span class="sxs-lookup"><span data-stu-id="08e8d-103">Hyper-V glossary</span></span>

<span data-ttu-id="08e8d-104">В этом разделе содержится глоссарий терминов, используемых в документации по пакету SDK для виртуализации Windows.</span><span class="sxs-lookup"><span data-stu-id="08e8d-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="08e8d-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**вязывания**</span><span class="sxs-lookup"><span data-stu-id="08e8d-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-106">Процесс, с помощью которого службы и уровни программного обеспечения связываются вместе.</span><span class="sxs-lookup"><span data-stu-id="08e8d-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="08e8d-107">При установке сетевой службы устанавливаются отношения привязки и зависимости для служб.</span><span class="sxs-lookup"><span data-stu-id="08e8d-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Создание**</span><span class="sxs-lookup"><span data-stu-id="08e8d-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-109">Моментальный снимок виртуальной машины, который позволяет администратору восстановить виртуальную машину в ее состояние на момент создания контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="08e8d-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**свернут**</span><span class="sxs-lookup"><span data-stu-id="08e8d-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-111">Уменьшение размера динамически расширяющегося виртуального жесткого диска за счет удаления неиспользуемого пространства из VHD-файла.</span><span class="sxs-lookup"><span data-stu-id="08e8d-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**Разностный виртуальный жесткий диск**</span><span class="sxs-lookup"><span data-stu-id="08e8d-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-113">Виртуальный жесткий диск, на котором хранятся изменения в связанном родительском виртуальном жестком диске, чтобы сохранить родительский объект без изменений.</span><span class="sxs-lookup"><span data-stu-id="08e8d-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="08e8d-114">Разностный диск — это отдельный VHD-файл, связанный с VHD-файлом родительского диска.</span><span class="sxs-lookup"><span data-stu-id="08e8d-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="08e8d-115">Изменения продолжают накапливаться на разностном диске, пока он не будет объединен с родительским диском.</span><span class="sxs-lookup"><span data-stu-id="08e8d-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**динамически расширяемый виртуальный жесткий диск**</span><span class="sxs-lookup"><span data-stu-id="08e8d-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-117">Виртуальный жесткий диск, размер которого увеличивается каждый раз при его изменении.</span><span class="sxs-lookup"><span data-stu-id="08e8d-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="08e8d-118">Этот тип виртуального жесткого диска запускается в виде файла VHD размером 3 КБ и может увеличиваться до максимального размера, указанного при создании файла.</span><span class="sxs-lookup"><span data-stu-id="08e8d-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="08e8d-119">Единственным способом уменьшения размера файла является Обнуление удаленных данных и последующее сжатие виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="08e8d-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**виртуальный жесткий диск фиксированного размера**</span><span class="sxs-lookup"><span data-stu-id="08e8d-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-121">Виртуальный жесткий диск с фиксированным размером, который определяется и для которого выделяется пространство при создании диска.</span><span class="sxs-lookup"><span data-stu-id="08e8d-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="08e8d-122">При добавлении или удалении данных размер диска не изменяется.</span><span class="sxs-lookup"><span data-stu-id="08e8d-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Виртуальная машина поколения 1**</span><span class="sxs-lookup"><span data-stu-id="08e8d-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-124">Виртуальная машина, которая содержит то же виртуальное оборудование, что и версии Hyper-V до Windows 8.1 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="08e8d-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Виртуальная машина поколения 2**</span><span class="sxs-lookup"><span data-stu-id="08e8d-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-126">Виртуальная машина (VM), которая содержит упрощенную виртуальную модель оборудования и использует встроенное по UEFI вместо BIOS.</span><span class="sxs-lookup"><span data-stu-id="08e8d-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="08e8d-127">На этой виртуальной машине удаляются большинство эмулированных устройств, что снижает сложность управления и повышает уровень уязвимости.</span><span class="sxs-lookup"><span data-stu-id="08e8d-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**Гостевая операционная система**</span><span class="sxs-lookup"><span data-stu-id="08e8d-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-129">Операционная система, работающая на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="08e8d-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Службы Integration Services**</span><span class="sxs-lookup"><span data-stu-id="08e8d-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-131">Набор служб и драйверов программного обеспечения, обеспечивающий максимальную производительность и повышающий удобство работы пользователей в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="08e8d-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="08e8d-132">Службы Integration Services доступны только для поддерживаемых гостевых операционных систем.</span><span class="sxs-lookup"><span data-stu-id="08e8d-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**пара "ключ-значение"**</span><span class="sxs-lookup"><span data-stu-id="08e8d-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-134">Набор элементов данных, содержащий уникальный идентификатор, называемый ключом, и значение, которое является реальными данными для ключа.</span><span class="sxs-lookup"><span data-stu-id="08e8d-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**физический компьютер**</span><span class="sxs-lookup"><span data-stu-id="08e8d-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-136">Аппаратный компьютер, а не на виртуальную машину, основанную на программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="08e8d-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**сохраненное состояние**</span><span class="sxs-lookup"><span data-stu-id="08e8d-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-138">Способ хранения виртуальной машины, чтобы его можно было быстро возобновить, как и портативный компьютер в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="08e8d-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="08e8d-139">При помещении работающей виртуальной машины в сохраненное состояние Virtual Server и Hyper-V останавливают виртуальную машину, записывают данные, которые находятся в памяти, во временные файлы, а также останавливают потребление системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08e8d-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="08e8d-140">Восстановление виртуальной машины из сохраненного состояния возвращает ее в то же состояние, в котором она находилась при сохранении состояния.</span><span class="sxs-lookup"><span data-stu-id="08e8d-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**Виртуальный гибкий диск**</span><span class="sxs-lookup"><span data-stu-id="08e8d-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-142">Файловая версия физического гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="08e8d-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="08e8d-143">Виртуальный гибкий диск хранится в виде файла с расширением VFD.</span><span class="sxs-lookup"><span data-stu-id="08e8d-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**виртуальный жесткий диск**</span><span class="sxs-lookup"><span data-stu-id="08e8d-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-145">Среда хранения для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="08e8d-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="08e8d-146">Она может находиться в любой топологии хранилища, к которой может получить доступ операционная система узла, включая внешние устройства, сети хранения данных и хранилище, подключенное к сети.</span><span class="sxs-lookup"><span data-stu-id="08e8d-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="08e8d-147">Расширение имени файла —. VHD.</span><span class="sxs-lookup"><span data-stu-id="08e8d-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**Виртуальная машина**</span><span class="sxs-lookup"><span data-stu-id="08e8d-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-149">Компьютер в пределах компьютера, реализованный в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="08e8d-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="08e8d-150">Виртуальная машина эмулирует полную аппаратную систему, от процессора до сетевой карты, в автономной изолированной программной среде, обеспечивая одновременную работу несовместимых операционных систем.</span><span class="sxs-lookup"><span data-stu-id="08e8d-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="08e8d-151">Каждая дочерняя операционная система выполняется в собственной изолированной программной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="08e8d-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**Конфигурация виртуальной машины**</span><span class="sxs-lookup"><span data-stu-id="08e8d-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-153">Конфигурация ресурсов, назначенных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="08e8d-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="08e8d-154">К примерам относятся такие устройства, как диски и сетевые адаптеры, а также память и процессоры.</span><span class="sxs-lookup"><span data-stu-id="08e8d-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Служба управления виртуальными машинами**</span><span class="sxs-lookup"><span data-stu-id="08e8d-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-156">Служба Hyper-V, обеспечивающая доступ к виртуальным машинам для управления.</span><span class="sxs-lookup"><span data-stu-id="08e8d-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**моментальный снимок виртуальной машины**</span><span class="sxs-lookup"><span data-stu-id="08e8d-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-158">Файловый снимок состояния, данных диска и конфигурации виртуальной машины в конкретный момент времени.</span><span class="sxs-lookup"><span data-stu-id="08e8d-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**Виртуальная сеть**</span><span class="sxs-lookup"><span data-stu-id="08e8d-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-160">Виртуальная версия коммутатора физической сети.</span><span class="sxs-lookup"><span data-stu-id="08e8d-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="08e8d-161">Виртуальную сеть можно настроить для предоставления доступа к локальным или внешним сетевым ресурсам для одной или нескольких виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="08e8d-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Диспетчер виртуальной сети**</span><span class="sxs-lookup"><span data-stu-id="08e8d-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-163">Служба Hyper-V, используемая для создания виртуальных сетей и управления ими.</span><span class="sxs-lookup"><span data-stu-id="08e8d-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**виртуальный коммутатор**</span><span class="sxs-lookup"><span data-stu-id="08e8d-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-165">См. раздел виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="08e8d-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="08e8d-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Изменение размера VHDX**</span><span class="sxs-lookup"><span data-stu-id="08e8d-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="08e8d-167">Операция, которая сжимает или развертывает виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="08e8d-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



