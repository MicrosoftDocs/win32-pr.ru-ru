---
description: Получение имен образцов, на которые имеются ссылки в шейдере.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Функция D3DXGetShaderSamplers (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713663"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="604af-103">Функция D3DXGetShaderSamplers</span><span class="sxs-lookup"><span data-stu-id="604af-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="604af-104">Получение имен образцов, на которые имеются ссылки в шейдере.</span><span class="sxs-lookup"><span data-stu-id="604af-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="604af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="604af-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="604af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="604af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604af-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="604af-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="604af-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="604af-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="604af-109">Указатель на поток функции шейдера DWORD.</span><span class="sxs-lookup"><span data-stu-id="604af-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="604af-110">*псамплерс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="604af-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="604af-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="604af-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="604af-112">Указатель на массив Лпкстрс.</span><span class="sxs-lookup"><span data-stu-id="604af-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="604af-113">Функция будет заполнять этот массив указателями на имена образцов, содержащихся в *пфунктион*.</span><span class="sxs-lookup"><span data-stu-id="604af-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="604af-114">Максимальный размер массива — это максимальное количество регистров образцов (16 для VS \_ 3 \_ 0 и PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="604af-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="604af-115">Чтобы узнать число используемых проб, проверьте *pCount* после вызова **D3DXGetShaderSamplers** с псамплерс = **null**.</span><span class="sxs-lookup"><span data-stu-id="604af-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="604af-116">*pCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="604af-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="604af-117">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="604af-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="604af-118">Возвращает число образцов, на которые ссылается шейдер.</span><span class="sxs-lookup"><span data-stu-id="604af-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604af-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="604af-119">Return value</span></span>

<span data-ttu-id="604af-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="604af-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="604af-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="604af-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="604af-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="604af-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="604af-123">Требования</span><span class="sxs-lookup"><span data-stu-id="604af-123">Requirements</span></span>



| <span data-ttu-id="604af-124">Требование</span><span class="sxs-lookup"><span data-stu-id="604af-124">Requirement</span></span> | <span data-ttu-id="604af-125">Значение</span><span class="sxs-lookup"><span data-stu-id="604af-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="604af-126">Header</span><span class="sxs-lookup"><span data-stu-id="604af-126">Header</span></span><br/>  | <dl> <span data-ttu-id="604af-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="604af-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="604af-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="604af-128">Library</span></span><br/> | <dl> <span data-ttu-id="604af-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="604af-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="604af-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="604af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604af-131">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="604af-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
