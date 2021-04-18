---
description: Все облака, журналы состояния и Вапор могут быть созданы с помощью расширения технологии объявления.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Облака, состояния и Вапор (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567899"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="fdc6c-103">Облака, состояния и Вапор (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fdc6c-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="fdc6c-104">Все облака, журналы состояния и Вапор могут быть созданы с помощью расширения технологии объявления.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="fdc6c-105">См. раздел [объявления (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="fdc6c-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="fdc6c-106">При повороте объявления на двух осях, а не на одной, приложение может позволить пользователю просматривать рекламу с любого угла.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="fdc6c-107">Как правило, приложение поворачивает объявление на горизонтальной и вертикальной оси.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="fdc6c-108">Чтобы создать простое облако, приложение может повернуть прямоугольный примитив на одной или двух осях, чтобы примитив отгранен пользователю.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="fdc6c-109">Затем текстуру, подобную облачной, можно применить к примитиву с прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="fdc6c-110">Дополнительные сведения о применении прозрачных текстур к примитивам см. в разделе [смешение текстур (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="fdc6c-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="fdc6c-111">Вы можете анимировать облако, применяя ряд текстур с течением времени.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="fdc6c-112">Приложение может создавать более сложные облака, формируя их из группы примитивов.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="fdc6c-113">Каждая часть облака является прямоугольным примитивом.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="fdc6c-114">Примитивы можно перемещать независимо от времени, чтобы получить внешний вид динамической тумана.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="fdc6c-115">Эта концепция показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-115">The following illustration shows this concept.</span></span>

![Иллюстрация примитивов, образующих более сложные облака](images/cloud.png)

<span data-ttu-id="fdc6c-117">Внешний вид состояния отображается так же, как и облака.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="fdc6c-118">Обычно требуется несколько объявлений, например сложных облаков.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="fdc6c-119">Как правило, билловс и растет с течением времени, поэтому объявления, составляющие Плуме, должны перемещаться соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="fdc6c-120">Может потребоваться добавить дополнительные объявления, так как Плуме растет и разбросаны.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="fdc6c-121">Вапорный след — это Плуме, который не растет.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="fdc6c-122">Однако, как и в случае с плумеом, он разбросается с течением времени.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="fdc6c-123">На следующем рисунке показана методика использования объявлений для имитации вапорного следа.</span><span class="sxs-lookup"><span data-stu-id="fdc6c-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![Иллюстрация объявлений, имитирующих вапорный след](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="fdc6c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="fdc6c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdc6c-126">Примеры альфа</span><span class="sxs-lookup"><span data-stu-id="fdc6c-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



