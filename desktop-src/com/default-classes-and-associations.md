---
title: Классы и ассоциации по умолчанию
description: Для определенных категорий один класс может быть связан как класс по умолчанию.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410622"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="1547c-103">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1547c-103">Default Classes and Associations</span></span>

<span data-ttu-id="1547c-104">Для определенных категорий один класс может быть связан как класс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1547c-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="1547c-105">Класс по умолчанию выбирается каждый раз, когда требуется конкретная категория объекта.</span><span class="sxs-lookup"><span data-stu-id="1547c-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="1547c-106">Хотя это может оказаться нецелесообразным для всех категорий компонентов, установка класса по умолчанию может быть полезной, если определенный класс должен быть загружен из списка возможных классов без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="1547c-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="1547c-107">Администраторы определяют, какой класс можно использовать, управляя реестром.</span><span class="sxs-lookup"><span data-stu-id="1547c-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="1547c-108">Чтобы связать класс по умолчанию с категорией, необходимо ввести ключ CLSID с тем же идентификатором CLSID, что и идентификатор CATID категории компонента, выбранной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1547c-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="1547c-109">Затем добавьте в этот раздел ключ Треатас, используя значение для идентификатора CLSID класса по умолчанию для категории.</span><span class="sxs-lookup"><span data-stu-id="1547c-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="1547c-110">Чтобы использовать класс по умолчанию для категории компонента, используйте [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или [**КОЖЕТКЛАССОБЖЕКТ**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), УКАЗАВ CATID для параметра CLSID.</span><span class="sxs-lookup"><span data-stu-id="1547c-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="1547c-111">При этом автоматически перенаправляется на идентификатор CLSID, установленный по умолчанию для этой категории.</span><span class="sxs-lookup"><span data-stu-id="1547c-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="1547c-112">Запись реестра выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1547c-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="1547c-113">Во время установки компонент может проверить наличие ключей класса по умолчанию для его категорий и предоставить пользователю возможность переопределения текущих параметров.</span><span class="sxs-lookup"><span data-stu-id="1547c-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1547c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1547c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1547c-115">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="1547c-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="1547c-116">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="1547c-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="1547c-117">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="1547c-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="1547c-118">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="1547c-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="1547c-119">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="1547c-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




