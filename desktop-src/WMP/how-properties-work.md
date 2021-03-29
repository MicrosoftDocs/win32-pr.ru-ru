---
title: Как работают свойства
description: Как работают свойства
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Подключаемые модули проигрывателя Windows Media, пример свойств Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля "Echo DSP", свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777099"
---
# <a name="how-properties-work"></a><span data-ttu-id="afe6b-108">Как работают свойства</span><span class="sxs-lookup"><span data-stu-id="afe6b-108">How Properties Work</span></span>

<span data-ttu-id="afe6b-109">Значения свойств хранятся в переменных членов.</span><span class="sxs-lookup"><span data-stu-id="afe6b-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="afe6b-110">Свойства становятся доступными парами методов.</span><span class="sxs-lookup"><span data-stu-id="afe6b-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="afe6b-111">Один метод предоставляет реализацию для указания значения свойства; его имя начинается с «вставить \_ ».</span><span class="sxs-lookup"><span data-stu-id="afe6b-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="afe6b-112">Другой метод предоставляет реализацию для получения значения свойства. его имя начинается с Get \_ .</span><span class="sxs-lookup"><span data-stu-id="afe6b-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="afe6b-113">Определение интерфейса находится в файле Echo. idl.</span><span class="sxs-lookup"><span data-stu-id="afe6b-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="afe6b-114">Прототипы методов свойств находятся в Echo. h.</span><span class="sxs-lookup"><span data-stu-id="afe6b-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="afe6b-115">Они реализуются в Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="afe6b-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="afe6b-116">В следующих трех разделах показано, как изменить существующие методы свойств в соответствии со своими потребностями и как добавить методы для дополнительного свойства.</span><span class="sxs-lookup"><span data-stu-id="afe6b-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="afe6b-117">Переменные для хранения свойств</span><span class="sxs-lookup"><span data-stu-id="afe6b-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="afe6b-118">Изменение свойства Scale</span><span class="sxs-lookup"><span data-stu-id="afe6b-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="afe6b-119">Добавление свойства "Mix!"</span><span class="sxs-lookup"><span data-stu-id="afe6b-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="afe6b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="afe6b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe6b-121">**Свойства образца Echo**</span><span class="sxs-lookup"><span data-stu-id="afe6b-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




