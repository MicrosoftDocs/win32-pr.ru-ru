---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя для каждого уровня MIP заданной текстуры тома.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Функция D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354860"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="c93ec-103">Функция D3DXFillVolumeTexture</span><span class="sxs-lookup"><span data-stu-id="c93ec-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="c93ec-104">Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя для каждого уровня MIP заданной текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="c93ec-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c93ec-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="c93ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c93ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93ec-107">*птекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c93ec-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ec-108">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c93ec-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="c93ec-109">Указатель на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий текстуру с заливкой.</span><span class="sxs-lookup"><span data-stu-id="c93ec-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="c93ec-110">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c93ec-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ec-111">Тип: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="c93ec-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="c93ec-112">Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c93ec-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="c93ec-113">Функция соответствует прототипу [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="c93ec-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93ec-114">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c93ec-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ec-115">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c93ec-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c93ec-116">Указатель на произвольный блок определяемых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="c93ec-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="c93ec-117">Этот указатель будет передан функции, предоставленной в *пфунктион*.</span><span class="sxs-lookup"><span data-stu-id="c93ec-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93ec-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c93ec-118">Return value</span></span>

<span data-ttu-id="c93ec-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c93ec-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c93ec-120">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c93ec-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c93ec-121">Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c93ec-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93ec-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c93ec-122">Remarks</span></span>

<span data-ttu-id="c93ec-123">Если том не является динамическим (поскольку при его создании используется значение 0) и находится в видеопамяти (пул памяти со значением D3DPOOL \_ по умолчанию), **D3DXFillVolumeTexture** не удастся, так как том не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c93ec-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="c93ec-124">В этом примере создается функция с именем Колорволумефилл, которая основывается на D3DXFillVolumeTexture.</span><span class="sxs-lookup"><span data-stu-id="c93ec-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c93ec-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c93ec-125">Requirements</span></span>



| <span data-ttu-id="c93ec-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c93ec-126">Requirement</span></span> | <span data-ttu-id="c93ec-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c93ec-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c93ec-128">Header</span><span class="sxs-lookup"><span data-stu-id="c93ec-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c93ec-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93ec-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c93ec-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c93ec-130">Library</span></span><br/> | <dl> <span data-ttu-id="c93ec-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c93ec-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c93ec-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c93ec-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93ec-133">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c93ec-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
