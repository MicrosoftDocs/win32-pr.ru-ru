---
description: Математическая библиотека, предоставляемая библиотекой служебной программы D3DX, предоставляет функции для вычисления трехмерных математических операций.
ms.assetid: 6e180c12-8cbe-4013-8bb4-3ac5bb9c65f1
title: Математические функции (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5401299b1aafd5663d8aaefefa4c7fa0da88a89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896314"
---
# <a name="math-functions-direct3d-10-graphics"></a><span data-ttu-id="0bab9-103">Математические функции (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0bab9-103">Math Functions (Direct3D 10 Graphics)</span></span>

> [!Note]  
> <span data-ttu-id="0bab9-104">Математические функции библиотеки служебной программы D3DX являются устаревшими для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0bab9-104">The math functions of the D3DX utility library are deprecated for Windows 8.</span></span> <span data-ttu-id="0bab9-105">Вместо этого рекомендуется использовать [директксмас](../dxmath/directxmath-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="0bab9-105">We recommend that you use [DirectXMath](../dxmath/directxmath-portal.md) instead.</span></span>

 

<span data-ttu-id="0bab9-106">Математическая библиотека, предоставляемая библиотекой служебной программы D3DX, предоставляет функции для вычисления трехмерных математических операций.</span><span class="sxs-lookup"><span data-stu-id="0bab9-106">The math library provided by the D3DX utility library supplies functions to compute 3D mathematical operations.</span></span> <span data-ttu-id="0bab9-107">Каждая из функций может принимать тот же объект, что и переданный параметр, \[ \] и возвращать \[ выходные \] Параметры.</span><span class="sxs-lookup"><span data-stu-id="0bab9-107">Each of the functions can take the same object as the passed \[in\] and returned \[out\] parameters.</span></span> <span data-ttu-id="0bab9-108">Кроме того, параметры out обычно возвращаются в виде возвращаемых значений, чтобы выходные данные одной математической функции можно было использовать в качестве параметра для другой математической функции.</span><span class="sxs-lookup"><span data-stu-id="0bab9-108">Also, out parameters are typically returned as return values, so that the output of one math function can be used as a parameter for another math function.</span></span>

-   [<span data-ttu-id="0bab9-109">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="0bab9-109">**D3DXColorAdjustContrast**</span></span>](d3d10-d3dxcoloradjustcontrast.md)
-   [<span data-ttu-id="0bab9-110">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="0bab9-110">**D3DXColorAdjustSaturation**</span></span>](d3d10-d3dxcoloradjustsaturation.md)
-   [<span data-ttu-id="0bab9-111">**D3DXCreateMatrixStack**</span><span class="sxs-lookup"><span data-stu-id="0bab9-111">**D3DXCreateMatrixStack**</span></span>](d3d10-d3dxcreatematrixstack.md)
-   [<span data-ttu-id="0bab9-112">**D3DXCpuOptimizations**</span><span class="sxs-lookup"><span data-stu-id="0bab9-112">**D3DXCpuOptimizations**</span></span>](d3d10-d3dxcpuoptimizations.md)
-   [<span data-ttu-id="0bab9-113">**D3DXFloat16To32Array**</span><span class="sxs-lookup"><span data-stu-id="0bab9-113">**D3DXFloat16To32Array**</span></span>](d3d10-d3dxfloat16to32array.md)
-   [<span data-ttu-id="0bab9-114">**D3DXFloat32To16Array**</span><span class="sxs-lookup"><span data-stu-id="0bab9-114">**D3DXFloat32To16Array**</span></span>](d3d10-d3dxfloat32to16array.md)
-   [<span data-ttu-id="0bab9-115">**D3DXFresnelTerm**</span><span class="sxs-lookup"><span data-stu-id="0bab9-115">**D3DXFresnelTerm**</span></span>](d3d10-d3dxfresnelterm.md)
-   [<span data-ttu-id="0bab9-116">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="0bab9-116">**D3DXMatrixAffineTransformation**</span></span>](d3d10-d3dxmatrixaffinetransformation.md)
-   [<span data-ttu-id="0bab9-117">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="0bab9-117">**D3DXMatrixAffineTransformation2D**</span></span>](d3d10-d3dxmatrixaffinetransformation2d.md)
-   [<span data-ttu-id="0bab9-118">**D3DXMatrixDecompose**</span><span class="sxs-lookup"><span data-stu-id="0bab9-118">**D3DXMatrixDecompose**</span></span>](d3d10-d3dxmatrixdecompose.md)
-   [<span data-ttu-id="0bab9-119">**D3DXMatrixDeterminant**</span><span class="sxs-lookup"><span data-stu-id="0bab9-119">**D3DXMatrixDeterminant**</span></span>](d3d10-d3dxmatrixdeterminant.md)
-   [<span data-ttu-id="0bab9-120">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="0bab9-120">**D3DXMatrixInverse**</span></span>](d3d10-d3dxmatrixinverse.md)
-   [<span data-ttu-id="0bab9-121">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-121">**D3DXMatrixLookAtLH**</span></span>](d3d10-d3dxmatrixlookatlh.md)
-   [<span data-ttu-id="0bab9-122">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-122">**D3DXMatrixLookAtRH**</span></span>](d3d10-d3dxmatrixlookatrh.md)
-   [<span data-ttu-id="0bab9-123">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="0bab9-123">**D3DXMatrixMultiply**</span></span>](d3d10-d3dxmatrixmultiply.md)
-   [<span data-ttu-id="0bab9-124">**D3DXMatrixMultiplyTranspose**</span><span class="sxs-lookup"><span data-stu-id="0bab9-124">**D3DXMatrixMultiplyTranspose**</span></span>](d3d10-d3dxmatrixmultiplytranspose.md)
-   [<span data-ttu-id="0bab9-125">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-125">**D3DXMatrixOrthoLH**</span></span>](d3d10-d3dxmatrixortholh.md)
-   [<span data-ttu-id="0bab9-126">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-126">**D3DXMatrixOrthoRH**</span></span>](d3d10-d3dxmatrixorthorh.md)
-   [<span data-ttu-id="0bab9-127">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-127">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3d10-d3dxmatrixorthooffcenterlh.md)
-   [<span data-ttu-id="0bab9-128">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-128">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3d10-d3dxmatrixorthooffcenterrh.md)
-   [<span data-ttu-id="0bab9-129">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-129">**D3DXMatrixPerspectiveFovLH**</span></span>](d3d10-d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="0bab9-130">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="0bab9-130">**D3DXMatrixPerspectiveFovRH**</span></span>](d3d10-d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="0bab9-131">**D3DXMatrixReflect**</span><span class="sxs-lookup"><span data-stu-id="0bab9-131">**D3DXMatrixReflect**</span></span>](d3d10-d3dxmatrixreflect.md)
-   [<span data-ttu-id="0bab9-132">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="0bab9-132">**D3DXMatrixRotationAxis**</span></span>](d3d10-d3dxmatrixrotationaxis.md)
-   [<span data-ttu-id="0bab9-133">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="0bab9-133">**D3DXMatrixRotationX**</span></span>](d3d10-d3dxmatrixrotationx.md)
-   [<span data-ttu-id="0bab9-134">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="0bab9-134">**D3DXMatrixRotationY**</span></span>](d3d10-d3dxmatrixrotationy.md)
-   [<span data-ttu-id="0bab9-135">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="0bab9-135">**D3DXMatrixRotationZ**</span></span>](d3d10-d3dxmatrixrotationz.md)
-   [<span data-ttu-id="0bab9-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="0bab9-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3d10-d3dxmatrixrotationyawpitchroll.md)
-   [<span data-ttu-id="0bab9-137">**D3DXMatrixScaling**</span><span class="sxs-lookup"><span data-stu-id="0bab9-137">**D3DXMatrixScaling**</span></span>](d3d10-d3dxmatrixscaling.md)
-   [<span data-ttu-id="0bab9-138">**D3DXMatrixShadow**</span><span class="sxs-lookup"><span data-stu-id="0bab9-138">**D3DXMatrixShadow**</span></span>](d3d10-d3dxmatrixshadow.md)
-   [<span data-ttu-id="0bab9-139">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="0bab9-139">**D3DXMatrixTransformation**</span></span>](d3d10-d3dxmatrixtransformation.md)
-   [<span data-ttu-id="0bab9-140">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="0bab9-140">**D3DXMatrixTransformation2D**</span></span>](d3d10-d3dxmatrixtransformation2d.md)
-   [<span data-ttu-id="0bab9-141">**D3DXMatrixTranslation**</span><span class="sxs-lookup"><span data-stu-id="0bab9-141">**D3DXMatrixTranslation**</span></span>](d3d10-d3dxmatrixtranslation.md)
-   [<span data-ttu-id="0bab9-142">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="0bab9-142">**D3DXMatrixTranspose**</span></span>](d3d10-d3dxmatrixtranspose.md)
-   [<span data-ttu-id="0bab9-143">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="0bab9-143">**D3DXPlaneFromPointNormal**</span></span>](d3d10-d3dxplanefrompointnormal.md)
-   [<span data-ttu-id="0bab9-144">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="0bab9-144">**D3DXPlaneFromPoints**</span></span>](d3d10-d3dxplanefrompoints.md)
-   [<span data-ttu-id="0bab9-145">**D3DXPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="0bab9-145">**D3DXPlaneIntersectLine**</span></span>](d3d10-d3dxplaneintersectline.md)
-   [<span data-ttu-id="0bab9-146">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="0bab9-146">**D3DXPlaneNormalize**</span></span>](d3d10-d3dxplanenormalize.md)
-   [<span data-ttu-id="0bab9-147">**D3DXPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="0bab9-147">**D3DXPlaneTransform**</span></span>](d3d10-d3dxplanetransform.md)
-   [<span data-ttu-id="0bab9-148">**D3DXPlaneTransformArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-148">**D3DXPlaneTransformArray**</span></span>](d3d10-d3dxplanetransformarray.md)
-   [<span data-ttu-id="0bab9-149">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="0bab9-149">**D3DXQuaternionBaryCentric**</span></span>](d3d10-d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="0bab9-150">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="0bab9-150">**D3DXQuaternionExp**</span></span>](d3d10-d3dxquaternionexp.md)
-   [<span data-ttu-id="0bab9-151">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="0bab9-151">**D3DXQuaternionInverse**</span></span>](d3d10-d3dxquaternioninverse.md)
-   [<span data-ttu-id="0bab9-152">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="0bab9-152">**D3DXQuaternionLn**</span></span>](d3d10-d3dxquaternionln.md)
-   [<span data-ttu-id="0bab9-153">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="0bab9-153">**D3DXQuaternionMultiply**</span></span>](d3d10-d3dxquaternionmultiply.md)
-   [<span data-ttu-id="0bab9-154">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="0bab9-154">**D3DXQuaternionNormalize**</span></span>](d3d10-d3dxquaternionnormalize.md)
-   [<span data-ttu-id="0bab9-155">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="0bab9-155">**D3DXQuaternionRotationAxis**</span></span>](d3d10-d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="0bab9-156">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="0bab9-156">**D3DXQuaternionRotationMatrix**</span></span>](d3d10-d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="0bab9-157">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="0bab9-157">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3d10-d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="0bab9-158">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="0bab9-158">**D3DXQuaternionSlerp**</span></span>](d3d10-d3dxquaternionslerp.md)
-   [<span data-ttu-id="0bab9-159">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="0bab9-159">**D3DXQuaternionSquad**</span></span>](d3d10-d3dxquaternionsquad.md)
-   [<span data-ttu-id="0bab9-160">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="0bab9-160">**D3DXQuaternionSquadSetup**</span></span>](d3d10-d3dxquaternionsquadsetup.md)
-   [<span data-ttu-id="0bab9-161">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="0bab9-161">**D3DXQuaternionToAxisAngle**</span></span>](d3d10-d3dxquaterniontoaxisangle.md)
-   [<span data-ttu-id="0bab9-162">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="0bab9-162">**D3DXSHEvalConeLight**</span></span>](d3d10-d3dxshevalconelight.md)
-   [<span data-ttu-id="0bab9-163">**D3DXSHEvalDirection**</span><span class="sxs-lookup"><span data-stu-id="0bab9-163">**D3DXSHEvalDirection**</span></span>](d3d10-d3dxshevaldirection.md)
-   [<span data-ttu-id="0bab9-164">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="0bab9-164">**D3DXSHEvalDirectionalLight**</span></span>](d3d10-d3dxshevaldirectionallight.md)
-   [<span data-ttu-id="0bab9-165">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="0bab9-165">**D3DXSHEvalHemisphereLight**</span></span>](d3d10-d3dxshevalhemispherelight.md)
-   [<span data-ttu-id="0bab9-166">**D3DXSHMultiply2**</span><span class="sxs-lookup"><span data-stu-id="0bab9-166">**D3DXSHMultiply2**</span></span>](d3d10-d3dxshmultiply2.md)
-   [<span data-ttu-id="0bab9-167">**D3DXSHMultiply3**</span><span class="sxs-lookup"><span data-stu-id="0bab9-167">**D3DXSHMultiply3**</span></span>](d3d10-d3dxshmultiply3.md)
-   [<span data-ttu-id="0bab9-168">**D3DXSHMultiply4**</span><span class="sxs-lookup"><span data-stu-id="0bab9-168">**D3DXSHMultiply4**</span></span>](d3d10-d3dxshmultiply4.md)
-   [<span data-ttu-id="0bab9-169">**D3DXSHMultiply5**</span><span class="sxs-lookup"><span data-stu-id="0bab9-169">**D3DXSHMultiply5**</span></span>](d3d10-d3dxshmultiply5.md)
-   [<span data-ttu-id="0bab9-170">**D3DXSHMultiply6**</span><span class="sxs-lookup"><span data-stu-id="0bab9-170">**D3DXSHMultiply6**</span></span>](d3d10-d3dxshmultiply6.md)
-   [<span data-ttu-id="0bab9-171">**D3DX10SHProjectCubeMap**</span><span class="sxs-lookup"><span data-stu-id="0bab9-171">**D3DX10SHProjectCubeMap**</span></span>](d3dx10shprojectcubemap.md)
-   [<span data-ttu-id="0bab9-172">**D3DXSHRotate**</span><span class="sxs-lookup"><span data-stu-id="0bab9-172">**D3DXSHRotate**</span></span>](d3d10-d3dxshrotate.md)
-   [<span data-ttu-id="0bab9-173">**D3DXSHRotateZ**</span><span class="sxs-lookup"><span data-stu-id="0bab9-173">**D3DXSHRotateZ**</span></span>](d3d10-d3dxshrotatez.md)
-   [<span data-ttu-id="0bab9-174">**D3DXSHScale**</span><span class="sxs-lookup"><span data-stu-id="0bab9-174">**D3DXSHScale**</span></span>](d3d10-d3dxshscale.md)
-   [<span data-ttu-id="0bab9-175">**D3DXVec2BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="0bab9-175">**D3DXVec2BaryCentric**</span></span>](d3d10-d3dxvec2barycentric.md)
-   [<span data-ttu-id="0bab9-176">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="0bab9-176">**D3DXVec2CatmullRom**</span></span>](d3d10-d3dxvec2catmullrom.md)
-   [<span data-ttu-id="0bab9-177">**D3DXVec2Hermite**</span><span class="sxs-lookup"><span data-stu-id="0bab9-177">**D3DXVec2Hermite**</span></span>](d3d10-d3dxvec2hermite.md)
-   [<span data-ttu-id="0bab9-178">**D3DXVec2Normalize**</span><span class="sxs-lookup"><span data-stu-id="0bab9-178">**D3DXVec2Normalize**</span></span>](d3d10-d3dxvec2normalize.md)
-   [<span data-ttu-id="0bab9-179">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="0bab9-179">**D3DXVec2Transform**</span></span>](d3d10-d3dxvec2transform.md)
-   [<span data-ttu-id="0bab9-180">**D3DXVec2TransformArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-180">**D3DXVec2TransformArray**</span></span>](d3d10-d3dxvec2transformarray.md)
-   [<span data-ttu-id="0bab9-181">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="0bab9-181">**D3DXVec2TransformCoord**</span></span>](d3d10-d3dxvec2transformcoord.md)
-   [<span data-ttu-id="0bab9-182">**D3DXVec2TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-182">**D3DXVec2TransformCoordArray**</span></span>](d3d10-d3dxvec2transformcoordarray.md)
-   [<span data-ttu-id="0bab9-183">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="0bab9-183">**D3DXVec2TransformNormal**</span></span>](d3d10-d3dxvec2transformnormal.md)
-   [<span data-ttu-id="0bab9-184">**D3DXVec2TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-184">**D3DXVec2TransformNormalArray**</span></span>](d3d10-d3dxvec2transformnormalarray.md)
-   [<span data-ttu-id="0bab9-185">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="0bab9-185">**D3DXVec3BaryCentric**</span></span>](d3d10-d3dxvec3barycentric.md)
-   [<span data-ttu-id="0bab9-186">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="0bab9-186">**D3DXVec3CatmullRom**</span></span>](d3d10-d3dxvec3catmullrom.md)
-   [<span data-ttu-id="0bab9-187">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="0bab9-187">**D3DXVec3Hermite**</span></span>](d3d10-d3dxvec3hermite.md)
-   [<span data-ttu-id="0bab9-188">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="0bab9-188">**D3DXVec3Normalize**</span></span>](d3d10-d3dxvec3normalize.md)
-   [<span data-ttu-id="0bab9-189">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="0bab9-189">**D3DXVec3Project**</span></span>](d3d10-d3dxvec3project.md)
-   [<span data-ttu-id="0bab9-190">**D3DXVec3ProjectArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-190">**D3DXVec3ProjectArray**</span></span>](d3d10-d3dxvec3projectarray.md)
-   [<span data-ttu-id="0bab9-191">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="0bab9-191">**D3DXVec3Transform**</span></span>](d3d10-d3dxvec3transform.md)
-   [<span data-ttu-id="0bab9-192">**D3DXVec3TransformArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-192">**D3DXVec3TransformArray**</span></span>](d3d10-d3dxvec3transformarray.md)
-   [<span data-ttu-id="0bab9-193">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="0bab9-193">**D3DXVec3TransformCoord**</span></span>](d3d10-d3dxvec3transformcoord.md)
-   [<span data-ttu-id="0bab9-194">**D3DXVec3TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-194">**D3DXVec3TransformCoordArray**</span></span>](d3d10-d3dxvec3transformcoordarray.md)
-   [<span data-ttu-id="0bab9-195">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="0bab9-195">**D3DXVec3TransformNormal**</span></span>](d3d10-d3dxvec3transformnormal.md)
-   [<span data-ttu-id="0bab9-196">**D3DXVec3TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-196">**D3DXVec3TransformNormalArray**</span></span>](d3d10-d3dxvec3transformnormalarray.md)
-   [<span data-ttu-id="0bab9-197">**D3DXVec4BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="0bab9-197">**D3DXVec4BaryCentric**</span></span>](d3d10-d3dxvec4barycentric.md)
-   [<span data-ttu-id="0bab9-198">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="0bab9-198">**D3DXVec4CatmullRom**</span></span>](d3d10-d3dxvec4catmullrom.md)
-   [<span data-ttu-id="0bab9-199">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="0bab9-199">**D3DXVec4Cross**</span></span>](d3d10-d3dxvec4cross.md)
-   [<span data-ttu-id="0bab9-200">**D3DXVec4Hermite**</span><span class="sxs-lookup"><span data-stu-id="0bab9-200">**D3DXVec4Hermite**</span></span>](d3d10-d3dxvec4hermite.md)
-   [<span data-ttu-id="0bab9-201">**D3DXVec4Normalize**</span><span class="sxs-lookup"><span data-stu-id="0bab9-201">**D3DXVec4Normalize**</span></span>](d3d10-d3dxvec4normalize.md)
-   [<span data-ttu-id="0bab9-202">**D3DXVec4Transform**</span><span class="sxs-lookup"><span data-stu-id="0bab9-202">**D3DXVec4Transform**</span></span>](d3d10-d3dxvec4transform.md)
-   [<span data-ttu-id="0bab9-203">**D3DXVec4TransformArray**</span><span class="sxs-lookup"><span data-stu-id="0bab9-203">**D3DXVec4TransformArray**</span></span>](d3d10-d3dxvec4transformarray.md)

## <a name="resolving-link-errors-with-d3dx-math-functions"></a><span data-ttu-id="0bab9-204">Разрешение ошибок ссылок с помощью математических функций D3DX</span><span class="sxs-lookup"><span data-stu-id="0bab9-204">Resolving Link Errors with D3DX Math Functions</span></span>

<span data-ttu-id="0bab9-205">Математические функции D3DX реализуются одинаково в D3DX10 (D3DX10math. h) и D3DX9 (D3DX9math. h).</span><span class="sxs-lookup"><span data-stu-id="0bab9-205">The D3DX math functions are implemented identically in D3DX10 (D3DX10math.h) and D3DX9 (D3DX9math.h).</span></span> <span data-ttu-id="0bab9-206">Это может привести к ошибкам связи, если проект реализует как код DirectX 9, так и DirectX 10, и пытается связать функцию из одного заголовка с противоположной библиотекой.</span><span class="sxs-lookup"><span data-stu-id="0bab9-206">This can cause link errors if a project implements both DirectX 9 and DirectX 10 code, and attempts to link a function from one header with the opposite library.</span></span>

<span data-ttu-id="0bab9-207">Чтобы устранить проблему, связанную с включением обоих заголовков, D3DX10math. h включает следующие \# определения:</span><span class="sxs-lookup"><span data-stu-id="0bab9-207">To eliminate the problem of including both headers, D3DX10math.h includes the following \#define:</span></span>


```
#ifndef __D3DX9MATH_H__
#define __D3DX9MATH_H__
```



<span data-ttu-id="0bab9-208">Чтобы устранить возможные ошибки связи, в примерах SDK для DX сначала должна быть ссылка на библиотеки D3DX9 (D3DX9d. lib и D3DX9. lib), а затем библиотеки D3DX10 (D3DX10d. lib и D3DX10. lib).</span><span class="sxs-lookup"><span data-stu-id="0bab9-208">To eliminate possible link errors, the DX SDK samples link to D3DX9 libraries first (D3DX9d.lib and D3DX9.lib) and then the D3DX10 libraries second (D3DX10d.lib and D3DX10.lib).</span></span> <span data-ttu-id="0bab9-209">Эти параметры находятся в разделе проект или свойства, если используется Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0bab9-209">These settings are under Project/Properties if you are using Visual Studio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bab9-210">См. также</span><span class="sxs-lookup"><span data-stu-id="0bab9-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bab9-211">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="0bab9-211">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
