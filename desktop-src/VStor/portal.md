---
description: Инкапсулирует жесткий диск в один файл для использования операционной системой в качестве виртуального диска. Виртуальные диски могут работать как загрузочные диски и могут размещать собственные файловые системы (NTFS, FAT, exFAT и UDF), а также поддерживают стандартные операции с дисками и файлами.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Виртуальный диск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263091"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="17c28-104"><span id="vhd.portal"></span>Виртуальный диск</span><span class="sxs-lookup"><span data-stu-id="17c28-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="17c28-105"><span id="purpose"></span>Назначение</span><span class="sxs-lookup"><span data-stu-id="17c28-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="17c28-106">Формат виртуального жесткого диска (VHD) представляет собой общедоступную спецификацию формата изображения, указывающую виртуальный жесткий диск, инкапсулированный в одном файле, который может размещать собственные файловые системы при поддержке стандартных операций с дисками и файлами.</span><span class="sxs-lookup"><span data-stu-id="17c28-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="17c28-107">Пример использования файлов VHD — компонент [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) в windows Server 2008, Virtual Server и Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="17c28-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="17c28-108">Эти продукты используют виртуальные жесткие диски, чтобы содержать образ операционной системы Windows, используемый виртуальной машиной в качестве системного загрузочного диска.</span><span class="sxs-lookup"><span data-stu-id="17c28-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="17c28-109"><span id="developer_audience_heading"></span>Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="17c28-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="17c28-110">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) интегрирует встроенную поддержку VHD для работы с виртуальными жесткими дисками, упрощая для разработчиков и администраторов создание, Администрирование и развертывание образов Windows в VHD с помощью средства поддержки API платформы или управления.</span><span class="sxs-lookup"><span data-stu-id="17c28-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="17c28-111">Для включения этих операций не требуется устанавливать отдельные приложения или использовать средство синтаксического анализа формата VHD.</span><span class="sxs-lookup"><span data-stu-id="17c28-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="17c28-112">Эти API-интерфейсы позволяют использовать универсальные виртуальные жесткие диски независимо от других технологий виртуализации.</span><span class="sxs-lookup"><span data-stu-id="17c28-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="17c28-113"><span id="run_time_requirements_heading"></span>Требования к времени выполнения</span><span class="sxs-lookup"><span data-stu-id="17c28-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="17c28-114">VHD поддерживается в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="17c28-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="17c28-115"><span id="in_this_section"></span>В этом разделе</span><span class="sxs-lookup"><span data-stu-id="17c28-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17c28-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="17c28-116">Topic</span></span></th>
<th><span data-ttu-id="17c28-117">Описание</span><span class="sxs-lookup"><span data-stu-id="17c28-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17c28-118"><a href="about-vhd.md">О виртуальных жестких дисках</a></span><span class="sxs-lookup"><span data-stu-id="17c28-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="17c28-119">Описание формата VHD с советами и рекомендациями по использованию API.</span><span class="sxs-lookup"><span data-stu-id="17c28-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c28-120"><a href="vhd-reference.md">Ссылка на виртуальный жесткий диск</a></span><span class="sxs-lookup"><span data-stu-id="17c28-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="17c28-121">Описание функций, структур и перечислений API виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="17c28-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="17c28-122"><span id="related_topics"></span>Связанные темы</span><span class="sxs-lookup"><span data-stu-id="17c28-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="17c28-123">Служба виртуальных дисков</span><span class="sxs-lookup"><span data-stu-id="17c28-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
