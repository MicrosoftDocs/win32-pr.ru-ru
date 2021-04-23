---
description: Существует несколько различных типов теневых копий, которые может создать инициатор запроса.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Создание простой теневой копии для резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809424"
---
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="13e86-103">Создание простой теневой копии для резервного копирования</span><span class="sxs-lookup"><span data-stu-id="13e86-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="13e86-104">Существует несколько различных типов теневых копий, которые может создать инициатор запроса.</span><span class="sxs-lookup"><span data-stu-id="13e86-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="13e86-105">Однако для большинства приложений резервного копирования необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="13e86-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="13e86-106">Вызовите [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) с контекстом \_ \_ резервного копирования VSS CTX.</span><span class="sxs-lookup"><span data-stu-id="13e86-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="13e86-107">Вызовите метод [**ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , чтобы инициализировать обмен данными с модулями записи.</span><span class="sxs-lookup"><span data-stu-id="13e86-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="13e86-108">Вызовите метод [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , чтобы добавить файл и компоненты базы данных в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="13e86-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="13e86-109">Вызовите метод [**ивссбаккупкомпонентс:: стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) , чтобы инициализировать механизм теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="13e86-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="13e86-110">Вызовите [**ивссбаккупкомпонентс:: аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) , чтобы включить тома в теневую копию.</span><span class="sxs-lookup"><span data-stu-id="13e86-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="13e86-111">Вызовите [**ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , чтобы уведомить модули записи об операциях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="13e86-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



