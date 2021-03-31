---
description: Инициатору запроса необходимо четко определить сведения о состоянии модуля записи, который участвует в процессе создания теневого копирования, а также во время операций резервного копирования и восстановления.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Определение состояния модуля записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273379"
---
# <a name="determining-writer-status"></a>Определение состояния модуля записи

Инициатору запроса необходимо четко определить сведения о состоянии модуля записи, который участвует в процессе создания теневого копирования, а также во время операций резервного копирования и восстановления. Для этого рекомендуется:

-   Запрашивающие стороны используют [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**Ивссбаккупкомпонентс:: жетвритерстатускаунт**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)и [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Как описано в статье [Общие сведения об обработке резервной копии в VSS](overview-of-processing-a-backup-under-vss.md) и [Общие сведения об обработке восстановления в VSS](overview-of-processing-a-restore-under-vss.md), эти методы наиболее полезны при вызове в четко определенной последовательности резервного копирования или восстановления. Как правило, это означает, что записи должны быть запрошены после того, как инициатор запроса завершил одну из своих задач и создал событие VSS.

    При обработке резервной копии инициатор запроса должен запрашивать модуль записи после завершения следующих методов. Запрашивающие стороны должны вызвать [**гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) после вызова [**баккупкомплете**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , чтобы задать для сеанса модуля записи завершенное состояние.

    > [!Note]  
    > Это необходимо только в Windows Server 2008 с пакетом обновления 2 (SP2) и более ранних версий.

     

    <dl> <dt>

[**Ивссбаккупкомпонентс::P Репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**Ивссбаккупкомпонентс::D Оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**Ивссбаккупкомпонентс:: Баккупкомплете**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Во время операций восстановления инициатор запроса должен запрашивать модуль записи после завершения следующих методов:
<dl> <dt>

[**Ивссбаккупкомпонентс::P восстановить**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**Ивссбаккупкомпонентс::P Остресторе**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Вызовы [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) , которые не являются частью четко определенной последовательности резервного копирования или восстановления, не предоставляют надежной картины состояния модуля записи, так как они могут отражать условия, не указывающие на сбой в текущей операции, например:
    -   Сбой предыдущего создания теневой копии
    -   Ошибка при выполнении раннего резервного копирования или восстановления
    -   Модуль записи, который сейчас обрабатывает событие, не отвечает

Таким образом, разработчики не должны полагаться на состояние модуля записи, возвращаемое процессами, которые затем инициатор запроса или пытается отслеживать ход выполнения одного экземпляра интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) с другим (возможно, в отдельном потоке).

Обратите внимание, что для операций резервного копирования, где необходимо проверять документы метаданных модуля записи Writer, не требуется вызывать [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) и [**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) после создания и обработки события [*Identify*](vssgloss-i.md) , вызванного [**ивссбаккупкомпонентс:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) сообщает только о состоянии тех модулей записи, метаданные которых были предоставлены в VSS с [](vssgloss-i.md) помощью средств записи, [**квссвритер:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (и возвращаются инициатору запроса [**ивссбаккупкомпонентс:: жетвритерметадатакаунт**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) и [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Если реализация модуля записи [**квссвритер:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) завершается ошибкой, метаданные этого модуля записи не будут входить в список документов метаданных модуля записи, предоставляемых VSS, сведения о состоянии будут недоступны, а вызов будет избыточным.

Для операций восстановления, где инициатору запроса не нужно изучать документы метаданных модуля записи исполняемых модулей записи, вызов [**ивссбаккупкомпонентс:: гасервритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) и [**Ивссбаккупкомпонентс:: жетвритерстатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) может быть более эффективным способом определения того, какие модули записи выполняются.

 

 



