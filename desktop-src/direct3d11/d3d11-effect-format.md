---
title: Формат эффектов (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Подробнее о: Формат эффектов (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262613"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="70e92-103">Формат эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="70e92-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="70e92-104">Результат (который часто хранится в файле с расширением файла. FX) объявляет состояние конвейера, установленное в результате действия.</span><span class="sxs-lookup"><span data-stu-id="70e92-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="70e92-105">Состояние эффектов можно разделить на три категории:</span><span class="sxs-lookup"><span data-stu-id="70e92-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="70e92-106">[Переменные](d3d11-effect-variable-syntax.md), которые обычно объявляются в верхней части результата.</span><span class="sxs-lookup"><span data-stu-id="70e92-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="70e92-107">[Функции](d3d11-effect-function-syntax.md), которые реализуют код шейдера или используются в качестве вспомогательных функций другими функциями.</span><span class="sxs-lookup"><span data-stu-id="70e92-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="70e92-108">[Методы](d3d11-effect-technique-syntax.md), которые можно разместить в группах эффектов и реализовать последовательности отрисовки с помощью одного или нескольких результатов.</span><span class="sxs-lookup"><span data-stu-id="70e92-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="70e92-109">Каждый проход задает одну или несколько [групп состояний](d3d11-effect-states.md) и вызывает функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="70e92-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![Схема категорий объявлений для эффектов, включая переменные сверху, функции в середине и методы в нижней части](images/d3d10-effect-intro.png)

<span data-ttu-id="70e92-111">На предыдущей схеме показаны категории состояния эффектов.</span><span class="sxs-lookup"><span data-stu-id="70e92-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="70e92-112">Определение двоичного формата эффекта можно найти в файле Binary \\ еффектбинариформат. h в исходном коде Effects.</span><span class="sxs-lookup"><span data-stu-id="70e92-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="70e92-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="70e92-113">In this section</span></span>



| <span data-ttu-id="70e92-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="70e92-114">Topic</span></span>                                                                   | <span data-ttu-id="70e92-115">Описание</span><span class="sxs-lookup"><span data-stu-id="70e92-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70e92-116">Синтаксис переменной Effect</span><span class="sxs-lookup"><span data-stu-id="70e92-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="70e92-117">Переменная Effect объявляется с помощью синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="70e92-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="70e92-118">Синтаксис аннотации</span><span class="sxs-lookup"><span data-stu-id="70e92-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="70e92-119">Заметка — это определяемая пользователем часть данных, объявленная с синтаксисом, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="70e92-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="70e92-120">Синтаксис функции Effect</span><span class="sxs-lookup"><span data-stu-id="70e92-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="70e92-121">Функция Effect написана на HLSL и объявлена с синтаксисом, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="70e92-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="70e92-122">Синтаксис методики эффектов</span><span class="sxs-lookup"><span data-stu-id="70e92-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="70e92-123">Метод влияния объявляется с помощью синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="70e92-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="70e92-124">Группы состояний эффектов</span><span class="sxs-lookup"><span data-stu-id="70e92-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="70e92-125">Состояния эффектов — это пары "имя — значение" в виде выражения.</span><span class="sxs-lookup"><span data-stu-id="70e92-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="70e92-126">Синтаксис группы эффектов</span><span class="sxs-lookup"><span data-stu-id="70e92-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="70e92-127">Группа эффектов объявляется с использованием синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="70e92-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="70e92-128">См. также</span><span class="sxs-lookup"><span data-stu-id="70e92-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70e92-129">Справочник по эффектам 11</span><span class="sxs-lookup"><span data-stu-id="70e92-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





