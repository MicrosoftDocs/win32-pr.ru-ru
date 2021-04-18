---
description: Результат (который часто хранится в файле с расширением файла. FX) объявляет состояние конвейера, установленное в результате действия.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Формат эффектов (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423489"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="40f7c-103">Формат эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="40f7c-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="40f7c-104">Результат (который часто хранится в файле с расширением файла. FX) объявляет состояние конвейера, установленное в результате действия.</span><span class="sxs-lookup"><span data-stu-id="40f7c-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="40f7c-105">Состояние эффектов можно разделить на три категории:</span><span class="sxs-lookup"><span data-stu-id="40f7c-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="40f7c-106">[Переменные](d3d10-effect-variable-syntax.md), которые обычно объявляются в верхней части результата.</span><span class="sxs-lookup"><span data-stu-id="40f7c-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="40f7c-107">[Функции](d3d10-effect-function-syntax.md), которые реализуют код шейдера или используются в качестве вспомогательных функций другими функциями.</span><span class="sxs-lookup"><span data-stu-id="40f7c-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="40f7c-108">[Метод](d3d10-effect-technique-syntax.md), который реализует последовательности отрисовки с помощью одного или нескольких эффектов.</span><span class="sxs-lookup"><span data-stu-id="40f7c-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="40f7c-109">Каждый проход задает одну или несколько [групп состояний](d3d10-effect-states.md) и вызывает функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="40f7c-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![Схема категорий состояния эффектов](images/d3d10-effect-intro.png)

<span data-ttu-id="40f7c-111">На предыдущей схеме показаны категории состояния эффектов.</span><span class="sxs-lookup"><span data-stu-id="40f7c-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f7c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="40f7c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f7c-113">Справочник по действиям</span><span class="sxs-lookup"><span data-stu-id="40f7c-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



