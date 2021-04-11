---
description: Windows Server 2008;
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Новые возможности VSS в Windows Server 2008 и Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145193"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Новые возможности VSS в Windows Server 2008 и Windows Vista SP1

Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) вносят следующие изменения в служба теневого копирования томов.

> [!Note]  
> Все изменения в Windows Vista относятся к Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1). Дополнительные сведения об этих изменениях см. в статье [новые возможности VSS в Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Новые интерфейсы VSS](#new-vss-interfaces)
-   [Новые перечисления VSS](#new-vss-enumerations)
-   [Новые структуры VSS](#new-vss-structures)
-   [Существующие изменения перечисления VSS](#existing-vss-enumeration-modifications)
-   [Существующие изменения интерфейса VSS](#existing-vss-interface-modifications)
-   [Новые модули записи VSS](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Новые интерфейсы VSS

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**ивсшардвареснапшотпровидерекс**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Новые перечисления VSS

<dl>

[**\_\_Параметры оборудования \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_сбой защиты \_ VSS**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_уровень защиты \_ VSS**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Новые структуры VSS

<dl>

[**\_ \_ сведения о защите томов VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Существующие изменения перечисления VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ схемы резервного копирования**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Добавлено значение:
</dt> <dd>

\_модуль записи BS в VSS \_ \_ поддерживает \_ параллельное \_ восстановление

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

\_ \_ \_ отложенный \_ моментальный снимок для службы VSS VOLSNAP attr

Восстановление из службы VSS \_ VOLSNAP \_ attr \_ TxF \_

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Существующие изменения интерфейса VSS

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Интерфейс [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Добавленный метод:
</dt> <dd>

[**бреакснапшотсетекс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Новые модули записи VSS

В Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) представлены следующие модули записи VSS:

-   Модуль записи конфигурации IIS
-   Модуль записи метабазы IIS
-   Модуль записи VSS NPS
-   Модуль записи VSS шлюза службы удаленных рабочих столов (службы терминалов)
-   Модуль записи VSS лицензирования службы удаленных рабочих столов (службы терминалов)

Эти модули записи описаны в встроенных [модулях записи VSS](in-box-vss-writers.md).

 

 



