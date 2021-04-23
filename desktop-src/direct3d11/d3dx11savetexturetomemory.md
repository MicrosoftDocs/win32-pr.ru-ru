---
title: Функция D3DX11SaveTextureToMemory (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Каптуретекстуре затем Саветоксксксмемори (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Сохранение текстуры в памяти.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273890"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="e8efc-106">Функция D3DX11SaveTextureToMemory</span><span class="sxs-lookup"><span data-stu-id="e8efc-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="e8efc-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="e8efc-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8efc-108">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **каптуретекстуре** затем **саветоксксксмемори** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).</span><span class="sxs-lookup"><span data-stu-id="e8efc-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="e8efc-109">Сохранение текстуры в памяти.</span><span class="sxs-lookup"><span data-stu-id="e8efc-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8efc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8efc-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e8efc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8efc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8efc-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="e8efc-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="e8efc-113">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="e8efc-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="e8efc-114">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="e8efc-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="e8efc-115">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8efc-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8efc-116">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="e8efc-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="e8efc-117">Указатель на текстуру, которую необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="e8efc-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="e8efc-118">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="e8efc-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="e8efc-119">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8efc-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8efc-120">Тип: **[ **D3DX11 \_ image \_ File \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="e8efc-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="e8efc-121">Формат текстуры будет сохранен как.</span><span class="sxs-lookup"><span data-stu-id="e8efc-121">The format the texture will be saved as.</span></span> <span data-ttu-id="e8efc-122">См. раздел [**\_ \_ \_ Формат файла изображения D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e8efc-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8efc-123">*ппдестбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8efc-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8efc-124">Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="e8efc-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="e8efc-125">Адрес указателя на память, содержащую сохраненную текстуру.</span><span class="sxs-lookup"><span data-stu-id="e8efc-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="e8efc-126">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8efc-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8efc-127">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8efc-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8efc-128">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e8efc-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8efc-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8efc-129">Return value</span></span>

<span data-ttu-id="e8efc-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8efc-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8efc-131">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e8efc-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8efc-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e8efc-132">Requirements</span></span>



| <span data-ttu-id="e8efc-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e8efc-133">Requirement</span></span> | <span data-ttu-id="e8efc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e8efc-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8efc-135">Header</span><span class="sxs-lookup"><span data-stu-id="e8efc-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e8efc-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8efc-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e8efc-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8efc-137">Library</span></span><br/> | <dl> <span data-ttu-id="e8efc-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8efc-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e8efc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8efc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8efc-140">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="e8efc-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

