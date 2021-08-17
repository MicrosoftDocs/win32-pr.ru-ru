---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31221211ee10672cd16298feb38f0005375afa5162ecc8fe5a2a92af32201bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751369"
---
# <a name="r-volume-shadow-copy-service"></a>R (служба теневого копирования томов)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**у**
</dt> <dd>

Как минимум, любой процесс, взаимодействующий с VSS, создает теневые копии и наборы теневых копий одного или нескольких томов и управляет ими.

Как правило, инициатор запроса управляет теневыми копиями для поддержки некоторых других функций, таких как операции резервного копирования и восстановления и зеркальное отображение дисков. См. также [*теневое копирование*](vssgloss-s.md), [*Набор теневых копий*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**метод Restore**
</dt> <dd>

Спецификация метода восстановления процесса. Он контролирует такие проблемы, как перезапись файлов при восстановлении. Если параметр метода восстановления конфликтует с параметрами целевого объекта восстановления, приоритет имеет целевой объект восстановления. См. также *инструкцию RESTORE Target*.

</dd> <dt>

<span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**цель восстановления**
</dt> <dd>

В VSS целевой объект восстановления — это спецификация того, как инициатор запроса должен восстановить файл, например, если он должен перезаписать существующие файлы.

</dd> </dl>

 

 



