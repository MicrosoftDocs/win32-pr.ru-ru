---
description: Задает таблицу констант с данными в буфере.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'Метод ID3DXTextureShader:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664957"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="42fcd-103">Метод ID3DXTextureShader:: SetValue</span><span class="sxs-lookup"><span data-stu-id="42fcd-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="42fcd-104">Задает таблицу констант с данными в буфере.</span><span class="sxs-lookup"><span data-stu-id="42fcd-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fcd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42fcd-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="42fcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42fcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fcd-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42fcd-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fcd-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="42fcd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="42fcd-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="42fcd-109">Unique identifier to a constant.</span></span> <span data-ttu-id="42fcd-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="42fcd-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="42fcd-111">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42fcd-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fcd-112">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42fcd-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42fcd-113">Указатель на буфер, содержащий постоянные данные.</span><span class="sxs-lookup"><span data-stu-id="42fcd-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="42fcd-114">*Байт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42fcd-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fcd-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42fcd-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42fcd-116">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="42fcd-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fcd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42fcd-117">Return value</span></span>

<span data-ttu-id="42fcd-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42fcd-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42fcd-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="42fcd-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42fcd-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="42fcd-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fcd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="42fcd-121">Requirements</span></span>



| <span data-ttu-id="42fcd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="42fcd-122">Requirement</span></span> | <span data-ttu-id="42fcd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="42fcd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42fcd-124">Header</span><span class="sxs-lookup"><span data-stu-id="42fcd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="42fcd-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="42fcd-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="42fcd-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42fcd-126">Library</span></span><br/> | <dl> <span data-ttu-id="42fcd-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42fcd-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="42fcd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42fcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fcd-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="42fcd-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
