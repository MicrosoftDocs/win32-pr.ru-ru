---
description: в следующем списке перечислены дополнения и изменения в интерфейсе служба теневого копирования томов в Windows Server 2003 с пакетом обновления 1 (SP1).
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: новые возможности VSS в Windows Server 2003 с пакетом обновления 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344203"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>новые возможности VSS в Windows Server 2003 с пакетом обновления 1 (SP1)

в следующем списке перечислены дополнения и изменения в интерфейсе служба теневого копирования томов в Windows Server 2003 с пакетом обновления 1 (SP1).

## <a name="auto-recovery"></a>Автоматическое восстановление

[*Автоматическое восстановление*](vssgloss-a.md) позволяет записывающим компонентом времени обновлять компоненты в теневой копии, прежде чем теневая копия будет окончательно изменена на доступ только для чтения. Например, базе данных может потребоваться откатить все незавершенные транзакции для всех теневых копий (модуль записи базы данных установил флаг **\_ \_ \_ восстановления резервной копии VSS CF** для компонентов базы данных). Автоматическое восстановление, инициированное инициатором запроса, позволяет выполнять детализированное восстановление (например, восстановление одной таблицы в базе данных или одной папки на почтовом сервере) или откат для поддержки интеллектуального анализа данных для анализа, который будет слишком замедляться для рабочего сервера (инициатор запроса добавляет к контексту теневого копирования **\_ \_ инструкцию VSS VOLSNAP attr \_ ROLLBACK \_ Recovery** ). Автоматическое восстановление несовместимо с транспортными теневыми копиями, но эти же функции поддерживаются с помощью [быстрого восстановления с помощью переносимых теневых скопированных томов](fast-recovery-using-transportable-shadow-copied-volumes.md).

Следующие элементы программирования имеют изменения для поддержки автоматического восстановления:

Методы класса

-   [**Квссвритер:: Жетснапшотдевиценаме**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**Квссвритер:: Онпостснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Перечисления

-   [**\_ \_ Флаги компонента VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_\_ \_ атрибуты моментального снимка тома VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Методы интерфейса

-   [**Ивсспровидеркреатеснапшотсет::P Рефиналкоммитснапшотс**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**Ивсспровидеркреатеснапшотсет::P Остфиналкоммитснапшотс**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Полная поддержка переносимых теневых копий

транспортные теневые копии поддерживаются во всех выпусках Windows Server 2003 с пакетом обновления 1 (SP1). Дополнительные сведения см. в разделе [Импорт переносимых теневых скопированных томов](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Быстрое восстановление с помощью переносимых теневых скопированных томов

[Быстрое восстановление с помощью переносимых теневых скопированных томов](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Управление областью хранения теневых копий

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



