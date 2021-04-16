---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692355"
---
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="1a085-103">R (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="1a085-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="1a085-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="1a085-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1a085-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**у**</span><span class="sxs-lookup"><span data-stu-id="1a085-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="1a085-106">Как минимум, любой процесс, взаимодействующий с VSS, создает теневые копии и наборы теневых копий одного или нескольких томов и управляет ими.</span><span class="sxs-lookup"><span data-stu-id="1a085-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="1a085-107">Как правило, инициатор запроса управляет теневыми копиями для поддержки некоторых других функций, таких как операции резервного копирования и восстановления и зеркальное отображение дисков.</span><span class="sxs-lookup"><span data-stu-id="1a085-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="1a085-108">См. также [*теневое копирование*](vssgloss-s.md), [*Набор теневых копий*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="1a085-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a085-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**метод Restore**</span><span class="sxs-lookup"><span data-stu-id="1a085-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="1a085-110">Спецификация метода восстановления процесса.</span><span class="sxs-lookup"><span data-stu-id="1a085-110">A specification of the restore process method.</span></span> <span data-ttu-id="1a085-111">Он контролирует такие проблемы, как перезапись файлов при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="1a085-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="1a085-112">Если параметр метода восстановления конфликтует с параметрами целевого объекта восстановления, приоритет имеет целевой объект восстановления.</span><span class="sxs-lookup"><span data-stu-id="1a085-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="1a085-113">См. также *инструкцию RESTORE Target*.</span><span class="sxs-lookup"><span data-stu-id="1a085-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="1a085-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**цель восстановления**</span><span class="sxs-lookup"><span data-stu-id="1a085-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="1a085-115">В VSS целевой объект восстановления — это спецификация того, как инициатор запроса должен восстановить файл, например, если он должен перезаписать существующие файлы.</span><span class="sxs-lookup"><span data-stu-id="1a085-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



