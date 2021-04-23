---
description: Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Интерфейс ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355640"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="ba85d-103">Интерфейс ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ba85d-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="ba85d-104">Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.</span><span class="sxs-lookup"><span data-stu-id="ba85d-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="ba85d-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ba85d-105">Members</span></span>

<span data-ttu-id="ba85d-106">Интерфейс **ID3DXMatrixStack** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ba85d-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ba85d-107">**ID3DXMatrixStack** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba85d-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="ba85d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ba85d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ba85d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ba85d-109">Methods</span></span>

<span data-ttu-id="ba85d-110">Интерфейс **ID3DXMatrixStack** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ba85d-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="ba85d-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ba85d-111">Method</span></span>                                                                      | <span data-ttu-id="ba85d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ba85d-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba85d-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="ba85d-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="ba85d-114">Извлекает текущую матрицу в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="ba85d-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="ba85d-115">**лоадидентити**</span><span class="sxs-lookup"><span data-stu-id="ba85d-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="ba85d-116">Загружает удостоверение в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="ba85d-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="ba85d-117">**лоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="ba85d-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="ba85d-118">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="ba85d-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ba85d-119">**мултматрикс**</span><span class="sxs-lookup"><span data-stu-id="ba85d-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="ba85d-120">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="ba85d-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="ba85d-121">**мултматрикслокал**</span><span class="sxs-lookup"><span data-stu-id="ba85d-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="ba85d-122">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="ba85d-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="ba85d-123">**Рор**</span><span class="sxs-lookup"><span data-stu-id="ba85d-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="ba85d-124">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="ba85d-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="ba85d-125">**push**</span><span class="sxs-lookup"><span data-stu-id="ba85d-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="ba85d-126">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="ba85d-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="ba85d-127">**ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="ba85d-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="ba85d-128">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="ba85d-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="ba85d-129">**ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="ba85d-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="ba85d-130">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="ba85d-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="ba85d-131">**ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="ba85d-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="ba85d-132">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="ba85d-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="ba85d-133">**ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="ba85d-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="ba85d-134">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="ba85d-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="ba85d-135">**Измените**</span><span class="sxs-lookup"><span data-stu-id="ba85d-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="ba85d-136">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="ba85d-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="ba85d-137">**скалелокал**</span><span class="sxs-lookup"><span data-stu-id="ba85d-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="ba85d-138">Масштабировать текущую матрицу относительно источника объекта.</span><span class="sxs-lookup"><span data-stu-id="ba85d-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="ba85d-139">**Перевести**</span><span class="sxs-lookup"><span data-stu-id="ba85d-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="ba85d-140">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="ba85d-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="ba85d-141">**транслателокал**</span><span class="sxs-lookup"><span data-stu-id="ba85d-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="ba85d-142">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="ba85d-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba85d-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba85d-143">Remarks</span></span>

<span data-ttu-id="ba85d-144">Интерфейс ID3DX10MATRIXStack получается путем вызова функции [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="ba85d-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="ba85d-145">Тип LPD3DX10MATRIXSTACK определяется как указатель на интерфейс **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="ba85d-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="ba85d-146">Требования</span><span class="sxs-lookup"><span data-stu-id="ba85d-146">Requirements</span></span>



| <span data-ttu-id="ba85d-147">Требование</span><span class="sxs-lookup"><span data-stu-id="ba85d-147">Requirement</span></span> | <span data-ttu-id="ba85d-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ba85d-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba85d-149">Header</span><span class="sxs-lookup"><span data-stu-id="ba85d-149">Header</span></span><br/>  | <dl> <span data-ttu-id="ba85d-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba85d-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba85d-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba85d-151">Library</span></span><br/> | <dl> <span data-ttu-id="ba85d-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba85d-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba85d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba85d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba85d-154">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ba85d-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
