---
description: Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Интерфейс ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703977"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="03d11-103">Интерфейс ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="03d11-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="03d11-104">Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.</span><span class="sxs-lookup"><span data-stu-id="03d11-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="03d11-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="03d11-105">Members</span></span>

<span data-ttu-id="03d11-106">Интерфейс **ID3DXMATRIXStack** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="03d11-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="03d11-107">**ID3DXMATRIXStack** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03d11-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="03d11-108">Методы</span><span class="sxs-lookup"><span data-stu-id="03d11-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="03d11-109">Методы</span><span class="sxs-lookup"><span data-stu-id="03d11-109">Methods</span></span>

<span data-ttu-id="03d11-110">Интерфейс **ID3DXMATRIXStack** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="03d11-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="03d11-111">Метод</span><span class="sxs-lookup"><span data-stu-id="03d11-111">Method</span></span>                                                                       | <span data-ttu-id="03d11-112">Описание</span><span class="sxs-lookup"><span data-stu-id="03d11-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03d11-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="03d11-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="03d11-114">Извлекает текущую матрицу в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="03d11-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="03d11-115">**лоадидентити**</span><span class="sxs-lookup"><span data-stu-id="03d11-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="03d11-116">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="03d11-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="03d11-117">**лоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="03d11-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="03d11-118">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="03d11-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="03d11-119">**мултматрикс**</span><span class="sxs-lookup"><span data-stu-id="03d11-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="03d11-120">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="03d11-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="03d11-121">**мултматрикслокал**</span><span class="sxs-lookup"><span data-stu-id="03d11-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="03d11-122">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="03d11-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="03d11-123">**Рор**</span><span class="sxs-lookup"><span data-stu-id="03d11-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="03d11-124">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="03d11-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="03d11-125">**push**</span><span class="sxs-lookup"><span data-stu-id="03d11-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="03d11-126">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="03d11-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="03d11-127">**ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="03d11-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="03d11-128">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="03d11-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="03d11-129">**ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="03d11-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="03d11-130">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="03d11-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="03d11-131">**ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="03d11-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="03d11-132">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="03d11-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="03d11-133">**ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="03d11-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="03d11-134">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="03d11-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="03d11-135">**Измените**</span><span class="sxs-lookup"><span data-stu-id="03d11-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="03d11-136">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="03d11-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="03d11-137">**скалелокал**</span><span class="sxs-lookup"><span data-stu-id="03d11-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="03d11-138">Масштабировать текущую матрицу относительно источника объекта.</span><span class="sxs-lookup"><span data-stu-id="03d11-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="03d11-139">**Перевести**</span><span class="sxs-lookup"><span data-stu-id="03d11-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="03d11-140">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="03d11-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="03d11-141">**транслателокал**</span><span class="sxs-lookup"><span data-stu-id="03d11-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="03d11-142">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="03d11-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03d11-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03d11-143">Remarks</span></span>

<span data-ttu-id="03d11-144">Интерфейс **ID3DXMATRIXStack** получается путем вызова функции [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="03d11-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="03d11-145">Тип LPD3DXMATRIXSTACK определяется как указатель на интерфейс **ID3DXMATRIXStack** .</span><span class="sxs-lookup"><span data-stu-id="03d11-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="03d11-146">Требования</span><span class="sxs-lookup"><span data-stu-id="03d11-146">Requirements</span></span>



| <span data-ttu-id="03d11-147">Требование</span><span class="sxs-lookup"><span data-stu-id="03d11-147">Requirement</span></span> | <span data-ttu-id="03d11-148">Значение</span><span class="sxs-lookup"><span data-stu-id="03d11-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d11-149">Header</span><span class="sxs-lookup"><span data-stu-id="03d11-149">Header</span></span><br/>  | <dl> <span data-ttu-id="03d11-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d11-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="03d11-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03d11-151">Library</span></span><br/> | <dl> <span data-ttu-id="03d11-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03d11-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03d11-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03d11-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d11-154">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="03d11-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
