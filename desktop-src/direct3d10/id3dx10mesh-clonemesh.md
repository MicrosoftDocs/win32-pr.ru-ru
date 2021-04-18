---
description: Создает новую сетку и заполняет ее данными ранее загруженной сетки.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Метод ID3DX10Mesh:: Клонемеш (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713851"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="121dc-103">Метод ID3DX10Mesh:: Клонемеш</span><span class="sxs-lookup"><span data-stu-id="121dc-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="121dc-104">Создает новую сетку и заполняет ее данными ранее загруженной сетки.</span><span class="sxs-lookup"><span data-stu-id="121dc-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="121dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="121dc-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="121dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="121dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="121dc-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="121dc-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="121dc-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="121dc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="121dc-109">Флаги создания, применяемые к новой сетке.</span><span class="sxs-lookup"><span data-stu-id="121dc-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="121dc-110">См. раздел [**\_ Сетка D3DX10**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="121dc-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="121dc-111">*ппоссемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="121dc-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="121dc-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="121dc-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="121dc-113">Семантическое имя для данных о положении.</span><span class="sxs-lookup"><span data-stu-id="121dc-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="121dc-114">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="121dc-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="121dc-115">Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="121dc-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="121dc-116">Массив \_ структуры входного \_ элемента D3D10 \_ , описывающий формат вершины для возвращенной сетки.</span><span class="sxs-lookup"><span data-stu-id="121dc-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="121dc-117">См [**. \_ элемент D3D10 input \_ element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="121dc-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="121dc-118">*Деклкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="121dc-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="121dc-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="121dc-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="121dc-120">Число элементов в массиве Пдеск.</span><span class="sxs-lookup"><span data-stu-id="121dc-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="121dc-121">*ппклонемеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="121dc-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="121dc-122">Тип: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="121dc-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="121dc-123">Новая сетка.</span><span class="sxs-lookup"><span data-stu-id="121dc-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="121dc-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="121dc-124">Return value</span></span>

<span data-ttu-id="121dc-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="121dc-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="121dc-126">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="121dc-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="121dc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="121dc-127">Requirements</span></span>



| <span data-ttu-id="121dc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="121dc-128">Requirement</span></span> | <span data-ttu-id="121dc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="121dc-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="121dc-130">Header</span><span class="sxs-lookup"><span data-stu-id="121dc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="121dc-131"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="121dc-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="121dc-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="121dc-132">Library</span></span><br/> | <dl> <span data-ttu-id="121dc-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="121dc-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121dc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="121dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121dc-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="121dc-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="121dc-136">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="121dc-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
