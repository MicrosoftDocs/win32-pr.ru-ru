---
description: Нельзя создавать экземпляры измененных классов в локализованном пространстве имен. Измененные классы в локализованном пространстве имен обрабатываются так, как если бы они были абстрактными, хотя они не содержат абстрактный квалификатор.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Рекомендации для измененного класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273080"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="4ccbe-104">Рекомендации для измененного класса</span><span class="sxs-lookup"><span data-stu-id="4ccbe-104">Amended Class Considerations</span></span>

<span data-ttu-id="4ccbe-105">Нельзя создавать экземпляры измененных классов в локализованном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="4ccbe-106">Измененные классы в локализованном пространстве имен обрабатываются так, как если бы они были абстрактными, хотя они не содержат [**абстрактный**](standard-qualifiers.md) квалификатор.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="4ccbe-107">Если получить измененный класс из локализованного пространства имен с помощью \_ флага WBEM \_ \_ \_ , флаг измененных квалификаторов и порождение экземпляра из него будут содержать все измененные квалификаторы измененного класса.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="4ccbe-108">Этот новый класс нельзя сохранить в пространстве имен, содержащем определение базового класса, если только не выполняется операция **размещения** с \_ флагом WBEM, \_ используется \_ флаг измененных \_ квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="4ccbe-109">Этот флаг предписывает инструментарию WMI удалить все измененные квалификаторы перед сохранением объекта.</span><span class="sxs-lookup"><span data-stu-id="4ccbe-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="4ccbe-110">Если не указать \_ флаг WBEM \_ \_ , используйте измененные \_ квалификаторы, операция **размещения** завершается ошибкой с \_ \_ исправленным объектом WBEM E \_ .</span><span class="sxs-lookup"><span data-stu-id="4ccbe-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



