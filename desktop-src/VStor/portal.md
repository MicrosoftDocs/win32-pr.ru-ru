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
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Виртуальный диск

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Назначение

Формат виртуального жесткого диска (VHD) представляет собой общедоступную спецификацию формата изображения, указывающую виртуальный жесткий диск, инкапсулированный в одном файле, который может размещать собственные файловые системы при поддержке стандартных операций с дисками и файлами. Пример использования файлов VHD — компонент [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) в windows Server 2008, Virtual Server и Windows Virtual PC. Эти продукты используют виртуальные жесткие диски, чтобы содержать образ операционной системы Windows, используемый виртуальной машиной в качестве системного загрузочного диска.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Аудитория разработчиков

Пакет средств разработки программного обеспечения Microsoft Windows (SDK) интегрирует встроенную поддержку VHD для работы с виртуальными жесткими дисками, упрощая для разработчиков и администраторов создание, Администрирование и развертывание образов Windows в VHD с помощью средства поддержки API платформы или управления. Для включения этих операций не требуется устанавливать отдельные приложения или использовать средство синтаксического анализа формата VHD. Эти API-интерфейсы позволяют использовать универсальные виртуальные жесткие диски независимо от других технологий виртуализации.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Требования к времени выполнения

VHD поддерживается в Windows 7 и Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>В этом разделе

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">О виртуальных жестких дисках</a></p></td>
<td><p>Описание формата VHD с советами и рекомендациями по использованию API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Ссылка на виртуальный жесткий диск</a></p></td>
<td><p>Описание функций, структур и перечислений API виртуального жесткого диска.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Связанные темы

[Служба виртуальных дисков](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
