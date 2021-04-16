---
description: Сводка изменений API VSS в Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Сводка изменений API VSS в Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692870"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a>Сводка изменений API VSS в Windows Server 2003

## <a name="changes-in-the-vss-service"></a>Изменения в службе VSS

<dl> <dt>

<span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Добавлено событий:
</dt> <dd>

[*баккупшутдовн*](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a>Изменения в функциональных возможностях VSS

<dl> <dt>

<span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Дополнительные функции:
</dt> <dd>

[*Частичная поддержка файлов*](vssgloss-p.md)

[*направлено нацеливание*](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a>Новые интерфейсы VSS

[**ивссвмдепенденци**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a>Существующие изменения интерфейса VSS

<dl> <dt>

<span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>Интерфейс [**ивссасинк**](/windows/desktop/api/Vss/nn-vss-ivssasync)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:
</dt> <dd>

[**Ивссасинк:: wait**](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>Интерфейс [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивссбаккупкомпонентс:: Аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[**Ивссбаккупкомпонентс:: Куериревертстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[**Ивссбаккупкомпонентс:: Реверттоснапшот**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[**Ивссбаккупкомпонентс:: Сетранжесфилепас**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[**Ивссбаккупкомпонентс:: Сетресторестате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>Интерфейс [**ивсскреатевритерметадата**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивсскреатевритерметадата:: Аддкомпонентдепенденци**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[**Ивсскреатевритерметадата:: Сетбаккупсчема**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:
</dt> <dd>

[**Ивсскреатевритерметадата:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[**Ивсскреатевритерметадата:: Адддатабасефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[**Ивсскреатевритерметадата:: Адддатабаселогфилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[**Ивсскреатевритерметадата:: Аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>Интерфейс [**ивссексаминевритерметадата**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивссексаминевритерметадата:: Жетбаккупсчема**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>Интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Удаленные методы:
</dt> <dd>

**Ивсскомпонент:: Аддневтаржет**

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивсскомпонент:: Адддифференцедфилесбиластмодифитиме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[**Ивсскомпонент:: Жетдифференцедфиле**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[**Ивсскомпонент:: Жетдифференцедфилескаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Методы больше не зарезервированы:
</dt> <dd>

[**Ивсскомпонент:: Адддиректедтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[**Ивсскомпонент:: Жетдиректедтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>Интерфейс [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивссвмкомпонент:: dependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>Интерфейс [**ивссвмфиледеск**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Ивссвмфиледеск:: Жетбаккуптипемаск**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a>Существующие изменения класса VSS

<dl> <dt>

<span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>Класс [**квссвритер**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Измененные методы:
</dt> <dd>

[**Квссвритер:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Добавленные методы:
</dt> <dd>

[**Квссвритер:: SPContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[**Квссвритер:: Жетресторетипе**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[**Квссвритер:: Жетснапшотдевиценаме**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[**Квссвритер:: Онбаккупшутдовн**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a>Новые перечисления VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**\_схема резервного копирования VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd></dd> <dt>

<span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**\_ \_ Флаги компонента VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd></dd> <dt>

<span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**\_ \_ \_ тип резервного копирования спецификации файла VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)
</dt> <dd></dd> <dt>

<span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**\_тип восстановления \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)
</dt> <dd></dd> </dl>

## <a name="existing-vss-enumeration-modifications"></a>Существующие изменения перечисления VSS

<dl> <dt>

<span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ типов резервных копий**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

\_BT \_ Copy VSS

</dd> </dl> </dd> <dt>

<span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ целевых объектов восстановления**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)
</dt> <dd>

<dl> <dt>

<span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Удаленные значения:
</dt> <dd>

\_Новый VSS RT \_

</dd> </dl> </dd> <dt>

<span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ enum ресторемесод**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

\_Восстановление рме VSS при \_ \_ \_ перезагрузке, \_ Если \_ не может \_ заменить

</dd> </dl> </dd> <dt>

<span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ состояний моментальных снимков**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

обработка с применением VSS \_ SS \_ \_

\_ \_ ПРЕФИНАЛКОММИТ обработки VSS \_ SS

VSS \_ SS \_ префиналкоммиттед

\_ \_ ПОСТФИНАЛКОММИТ обработки VSS \_ SS

</dd> </dl> </dd> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

автовосстановление в VSS \_ VOLSNAP \_ attr \_

</dd> <dt>

<span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Зарезервированные значения теперь поддерживают:
</dt> <dd>

\_устройство с \_ \_ \_ поддержкой VSS VOLSNAP attr

Импорт атрибута VOLSNAP для VSS \_ \_ \_ импортирован

Служба VSS \_ VOLSNAP \_ attr \_ доступна \_ локально

\_удаленная служба VSS VOLSNAP \_ attr \_ доступна \_

</dd> </dl> </dd> <dt>

<span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ состояния модуля записи**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

\_сбой VSS \_ WS \_ в \_ баккупшутдовн

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a>Изменения в структурах VSS

<dl> <dt>

<span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>Служба [**VSS \_ Структура КОМПОНЕНТИНФО**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)
</dt> <dd>

<dl> <dt>

<span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Добавленные элементы:
</dt> <dd>

**бселектаблефорресторе**

**двкомпонентфлагс**

**кдепенденЦиес**

</dd> </dl> </dd> </dl>

 

 



