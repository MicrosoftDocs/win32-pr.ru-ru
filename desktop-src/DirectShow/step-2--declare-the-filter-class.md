---
description: Объявите класс C++, наследующий базовый класс, который выбран в качестве части записи фильтра преобразования.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Шаг 2. Объявление класса фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410067"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="5b851-104">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="5b851-104">Step 2.</span></span> <span data-ttu-id="5b851-105">Объявление класса фильтра</span><span class="sxs-lookup"><span data-stu-id="5b851-105">Declare the Filter Class</span></span>

<span data-ttu-id="5b851-106">Это шаг 2 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5b851-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="5b851-107">Начните с объявления класса C++, который наследует базовый класс:</span><span class="sxs-lookup"><span data-stu-id="5b851-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="5b851-108">Каждый из классов фильтров имеет связанные классы закрепления.</span><span class="sxs-lookup"><span data-stu-id="5b851-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="5b851-109">В зависимости от конкретных потребностей фильтра может потребоваться переопределить классы закрепления.</span><span class="sxs-lookup"><span data-stu-id="5b851-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="5b851-110">В случае с **ктрансформфилтер** ПИН-коды делегируют большую часть своей работы в фильтр, поэтому вам, скорее всего, не придется переопределять эти ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="5b851-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="5b851-111">Необходимо создать уникальный идентификатор CLSID для фильтра.</span><span class="sxs-lookup"><span data-stu-id="5b851-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="5b851-112">Можно использовать служебную программу guidgen или uuidgen. никогда не копируйте существующий GUID.</span><span class="sxs-lookup"><span data-stu-id="5b851-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="5b851-113">Существует несколько способов объявления идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="5b851-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="5b851-114">В следующем примере используется макрос **define \_ GUID** :</span><span class="sxs-lookup"><span data-stu-id="5b851-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="5b851-115">Затем напишите метод-конструктор для фильтра:</span><span class="sxs-lookup"><span data-stu-id="5b851-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="5b851-116">Обратите внимание, что один из параметров конструктора [**ктрансформфилтер**](ctransformfilter-ctransformfilter.md) — это CLSID, определенный ранее.</span><span class="sxs-lookup"><span data-stu-id="5b851-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="5b851-117">Далее. [Шаг 3. Поддерживает согласование типов мультимедиа](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="5b851-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b851-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5b851-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b851-119">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b851-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



