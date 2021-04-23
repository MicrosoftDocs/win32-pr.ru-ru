---
description: Доступ к описанию вершины, переданному в D3DX10CreateMesh. Описание вершины описывает макет буферов вершин сетки.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'Метод ID3DX10Mesh:: Жетвертексдескриптион (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000373"
---
# <a name="id3dx10meshgetvertexdescription-method"></a><span data-ttu-id="c0b59-104">Метод ID3DX10Mesh:: Жетвертексдескриптион</span><span class="sxs-lookup"><span data-stu-id="c0b59-104">ID3DX10Mesh::GetVertexDescription method</span></span>

<span data-ttu-id="c0b59-105">Доступ к описанию вершины, переданному в [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span><span class="sxs-lookup"><span data-stu-id="c0b59-105">Access the vertex description passed into [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span></span> <span data-ttu-id="c0b59-106">Описание вершины описывает макет буферов вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="c0b59-106">The vertex description describes the layout of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0b59-107">Syntax</span></span>


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a><span data-ttu-id="c0b59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0b59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b59-109">*ппдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c0b59-109">*ppDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b59-110">Type: **const [**D3D10 \_ входного \_ элемента \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***</span><span class="sxs-lookup"><span data-stu-id="c0b59-110">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\*\***</span></span>

<span data-ttu-id="c0b59-111">Массив входных элементов, описывающих макет буферов вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="c0b59-111">Array of input elements that describe the layout of the mesh's vertex buffers.</span></span> <span data-ttu-id="c0b59-112">См [**. \_ элемент D3D10 input \_ element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="c0b59-112">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="c0b59-113">*пдеклкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0b59-113">*pDeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b59-114">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0b59-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c0b59-115">Количество входных элементов в Ппдеск.</span><span class="sxs-lookup"><span data-stu-id="c0b59-115">The number of input elements in ppDesc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b59-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-116">Return value</span></span>

<span data-ttu-id="c0b59-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0b59-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0b59-118">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c0b59-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b59-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c0b59-119">Requirements</span></span>



| <span data-ttu-id="c0b59-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c0b59-120">Requirement</span></span> | <span data-ttu-id="c0b59-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b59-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b59-122">Header</span><span class="sxs-lookup"><span data-stu-id="c0b59-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c0b59-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0b59-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0b59-124">Library</span></span><br/> | <dl> <span data-ttu-id="c0b59-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b59-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b59-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0b59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b59-127">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="c0b59-127">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="c0b59-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c0b59-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
