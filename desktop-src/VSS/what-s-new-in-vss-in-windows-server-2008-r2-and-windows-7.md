---
description: В Windows Server 2008 R2 и Windows 7 внесены следующие изменения в служба теневого копирования томов.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Новые возможности: VSS в Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692345"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Новые возможности: VSS в Windows Server 2008 R2 & Windows 7

В Windows Server 2008 R2 и Windows 7 внесены следующие изменения в служба теневого копирования томов.

## <a name="new-vss-interfaces"></a>Новые интерфейсы VSS

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**ивсскреатикспрессвритерметадата**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**ивссекспрессвритер**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Новые классы VSS

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Новые перечисления VSS

<dl>

[**\_Параметры восстановления \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Новые функции VSS

<dl>

[**креатевссекспрессвритер**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Существующие изменения интерфейса VSS

<dl>

Интерфейс [**ивсшардвареснапшотпровидерекс**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Добавленный метод: [ **ресинклунс**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Трассировка и ведение журнала событий VSS

Начиная с Windows Server 2008 R2 и Windows 7, для получения данных трассировки для инфраструктуры VSS можно использовать средство Всстраце, средство logman или средство tracelog. Дополнительные сведения см. в разделе [использование средств трассировки с VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>Повторная синхронизация LUN

В Windows Server 2008 R2 и Windows 7 инициаторы запросов VSS могут использовать функцию поставщика оборудования теневого копирования, называемую повторной синхронизацией LUN (или "синхронизация LUN"). Это схема быстрого восстановления, позволяющая администратору приложения восстанавливать данные из теневой копии на исходный логический номер устройства (LUN) или на новый LUN. Теневая копия может быть полным клоном теневой копии или разностной теневой копией. В любом случае, в конце операции повторной синхронизации, целевой LUN будет иметь то же содержимое, что и LUN теневого копирования. Во время операции повторной синхронизации массив выполняет копирование на уровне блока из теневой копии в целевой LUN. Дополнительные сведения см. в следующих разделах:

-   [Повторная синхронизация LUN — сценарий быстрого восстановления на сервере 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Использование теневых копий в [Служба теневого копирования томов](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Распространенные проблемы повторной синхронизации LUN](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Модули записи Express

В Windows Server 2008 R2 и Windows 7 интерфейс экспресс-выпуска VSS позволяет приложению регистрировать расположение файлов данных без реализации модуля записи VSS. Дополнительные сведения см. в разделе [Служба теневого копирования томов (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Новые модули записи VSS

В Windows Server 2008 R2 и Windows 7 представлены следующие модули записи VSS:

-   Модуль записи счетчиков производительности
-   Модуль записи планировщик задач
-   Модуль записи хранилища метаданных VSS

Эти новые модули записи описаны в встроенных [модулях записи VSS](in-box-vss-writers.md).

 

 
