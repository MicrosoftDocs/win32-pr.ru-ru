---
description: Компиляция результата.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'Метод ID3DXEffectCompiler:: Компилиффект (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354350"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="5a1b3-103">Метод ID3DXEffectCompiler:: Компилиффект</span><span class="sxs-lookup"><span data-stu-id="5a1b3-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="5a1b3-104">Компиляция результата.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a1b3-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="5a1b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a1b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a1b3-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a1b3-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1b3-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a1b3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a1b3-109">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-109">Compile options identified by various flags.</span></span> <span data-ttu-id="5a1b3-110">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="5a1b3-111">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1b3-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="5a1b3-112">*ппеффект* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5a1b3-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1b3-113">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a1b3-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a1b3-114">Буфер, содержащий скомпилированный результат.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="5a1b3-115">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5a1b3-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a1b3-116">*пперрормсгс* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5a1b3-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1b3-117">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a1b3-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5a1b3-118">Буфер, содержащий по крайней мере первое сообщение об ошибке компиляции.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="5a1b3-119">Это относится к ошибкам компилятора и ошибкам при компиляции на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="5a1b3-120">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5a1b3-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a1b3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a1b3-121">Return value</span></span>

<span data-ttu-id="5a1b3-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a1b3-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a1b3-123">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="5a1b3-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="5a1b3-124">Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="5a1b3-125">Если метод завершается с ошибкой, возвращается значение E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="5a1b3-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1b3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5a1b3-126">Requirements</span></span>



| <span data-ttu-id="5a1b3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5a1b3-127">Requirement</span></span> | <span data-ttu-id="5a1b3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5a1b3-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1b3-129">Header</span><span class="sxs-lookup"><span data-stu-id="5a1b3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5a1b3-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b3-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5a1b3-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a1b3-131">Library</span></span><br/> | <dl> <span data-ttu-id="5a1b3-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b3-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5a1b3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a1b3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1b3-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="5a1b3-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
