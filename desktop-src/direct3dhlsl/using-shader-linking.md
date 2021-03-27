---
title: Использование связывания шейдера
description: Мы покажем, как создавать предварительно скомпилированные функции HLSL, упаковывать их в библиотеки и связывать их с полными шейдерами во время выполнения.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793585"
---
# <a name="using-shader-linking"></a><span data-ttu-id="2a2cd-103">Использование связывания шейдера</span><span class="sxs-lookup"><span data-stu-id="2a2cd-103">Using shader linking</span></span>

<span data-ttu-id="2a2cd-104">Мы покажем, как создавать предварительно скомпилированные функции HLSL, упаковывать их в библиотеки и связывать их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="2a2cd-105">Связывание шейдера поддерживается начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="2a2cd-106">**Цель:** Узнайте, как использовать связывание с шейдером.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a2cd-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="2a2cd-107">Prerequisites</span></span>

<span data-ttu-id="2a2cd-108">Предполагается, что вы знакомы с C++.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="2a2cd-109">Также вы должны быть знакомы с основными принципами программирования графики.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="2a2cd-110">**Общее время выполнения:** 60 минут.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="2a2cd-111">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2a2cd-111">Where to go from here</span></span>

<span data-ttu-id="2a2cd-112">См. также [интерфейсы API компилятора HLSL](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2a2cd-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="2a2cd-113">Здесь показаны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2a2cd-113">We show you how to:</span></span>

-   <span data-ttu-id="2a2cd-114">Компиляция кода шейдера</span><span class="sxs-lookup"><span data-stu-id="2a2cd-114">Compile your shader code</span></span>
-   <span data-ttu-id="2a2cd-115">Загрузка скомпилированного кода в библиотеку шейдера</span><span class="sxs-lookup"><span data-stu-id="2a2cd-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="2a2cd-116">Привязка ресурсов из исходных слотов к конечным слотам</span><span class="sxs-lookup"><span data-stu-id="2a2cd-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="2a2cd-117">Создание графов функций-связей (Флгс) для шейдеров</span><span class="sxs-lookup"><span data-stu-id="2a2cd-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="2a2cd-118">Связывание графов шейдера с библиотекой шейдеров для создания большого двоичного объекта шейдера, который может использоваться средой выполнения Direct3D</span><span class="sxs-lookup"><span data-stu-id="2a2cd-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="2a2cd-119">Далее мы создадим библиотеку шейдеров и связываем ресурсы из исходных слотов с конечными слотами.</span><span class="sxs-lookup"><span data-stu-id="2a2cd-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="2a2cd-120">Упаковка библиотеки шейдеров</span><span class="sxs-lookup"><span data-stu-id="2a2cd-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="2a2cd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="2a2cd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a2cd-122">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="2a2cd-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="2a2cd-123">Графика Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2a2cd-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="2a2cd-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="2a2cd-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 