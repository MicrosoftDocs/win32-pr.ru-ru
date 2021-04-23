---
description: Расформирование шейдера.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Функция D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694162"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="cd2f7-103">Функция D3DXDisassembleShader</span><span class="sxs-lookup"><span data-stu-id="cd2f7-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="cd2f7-104">Расформирование шейдера.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="cd2f7-105">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="cd2f7-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cd2f7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd2f7-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="cd2f7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd2f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2f7-108">*пшадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd2f7-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2f7-109">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd2f7-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd2f7-110">Указатель на буфер памяти, содержащий данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="cd2f7-111">*Енаблеколоркоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd2f7-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2f7-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2f7-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2f7-113">Включите код цвета, чтобы упростить чтение дизассемблированного кода.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="cd2f7-114">*пкомментс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd2f7-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2f7-115">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2f7-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2f7-116">Необязательная строка комментария, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="cd2f7-117">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2f7-118">*ппдисассембли* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cd2f7-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2f7-119">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd2f7-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cd2f7-120">Возвращает буфер, содержащий десобранный шейдер.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="cd2f7-121">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cd2f7-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2f7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd2f7-122">Return value</span></span>

<span data-ttu-id="cd2f7-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd2f7-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd2f7-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd2f7-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cd2f7-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2f7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cd2f7-126">Requirements</span></span>



| <span data-ttu-id="cd2f7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cd2f7-127">Requirement</span></span> | <span data-ttu-id="cd2f7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2f7-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2f7-129">Header</span><span class="sxs-lookup"><span data-stu-id="cd2f7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cd2f7-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2f7-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cd2f7-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd2f7-131">Library</span></span><br/> | <dl> <span data-ttu-id="cd2f7-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd2f7-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cd2f7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd2f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2f7-134">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="cd2f7-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
