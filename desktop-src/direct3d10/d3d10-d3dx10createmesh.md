---
description: Создает объект сетки с помощью декларатора.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Функция D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685009"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="930c7-103">Функция D3DX10CreateMesh</span><span class="sxs-lookup"><span data-stu-id="930c7-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="930c7-104">Создает объект сетки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="930c7-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="930c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="930c7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="930c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="930c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930c7-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="930c7-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="930c7-109">Указатель на [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), объект устройства, связываемый с сеткой.</span><span class="sxs-lookup"><span data-stu-id="930c7-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-110">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-111">Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="930c7-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="930c7-112">Массив элементов [**D3D10 \_ \_ элемента ввода \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , описывающих формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="930c7-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="930c7-113">Этот параметр должен быть напрямую сопоставлен с гибким форматом вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="930c7-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="930c7-114">*Деклкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="930c7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="930c7-116">Число элементов в Пдекларатион.</span><span class="sxs-lookup"><span data-stu-id="930c7-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-117">*ппоситионсемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-118">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="930c7-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="930c7-119">Семантика, определяющая, какая часть объявления вершины содержит сведения о положении.</span><span class="sxs-lookup"><span data-stu-id="930c7-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-120">*Вертекскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="930c7-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="930c7-122">Число вершин для сетки.</span><span class="sxs-lookup"><span data-stu-id="930c7-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="930c7-123">Этот параметр должен быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="930c7-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-124">*Фацекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-125">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="930c7-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="930c7-126">Число граней для сетки.</span><span class="sxs-lookup"><span data-stu-id="930c7-126">Number of faces for the mesh.</span></span> <span data-ttu-id="930c7-127">Допустимый диапазон для этого числа больше 0 и один меньше максимального значения DWORD (обычно 65534), так как последний индекс зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="930c7-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-128">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="930c7-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="930c7-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="930c7-130">Сочетание одного или нескольких флагов из [**\_ сетки D3DX10**](d3dx10-mesh.md), указывая параметры сетки.</span><span class="sxs-lookup"><span data-stu-id="930c7-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="930c7-131">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="930c7-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="930c7-132">Тип: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="930c7-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="930c7-133">Адрес указателя на [**интерфейс ID3DX10Mesh**](id3dx10mesh.md), представляющий созданный объект сетки.</span><span class="sxs-lookup"><span data-stu-id="930c7-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930c7-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="930c7-134">Return value</span></span>

<span data-ttu-id="930c7-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="930c7-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="930c7-136">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="930c7-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="930c7-137">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="930c7-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="930c7-138">Требования</span><span class="sxs-lookup"><span data-stu-id="930c7-138">Requirements</span></span>



| <span data-ttu-id="930c7-139">Требование</span><span class="sxs-lookup"><span data-stu-id="930c7-139">Requirement</span></span> | <span data-ttu-id="930c7-140">Значение</span><span class="sxs-lookup"><span data-stu-id="930c7-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="930c7-141">Header</span><span class="sxs-lookup"><span data-stu-id="930c7-141">Header</span></span><br/>  | <dl> <span data-ttu-id="930c7-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="930c7-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="930c7-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="930c7-143">Library</span></span><br/> | <dl> <span data-ttu-id="930c7-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="930c7-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="930c7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="930c7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930c7-146">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="930c7-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="930c7-147">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="930c7-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
