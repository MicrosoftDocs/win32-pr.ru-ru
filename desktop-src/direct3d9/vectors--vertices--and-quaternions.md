---
description: В Direct3D вершины описывают положение и ориентацию. Каждая вершина в примитиве описывается вектором, который сообщает ее положение, цвет, координаты текстуры, и вектором нормали, который позволяет узнать ее ориентацию.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Векторы, вершины и кватернион (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537025"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="7983f-104">Векторы, вершины и кватернион (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7983f-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="7983f-105">В Direct3D вершины описывают положение и ориентацию.</span><span class="sxs-lookup"><span data-stu-id="7983f-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="7983f-106">Каждая вершина в примитиве описывается вектором, который сообщает ее положение, цвет, координаты текстуры, и вектором нормали, который позволяет узнать ее ориентацию.</span><span class="sxs-lookup"><span data-stu-id="7983f-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="7983f-107">Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , которые определяют вектор с тремя компонентами.</span><span class="sxs-lookup"><span data-stu-id="7983f-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="7983f-108">Кватернионы представляют собой альтернативу матричным методам, обычно используемым для 3D-вращения.</span><span class="sxs-lookup"><span data-stu-id="7983f-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="7983f-109">Кватернион представляет ось в 3D-пространстве и поворот вокруг этой оси.</span><span class="sxs-lookup"><span data-stu-id="7983f-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="7983f-110">Например, кватернион может представлять ось (1,1,2) и поворот на 1 радиан.</span><span class="sxs-lookup"><span data-stu-id="7983f-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="7983f-111">Кватернионы содержат полезную информацию, однако их истинная ценность заключается в двух операциях, которые можно выполнять над ними: композиции и интерполяции.</span><span class="sxs-lookup"><span data-stu-id="7983f-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="7983f-112">Выполнение композиции над кватернионами аналогично их объединению.</span><span class="sxs-lookup"><span data-stu-id="7983f-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="7983f-113">Записывается композиция двух кватернионов так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7983f-113">The composition of two quaternions is notated like the following illustration.</span></span>

![иллюстрация записи кватернионов](images/quateq.png)

<span data-ttu-id="7983f-115">Композиция двух кватернионов, применяемая к геометрии, означает "повернуть геометрию вокруг оси₂ на поворот₂, затем повернуть ее вокруг оси₁ на поворот₁".</span><span class="sxs-lookup"><span data-stu-id="7983f-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="7983f-116">В данном случае Q представляет поворот вокруг одной оси, который является результатом применения q₂ и затем q₁ к геометрии.</span><span class="sxs-lookup"><span data-stu-id="7983f-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="7983f-117">С помощью интерполяции кватернионов приложение может рассчитать плавный и рациональный путь от одной оси и ориентации к другой.</span><span class="sxs-lookup"><span data-stu-id="7983f-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="7983f-118">Таким образом, интерполяция между q₁ и q₂ — это простой способ анимировать движение от одной ориентации к другой.</span><span class="sxs-lookup"><span data-stu-id="7983f-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="7983f-119">При совместном использовании композиция и интерполяция дают возможность без труда манипулировать геометрией так, что манипуляции будут казаться сложными.</span><span class="sxs-lookup"><span data-stu-id="7983f-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="7983f-120">Например, предположим, что у вас есть геометрия, которую вы хотите повернуть для придания ей определенной ориентации.</span><span class="sxs-lookup"><span data-stu-id="7983f-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="7983f-121">Вам известно, что нужно повернуть ее на r₂ градусов вокруг оси₂, а затем на r₁ градусов вокруг оси₁, однако окончательный кватернион вам не известен.</span><span class="sxs-lookup"><span data-stu-id="7983f-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="7983f-122">Используя композицию, вы можете объединить два поворота применительно к геометрии и получить один кватернион, который будет представлять собой результат.</span><span class="sxs-lookup"><span data-stu-id="7983f-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="7983f-123">Затем можно выполнить интерполяцию из исходного кватерниона в составной для получения плавного перехода от одного к другому.</span><span class="sxs-lookup"><span data-stu-id="7983f-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="7983f-124">Библиотека служебной программы D3DX включает функции, помогающие работать с кватернион.</span><span class="sxs-lookup"><span data-stu-id="7983f-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="7983f-125">Например, функция [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) добавляет значение вращения к вектору, который определяет ось вращения, и возвращает результат в кватернион, определенный структурой [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="7983f-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="7983f-126">Кроме того, функция [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) формирует кватернионs, а [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) выполняет сферовую линейную интерполяцию между двумя кватерниона.</span><span class="sxs-lookup"><span data-stu-id="7983f-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="7983f-127">Приложения Direct3D могут использовать следующие функции, чтобы упростить задачу работы с кватерниона.</span><span class="sxs-lookup"><span data-stu-id="7983f-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="7983f-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7983f-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="7983f-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="7983f-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="7983f-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="7983f-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="7983f-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="7983f-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="7983f-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="7983f-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="7983f-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="7983f-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="7983f-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="7983f-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="7983f-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="7983f-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="7983f-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="7983f-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="7983f-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="7983f-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="7983f-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="7983f-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="7983f-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="7983f-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="7983f-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7983f-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="7983f-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="7983f-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="7983f-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7983f-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="7983f-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="7983f-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="7983f-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="7983f-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="7983f-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="7983f-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="7983f-146">Приложения Direct3D могут использовать следующие функции, чтобы упростить задачу работы с тремя компонентными векторами.</span><span class="sxs-lookup"><span data-stu-id="7983f-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="7983f-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="7983f-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="7983f-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7983f-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="7983f-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="7983f-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="7983f-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="7983f-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="7983f-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="7983f-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="7983f-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="7983f-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="7983f-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="7983f-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="7983f-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="7983f-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="7983f-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="7983f-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="7983f-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="7983f-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="7983f-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="7983f-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="7983f-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="7983f-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="7983f-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="7983f-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="7983f-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="7983f-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="7983f-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="7983f-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="7983f-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="7983f-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="7983f-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="7983f-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="7983f-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="7983f-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="7983f-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="7983f-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="7983f-166">Многие дополнительные функции, упрощающие задачи с использованием двух-и четырех компонентных векторов, включены в [математические функции](dx9-graphics-reference-d3dx-functions-math.md) , предоставляемые библиотекой служебной программы D3DX.</span><span class="sxs-lookup"><span data-stu-id="7983f-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7983f-167">См. также</span><span class="sxs-lookup"><span data-stu-id="7983f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7983f-168">Системы координат и геометрия</span><span class="sxs-lookup"><span data-stu-id="7983f-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



