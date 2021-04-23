---
description: Задайте значение произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'Метод ID3DXBaseEffect:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157215"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="21848-103">Метод ID3DXBaseEffect:: SetValue</span><span class="sxs-lookup"><span data-stu-id="21848-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="21848-104">Задайте значение произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры.</span><span class="sxs-lookup"><span data-stu-id="21848-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="21848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21848-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="21848-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21848-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21848-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21848-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21848-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="21848-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="21848-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="21848-109">Unique identifier.</span></span> <span data-ttu-id="21848-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="21848-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="21848-111">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21848-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21848-112">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21848-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21848-113">Указатель на буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="21848-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="21848-114">*Байт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21848-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21848-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21848-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21848-116">\[в \] байтах в буфере.</span><span class="sxs-lookup"><span data-stu-id="21848-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="21848-117">\_Если вы уверены, что размер буфера достаточно велик, чтобы вместить весь параметр, и вы хотите пропустить проверку размера, передайте значение D3DX по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21848-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21848-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21848-118">Return value</span></span>

<span data-ttu-id="21848-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21848-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21848-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="21848-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21848-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="21848-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21848-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21848-122">Remarks</span></span>

<span data-ttu-id="21848-123">Этот метод можно использовать вместо почти всех вызовов API набора эффектов.</span><span class="sxs-lookup"><span data-stu-id="21848-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="21848-124">Требования</span><span class="sxs-lookup"><span data-stu-id="21848-124">Requirements</span></span>



| <span data-ttu-id="21848-125">Требование</span><span class="sxs-lookup"><span data-stu-id="21848-125">Requirement</span></span> | <span data-ttu-id="21848-126">Значение</span><span class="sxs-lookup"><span data-stu-id="21848-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21848-127">Header</span><span class="sxs-lookup"><span data-stu-id="21848-127">Header</span></span><br/>  | <dl> <span data-ttu-id="21848-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="21848-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="21848-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21848-129">Library</span></span><br/> | <dl> <span data-ttu-id="21848-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21848-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21848-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21848-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21848-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="21848-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="21848-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="21848-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
