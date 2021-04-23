---
description: Загружает первую иерархию кадров из файла. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Функция D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91cf119fc8907701f87ebb5bda1bb0bf45294aba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703979"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="aae80-103">Функция D3DXLoadMeshHierarchyFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="aae80-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="aae80-104">Загружает первую иерархию кадров из файла. x.</span><span class="sxs-lookup"><span data-stu-id="aae80-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aae80-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="aae80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aae80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae80-107">*пмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae80-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae80-109">Указатель на буфер, содержащий иерархию сетки.</span><span class="sxs-lookup"><span data-stu-id="aae80-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="aae80-110">*Сизеофмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae80-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae80-112">Размер буфера Пмемори в байтах.</span><span class="sxs-lookup"><span data-stu-id="aae80-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aae80-113">*Мешоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae80-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae80-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="aae80-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="aae80-116">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-117">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="aae80-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="aae80-118">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="aae80-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="aae80-119">*паллок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-120">Тип: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="aae80-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="aae80-121">Указатель на интерфейс [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="aae80-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="aae80-122">*пусердаталоадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae80-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-123">Тип: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="aae80-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="aae80-124">Предоставленный приложением интерфейс, позволяющий загружать пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="aae80-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="aae80-125">См. [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="aae80-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="aae80-126">*ппфрамехеирарчи* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aae80-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-127">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="aae80-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="aae80-128">Возвращает указатель на иерархию загруженных кадров.</span><span class="sxs-lookup"><span data-stu-id="aae80-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="aae80-129">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="aae80-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="aae80-130">*ппанимконтроллер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aae80-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae80-131">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="aae80-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="aae80-132">Возвращает указатель на контроллер анимации, соответствующий анимации в файле. x.</span><span class="sxs-lookup"><span data-stu-id="aae80-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="aae80-133">Он создается с отслеживанием и событиями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aae80-133">This is created with default tracks and events.</span></span> <span data-ttu-id="aae80-134">См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="aae80-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae80-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aae80-135">Return value</span></span>

<span data-ttu-id="aae80-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aae80-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aae80-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="aae80-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aae80-138">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="aae80-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aae80-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aae80-139">Remarks</span></span>

<span data-ttu-id="aae80-140">Все сетки в файле будут свернуты в одну выходную сетку.</span><span class="sxs-lookup"><span data-stu-id="aae80-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="aae80-141">Если файл содержит иерархию рамок, все преобразования будут применены к сетке.</span><span class="sxs-lookup"><span data-stu-id="aae80-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae80-142">Требования</span><span class="sxs-lookup"><span data-stu-id="aae80-142">Requirements</span></span>



| <span data-ttu-id="aae80-143">Требование</span><span class="sxs-lookup"><span data-stu-id="aae80-143">Requirement</span></span> | <span data-ttu-id="aae80-144">Значение</span><span class="sxs-lookup"><span data-stu-id="aae80-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae80-145">Header</span><span class="sxs-lookup"><span data-stu-id="aae80-145">Header</span></span><br/>  | <dl> <span data-ttu-id="aae80-146"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae80-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="aae80-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aae80-147">Library</span></span><br/> | <dl> <span data-ttu-id="aae80-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aae80-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aae80-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae80-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae80-150">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="aae80-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
