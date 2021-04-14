---
description: Искажение, видимое в пикселей текстуры трехмерного объекта, поверхность которого ориентирована на угол относительно плоскости экрана, называется анизотропной.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Анизотропная фильтрация текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496566"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a><span data-ttu-id="52d8c-103">Анизотропная фильтрация текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="52d8c-103">Anisotropic Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="52d8c-104">Искажение, видимое в пикселей текстуры трехмерного объекта, поверхность которого ориентирована на угол относительно плоскости экрана, называется анизотропной.</span><span class="sxs-lookup"><span data-stu-id="52d8c-104">The distortion visible in the texels of a 3D object whose surface is oriented at an angle with respect to the plane of the screen is called anisotropy.</span></span> <span data-ttu-id="52d8c-105">Если пиксель из анизотропного примитива сопоставляется текселям, его форма искажается.</span><span class="sxs-lookup"><span data-stu-id="52d8c-105">When a pixel from an anisotropic primitive is mapped to texels, its shape is distorted.</span></span> <span data-ttu-id="52d8c-106">Direct3D измеряет анизотропию пикселя как удлинение, то есть длину, разделенную на ширину, экранного пикселя, который сопоставляется в пространстве текстуры инверсивно.</span><span class="sxs-lookup"><span data-stu-id="52d8c-106">Direct3D measures the anisotropy of a pixel as the elongation - that is, length divided by width - of a screen pixel that is inverse-mapped into texture space.</span></span>

<span data-ttu-id="52d8c-107">Для улучшения результатов отрисовки анизотропную фильтрацию текстур можно использовать в сочетании с линейной фильтрацией текстур или MIP-фильтрацией текстур.</span><span class="sxs-lookup"><span data-stu-id="52d8c-107">You can use anisotropic texture filtering in conjunction with linear texture filtering or mipmap texture filtering to improve rendering results.</span></span> <span data-ttu-id="52d8c-108">Приложение обеспечивает фильтрацию с помощью анизотропной фильтрации текстур путем вызова метода [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="52d8c-108">Your application enables anisotropic texture filtering by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="52d8c-109">Задайте для первого параметра значение целочисленного индекса (0-7) текстуры, для которой выбирается метод фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="52d8c-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="52d8c-110">Передайте D3DSAMP \_ магфилтер, D3DSAMP \_ МИНФИЛТЕР или D3DSAMP \_ мипфилтер во второй параметр, чтобы задать фильтр увеличения, минификации или функции текстурирования.</span><span class="sxs-lookup"><span data-stu-id="52d8c-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="52d8c-111">Задайте для третьего параметра значение D3DTEXF \_ анизотроп.</span><span class="sxs-lookup"><span data-stu-id="52d8c-111">Set the third parameter to D3DTEXF\_ANISOTROPIC.</span></span>

<span data-ttu-id="52d8c-112">В приложении также должно быть задано значение, большее, чем единица анизотроп.</span><span class="sxs-lookup"><span data-stu-id="52d8c-112">Your application must also set the degree of anisotropy to a value greater than one.</span></span> <span data-ttu-id="52d8c-113">Для этого вызовите метод [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="52d8c-113">Do this by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="52d8c-114">Задайте для первого параметра значение целочисленного индекса (0-7) текстуры, для которой задается степень исотропи.</span><span class="sxs-lookup"><span data-stu-id="52d8c-114">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are setting the degree of isotropy.</span></span> <span data-ttu-id="52d8c-115">Передайте D3DSAMP \_ максанисотропи в качестве значения второго параметра.</span><span class="sxs-lookup"><span data-stu-id="52d8c-115">Pass D3DSAMP\_MAXANISOTROPY as the value of the second parameter.</span></span> <span data-ttu-id="52d8c-116">Последний параметр должен быть степенью исотропи.</span><span class="sxs-lookup"><span data-stu-id="52d8c-116">The final parameter should be the degree of isotropy.</span></span>

<span data-ttu-id="52d8c-117">Можно отключить фильтрацию исотропик, задав для степени исотропи значение 1; любое значение, большее одного, включает его.</span><span class="sxs-lookup"><span data-stu-id="52d8c-117">You can disable isotropic filtering by setting the degree of isotropy to one; any value larger than one enables it.</span></span> <span data-ttu-id="52d8c-118">Проверьте флаг Максанисотропи в структуре [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , чтобы определить возможный диапазон значений для уровня анизотроп.</span><span class="sxs-lookup"><span data-stu-id="52d8c-118">Check the MaxAnisotropy flag in the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine the possible range of values for the degree of anisotropy.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52d8c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="52d8c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52d8c-120">Фильтрация текстур</span><span class="sxs-lookup"><span data-stu-id="52d8c-120">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
