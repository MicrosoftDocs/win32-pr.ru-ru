---
description: Эти константы используются при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Константы D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342162"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="ae8a8-103">\_Константы эффектов D3D10</span><span class="sxs-lookup"><span data-stu-id="ae8a8-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="ae8a8-104">Эти константы используются при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="ae8a8-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="ae8a8-105">\#define</span></span>                                 | <span data-ttu-id="ae8a8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ae8a8-106">Value</span></span>        | <span data-ttu-id="ae8a8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ae8a8-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8a8-108">\_ \_ \_ Дочерний \_ Результат компиляции D3D10 Effect</span><span class="sxs-lookup"><span data-stu-id="ae8a8-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="ae8a8-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="ae8a8-109">1 << 0</span></span> | <span data-ttu-id="ae8a8-110">Скомпилируйте файл. FX для дочернего действия.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="ae8a8-111">Дочерние эффекты не имеют инициализаций для общих значений, так как они инициализируются в пуле эффектов.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="ae8a8-112">\_Компиляция эффектов \_ D3D10 \_ Разрешать выполнение \_ операций с высокой скоростью \_</span><span class="sxs-lookup"><span data-stu-id="ae8a8-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="ae8a8-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="ae8a8-113">1 << 1</span></span> | <span data-ttu-id="ae8a8-114">По умолчанию включен режим производительности.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="ae8a8-115">Режим производительности запрещает изменять объекты изменяемого состояния, предотвращая отображение нелитеральных выражений в определениях объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="ae8a8-116">При указании этого флага режим будет отключен и разрешено использовать изменяемые объекты состояния.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="ae8a8-117">D3D10 \_ воздействие на \_ один \_ поток</span><span class="sxs-lookup"><span data-stu-id="ae8a8-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="ae8a8-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="ae8a8-118">1 << 3</span></span> | <span data-ttu-id="ae8a8-119">Не пытайтесь выполнить синхронизацию с другими потоками, загружая эффекты в один и тот же пул.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="ae8a8-120">Эти константы определяются как макросы в d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="ae8a8-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae8a8-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ae8a8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae8a8-122">Константы эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ae8a8-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



