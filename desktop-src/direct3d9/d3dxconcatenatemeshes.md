---
description: Объединяет группу сеток в одну общую сеть. Этот метод может при необходимости применить преобразование матрицы к каждой входной сетке и ее координатам текстуры.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Функция D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694211"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="81f33-104">Функция D3DXConcatenateMeshes</span><span class="sxs-lookup"><span data-stu-id="81f33-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="81f33-105">Объединяет группу сеток в одну общую сеть.</span><span class="sxs-lookup"><span data-stu-id="81f33-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="81f33-106">Этот метод может при необходимости применить преобразование матрицы к каждой входной сетке и ее координатам текстуры.</span><span class="sxs-lookup"><span data-stu-id="81f33-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81f33-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="81f33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81f33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f33-109">*ппмешес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="81f33-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="81f33-111">Массив указателей входной сетки (см. [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="81f33-112">Число элементов в массиве — Нуммешес.</span><span class="sxs-lookup"><span data-stu-id="81f33-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-113">*Нуммешес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81f33-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81f33-115">Количество входных сеток для сцепления.</span><span class="sxs-lookup"><span data-stu-id="81f33-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-116">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81f33-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81f33-118">Параметры создания сетки; Это сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="81f33-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="81f33-119">Параметры создания сетки эквивалентны параметрам Options, необходимым для [**D3DXCreateMesh**](d3dxcreatemesh.md).</span><span class="sxs-lookup"><span data-stu-id="81f33-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f33-120">*пжеомксформс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-121">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81f33-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81f33-122">Необязательный массив преобразований Geometry.</span><span class="sxs-lookup"><span data-stu-id="81f33-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="81f33-123">Число элементов в массиве — Нуммешес; Каждый элемент является матрицей преобразования (см. [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="81f33-124">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="81f33-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-125">*птекстурексформс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-126">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81f33-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81f33-127">Необязательный массив преобразований текстур.</span><span class="sxs-lookup"><span data-stu-id="81f33-127">Optional array of texture transforms.</span></span> <span data-ttu-id="81f33-128">Число элементов в массиве — Нуммешес; Каждый элемент является матрицей преобразования (см. [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="81f33-129">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="81f33-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-130">*пдекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-131">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="81f33-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="81f33-132">Необязательный указатель на объявление вершины (см. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="81f33-133">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="81f33-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-134">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81f33-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-135">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="81f33-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="81f33-136">Указатель на устройство [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , которое используется для создания новой сетки.</span><span class="sxs-lookup"><span data-stu-id="81f33-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="81f33-137">*ппмешаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81f33-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81f33-138">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="81f33-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="81f33-139">Адрес указателя на созданную сетку (см. [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f33-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81f33-140">Return value</span></span>

<span data-ttu-id="81f33-141">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81f33-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81f33-142">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="81f33-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81f33-143">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="81f33-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f33-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81f33-144">Remarks</span></span>

<span data-ttu-id="81f33-145">Если [объявление вершины](vertex-declaration.md) не указано в параметре создания сетки параметров, метод создаст объединение всех объявлений вершин подсетей, продвижение каналов и типов при необходимости.</span><span class="sxs-lookup"><span data-stu-id="81f33-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="81f33-146">Метод создаст таблицу атрибутов из таблиц атрибутов входных сеток.</span><span class="sxs-lookup"><span data-stu-id="81f33-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="81f33-147">Чтобы обеспечить создание таблицы атрибутов, вызовите [**optimize**](id3dxmesh--optimize.md) с флагами, установленными в D3DXMESHOPT \_ Compact и D3DXMESHOPT \_ Аттрсорт (см. [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="81f33-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="81f33-148">Требования</span><span class="sxs-lookup"><span data-stu-id="81f33-148">Requirements</span></span>



| <span data-ttu-id="81f33-149">Требование</span><span class="sxs-lookup"><span data-stu-id="81f33-149">Requirement</span></span> | <span data-ttu-id="81f33-150">Значение</span><span class="sxs-lookup"><span data-stu-id="81f33-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81f33-151">Header</span><span class="sxs-lookup"><span data-stu-id="81f33-151">Header</span></span><br/>  | <dl> <span data-ttu-id="81f33-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f33-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="81f33-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81f33-153">Library</span></span><br/> | <dl> <span data-ttu-id="81f33-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81f33-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81f33-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81f33-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f33-156">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="81f33-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
