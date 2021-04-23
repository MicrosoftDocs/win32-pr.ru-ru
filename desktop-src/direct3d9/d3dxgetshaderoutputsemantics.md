---
description: Получение семантики для всех выходных элементов шейдера.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Функция D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547895"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="2082c-103">Функция D3DXGetShaderOutputSemantics</span><span class="sxs-lookup"><span data-stu-id="2082c-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="2082c-104">Получение семантики для всех выходных элементов шейдера.</span><span class="sxs-lookup"><span data-stu-id="2082c-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2082c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2082c-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="2082c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2082c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2082c-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2082c-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2082c-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2082c-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2082c-109">Указатель на поток функции шейдера DWORD.</span><span class="sxs-lookup"><span data-stu-id="2082c-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="2082c-110">*псемантикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2082c-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2082c-111">Тип: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="2082c-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="2082c-112">Указатель на массив структур [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="2082c-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="2082c-113">Функция будет заполнять этот массив семантикой для каждого выходного элемента, на который ссылается шейдер.</span><span class="sxs-lookup"><span data-stu-id="2082c-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="2082c-114">Предполагается, что этот массив содержит по крайней мере элементы MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="2082c-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="2082c-115">Однако вызов **D3DXGetShaderOutputSemantics** с Псемантикс = **null** возвратит количество элементов, необходимых для pCount.</span><span class="sxs-lookup"><span data-stu-id="2082c-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="2082c-116">*pCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2082c-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2082c-117">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2082c-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2082c-118">Возвращает количество элементов в Псемантикс.</span><span class="sxs-lookup"><span data-stu-id="2082c-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2082c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2082c-119">Return value</span></span>

<span data-ttu-id="2082c-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2082c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2082c-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2082c-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2082c-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2082c-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2082c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2082c-123">Requirements</span></span>



| <span data-ttu-id="2082c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2082c-124">Requirement</span></span> | <span data-ttu-id="2082c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2082c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2082c-126">Header</span><span class="sxs-lookup"><span data-stu-id="2082c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2082c-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2082c-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2082c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2082c-128">Library</span></span><br/> | <dl> <span data-ttu-id="2082c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2082c-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2082c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2082c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2082c-131">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="2082c-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
