---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры Куба.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Функция D3DXFillCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694154"
---
# <a name="d3dxfillcubetexture-function"></a><span data-ttu-id="14e46-103">Функция D3DXFillCubeTexture</span><span class="sxs-lookup"><span data-stu-id="14e46-103">D3DXFillCubeTexture function</span></span>

<span data-ttu-id="14e46-104">Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="14e46-104">Uses a user-provided function to fill each texel of each mip level of a given cube texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14e46-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a><span data-ttu-id="14e46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14e46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e46-107">*птекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14e46-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14e46-108">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="14e46-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="14e46-109">Указатель на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий текстуру с заливкой.</span><span class="sxs-lookup"><span data-stu-id="14e46-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="14e46-110">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14e46-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e46-111">Тип: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="14e46-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="14e46-112">Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="14e46-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="14e46-113">Функция соответствует прототипу [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="14e46-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="14e46-114">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14e46-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e46-115">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14e46-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14e46-116">Указатель на произвольный блок определяемых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="14e46-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="14e46-117">Этот указатель будет передан функции, предоставленной в *пфунктион*.</span><span class="sxs-lookup"><span data-stu-id="14e46-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e46-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14e46-118">Return value</span></span>

<span data-ttu-id="14e46-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14e46-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14e46-120">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="14e46-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14e46-121">Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="14e46-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e46-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14e46-122">Remarks</span></span>

<span data-ttu-id="14e46-123">Ниже приведен пример, в котором создается функция с именем Колоркубефилл, которая основывается на D3DXFillCubeTexture.</span><span class="sxs-lookup"><span data-stu-id="14e46-123">Here is an example that creates a function called ColorCubeFill, which relies on D3DXFillCubeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="14e46-124">Требования</span><span class="sxs-lookup"><span data-stu-id="14e46-124">Requirements</span></span>



| <span data-ttu-id="14e46-125">Требование</span><span class="sxs-lookup"><span data-stu-id="14e46-125">Requirement</span></span> | <span data-ttu-id="14e46-126">Значение</span><span class="sxs-lookup"><span data-stu-id="14e46-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14e46-127">Header</span><span class="sxs-lookup"><span data-stu-id="14e46-127">Header</span></span><br/>  | <dl> <span data-ttu-id="14e46-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e46-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="14e46-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14e46-129">Library</span></span><br/> | <dl> <span data-ttu-id="14e46-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14e46-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="14e46-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14e46-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e46-132">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="14e46-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
