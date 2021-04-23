---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Функция D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354863"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="0842d-103">Функция D3DXFillTexture</span><span class="sxs-lookup"><span data-stu-id="0842d-103">D3DXFillTexture function</span></span>

<span data-ttu-id="0842d-104">Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры.</span><span class="sxs-lookup"><span data-stu-id="0842d-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0842d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0842d-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="0842d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0842d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0842d-107">*птекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0842d-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0842d-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0842d-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0842d-109">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру с заливкой.</span><span class="sxs-lookup"><span data-stu-id="0842d-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="0842d-110">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0842d-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0842d-111">Тип: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="0842d-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="0842d-112">Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="0842d-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="0842d-113">Функция соответствует прототипу [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="0842d-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="0842d-114">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0842d-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0842d-115">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0842d-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0842d-116">Указатель на произвольный блок определяемых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="0842d-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="0842d-117">Этот указатель будет передан функции, предоставленной в *пфунктион*.</span><span class="sxs-lookup"><span data-stu-id="0842d-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0842d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0842d-118">Return value</span></span>

<span data-ttu-id="0842d-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0842d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0842d-120">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0842d-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0842d-121">Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0842d-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0842d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0842d-122">Remarks</span></span>

<span data-ttu-id="0842d-123">Ниже приведен пример, в котором создается функция с именем Колорфилл, которая основывается на D3DXFillTexture.</span><span class="sxs-lookup"><span data-stu-id="0842d-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0842d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0842d-124">Requirements</span></span>



| <span data-ttu-id="0842d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0842d-125">Requirement</span></span> | <span data-ttu-id="0842d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0842d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0842d-127">Header</span><span class="sxs-lookup"><span data-stu-id="0842d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0842d-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0842d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0842d-129">Library</span></span><br/> | <dl> <span data-ttu-id="0842d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0842d-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0842d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0842d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0842d-132">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0842d-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
