---
description: Интерфейс ID3DXMATRIXStack. приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.
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
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093322"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="f3ccc-103">Интерфейс ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="f3ccc-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="f3ccc-104">Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="f3ccc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f3ccc-105">Members</span></span>

<span data-ttu-id="f3ccc-106">Интерфейс **ID3DXMATRIXStack** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f3ccc-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3ccc-107">**ID3DXMATRIXStack** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f3ccc-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="f3ccc-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f3ccc-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f3ccc-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f3ccc-109">Methods</span></span>

<span data-ttu-id="f3ccc-110">Интерфейс **ID3DXMATRIXStack** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="f3ccc-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f3ccc-111">Method</span></span>                                                                       | <span data-ttu-id="f3ccc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f3ccc-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3ccc-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="f3ccc-114">Извлекает текущую матрицу в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="f3ccc-115">**лоадидентити**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="f3ccc-116">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f3ccc-117">**лоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="f3ccc-118">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="f3ccc-119">**мултматрикс**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="f3ccc-120">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="f3ccc-121">**мултматрикслокал**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="f3ccc-122">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="f3ccc-123">**Рор**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="f3ccc-124">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="f3ccc-125">**push**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="f3ccc-126">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="f3ccc-127">**ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="f3ccc-128">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="f3ccc-129">**ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="f3ccc-130">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="f3ccc-131">**ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="f3ccc-132">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="f3ccc-133">**ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="f3ccc-134">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="f3ccc-135">**Масштабирование**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="f3ccc-136">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="f3ccc-137">**скалелокал**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="f3ccc-138">Масштабировать текущую матрицу относительно источника объекта.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="f3ccc-139">**Перевести**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="f3ccc-140">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="f3ccc-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="f3ccc-141">**транслателокал**</span><span class="sxs-lookup"><span data-stu-id="f3ccc-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="f3ccc-142">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="f3ccc-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3ccc-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="f3ccc-143">Remarks</span></span>

<span data-ttu-id="f3ccc-144">Интерфейс **ID3DXMATRIXStack** получается путем вызова функции [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ccc-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="f3ccc-145">Тип LPD3DXMATRIXSTACK определяется как указатель на интерфейс **ID3DXMATRIXStack** .</span><span class="sxs-lookup"><span data-stu-id="f3ccc-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="f3ccc-146">Требования</span><span class="sxs-lookup"><span data-stu-id="f3ccc-146">Requirements</span></span>



| <span data-ttu-id="f3ccc-147">Требование</span><span class="sxs-lookup"><span data-stu-id="f3ccc-147">Requirement</span></span> | <span data-ttu-id="f3ccc-148">Значение</span><span class="sxs-lookup"><span data-stu-id="f3ccc-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ccc-149">Header</span><span class="sxs-lookup"><span data-stu-id="f3ccc-149">Header</span></span><br/>  | <dl> <span data-ttu-id="f3ccc-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ccc-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f3ccc-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3ccc-151">Library</span></span><br/> | <dl> <span data-ttu-id="f3ccc-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3ccc-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3ccc-153">См. также</span><span class="sxs-lookup"><span data-stu-id="f3ccc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ccc-154">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f3ccc-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
