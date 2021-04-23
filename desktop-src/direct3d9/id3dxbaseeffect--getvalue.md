---
description: Получение значения произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры. Этот метод можно использовать вместо почти всех вызовов Жеткскскс в ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'Метод ID3DXBaseEffect:: GetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703633"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="2271e-104">Метод ID3DXBaseEffect:: GetValue</span><span class="sxs-lookup"><span data-stu-id="2271e-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="2271e-105">Получение значения произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры.</span><span class="sxs-lookup"><span data-stu-id="2271e-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="2271e-106">Этот метод можно использовать вместо почти всех вызовов Жеткскскс в [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="2271e-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2271e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2271e-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="2271e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2271e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2271e-109">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2271e-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2271e-110">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2271e-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2271e-111">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2271e-111">Unique identifier.</span></span> <span data-ttu-id="2271e-112">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2271e-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2271e-113">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2271e-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2271e-114">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2271e-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2271e-115">Возвращает буфер, содержащий значение.</span><span class="sxs-lookup"><span data-stu-id="2271e-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="2271e-116">*Байт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2271e-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2271e-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2271e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2271e-118">\[в \] байтах в буфере.</span><span class="sxs-lookup"><span data-stu-id="2271e-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="2271e-119">\_Если вы уверены, что размер буфера достаточно велик, чтобы вместить весь параметр, и вы хотите пропустить проверку размера, передайте значение D3DX по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2271e-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2271e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2271e-120">Return value</span></span>

<span data-ttu-id="2271e-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2271e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2271e-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2271e-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2271e-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2271e-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2271e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2271e-124">Requirements</span></span>



| <span data-ttu-id="2271e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2271e-125">Requirement</span></span> | <span data-ttu-id="2271e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2271e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2271e-127">Header</span><span class="sxs-lookup"><span data-stu-id="2271e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2271e-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2271e-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2271e-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2271e-129">Library</span></span><br/> | <dl> <span data-ttu-id="2271e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2271e-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2271e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2271e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2271e-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2271e-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2271e-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="2271e-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
