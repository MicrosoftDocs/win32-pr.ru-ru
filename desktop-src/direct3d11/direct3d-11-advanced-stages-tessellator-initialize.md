---
title: Инициализация этапа тесселяции
description: В этом разделе показано, как инициализировать этап тесселяции.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996738"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="e4da1-103">Поэтапное руководство. Инициализация этапа тесселяции</span><span class="sxs-lookup"><span data-stu-id="e4da1-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="e4da1-104">Как правило, тесселяция расширяет компактную, определяемую пользователем модель исправления на геометрию, которая содержит программируемый объем данных.</span><span class="sxs-lookup"><span data-stu-id="e4da1-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="e4da1-105">Геометрический объект обычно представляет собой набор треугольников, представляющий подробную геометрию поверхности.</span><span class="sxs-lookup"><span data-stu-id="e4da1-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="e4da1-106">В этом разделе показано, как инициализировать этап тесселяции.</span><span class="sxs-lookup"><span data-stu-id="e4da1-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="e4da1-107">Этап тесселяции — это второй из трех этапов, которые работают вместе для тесселяции или мозаичной плитки поверхности.</span><span class="sxs-lookup"><span data-stu-id="e4da1-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="e4da1-108">Первый этап — это этап поверхности-шейдера; Он действует один раз для каждого исправления и настраивает, как работает следующий этап (тесселяция предопределенной функции).</span><span class="sxs-lookup"><span data-stu-id="e4da1-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="e4da1-109">Шейдер поверхности также создает определяемые пользователем выходные данные, такие как точки управления выводом и константы исправления, которые отправляются за пререзками непосредственно на третий этап, этап шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="e4da1-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="e4da1-110">Шейдер домена вызывается один раз для каждой точки тесселяции и оценивает положения поверхности.</span><span class="sxs-lookup"><span data-stu-id="e4da1-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="e4da1-111">Этап тесселяции — это фиксированный этап функции, отсутствует шейдер для создания и не задается состояние.</span><span class="sxs-lookup"><span data-stu-id="e4da1-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="e4da1-112">Он получает все свое состояние установки с этапа поверхности-шейдера; После инициализации этапа поверхности-шейдера этап тесселяции автоматически инициализируется.</span><span class="sxs-lookup"><span data-stu-id="e4da1-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="e4da1-113">**Инициализация этапа тесселяции**</span><span class="sxs-lookup"><span data-stu-id="e4da1-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="e4da1-114">Инициализируйте этап поверхности-шейдера с помощью [**ссылку ID3D11DeviceContext:: хссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="e4da1-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="e4da1-115">*ппклассинстанцес* — это указатель на массив интерфейсов шейдера, представленных указателями [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) , и количество интерфейсов, представленных *нумклассинстанцес*.</span><span class="sxs-lookup"><span data-stu-id="e4da1-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="e4da1-116">Если не используется, эти параметры могут иметь **значение NULL** и 0 соответственно.</span><span class="sxs-lookup"><span data-stu-id="e4da1-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="e4da1-117">После инициализации этапа поверхности-шейдера также следует инициализировать этап шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="e4da1-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4da1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e4da1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4da1-119">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e4da1-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="e4da1-120">Общие сведения об тесселяции</span><span class="sxs-lookup"><span data-stu-id="e4da1-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




