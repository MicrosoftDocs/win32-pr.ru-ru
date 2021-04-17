---
description: Класс Ксистемклокк реализует часы, возвращающие системное время.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Класс Ксистемклокк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559212"
---
# <a name="csystemclock-class"></a><span data-ttu-id="ac32e-103">Класс Ксистемклокк</span><span class="sxs-lookup"><span data-stu-id="ac32e-103">CSystemClock class</span></span>

![Иерархия классов ксистемклокк](images/sclock01.png)

<span data-ttu-id="ac32e-105">`CSystemClock`Класс реализует часы, возвращающие системное время.</span><span class="sxs-lookup"><span data-stu-id="ac32e-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="ac32e-106">Этот класс является производным от класса [**кбасереференцеклокк**](cbasereferenceclock.md) и добавляет поддержку интерфейсов **IPersist** и [**иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .</span><span class="sxs-lookup"><span data-stu-id="ac32e-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="ac32e-107">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="ac32e-107">Public Methods</span></span>                                        | <span data-ttu-id="ac32e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ac32e-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="ac32e-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ac32e-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="ac32e-110">Создает экземпляр этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ac32e-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="ac32e-111">**ксистемклокк**</span><span class="sxs-lookup"><span data-stu-id="ac32e-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="ac32e-112">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ac32e-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="ac32e-113">Методы Иамклоккаджуст</span><span class="sxs-lookup"><span data-stu-id="ac32e-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="ac32e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ac32e-114">Description</span></span>                                         |
| [<span data-ttu-id="ac32e-115">**сетклоккделта**</span><span class="sxs-lookup"><span data-stu-id="ac32e-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="ac32e-116">Корректирует время.</span><span class="sxs-lookup"><span data-stu-id="ac32e-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="ac32e-117">Методы IPersist</span><span class="sxs-lookup"><span data-stu-id="ac32e-117">IPersist Methods</span></span>                                      | <span data-ttu-id="ac32e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ac32e-118">Description</span></span>                                         |
| [<span data-ttu-id="ac32e-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="ac32e-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="ac32e-120">Возвращает идентификатор класса (CLSID) объекта.</span><span class="sxs-lookup"><span data-stu-id="ac32e-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



