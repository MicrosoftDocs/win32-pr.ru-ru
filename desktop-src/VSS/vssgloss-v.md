---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: cbaa7eff-a88b-4b0e-b7b5-5c0d99397942
title: V (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da999c820e7a18ce27fc6fac144f88d1d1dafee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541719"
---
# <a name="v-volume-shadow-copy-service"></a><span data-ttu-id="54462-103">V (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="54462-103">V (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="54462-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="54462-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="54462-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**тома**</span><span class="sxs-lookup"><span data-stu-id="54462-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="54462-106">Логическая единица хранения.</span><span class="sxs-lookup"><span data-stu-id="54462-106">A logical storage unit.</span></span> <span data-ttu-id="54462-107">Том является целевым объектом операций создания теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="54462-107">A volume is the target of shadow copy creation operations.</span></span>

</dd> <dt>

<span data-ttu-id="54462-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**имя GUID тома**</span><span class="sxs-lookup"><span data-stu-id="54462-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**volume GUID name**</span></span>
</dt> <dd>

<span data-ttu-id="54462-109">Уникальное имя тома.</span><span class="sxs-lookup"><span data-stu-id="54462-109">A unique name for a volume.</span></span> <span data-ttu-id="54462-110">Имя GUID тома является строкой следующего вида:</span><span class="sxs-lookup"><span data-stu-id="54462-110">A volume GUID name is a string of the following form:</span></span>

<span data-ttu-id="54462-111">\\\\?\\ Том {GUID}</span><span class="sxs-lookup"><span data-stu-id="54462-111">\\\\?\\Volume{GUID}</span></span>\\

<span data-ttu-id="54462-112">(Обратите внимание на конечную \\ позицию ""), где GUID — это глобальный уникальный идентификатор тома.</span><span class="sxs-lookup"><span data-stu-id="54462-112">(note the trailing "\\") where GUID is a globally unique identifier for the volume.</span></span> <span data-ttu-id="54462-113">Операционная система назначает имя тома при первом обнаружении тома, например во время форматирования или установки.</span><span class="sxs-lookup"><span data-stu-id="54462-113">The operating system assigns a volume name when it first encounters a volume, for example, during formatting or installation.</span></span>

<span data-ttu-id="54462-114">Обратите внимание, что том может иметь несколько имен GUID тома.</span><span class="sxs-lookup"><span data-stu-id="54462-114">Note that a volume can have more than one volume GUID name.</span></span>

</dd> </dl>

 

 



