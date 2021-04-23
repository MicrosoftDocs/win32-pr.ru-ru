---
title: Рекомендации по реализации IPropertySetStorage
description: При рассмотрении способа предоставления реализации интерфейса IPropertySetStorage, считывающего и записывающего формат набора свойств COM, возникают некоторые проблемы. Они описаны в следующих разделах.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778275"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="3b275-104">Рекомендации по реализации IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="3b275-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="3b275-105">При рассмотрении способа предоставления реализации интерфейса [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , считывающего и записывающего формат набора свойств COM, возникают некоторые проблемы.</span><span class="sxs-lookup"><span data-stu-id="3b275-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="3b275-106">Они описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="3b275-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="3b275-107">Имена в IStorage</span><span class="sxs-lookup"><span data-stu-id="3b275-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="3b275-108">Объекты хранения и потока для набора свойств</span><span class="sxs-lookup"><span data-stu-id="3b275-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="3b275-109">Установка идентификатора класса набора свойств</span><span class="sxs-lookup"><span data-stu-id="3b275-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="3b275-110">Точки синхронизации</span><span class="sxs-lookup"><span data-stu-id="3b275-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="3b275-111">Кодовые страницы и строки в Юникоде</span><span class="sxs-lookup"><span data-stu-id="3b275-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="3b275-112">Словарь</span><span class="sxs-lookup"><span data-stu-id="3b275-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="3b275-113">Расширения</span><span class="sxs-lookup"><span data-stu-id="3b275-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="3b275-114">Сериализация набора свойств</span><span class="sxs-lookup"><span data-stu-id="3b275-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="3b275-115">Дополнительные сведения см. в статье [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) в разделе "Справочник" раздела "интерфейсы".</span><span class="sxs-lookup"><span data-stu-id="3b275-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




