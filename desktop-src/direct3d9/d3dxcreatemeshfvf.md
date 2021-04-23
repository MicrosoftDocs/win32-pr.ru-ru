---
description: Создает объект сетки, используя код гибкого формата вершин (ФВФ).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: Функция D3DXCreateMeshFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694309"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="d9b3a-103">Функция D3DXCreateMeshFVF</span><span class="sxs-lookup"><span data-stu-id="d9b3a-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="d9b3a-104">Создает объект сетки, используя код гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="d9b3a-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9b3a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d9b3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b3a-107">*Нумфацес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9b3a-109">Число граней для сетки.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-109">Number of faces for the mesh.</span></span> <span data-ttu-id="d9b3a-110">Допустимый диапазон для этого числа больше 0 и один меньше, чем максимальное значение DWORD, обычно 2 ³ ²-1, так как последний индекс зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3a-111">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9b3a-113">Число вершин для сетки.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="d9b3a-114">Этот параметр должен быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3a-115">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-116">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9b3a-117">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , в котором указываются параметры создания сетки.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3a-118">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9b3a-120">Сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="d9b3a-121">Эта функция не поддерживает D3DFVF \_ ксизрхв.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3a-122">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-123">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d9b3a-124">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связываемый с сеткой.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3a-125">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9b3a-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b3a-126">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9b3a-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d9b3a-127">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий созданный объект сетки.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b3a-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9b3a-128">Return value</span></span>

<span data-ttu-id="d9b3a-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9b3a-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9b3a-131">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d9b3a-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b3a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d9b3a-132">Requirements</span></span>



| <span data-ttu-id="d9b3a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d9b3a-133">Requirement</span></span> | <span data-ttu-id="d9b3a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b3a-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b3a-135">Header</span><span class="sxs-lookup"><span data-stu-id="d9b3a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b3a-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b3a-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d9b3a-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9b3a-137">Library</span></span><br/> | <dl> <span data-ttu-id="d9b3a-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9b3a-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9b3a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9b3a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b3a-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="d9b3a-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d9b3a-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="d9b3a-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
