---
description: Задайте данные индекса сетки.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'Метод ID3DX10Mesh:: Сетиндексдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713843"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="14c7e-103">Метод ID3DX10Mesh:: Сетиндексдата</span><span class="sxs-lookup"><span data-stu-id="14c7e-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="14c7e-104">Задайте данные индекса сетки.</span><span class="sxs-lookup"><span data-stu-id="14c7e-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14c7e-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="14c7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c7e-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14c7e-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c7e-108">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="14c7e-108">Type: **const void\***</span></span>

<span data-ttu-id="14c7e-109">Данные индекса.</span><span class="sxs-lookup"><span data-stu-id="14c7e-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="14c7e-110">*Циндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14c7e-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c7e-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14c7e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14c7e-112">Число индексов в pData.</span><span class="sxs-lookup"><span data-stu-id="14c7e-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c7e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14c7e-113">Return value</span></span>

<span data-ttu-id="14c7e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14c7e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14c7e-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="14c7e-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14c7e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="14c7e-116">Requirements</span></span>



| <span data-ttu-id="14c7e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="14c7e-117">Requirement</span></span> | <span data-ttu-id="14c7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="14c7e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14c7e-119">Header</span><span class="sxs-lookup"><span data-stu-id="14c7e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="14c7e-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c7e-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="14c7e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14c7e-121">Library</span></span><br/> | <dl> <span data-ttu-id="14c7e-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c7e-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c7e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14c7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c7e-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="14c7e-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="14c7e-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="14c7e-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
