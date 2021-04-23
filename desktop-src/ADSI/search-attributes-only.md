---
title: Только атрибуты поиска
description: Иногда можно выполнить поиск для определения типа данных, доступных для объекта.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Поиск по атрибутам только ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986091"
---
# <a name="search-attributes-only"></a><span data-ttu-id="06382-104">Только атрибуты поиска</span><span class="sxs-lookup"><span data-stu-id="06382-104">Search Attributes Only</span></span>

<span data-ttu-id="06382-105">Иногда можно выполнить поиск для определения типа данных, доступных для объекта.</span><span class="sxs-lookup"><span data-stu-id="06382-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="06382-106">В этом случае вы заинтересованы только в атрибутах, а не на значениях объекта.</span><span class="sxs-lookup"><span data-stu-id="06382-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="06382-107">Для этого необходимо установить параметр "только атрибуты поиска".</span><span class="sxs-lookup"><span data-stu-id="06382-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="06382-108">При указании этого параметра возвращаются имена атрибутов без их значений.</span><span class="sxs-lookup"><span data-stu-id="06382-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="06382-109">Однако результирующий набор включает только те атрибуты, которые имеют присвоенные значения.</span><span class="sxs-lookup"><span data-stu-id="06382-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="06382-110">Например, рассмотрим объект со следующими атрибутами:</span><span class="sxs-lookup"><span data-stu-id="06382-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="06382-111">Если задан параметр только атрибуты поиска, результирующий набор включает:</span><span class="sxs-lookup"><span data-stu-id="06382-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="06382-112">Дополнительные сведения об использовании параметра поиска только атрибуты с конкретным интерфейсом поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="06382-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="06382-113">Возвращение только имен атрибутов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="06382-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="06382-114">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="06382-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="06382-115">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="06382-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




