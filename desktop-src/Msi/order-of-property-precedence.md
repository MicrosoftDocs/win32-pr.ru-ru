---
description: Установщик устанавливает свойства с помощью следующего порядка приоритета. Значение свойства в этом списке может переопределять значение, которое поступает после него, и переопределяться перед ним в списке.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Порядок приоритета свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674375"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="43c3e-104">Порядок приоритета свойств</span><span class="sxs-lookup"><span data-stu-id="43c3e-104">Order of Property Precedence</span></span>

<span data-ttu-id="43c3e-105">Установщик устанавливает свойства с помощью следующего порядка приоритета.</span><span class="sxs-lookup"><span data-stu-id="43c3e-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="43c3e-106">Значение свойства в этом списке может переопределять значение, которое поступает после него, и переопределяться перед ним в списке.</span><span class="sxs-lookup"><span data-stu-id="43c3e-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="43c3e-107">Свойства, заданные операционной средой.</span><span class="sxs-lookup"><span data-stu-id="43c3e-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="43c3e-108">[Открытые свойства](public-properties.md) , заданные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="43c3e-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="43c3e-109">Общие свойства, перечисленные в свойстве [**админпропертиес**](adminproperties.md) во время [административной установки](administrative-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="43c3e-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="43c3e-110">Открытые или закрытые свойства, заданные во время применения [*преобразования*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="43c3e-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="43c3e-111">Открытое или закрытое свойство, заданное путем создания [таблицы свойств](property-table.md) MSI файла.</span><span class="sxs-lookup"><span data-stu-id="43c3e-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43c3e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="43c3e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43c3e-113">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="43c3e-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



