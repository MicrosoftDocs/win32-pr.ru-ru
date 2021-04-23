---
description: Создает сетку из сетки контрольных исправлений.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Функция D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355860"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="afc70-103">Функция D3DXCreatePatchMesh</span><span class="sxs-lookup"><span data-stu-id="afc70-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="afc70-104">Создает сетку из сетки контрольных исправлений.</span><span class="sxs-lookup"><span data-stu-id="afc70-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afc70-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="afc70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="afc70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc70-107">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-108">Тип: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="afc70-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="afc70-109">Структура сведений об исправлении.</span><span class="sxs-lookup"><span data-stu-id="afc70-109">Patch information structure.</span></span> <span data-ttu-id="afc70-110">Дополнительные сведения см. в разделе [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="afc70-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="afc70-111">*двнумпатчес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afc70-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afc70-113">Число исправлений.</span><span class="sxs-lookup"><span data-stu-id="afc70-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="afc70-114">*двнумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afc70-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afc70-116">Число вершин управления в данном исправлении.</span><span class="sxs-lookup"><span data-stu-id="afc70-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="afc70-117">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-118">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afc70-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afc70-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="afc70-119">Unused.</span></span> <span data-ttu-id="afc70-120">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="afc70-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="afc70-121">*пдекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-122">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="afc70-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="afc70-123">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="afc70-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="afc70-124">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afc70-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-125">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="afc70-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="afc70-126">Указатель устройства, создающего сетку исправлений.</span><span class="sxs-lookup"><span data-stu-id="afc70-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="afc70-127">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="afc70-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="afc70-128">*ппатчмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="afc70-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc70-129">Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="afc70-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="afc70-130">Указатель на созданный объект [**ID3DXPatchMesh**](id3dxpatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="afc70-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc70-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afc70-131">Return value</span></span>

<span data-ttu-id="afc70-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="afc70-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="afc70-133">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="afc70-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="afc70-134">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="afc70-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc70-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afc70-135">Remarks</span></span>

<span data-ttu-id="afc70-136">Этот метод принимает сетку входного исправления и преобразует ее в тесселяцию сетки.</span><span class="sxs-lookup"><span data-stu-id="afc70-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="afc70-137">В сетчатых обновлениях используются 16-битные буферы индексов.</span><span class="sxs-lookup"><span data-stu-id="afc70-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="afc70-138">Таким образом, индексы для [**локкиндексбуффер**](id3dxpatchmesh--lockindexbuffer.md) являются 16 битами.</span><span class="sxs-lookup"><span data-stu-id="afc70-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc70-139">Требования</span><span class="sxs-lookup"><span data-stu-id="afc70-139">Requirements</span></span>



| <span data-ttu-id="afc70-140">Требование</span><span class="sxs-lookup"><span data-stu-id="afc70-140">Requirement</span></span> | <span data-ttu-id="afc70-141">Значение</span><span class="sxs-lookup"><span data-stu-id="afc70-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc70-142">Header</span><span class="sxs-lookup"><span data-stu-id="afc70-142">Header</span></span><br/>  | <dl> <span data-ttu-id="afc70-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc70-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="afc70-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="afc70-144">Library</span></span><br/> | <dl> <span data-ttu-id="afc70-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afc70-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afc70-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afc70-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc70-147">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="afc70-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="afc70-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="afc70-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
