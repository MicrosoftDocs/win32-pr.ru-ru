---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809803"
---
# <a name="i-volume-shadow-copy-service"></a>I (служба теневого копирования томов)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) . J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Выявление события**
</dt> <dd>

Событие VSS, указывающее, что модулю записи или инициатору запроса необходимо запросить текущий модуль записи. Он используется для создания сведений о метаданных текущего модуля записи. См. также [*инициатор запроса*](vssgloss-r.md), [*модуль записи*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**Включение неявного компонента**
</dt> <dd>

Не добавляйте сведения о компоненте в документ компонентов резервного копирования инициатора запроса, когда он участвует в операции резервного копирования или восстановления.

Невыбираемые компоненты с выбираемым предком неявным образом включаются только при включении их предков.

Выбираемые компоненты с выбираемым предком могут включаться неявно, если родительский элемент включен или может быть включен явным образом.

Невыбираемые компоненты без выбранных предков никогда не включаются в операцию резервного копирования или восстановления. все такие компоненты должны быть явно добавлены в документ компонентов резервного копирования, если участвуют компоненты модуля записи.

Выбираемые компоненты без выбираемых для выбора предков, выбранных инициатором запроса для участия в резервной копии или восстановлении, не могут быть неявно включены в операцию, но должны быть явно добавлены в документ компонентов резервного копирования.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**операции добавочного резервного копирования**
</dt> <dd>

Операция резервного копирования или восстановления выполняется только для файлов, созданных или измененных с момента сохранения последней полной, добавочной или разностной резервной копии. См. также [*разностные операции резервного копирования*](vssgloss-d.md).

</dd> </dl>

 

 



