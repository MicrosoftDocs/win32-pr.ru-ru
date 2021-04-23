---
description: Выражения — это математические или логические операторы, которые используются в правой части знака равенства. Существует много типов выражений.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Выражения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672945"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="2ba90-104">Выражения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ba90-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="2ba90-105">Выражения — это математические или логические операторы, которые используются в правой части знака равенства.</span><span class="sxs-lookup"><span data-stu-id="2ba90-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="2ba90-106">Существует много типов выражений.</span><span class="sxs-lookup"><span data-stu-id="2ba90-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="2ba90-107">Выражения</span><span class="sxs-lookup"><span data-stu-id="2ba90-107">Expressions</span></span>

1.  <span data-ttu-id="2ba90-108">Ссылка на переменную</span><span class="sxs-lookup"><span data-stu-id="2ba90-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="2ba90-109">Числовые скалярные</span><span class="sxs-lookup"><span data-stu-id="2ba90-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="2ba90-110">Числовое выражение</span><span class="sxs-lookup"><span data-stu-id="2ba90-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="2ba90-111">Здесь поддерживаются все стандартные числовые выражения ХЛЛ.</span><span class="sxs-lookup"><span data-stu-id="2ba90-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="2ba90-112">Конструктор</span><span class="sxs-lookup"><span data-stu-id="2ba90-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="2ba90-113">Список инициализаторов</span><span class="sxs-lookup"><span data-stu-id="2ba90-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="2ba90-114">Скаляры должны быть литеральными скалярными значениями.</span><span class="sxs-lookup"><span data-stu-id="2ba90-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="2ba90-115">Число инициализаторов должно быть совместимо с переменной (State) в левой части знака равенства.</span><span class="sxs-lookup"><span data-stu-id="2ba90-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="2ba90-116">Выражение OR</span><span class="sxs-lookup"><span data-stu-id="2ba90-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="2ba90-117">Токены должны быть совместимы с переменной (штат) в левой части знака равенства.</span><span class="sxs-lookup"><span data-stu-id="2ba90-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="2ba90-118">В токенах регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="2ba90-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="2ba90-119">NULL</span><span class="sxs-lookup"><span data-stu-id="2ba90-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="2ba90-120">Значение NULL может быть назначено шейдеру, образцу или объекту текстуры.</span><span class="sxs-lookup"><span data-stu-id="2ba90-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="2ba90-121">Блок сборки</span><span class="sxs-lookup"><span data-stu-id="2ba90-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="2ba90-122">Блоки сборки PS должны быть назначены состоянию PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="2ba90-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="2ba90-123">Блоки сборок VS должны быть назначены состоянию ВЕРТЕКСШАДЕР.</span><span class="sxs-lookup"><span data-stu-id="2ba90-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="2ba90-124">Блок состояния образца</span><span class="sxs-lookup"><span data-stu-id="2ba90-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="2ba90-125">Блоки состояний образцов — это последовательности неиндексированного состояния этапа образца или назначения текстур.</span><span class="sxs-lookup"><span data-stu-id="2ba90-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="2ba90-126">Блоки состояния образцов должны быть назначены состоянию эффектов образца.</span><span class="sxs-lookup"><span data-stu-id="2ba90-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="2ba90-127">Блок состояния состояния эффектов</span><span class="sxs-lookup"><span data-stu-id="2ba90-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="2ba90-128">Блоки состояния — это последовательности общего состояния.</span><span class="sxs-lookup"><span data-stu-id="2ba90-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="2ba90-129">Блоки состояния могут быть вложенными, но не могут содержать циклических ссылок.</span><span class="sxs-lookup"><span data-stu-id="2ba90-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="2ba90-130">Блоки состояния должны быть назначены состоянию влияния СТАТЕБЛОКК.</span><span class="sxs-lookup"><span data-stu-id="2ba90-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="2ba90-131">HLSL компилировать</span><span class="sxs-lookup"><span data-stu-id="2ba90-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="2ba90-132">Целевой шейдер вершин и \_ m \_ n указывает версию D3DVSа \_ вершинного шейдера версии (m, n).</span><span class="sxs-lookup"><span data-stu-id="2ba90-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="2ba90-133">Цель PS m n пиксельного шейдера \_ \_ указывает \_ версию шейдера D3DPS (m, n) пикселей.</span><span class="sxs-lookup"><span data-stu-id="2ba90-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="2ba90-134">Выражения верхнего уровня для языковой компиляции вершинных шейдеров могут быть назначены только состоянию влияния ВЕРТЕКСШАДЕР.</span><span class="sxs-lookup"><span data-stu-id="2ba90-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="2ba90-135">Выражения высокого уровня языковой компиляции для шейдера пикселей могут быть назначены только состоянию PIXELSHADER Effect.</span><span class="sxs-lookup"><span data-stu-id="2ba90-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba90-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2ba90-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba90-137">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="2ba90-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



