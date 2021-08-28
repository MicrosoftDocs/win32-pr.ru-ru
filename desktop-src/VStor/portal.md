---
description: Инкапсулирует жесткий диск в один файл для использования операционной системой в качестве виртуального диска. Виртуальные диски могут работать как загрузочные диски и могут размещать собственные файловые системы (NTFS, FAT, exFAT и UDF), а также поддерживают стандартные операции с дисками и файлами.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Виртуальный диск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfa2d39ea786029e8be319d7affaa2214682ce05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480990"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Виртуальный диск

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Назначение

Формат виртуального жесткого диска (VHD) представляет собой общедоступную спецификацию формата изображения, указывающую виртуальный жесткий диск, инкапсулированный в одном файле, который может размещать собственные файловые системы при поддержке стандартных операций с дисками и файлами. пример использования файлов VHD — компонент [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) в Windows Server 2008, virtual Server и Windows virtual PC. эти продукты используют виртуальные жесткие диски, чтобы содержать Windows образ операционной системы, используемый виртуальной машиной в качестве системного загрузочного диска.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Аудитория разработчиков

пакет средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK) интегрирует встроенную поддержку vhd для работы с виртуальными жесткими дисками, упрощая для разработчиков и администраторов создание, администрирование и развертывание образов Windows в vhd с помощью средства поддержки API платформы или инструментов управления. Для включения этих операций не требуется устанавливать отдельные приложения или использовать средство синтаксического анализа формата VHD. Эти API-интерфейсы позволяют использовать универсальные виртуальные жесткие диски независимо от других технологий виртуализации.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Требования к времени выполнения

VHD поддерживается в Windows 7 и Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>В этом разделе


| Раздел | Описание | 
|-------|-------------|
| <p><a href="about-vhd.md">О виртуальных жестких дисках</a></p> | <p>Описание формата VHD с советами и рекомендациями по использованию API.</p> | 
| <p><a href="vhd-reference.md">Ссылка на виртуальный жесткий диск</a></p> | <p>Описание функций, структур и перечислений API виртуального жесткого диска.</p> | 


 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Связанные темы

[Служба виртуальных дисков](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
