---
title: Создание шейдера поверхности
description: В этом разделе показано, как создать шейдер поверхности.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773718"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="baf43-103">Руководство. Создание шейдера поверхности</span><span class="sxs-lookup"><span data-stu-id="baf43-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="baf43-104">Шейдер поверхности — это первый из трех этапов, которые работают вместе для реализации [тесселяции](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="baf43-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="baf43-105">Поверхности-шейдер выводит на этап тесселяции, а также на этап шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="baf43-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="baf43-106">В этом разделе показано, как создать шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="baf43-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="baf43-107">Шейдер поверхности преобразует набор контрольных точек ввода (от шейдера вершин) в набор контрольных точек вывода.</span><span class="sxs-lookup"><span data-stu-id="baf43-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="baf43-108">Количество входных и выходных точек может различаться в зависимости от преобразования (типичное преобразование — это преобразование «основание»).</span><span class="sxs-lookup"><span data-stu-id="baf43-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="baf43-109">Шейдер поверхности также выводит сведения о константе исправления, такие как факторы тесселяции, для шейдера домена и тесселяции.</span><span class="sxs-lookup"><span data-stu-id="baf43-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="baf43-110">На этапе тесселяции с фиксированной функцией используются факторы тесселяции, а также другое состояние, объявленное в шейдере поверхности, чтобы определить, сколько нужно тесселяции.</span><span class="sxs-lookup"><span data-stu-id="baf43-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="baf43-111">**Создание шейдера поверхности**</span><span class="sxs-lookup"><span data-stu-id="baf43-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="baf43-112">Создайте шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="baf43-112">Design a hull shader.</span></span> <span data-ttu-id="baf43-113">См. раздел [руководство. Проектирование шейдера поверхности](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="baf43-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="baf43-114">Компиляция кода шейдера</span><span class="sxs-lookup"><span data-stu-id="baf43-114">Compile the shader code</span></span>
3.  <span data-ttu-id="baf43-115">Создайте объект поверхности-Shader с помощью [**ID3D11Device:: креатехуллшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="baf43-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="baf43-116">Инициализируйте стадию конвейера с помощью [**ссылку ID3D11DeviceContext:: хссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="baf43-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="baf43-117">При наличии привязки шейдера поверхности необходимо привязать шейдер домена к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="baf43-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="baf43-118">В частности, недопустимый прямой потоковая передача контрольных точек шейдера поверхности с помощью шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="baf43-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baf43-119">См. также</span><span class="sxs-lookup"><span data-stu-id="baf43-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baf43-120">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="baf43-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="baf43-121">Общие сведения об тесселяции</span><span class="sxs-lookup"><span data-stu-id="baf43-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




