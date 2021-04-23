---
description: Возвращает версию шейдера скомпилированного шейдера.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Функция D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157183"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="d7337-103">Функция D3DXGetShaderVersion</span><span class="sxs-lookup"><span data-stu-id="d7337-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="d7337-104">Возвращает версию шейдера скомпилированного шейдера.</span><span class="sxs-lookup"><span data-stu-id="d7337-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7337-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7337-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="d7337-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7337-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7337-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7337-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7337-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7337-109">Указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="d7337-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7337-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7337-110">Return value</span></span>

<span data-ttu-id="d7337-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7337-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7337-112">Возвращает версию шейдера данного шейдера или нуль, если функция шейдера имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d7337-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7337-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d7337-113">Requirements</span></span>



| <span data-ttu-id="d7337-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d7337-114">Requirement</span></span> | <span data-ttu-id="d7337-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7337-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7337-116">Header</span><span class="sxs-lookup"><span data-stu-id="d7337-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d7337-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7337-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d7337-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7337-118">Library</span></span><br/> | <dl> <span data-ttu-id="d7337-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7337-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d7337-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7337-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7337-121">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="d7337-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
