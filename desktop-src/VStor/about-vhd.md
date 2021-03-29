---
description: Формат виртуального жесткого диска (VHD) представляет собой общедоступную спецификацию формата изображения, которая позволяет инкапсулировать жесткий диск в отдельный файл для использования операционной системой в качестве виртуального диска во всех тех же целях, где используются физические жесткие диски.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: О виртуальных жестких дисках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809791"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span data-ttu-id="bdd7e-103"><span id="vhd.about_vhd"></span>О виртуальных жестких дисках</span><span class="sxs-lookup"><span data-stu-id="bdd7e-103"><span id="vhd.about_vhd"></span>About VHD</span></span>

<span data-ttu-id="bdd7e-104">Формат виртуального жесткого диска (VHD) представляет собой общедоступную [спецификацию](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) формата изображения, которая позволяет инкапсулировать жесткий диск в отдельный файл для использования операционной системой в качестве *виртуального диска* во всех тех же целях, где используются физические жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-104">The Virtual Hard Disk (VHD) format is a publicly-available image format [specification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) that allows encapsulation of the hard disk into an individual file for use by the operating system as a *virtual disk* in all the same ways physical hard disks are used.</span></span> <span data-ttu-id="bdd7e-105">Эти виртуальные диски могут размещать собственные файловые системы (NTFS, FAT, exFAT и UDF), поддерживающие стандартные операции с дисками и файлами.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-105">These virtual disks are capable of hosting native file systems (NTFS, FAT, exFAT, and UDFS) while supporting standard disk and file operations.</span></span> <span data-ttu-id="bdd7e-106">Поддержка API VHD позволяет управлять виртуальными дисками.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-106">VHD API support allows management of the virtual disks.</span></span> <span data-ttu-id="bdd7e-107">Виртуальные диски, созданные с помощью API виртуального жесткого диска, могут работать как загрузочные диски.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-107">Virtual disks created with the VHD API can function as boot disks.</span></span>

<span data-ttu-id="bdd7e-108">Пример использования файлов VHD — компонент [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) в Windows 7, windows Server 2008, Virtual Server и Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-108">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows 7, Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="bdd7e-109">Эти продукты используют API виртуального жесткого диска для размещения образа операционной системы Windows, используемого виртуальной машиной в качестве системного загрузочного диска.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-109">These products use the VHD API to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

<span data-ttu-id="bdd7e-110">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) интегрирует встроенную поддержку VHD для работы с виртуальными дисками, облегчая разработчикам и администраторам создание, Администрирование и развертывание образов Windows в VHD-файлах с помощью API платформы или средства управления.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with virtual disks, making it easier for developers and administrators to create, manage, and deploy Windows images in VHD files using either the platform API support or management tools.</span></span> <span data-ttu-id="bdd7e-111">Для включения этих операций не требуется устанавливать отдельные приложения или использовать средство синтаксического анализа формата VHD.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="bdd7e-112">Эти API-интерфейсы позволяют использовать универсальные виртуальные диски независимо от других технологий виртуализации.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-112">These APIs allow for generic use of virtual disks independent of any other virtualization technologies.</span></span>

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span data-ttu-id="bdd7e-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Терминология</span><span class="sxs-lookup"><span data-stu-id="bdd7e-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminology</span></span>

<span data-ttu-id="bdd7e-114">Термин *резервное хранилище* используется для ссылки на физический файл, существующий на фактическом жестком диске.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-114">The term *backing store* is used to refer to the physical file that exists on the actual hard disk.</span></span> <span data-ttu-id="bdd7e-115">Резервное хранилище представлено *файлом образа VHD*.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-115">The backing store is represented by a *VHD image file*.</span></span>

<span data-ttu-id="bdd7e-116">Термины *динамические*, *расширяемые* и *разреженные* часто взаимозаменяемы при обращении к динамически расширяемым виртуальным дискам.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-116">The terms *dynamic*, *expandable*, and *sparse* are often used interchangeably when referring to dynamically expandable virtual disks.</span></span> <span data-ttu-id="bdd7e-117">Для технологии виртуального жесткого диска эти термины идентичны.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-117">For VHD technology, these terms are identical.</span></span>

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span data-ttu-id="bdd7e-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Общие сведения о компонентах системы VHD</span><span class="sxs-lookup"><span data-stu-id="bdd7e-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD System Features Overview</span></span>

<span data-ttu-id="bdd7e-119">На следующей диаграмме представлен обзор возможностей виртуального жесткого диска и их связей.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-119">The following diagram presents an overview of the VHD features and their relationships.</span></span>

![Схема блокировки виртуальных жестких дисков](images/vhd.png)

<span data-ttu-id="bdd7e-121">Ниже приведено краткое описание описанных выше функций.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-121">The following is a summary explanation of the previously described features.</span></span>

<span data-ttu-id="bdd7e-122">Собственные API Windows для пользовательского режима:</span><span class="sxs-lookup"><span data-stu-id="bdd7e-122">User Mode Native Windows APIs:</span></span>

-   <span data-ttu-id="bdd7e-123">Библиотека VirtDisk.dll-Common для интерфейсов API управления VHD.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-123">VirtDisk.dll - Common library for VHD management APIs.</span></span>

<span data-ttu-id="bdd7e-124">Специальные оболочки управления для домена в пользовательском режиме:</span><span class="sxs-lookup"><span data-stu-id="bdd7e-124">User Mode Domain-specific Management Wrappers:</span></span>

