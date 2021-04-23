---
description: Методы обеспечивают свою мощность визуализации. Метод инкапсулирует состояние действия, которое определяет стиль отрисовки. Метод состоит из одного или нескольких проходов.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Методы и проходы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682328"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="26a21-105">Методы и проходы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="26a21-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="26a21-106">Методы обеспечивают свою мощность визуализации.</span><span class="sxs-lookup"><span data-stu-id="26a21-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="26a21-107">Метод инкапсулирует состояние действия, которое определяет стиль отрисовки.</span><span class="sxs-lookup"><span data-stu-id="26a21-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="26a21-108">Метод состоит из одного или нескольких проходов.</span><span class="sxs-lookup"><span data-stu-id="26a21-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="26a21-109">Технологий</span><span class="sxs-lookup"><span data-stu-id="26a21-109">Techniques</span></span>

<span data-ttu-id="26a21-110">Синтаксис вызова метода выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26a21-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="26a21-111">Где:</span><span class="sxs-lookup"><span data-stu-id="26a21-111">Where:</span></span>

-   <span data-ttu-id="26a21-112">ID — это необязательное уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="26a21-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="26a21-113">Аннотация — ноль или более дополнительных элементов пользовательской информации.</span><span class="sxs-lookup"><span data-stu-id="26a21-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="26a21-114">См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="26a21-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="26a21-115">passs — ноль или более проходов.</span><span class="sxs-lookup"><span data-stu-id="26a21-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="26a21-116">Каждый этап содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="26a21-116">Each pass contains state assignments.</span></span> <span data-ttu-id="26a21-117">См. ниже.</span><span class="sxs-lookup"><span data-stu-id="26a21-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="26a21-118">Соответствующий</span><span class="sxs-lookup"><span data-stu-id="26a21-118">Passes</span></span>

<span data-ttu-id="26a21-119">Этап содержит назначения состояния, необходимые для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="26a21-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="26a21-120">Где:</span><span class="sxs-lookup"><span data-stu-id="26a21-120">Where:</span></span>

-   <span data-ttu-id="26a21-121">ID — это необязательное уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="26a21-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="26a21-122">Аннотация — это одна или несколько необязательных частей пользовательской информации.</span><span class="sxs-lookup"><span data-stu-id="26a21-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="26a21-123">См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="26a21-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="26a21-124">присваивания присваивают 0 или более значений состояния или оценивают одно или несколько выражений.</span><span class="sxs-lookup"><span data-stu-id="26a21-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="26a21-125">См. раздел [состояния эффектов (Direct3D 9)](effect-states.md) и [выражения (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="26a21-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="26a21-126">Пропускает все, кроме последнего назначения в наборе повторяющихся назначений в одно и то же состояние.</span><span class="sxs-lookup"><span data-stu-id="26a21-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26a21-127">См. также</span><span class="sxs-lookup"><span data-stu-id="26a21-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26a21-128">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="26a21-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



