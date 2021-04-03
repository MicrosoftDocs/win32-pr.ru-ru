---
title: Леса
description: Лес — это набор из одного или нескольких деревьев доменов, которые не формируют смежное пространство имен.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Active Directory лесов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987334"
---
# <a name="forests"></a><span data-ttu-id="d3dc2-104">Леса</span><span class="sxs-lookup"><span data-stu-id="d3dc2-104">Forests</span></span>

<span data-ttu-id="d3dc2-105">[*Лес*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) — это набор из одного или нескольких деревьев доменов, которые не формируют смежное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="d3dc2-106">Все деревья в лесу совместно используют общую схему, конфигурацию и глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="d3dc2-107">Все деревья в определенном доверии леса обмениваются данными в соответствии с транзитивными иерархическими отношениями доверия Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="d3dc2-108">В отличие от деревьев, лес не требует уникального имени.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="d3dc2-109">Лес существует как набор объектов перекрестной ссылки и отношений доверия Kerberos, распознаваемых деревьями членов.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="d3dc2-110">Деревья в лесу образуют иерархию в целях доверия Kerberos. имя дерева в корне дерева доверия ссылается на заданный лес.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="d3dc2-111">На следующем рисунке показан лес несмежных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="d3dc2-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![лес несмежных пространств имен](images/forests.png)

 

 