---
description: Создает объект шейдера текстуры из скомпилированного шейдера.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Функция D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354903"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="b21e7-103">Функция D3DXCreateTextureShader</span><span class="sxs-lookup"><span data-stu-id="b21e7-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="b21e7-104">Создает объект шейдера текстуры из скомпилированного шейдера.</span><span class="sxs-lookup"><span data-stu-id="b21e7-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b21e7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="b21e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b21e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21e7-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b21e7-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21e7-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b21e7-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b21e7-109">Указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="b21e7-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="b21e7-110">*пптекстурешадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b21e7-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b21e7-111">Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="b21e7-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="b21e7-112">Возвращает объект [**ID3DXTextureShader**](id3dxtextureshader.md) , который можно использовать для процедурного заполнения содержимого текстуры с помощью функций [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .</span><span class="sxs-lookup"><span data-stu-id="b21e7-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b21e7-113">Return value</span></span>

<span data-ttu-id="b21e7-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b21e7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b21e7-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b21e7-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b21e7-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b21e7-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21e7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b21e7-117">Requirements</span></span>



| <span data-ttu-id="b21e7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b21e7-118">Requirement</span></span> | <span data-ttu-id="b21e7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b21e7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21e7-120">Header</span><span class="sxs-lookup"><span data-stu-id="b21e7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b21e7-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b21e7-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b21e7-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b21e7-122">Library</span></span><br/> | <dl> <span data-ttu-id="b21e7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b21e7-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b21e7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b21e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21e7-125">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="b21e7-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
