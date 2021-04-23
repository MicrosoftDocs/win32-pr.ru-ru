---
description: Возвращает индекс образца.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'Метод ID3DXConstantTable:: Жетсамплериндекс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713735"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a><span data-ttu-id="66fac-103">Метод ID3DXConstantTable:: Жетсамплериндекс</span><span class="sxs-lookup"><span data-stu-id="66fac-103">ID3DXConstantTable::GetSamplerIndex method</span></span>

<span data-ttu-id="66fac-104">Возвращает индекс образца.</span><span class="sxs-lookup"><span data-stu-id="66fac-104">Returns the sampler index.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66fac-105">Syntax</span></span>


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a><span data-ttu-id="66fac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66fac-107">*хконстант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="66fac-107">*hConstant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66fac-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="66fac-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="66fac-109">Маркер образца.</span><span class="sxs-lookup"><span data-stu-id="66fac-109">The sampler handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66fac-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66fac-110">Return value</span></span>

<span data-ttu-id="66fac-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66fac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66fac-112">Возвращает номер индекса образца выборки из таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="66fac-112">Returns the sampler index number from the constant table.</span></span>

## <a name="requirements"></a><span data-ttu-id="66fac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="66fac-113">Requirements</span></span>



| <span data-ttu-id="66fac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="66fac-114">Requirement</span></span> | <span data-ttu-id="66fac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="66fac-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fac-116">Header</span><span class="sxs-lookup"><span data-stu-id="66fac-116">Header</span></span><br/>  | <dl> <span data-ttu-id="66fac-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fac-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="66fac-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66fac-118">Library</span></span><br/> | <dl> <span data-ttu-id="66fac-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66fac-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="66fac-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66fac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fac-121">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="66fac-121">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
