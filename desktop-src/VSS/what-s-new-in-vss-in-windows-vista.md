---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Новые возможности VSS в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692344"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Новые возможности VSS в Windows Vista

В Windows Vista появились следующие изменения в служба теневого копирования томов.

Обратите внимание, что все изменения для Windows Vista также относятся к Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).

## <a name="new-vss-interfaces"></a>Новые интерфейсы VSS

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**ивсскомпонентекс**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**ивсскреатевритерметадатаекс**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Новые классы VSS

[**квссвритерекс**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Новые перечисления VSS

[**\_тип НАКАТУ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Существующие изменения перечисления VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ схемы резервного копирования**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

\_ \_ полномочное \_ восстановление в VSS

\_ \_ независимое \_ состояние системы "BS \_ " VSS

\_ \_ Переименование восстанавливаемого восстановления VSS \_

\_ \_ Восстановление накатуа BS VSS \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Служба [**VSS \_ Перечисление \_ флагов компонентов**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

VSS \_ CF \_ не \_ является \_ состоянием системы

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Перечисление [**\_ \_ \_ \_ атрибутов моментальных снимков тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Добавленные значения:
</dt> <dd>

Служба VSS \_ VOLSNAP \_ attr \_ без \_ автовосстановления

Служба VSS \_ VOLSNAP \_ attr \_ не \_ транзакционная

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Трассировка и ведение журнала событий VSS

-   Теперь файл трассировки VSS можно найти на любом локальном томе. В версиях Windows, предшествовавших Windows Vista, файл трассировки VSS не удалось найти на томе, который был в наборе теневых копий.
-   Многие записи в журнале событий были изменены, чтобы сделать их более четкими.
-   Все записи журнала событий VSS теперь содержат сведения о контексте.

## <a name="vss-error-reporting"></a>Отчеты об ошибках VSS

-   Описания всех кодов ошибок VSS теперь можно получить, вызвав функцию [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ флага хмодуле, указанного в параметре *dwFlags* .
-   Сообщения с кодом ошибки VSS содержатся в vsstrace.dll. В параметре *лпсаурце* должен быть указан обработчик для этого модуля.

## <a name="excluding-files-from-shadow-copies"></a>Исключение файлов из теневых копий

Приложения или службы могут использовать раздел реестра Филесноттоснапшот, чтобы указать файлы, которые будут удалены из вновь создаваемых теневых копий. Дополнительные сведения см. в разделе [исключение файлов из теневых копий](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Резервное копирование и восстановление совместимости приложений

Разработчикам приложений для резервного копирования и восстановления необходимо знать о некоторых новых возможностях Windows Vista и Windows Server 2008. Контрольный список совместимости приложений см. в разделе [совместимость приложений для резервного копирования и восстановления](application-compatibility-for-backup-and-restore.md).

 

 
