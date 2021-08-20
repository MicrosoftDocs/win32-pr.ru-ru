---
description: Как правило, создание теневой копии зависит от типа создаваемой теневой копии, ее контекста и роли, которая прилагается к модулям записи в операции теневого копирования.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Сведения о создании теневой копии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998134"
---
# <a name="shadow-copy-creation-details"></a>Сведения о создании теневой копии

Как правило, создание теневой копии зависит от типа создаваемой теневой копии, ее контекста и роли, которая прилагается к модулям записи в операции теневого копирования. (Дополнительные сведения см. в разделе [конфигурации контекста теневого копирования](shadow-copy-context-configurations.md) .)

Контекст теневой копии задается путем вызова метода [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) . Перед вызовом метода [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) для создания теневой копии запрашивающие стороны должны вызывать методы [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) в порядке, указанном в следующих разделах.

## <a name="prerequisites-for-all-shadow-copies"></a>Необходимые условия для всех теневых копий

Независимо от уровня участия в записи, создание любой теневой копии всегда требует, чтобы запрашивающий был инициализирован с вызовами [**ивссбаккупкомпонентс:: инитиализефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) и [**Ивссбаккупкомпонентс:: стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Если этот вызов не выполняется, метод [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) возвратит ошибку.

## <a name="shadow-copies-with-writer-participation"></a>Теневые копии с участием в модуле записи

Если в контексте теневого копирования задано участие в записи (то есть [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) вызывается с **\_ \_ резервным копированием VSS CTX** или **\_ \_ \_ откат приложения VSS CTX**):

-   Запрашивающие стороны должны всегда вызывать [**ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , если контекст теневого копирования поддерживает участие в записи. Если контекст теневого копирования поддерживает участие в записи и метод **ивссбаккупкомпонентс:: гасервритерметадата** не вызывается до [**Ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), будет возвращена ошибка.
-   Если инициатор запроса хочет выбрать определенные компоненты модуля записи, он должен вызвать [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) перед вызовом [**стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) для создания набора теневых копий.
-   Для создания набора теневых копий необходимо вызвать [**стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) .
-   Инициаторы запроса могут добавить один или несколько томов в набор теневых копий, вызвав [**аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Некоторые компоненты модуля записи могут не указывать какие либо затронутые тома. В этом случае допустимо, чтобы моментальный снимок был пустым (то есть не должен содержать томов).
-   Чтобы гарантировать согласованность метаданных модуля записи, инициатор запроса должен всегда вызывать [**ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , даже если компоненты не выбраны. Это приводит к тому, что VSS создает событие **PrepareForBackup** , в котором VSS вызывает метод [**Квссвритер:: онпрепаребаккуп**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) для каждого модуля записи участия.
-   Служба VSS создаст [*препарефорснапшот*](vssgloss-p.md) и [*заморозить*](vssgloss-f.md) события перед созданием теневой копии в ответ на [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Модули записи будут выполнять обработку событий с помощью [**квссвритер:: онпрепареснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) и [**квссвритер:: onfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   После создания теневой копии в ответ на [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)службы VSS создают события [*разморозки*](vssgloss-t.md) и события [*моментального снимка*](vssgloss-p.md) . Модули записи будут выполнять обработку событий с помощью [**квссвритер:: размораживание**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) и [**квссвритер:: онпостснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Теневые копии без участия в записи

Создание теневых копий без участия в записи не рекомендуется для стандартных приложений резервного копирования (см. статью [резервное копирование без участия в записи](backups-without-writer-participation.md)).

Существуют такие средства, как быстрое резервное копирование диска для обеспечения безопасности от случайного повреждения файлов, которое может быть проведено без явного участия в записи. Такая теневая копия будет иметь контекст **\_ CTX \_ \_ \_ резервной копии общей папки VSS** или **VSS \_ CTX \_ NAS \_ ROLLBACK**.

Для этого типа теневого копирования Обратите внимание на следующее:

-   Запрашивающие стороны должны по-прежнему вызывать необходимые методы, перечисленные в статье [необходимые условия для всех теневых копий](#prerequisites-for-all-shadow-copies).
-   Инициаторы запроса могут вызывать [**ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), но это не является обязательным.
-   Если инициаторы запроса вызывают [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**Ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)или [**ивссбаккупкомпонентс:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), будет возвращена ошибка.
-   Поставщики не будут создавать события [*препарефорснапшот*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*разморозить*](vssgloss-t.md)или [*моментальные снимки*](vssgloss-p.md) для этого типа теневой копии.

 

 



