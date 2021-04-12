---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263097"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="e72e9-103">L (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="e72e9-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="e72e9-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J K](vssgloss-i.md) L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e72e9-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e72e9-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**логический путь**</span><span class="sxs-lookup"><span data-stu-id="e72e9-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="e72e9-106">Механизм описания компонентов модуля записи.</span><span class="sxs-lookup"><span data-stu-id="e72e9-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="e72e9-107">Он используется для выражения связей между компонентами, в особенности их иерархия.</span><span class="sxs-lookup"><span data-stu-id="e72e9-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="e72e9-108">Например, если модуль записи управляет несколькими электронными книгами, он может назначить логические пути " \\ Book \\ book1" и " \\ Book \\ book2" в компоненты файловой группы, содержащие каждую книгу.</span><span class="sxs-lookup"><span data-stu-id="e72e9-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="e72e9-109">При указании подкомпонентов требуются логические пути.</span><span class="sxs-lookup"><span data-stu-id="e72e9-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="e72e9-110">По соглашению обратная косая черта " \\ " используется для разделения элементов логического пути.</span><span class="sxs-lookup"><span data-stu-id="e72e9-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="e72e9-111">Кроме того, не существует ограничений на символы, которые могут присутствовать в логическом пути, отличном от **null** .</span><span class="sxs-lookup"><span data-stu-id="e72e9-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="e72e9-112">Логический путь может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e72e9-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="e72e9-113">По соглашению, компоненты с логическими путями, равными **null** , говорят на верхнем уровне иерархии логических путей записи.</span><span class="sxs-lookup"><span data-stu-id="e72e9-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="e72e9-114">См. также [*компонент*](vssgloss-c.md), [*подкомпонент*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="e72e9-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



