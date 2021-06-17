---
description: Сведения о визуализации влияния на Direct3D 10. Можно использовать для хранения информации или для отрисовки с помощью группы состояний.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Отрисовка влияния (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262576"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="bbdd7-104">Отрисовка влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-104">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="bbdd7-105">Можно использовать для хранения информации или для отрисовки с помощью группы состояний.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-105">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="bbdd7-106">Каждый метод задает шейдеры вершин, шейдеры Geometry, шейдеры пикселей, состояние вытягивания, цвет и состояние текстуры, а другое состояние конвейера.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-106">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="bbdd7-107">Таким образом, после упорядочения состояния в результате можно инкапсулировать результат, полученный из этого состояния, путем создания и отрисовки этого результата.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-107">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="bbdd7-108">Для подготовки к отрисовке эффектов следует выполнить несколько действий.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-108">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="bbdd7-109">Первый — это компиляция, которая проверяет HLSL, например код, в соответствии с синтаксисом языка HLSL и правилами платформы влияния.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-109">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="bbdd7-110">Вы можете компилировать результат из приложения с помощью вызовов API или компилировать результат в автономном режиме с помощью служебной программы компилятора эффектов.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-110">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="bbdd7-111">После успешной компиляции результата создайте его, вызвав другой (но очень похожий) набор интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-111">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="bbdd7-112">После создания этого действия существуют два оставшихся шага для его использования.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-112">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="bbdd7-113">Во-первых, необходимо инициализировать значения состояний эффектов (значения переменных эффектов), используя несколько методов для настройки состояния.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-113">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="bbdd7-114">Для некоторых переменных это можно сделать один раз при создании результата. другие необходимо обновлять каждый раз, когда приложение вызывает цикл визуализации.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-114">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="bbdd7-115">После установки переменных эффектов вы указываете среде выполнения, что она должна отображать влияние, применяя методику.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-115">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="bbdd7-116">Эти разделы подробно обсуждаются ниже.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-116">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="bbdd7-117">Компиляция эффекта (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-117">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="bbdd7-118">Создание влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-118">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="bbdd7-119">Установка состояния действия (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-119">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="bbdd7-120">Применение методики (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-120">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="bbdd7-121">Естественно, существуют [соображения по производительности](d3d10-graphics-programming-guide-effects-performance.md) при использовании эффектов.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-121">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="bbdd7-122">Эти рекомендации в основном одинаковы, если не применяется ни один из эффектов.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-122">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="bbdd7-123">Такие вещи, как минимизация объема изменений состояния или организация переменных, нуждающихся в обновлении с периодичностью.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-123">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="bbdd7-124">Эти приемы используются для того, чтобы максимально сокращать объем данных, которые необходимо отправить с ЦП на графический процессор, и, следовательно, сокращать потенциальные проблемы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-124">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbdd7-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bbdd7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbdd7-126">Эффекты (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-126">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



