---
description: 'Инициатор запроса может разбивать набор теневых копий с помощью метода Ивссбаккупкомпонентс:: Бреакснапшотсет или IVssBackupComponentsEx2:: Бреакснапшотсетекс.'
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Критические теневые копии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032904"
---
# <a name="breaking-shadow-copies"></a>Критические теневые копии

Инициатор запроса может разбивать набор теневых копий с помощью метода [**ивссбаккупкомпонентс:: бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) или [**IVssBackupComponentsEx2:: бреакснапшотсетекс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) .

Поврежденная теневая копия — это том, содержащий теневую копию, которая больше не управляется службой VSS. Критическое назначение теневой копии означает, что [*поставщик*](vssgloss-p.md) теневой копии является [*поставщиком оборудования*](vssgloss-h.md). Это связано с тем, что только поставщики оборудования могут реализовать теневую копию в качестве реального тома с жизненным циклом, не зависящим от VSS. Если служба VSS не управляет таким томом, он по-прежнему доступен.

Поставщики программного обеспечения поддерживают теневые копии только при работе с операциями VSS. По этой причине для поставщиков программного обеспечения не имеет смысла прерывать теневую копию.

Если теневая копия была под управлением поставщика оборудования, инициатору запроса необходимо импортировать теневую копию перед вызовом [**бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) или [**бреакснапшотсетекс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex). В случае непереносимого (созданного поставщиком оборудования) теневых копий они импортируются неявно как часть вызова [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .

После того как инициатор запроса вызвал [**бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) или [**бреакснапшотсетекс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), набор теневых копий по-прежнему доступен через объекты устройств или другие пути доступа, но больше не является набором теневых копий. Ее можно управлять как одним или несколькими LUN с помощью COM-интерфейсов службы виртуальных дисков (VDS). С помощью VDS инициатор запроса может преобразовать LUN в чтение и запись, подключить их к буквам дисков, а также маску или снять маску для других компьютеров. Дополнительные сведения см. в [документации по API службы VDS](../vds/virtual-disk-service-portal.md) .

 

 
