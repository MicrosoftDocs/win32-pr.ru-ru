---
title: Идентификаторы свойств и пары смещений
description: За числом свойств, заданных свойством, является массив идентификаторов свойств/смещенных пар свойств.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661651"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="220ea-103">Идентификаторы свойств и пары смещений</span><span class="sxs-lookup"><span data-stu-id="220ea-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="220ea-104">За числом свойств, заданных свойством, является массив идентификаторов свойств/смещенных пар свойств.</span><span class="sxs-lookup"><span data-stu-id="220ea-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="220ea-105">Идентификаторы свойств — это 32-разрядные значения, которые уникально идентифицируют свойство в разделе.</span><span class="sxs-lookup"><span data-stu-id="220ea-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="220ea-106">Пары смещений обозначают расстояние от начала раздела до начала пары "тип-значение" Свойства.</span><span class="sxs-lookup"><span data-stu-id="220ea-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="220ea-107">Так как смещение задается относительно раздела, разделы можно копировать в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="220ea-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="220ea-108">Идентификаторы свойств не сортируются в каком бы то ни было определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="220ea-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="220ea-109">Свойства можно опустить из набора сохраненных свойств. читатели не должны полагаться на конкретный порядок или диапазон идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="220ea-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




