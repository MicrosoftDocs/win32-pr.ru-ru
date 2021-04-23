---
description: Задайте данные атрибутов сетки.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'Метод ID3DX10Mesh:: Сетаттрибутедата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273874"
---
# <a name="id3dx10meshsetattributedata-method"></a><span data-ttu-id="0402b-103">Метод ID3DX10Mesh:: Сетаттрибутедата</span><span class="sxs-lookup"><span data-stu-id="0402b-103">ID3DX10Mesh::SetAttributeData method</span></span>

<span data-ttu-id="0402b-104">Задайте данные атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="0402b-104">Set the mesh's attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0402b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0402b-105">Syntax</span></span>


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a><span data-ttu-id="0402b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0402b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0402b-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0402b-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0402b-108">Тип: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0402b-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0402b-109">Устанавливаемые данные атрибута.</span><span class="sxs-lookup"><span data-stu-id="0402b-109">The attribute data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0402b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0402b-110">Return value</span></span>

<span data-ttu-id="0402b-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0402b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0402b-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0402b-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0402b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0402b-113">Requirements</span></span>



| <span data-ttu-id="0402b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0402b-114">Requirement</span></span> | <span data-ttu-id="0402b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0402b-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0402b-116">Header</span><span class="sxs-lookup"><span data-stu-id="0402b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0402b-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0402b-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0402b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0402b-118">Library</span></span><br/> | <dl> <span data-ttu-id="0402b-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0402b-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0402b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0402b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0402b-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="0402b-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="0402b-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="0402b-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
