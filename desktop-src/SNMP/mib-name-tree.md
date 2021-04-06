---
title: Дерево имен MIB
description: Пространство имен для идентификаторов объектов MIB является иерархическим. Он структурирован таким образом, что каждому управляемому объекту можно назначить глобально уникальное имя.
ms.assetid: eb3c855c-b36b-4675-8df4-e11c128b2b34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d77b0cb4c64d9645f54ec7416c45ba1a4620ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068302"
---
# <a name="mib-name-tree"></a><span data-ttu-id="45140-104">Дерево имен MIB</span><span class="sxs-lookup"><span data-stu-id="45140-104">MIB Name Tree</span></span>

<span data-ttu-id="45140-105">Пространство имен для идентификаторов объектов MIB является иерархическим.</span><span class="sxs-lookup"><span data-stu-id="45140-105">The name space for MIB object identifiers is hierarchical.</span></span> <span data-ttu-id="45140-106">Он структурирован таким образом, что каждому управляемому объекту можно назначить глобально уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="45140-106">It is structured so that each manageable object can be assigned a globally unique name.</span></span>

<span data-ttu-id="45140-107">Центр для частей пространства имен назначается отдельным организациям.</span><span class="sxs-lookup"><span data-stu-id="45140-107">Authority for parts of the name space is assigned to individual organizations.</span></span> <span data-ttu-id="45140-108">Это позволяет организациям назначать имена без консультации с Интернетом для каждого назначения.</span><span class="sxs-lookup"><span data-stu-id="45140-108">This allows organizations to assign names without consulting an Internet authority for each assignment.</span></span> <span data-ttu-id="45140-109">Например, пространство имен, назначенное Microsoft, — это 1.3.6.1.4.1.311, которое определено в MSFT. MIB.</span><span class="sxs-lookup"><span data-stu-id="45140-109">For example, the name space assigned to Microsoft is 1.3.6.1.4.1.311, which is defined in MSFT.MIB.</span></span> <span data-ttu-id="45140-110">Корпорация Майкрософт имеет право назначать имена объектам в любом месте под этим пространством имен.</span><span class="sxs-lookup"><span data-stu-id="45140-110">Microsoft has the authority to assign names to objects anywhere below that name space.</span></span>

<span data-ttu-id="45140-111">Идентификатор объекта в иерархии записывается в виде последовательности субидентификаторов, начиная с корня и заканчивая объектом.</span><span class="sxs-lookup"><span data-stu-id="45140-111">The object identifier in the hierarchy is written as a sequence of subidentifiers beginning at the root and ending at the object.</span></span> <span data-ttu-id="45140-112">Подидентификаторы разделяются точкой.</span><span class="sxs-lookup"><span data-stu-id="45140-112">Subidentifiers are separated with a period.</span></span>

 

 




