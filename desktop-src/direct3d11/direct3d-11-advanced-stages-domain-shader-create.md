---
title: Создание шейдера домена
description: В этом разделе показано, как создать шейдер домена.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067499"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="d181e-103">Как создать Шейдер доменов</span><span class="sxs-lookup"><span data-stu-id="d181e-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="d181e-104">Шейдер доменов — это третий из трех этапов, которые работают вместе для реализации [тесселяции](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="d181e-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="d181e-105">Входные данные для этапа доменного шейдера берутся из шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="d181e-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="d181e-106">В этом разделе показано, как создать шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="d181e-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="d181e-107">Шейдер домена преобразует геометрию поверхности (созданную стадией тесселяции с фиксированной функцией) с помощью точек управления выходными данными шейдера поверхности, выходных данных исправления шейдеров поверхности-Constant Data и единого набора координат тесселяции UV.</span><span class="sxs-lookup"><span data-stu-id="d181e-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="d181e-108">**Создание шейдера домена**</span><span class="sxs-lookup"><span data-stu-id="d181e-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="d181e-109">Создайте шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="d181e-109">Design a domain shader.</span></span> <span data-ttu-id="d181e-110">См. раздел [как создать шейдер домена](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="d181e-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="d181e-111">Скомпилируйте код шейдера.</span><span class="sxs-lookup"><span data-stu-id="d181e-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="d181e-112">Создайте объект шейдера домена с помощью [**ID3D11Device:: креатедомаиншадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="d181e-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="d181e-113">Инициализируйте стадию конвейера с помощью [**ссылку ID3D11DeviceContext::D ссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="d181e-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="d181e-114">При наличии привязки шейдера поверхности необходимо привязать шейдер домена к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d181e-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="d181e-115">В частности, недопустимый прямой потоковая передача контрольных точек шейдера поверхности с помощью шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="d181e-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d181e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d181e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d181e-117">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d181e-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="d181e-118">Общие сведения об тесселяции</span><span class="sxs-lookup"><span data-stu-id="d181e-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




