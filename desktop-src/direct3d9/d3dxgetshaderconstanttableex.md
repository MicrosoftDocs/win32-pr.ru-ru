---
description: Функция D3DXGetShaderConstantTableEx — получает таблицу-константу шейдера, внедренную в шейдер.
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Функция D3DXGetShaderConstantTableEx (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114434"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="9b9a8-103">Функция D3DXGetShaderConstantTableEx</span><span class="sxs-lookup"><span data-stu-id="9b9a8-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="9b9a8-104">Возвращает таблицу-константу шейдера, внедренную в шейдер.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b9a8-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="9b9a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b9a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b9a8-107">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b9a8-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9a8-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b9a8-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b9a8-109">Указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a8-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b9a8-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9a8-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b9a8-112">Используйте флаг D3DXCONSTTABLE \_ LARGEADDRESSAWARE, чтобы получить доступ к 4 ГБ виртуального адресного пространства (а не по умолчанию — 2 ГБ).</span><span class="sxs-lookup"><span data-stu-id="9b9a8-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="9b9a8-113">Если дополнительного виртуального адресного пространства не требуется, используйте [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a8-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="9b9a8-114">*ппконстанттабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b9a8-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9a8-115">Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b9a8-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="9b9a8-116">Возвращает интерфейс таблицы констант (см. [**ID3DXConstantTable**](id3dxconstanttable.md)), который управляет таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b9a8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b9a8-117">Return value</span></span>

<span data-ttu-id="9b9a8-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b9a8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b9a8-119">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b9a8-120">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b9a8-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b9a8-121">Remarks</span></span>

<span data-ttu-id="9b9a8-122">Таблица констант создается [**D3DXCompileShader**](d3dxcompileshader.md) и внедряется в текст шейдера.</span><span class="sxs-lookup"><span data-stu-id="9b9a8-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9a8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9b9a8-123">Requirements</span></span>



| <span data-ttu-id="9b9a8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9b9a8-124">Requirement</span></span> | <span data-ttu-id="9b9a8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9a8-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9a8-126">Header</span><span class="sxs-lookup"><span data-stu-id="9b9a8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9b9a8-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9a8-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9b9a8-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b9a8-128">Library</span></span><br/> | <dl> <span data-ttu-id="9b9a8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b9a8-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9b9a8-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9b9a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9a8-131">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="9b9a8-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
