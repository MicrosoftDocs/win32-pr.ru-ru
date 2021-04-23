---
description: Возвращает размер байтового кода шейдера в байтах.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Функция D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713662"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="3f34a-103">Функция D3DXGetShaderSize</span><span class="sxs-lookup"><span data-stu-id="3f34a-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="3f34a-104">Возвращает размер байтового кода шейдера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3f34a-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f34a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f34a-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="3f34a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f34a-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f34a-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f34a-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f34a-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f34a-109">Указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="3f34a-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f34a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f34a-110">Return value</span></span>

<span data-ttu-id="3f34a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f34a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f34a-112">Возвращает размер байтового кода шейдера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3f34a-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f34a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3f34a-113">Requirements</span></span>



| <span data-ttu-id="3f34a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3f34a-114">Requirement</span></span> | <span data-ttu-id="3f34a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3f34a-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f34a-116">Header</span><span class="sxs-lookup"><span data-stu-id="3f34a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3f34a-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f34a-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3f34a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f34a-118">Library</span></span><br/> | <dl> <span data-ttu-id="3f34a-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f34a-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3f34a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f34a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f34a-121">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="3f34a-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
