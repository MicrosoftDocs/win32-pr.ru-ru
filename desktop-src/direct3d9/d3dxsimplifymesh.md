---
description: Формирует упрощенную сетку, используя указанные весовые коэффициенты, которые максимально близко к данному MinValue.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Функция D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713641"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="8d131-103">Функция D3DXSimplifyMesh</span><span class="sxs-lookup"><span data-stu-id="8d131-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="8d131-104">Формирует упрощенную сетку, используя указанные весовые коэффициенты, которые максимально близко к данному MinValue.</span><span class="sxs-lookup"><span data-stu-id="8d131-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d131-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d131-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8d131-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d131-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8d131-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8d131-109">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий исходную сетку.</span><span class="sxs-lookup"><span data-stu-id="8d131-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-110">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-111">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d131-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d131-112">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке, которую необходимо упростить.</span><span class="sxs-lookup"><span data-stu-id="8d131-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-113">*пвертексаттрибутевеигхтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-114">Тип: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d131-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="8d131-115">Указатель на структуру [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , содержащую вес для каждого компонента вершины.</span><span class="sxs-lookup"><span data-stu-id="8d131-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="8d131-116">Если этот параметр имеет значение **null**, используется структура по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d131-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="8d131-117">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="8d131-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-118">*пвертексвеигхтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d131-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d131-120">Указатель на массив весовых коэффициентов вершин.</span><span class="sxs-lookup"><span data-stu-id="8d131-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="8d131-121">Если этот параметр имеет значение **null**, все веса вершин имеют значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="8d131-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-122">*MinValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d131-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d131-124">Количество вершин или граней в зависимости от флага, установленного в параметре *Options* , с помощью которого можно упростить исходную сетку.</span><span class="sxs-lookup"><span data-stu-id="8d131-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-125">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d131-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d131-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d131-127">Задает параметры упрощения для сетки.</span><span class="sxs-lookup"><span data-stu-id="8d131-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="8d131-128">Можно задать один из флагов в [**D3DXMESHSIMP**](./d3dxmeshsimp.md) .</span><span class="sxs-lookup"><span data-stu-id="8d131-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="8d131-129">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d131-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d131-130">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d131-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8d131-131">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий возвращенную сетку упрощения.</span><span class="sxs-lookup"><span data-stu-id="8d131-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d131-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d131-132">Return value</span></span>

<span data-ttu-id="8d131-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d131-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d131-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8d131-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d131-135">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8d131-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d131-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d131-136">Remarks</span></span>

<span data-ttu-id="8d131-137">Эта функция создает сетку, которая содержит вершины или грани *MinValue* .</span><span class="sxs-lookup"><span data-stu-id="8d131-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="8d131-138">Если процесс упрощения не может сократить сетку до *MinValue*, вызов по-прежнему будет выполнен, так как значение *MinValue* является желаемым минимумом, а не абсолютным минимумом.</span><span class="sxs-lookup"><span data-stu-id="8d131-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="8d131-139">Если *пвертексаттрибутевеигхтс* имеет значение **null**, то структуре [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) по умолчанию присваиваются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8d131-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="8d131-140">Эта структура по умолчанию используется большинством приложений, так как она учитывает только геометрическую и нормальную корректировку.</span><span class="sxs-lookup"><span data-stu-id="8d131-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="8d131-141">В особых случаях необходимо изменить другие поля элементов.</span><span class="sxs-lookup"><span data-stu-id="8d131-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d131-142">Требования</span><span class="sxs-lookup"><span data-stu-id="8d131-142">Requirements</span></span>



| <span data-ttu-id="8d131-143">Требование</span><span class="sxs-lookup"><span data-stu-id="8d131-143">Requirement</span></span> | <span data-ttu-id="8d131-144">Значение</span><span class="sxs-lookup"><span data-stu-id="8d131-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d131-145">Header</span><span class="sxs-lookup"><span data-stu-id="8d131-145">Header</span></span><br/>  | <dl> <span data-ttu-id="8d131-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d131-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8d131-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d131-147">Library</span></span><br/> | <dl> <span data-ttu-id="8d131-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d131-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d131-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d131-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d131-150">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="8d131-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