-   <span data-ttu-id="bdd7e-125">[API-интерфейсы ВИРТУАЛЬНЫХ жестких дисков VDS](/windows/desktop/VDS/about-vds) — оболочки объектной модели VDS для интерфейсов Windows VHD.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-125">[VDS VHD APIs](/windows/desktop/VDS/about-vds) - VDS Object Model wrappers for the VHD Windows APIs.</span></span>

<span data-ttu-id="bdd7e-126">Драйверы режима ядра:</span><span class="sxs-lookup"><span data-stu-id="bdd7e-126">Kernel Mode Drivers:</span></span>

-   <span data-ttu-id="bdd7e-127">VDrvRoot.sys — перечислитель виртуального диска root.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-127">VDrvRoot.sys - Root virtual drive enumerator.</span></span>
-   <span data-ttu-id="bdd7e-128">FsDepends.sys Управление зависимостями томов.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-128">FsDepends.sys - Nested volume dependency management.</span></span>
-   <span data-ttu-id="bdd7e-129">Vhdmp.sys-средство синтаксического анализа VHD и поставщик свойств зависимостей.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-129">Vhdmp.sys - VHD parser and dependency property provider.</span></span>

<span data-ttu-id="bdd7e-130">В документации по пакету SDK в этом разделе рассматриваются встроенные интерфейсы API виртуальных жестких дисков Windows в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-130">The SDK documentation in this section covers the user-mode native Windows VHD APIs.</span></span>

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span data-ttu-id="bdd7e-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Типы виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="bdd7e-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtual Disk Types</span></span>

<span data-ttu-id="bdd7e-132">Существуют рекомендации по использованию виртуальных дисков и доступных типов виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-132">There are considerations for using virtual disks, and what types of virtual disks are available:</span></span>

-   <span data-ttu-id="bdd7e-133">**Исправлено**— файл образа VHD предварительно выделяется в резервном хранилище с максимальным требуемым размером.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-133">**Fixed**—The VHD image file is pre-allocated on the backing store for the maximum size requested.</span></span>
-   <span data-ttu-id="bdd7e-134">**Расширяемый**— также известен как динамический, динамически расширяемый и разреженный, файл образа VHD использует столько места резервного хранилища, сколько требуется для хранения фактических данных, которые в данный момент содержатся в виртуальном диске.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-134">**Expandable**—Also known as "dynamic", "dynamically expandable", and "sparse", the VHD image file uses only as much space on the backing store as needed to store the actual data the virtual disk currently contains.</span></span> <span data-ttu-id="bdd7e-135">При создании этого типа виртуального диска API виртуального жесткого диска не проверяет наличие свободного места на физическом диске в соответствии с требуемым максимальным размером, поэтому можно успешно создать динамический виртуальный диск с максимальным размером, превышающим объем свободного места на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-135">When creating this type of virtual disk, the VHD API does not test for free space on the physical disk based on the maximum size requested, therefore it is possible to successfully create a dynamic virtual disk with a maximum size larger than the available physical disk free space.</span></span> <span data-ttu-id="bdd7e-136">Дополнительные сведения см. в разделе [**експандвиртуалдиск**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="bdd7e-136">For more information, see [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span></span>
    <span data-ttu-id="bdd7e-137">**Примечание**  .  Максимальный размер динамического виртуального диска составляет 2 040 ГБ.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-137">**Note**  The maximum size of a dynamic virtual disk is 2,040 GB.</span></span>

     

-   <span data-ttu-id="bdd7e-138">**Разностное**— родительский виртуальный диск используется в качестве основания для этого типа, при этом все последующие записи, записанные на виртуальный диск, записываются в качестве отличий к новому файлу образа разностного VHD, а родительский файл образа VHD не изменяется.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-138">**Differencing**—A parent virtual disk is used as the basis of this type, with any subsequent writes written to the virtual disk as differences to the new differencing VHD image file, and the parent VHD image file is not modified.</span></span> <span data-ttu-id="bdd7e-139">Например, если в качестве родительского используется виртуальный диск операционной системы с начальной загрузкой и назначьте разностный виртуальный диск в качестве текущего виртуального диска, операционная система на родительском виртуальном диске остается в исходном состоянии для быстрого восстановления или для быстрого создания дополнительных образов загрузки на основе дополнительных разностных виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-139">For example, if you have a clean-install system boot operating system virtual disk as a parent and designate the differencing virtual disk as the current virtual disk for the system to use, then the operating system on the parent virtual disk stays in its original state for quick recovery or for quickly creating more boot images based on additional differencing virtual disks.</span></span> <span data-ttu-id="bdd7e-140">Дополнительные сведения см. в разделе [**мержевиртуалдиск**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="bdd7e-140">For more information, see [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span></span>
    <span data-ttu-id="bdd7e-141">**Примечание**  .  Максимальный размер разностного виртуального диска составляет 2 040 ГБ.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-141">**Note**  The maximum size of a differencing virtual disk is 2,040 GB.</span></span>

     

<span data-ttu-id="bdd7e-142">Все типы виртуальных дисков имеют минимальный размер 3 МБ.</span><span class="sxs-lookup"><span data-stu-id="bdd7e-142">All virtual disk types have a minimum size of 3 MB.</span></span>

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="bdd7e-143"><span id="related_topics"></span>Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bdd7e-143"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="bdd7e-144">О службе VDS</span><span class="sxs-lookup"><span data-stu-id="bdd7e-144">About VDS</span></span>](/windows/desktop/VDS/about-vds)

[<span data-ttu-id="bdd7e-145">Ссылка на виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="bdd7e-145">VHD Reference</span></span>](vhd-reference.md)

[<span data-ttu-id="bdd7e-146">Спецификация формата образа виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="bdd7e-146">Virtual Hard Disk Image Format Specification</span></span>](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
