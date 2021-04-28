---
description: Функция D3DXCreateMesh — создает объект сетки с помощью декларатора.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Функция D3DXCreateMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c7e1c0d626c74f5427f91a5b9eb796e3b79d5a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102762"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="bad78-103">Функция D3DXCreateMesh</span><span class="sxs-lookup"><span data-stu-id="bad78-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="bad78-104">Создает объект сетки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="bad78-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bad78-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="bad78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bad78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad78-107">*Нумфацес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bad78-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bad78-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bad78-109">Число граней для сетки.</span><span class="sxs-lookup"><span data-stu-id="bad78-109">Number of faces for the mesh.</span></span> <span data-ttu-id="bad78-110">Допустимый диапазон для этого числа больше 0 и один меньше максимального значения DWORD (обычно 65534), так как последний индекс зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="bad78-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bad78-111">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bad78-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bad78-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bad78-113">Число вершин для сетки.</span><span class="sxs-lookup"><span data-stu-id="bad78-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="bad78-114">Этот параметр должен быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="bad78-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="bad78-115">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bad78-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-116">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bad78-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bad78-117">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) с указанием параметров для сетки.</span><span class="sxs-lookup"><span data-stu-id="bad78-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bad78-118">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bad78-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-119">Тип: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="bad78-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="bad78-120">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="bad78-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="bad78-121">Этот параметр должен быть напрямую сопоставлен с гибким форматом вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="bad78-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="bad78-122">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bad78-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-123">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bad78-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bad78-124">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связываемый с сеткой.</span><span class="sxs-lookup"><span data-stu-id="bad78-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bad78-125">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bad78-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bad78-126">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="bad78-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="bad78-127">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий созданный объект сетки.</span><span class="sxs-lookup"><span data-stu-id="bad78-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad78-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bad78-128">Return value</span></span>

<span data-ttu-id="bad78-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bad78-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bad78-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bad78-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bad78-131">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bad78-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad78-132">Требования</span><span class="sxs-lookup"><span data-stu-id="bad78-132">Requirements</span></span>



| <span data-ttu-id="bad78-133">Требование</span><span class="sxs-lookup"><span data-stu-id="bad78-133">Requirement</span></span> | <span data-ttu-id="bad78-134">Значение</span><span class="sxs-lookup"><span data-stu-id="bad78-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bad78-135">Header</span><span class="sxs-lookup"><span data-stu-id="bad78-135">Header</span></span><br/>  | <dl> <span data-ttu-id="bad78-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad78-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bad78-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bad78-137">Library</span></span><br/> | <dl> <span data-ttu-id="bad78-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bad78-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bad78-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bad78-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad78-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="bad78-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="bad78-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="bad78-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
