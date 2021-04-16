---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692359"
---
# <a name="e-volume-shadow-copy-service"></a>E (служба теневого копирования томов)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**явное включение компонентов**
</dt> <dd>

Добавление сведений о компоненте в документ компонентов резервного копирования инициатора запроса при участии в операции резервного копирования или восстановления. Запрашивающие стороны используют [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) для явного включения компонента в операцию резервного копирования, а [**Ивссбаккупкомпонентс:: сетселектедфорресторе**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) или [**ивссбаккупкомпонентс:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) для явного включения компонента в операцию восстановления.

Если резервное копирование или восстановление какого-либо компонента модуля записи выполняется, все невыбираемые компоненты без выбора предков должны быть явно добавлены в операцию резервного копирования или восстановления.

Выбираемые компоненты без выбираемых для выбора предков, выбранных инициатором запроса для участия в резервной копии или восстановлении, необходимо явно включать в операцию.

Невыбираемые компоненты с выбираемым предком никогда не включаются явным образом.

Выбираемые компоненты с выбираемым предком могут быть явно добавлены или могут включаться неявно, если родительский элемент включен явным образом.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**доступная теневая копия**
</dt> <dd>

Теневая копия тома, которая подключена к системе и доступна для процессов, отличных от управляемых. Том теневой копии, подключенный под буквой диска или каталогом, называется "локально предоставлен". Том теневой копии, доступный через общую папку (за исключением теневых копий, доступных для клиента), называется "удаленно предоставлено". Все доступные теневые копии также отображаются на теневых копиях. См [*. также теневую копию,*](vssgloss-s.md) [*доступную для клиента*](vssgloss-c.md).

</dd> </dl>

 

 



