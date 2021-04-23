---
description: Расформирование результата.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Функция D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703793"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="98f1f-103">Функция D3DXDisassembleEffect</span><span class="sxs-lookup"><span data-stu-id="98f1f-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="98f1f-104">Расформирование результата.</span><span class="sxs-lookup"><span data-stu-id="98f1f-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98f1f-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="98f1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98f1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f1f-107">*пеффект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98f1f-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f1f-108">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="98f1f-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="98f1f-109">Указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) , который содержит результат.</span><span class="sxs-lookup"><span data-stu-id="98f1f-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="98f1f-110">*Енаблеколоркоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98f1f-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f1f-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98f1f-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98f1f-112">Включите выделение цветом, чтобы облегчить чтение дизассемблированного кода.</span><span class="sxs-lookup"><span data-stu-id="98f1f-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="98f1f-113">*ппдисассембли* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="98f1f-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98f1f-114">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="98f1f-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="98f1f-115">Возвращает буфер, содержащий десобранный шейдер.</span><span class="sxs-lookup"><span data-stu-id="98f1f-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="98f1f-116">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="98f1f-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f1f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98f1f-117">Return value</span></span>

<span data-ttu-id="98f1f-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98f1f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98f1f-119">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="98f1f-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98f1f-120">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="98f1f-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f1f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="98f1f-121">Requirements</span></span>



| <span data-ttu-id="98f1f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="98f1f-122">Requirement</span></span> | <span data-ttu-id="98f1f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="98f1f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f1f-124">Header</span><span class="sxs-lookup"><span data-stu-id="98f1f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="98f1f-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="98f1f-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="98f1f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98f1f-126">Library</span></span><br/> | <dl> <span data-ttu-id="98f1f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98f1f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="98f1f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98f1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f1f-129">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="98f1f-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
