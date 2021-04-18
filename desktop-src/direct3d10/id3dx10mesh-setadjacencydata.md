---
description: Задайте данные о смежности сетки.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'Метод ID3DX10Mesh:: Сетаджаценцидата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713845"
---
# <a name="id3dx10meshsetadjacencydata-method"></a><span data-ttu-id="2dbed-103">Метод ID3DX10Mesh:: Сетаджаценцидата</span><span class="sxs-lookup"><span data-stu-id="2dbed-103">ID3DX10Mesh::SetAdjacencyData method</span></span>

<span data-ttu-id="2dbed-104">Задайте данные о смежности сетки.</span><span class="sxs-lookup"><span data-stu-id="2dbed-104">Set the mesh's adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dbed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dbed-105">Syntax</span></span>


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="2dbed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dbed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dbed-107">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dbed-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dbed-108">Тип: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2dbed-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2dbed-109">Заданные соседства.</span><span class="sxs-lookup"><span data-stu-id="2dbed-109">The adjacency data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dbed-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dbed-110">Return value</span></span>

<span data-ttu-id="2dbed-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2dbed-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2dbed-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2dbed-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dbed-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2dbed-113">Requirements</span></span>



| <span data-ttu-id="2dbed-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2dbed-114">Requirement</span></span> | <span data-ttu-id="2dbed-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2dbed-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbed-116">Header</span><span class="sxs-lookup"><span data-stu-id="2dbed-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2dbed-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dbed-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dbed-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2dbed-118">Library</span></span><br/> | <dl> <span data-ttu-id="2dbed-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dbed-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dbed-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dbed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbed-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2dbed-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2dbed-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="2dbed-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
