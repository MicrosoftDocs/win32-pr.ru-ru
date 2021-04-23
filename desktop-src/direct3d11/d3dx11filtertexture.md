---
title: Функция D3DX11FilterTexture (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Женератемипмапс и GenerateMipMaps3D. Создает цепочку mipmap с помощью определенного фильтра текстуры.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987008"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="89355-106">Функция D3DX11FilterTexture</span><span class="sxs-lookup"><span data-stu-id="89355-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="89355-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="89355-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="89355-108">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **женератемипмапс** и **GenerateMipMaps3D**.</span><span class="sxs-lookup"><span data-stu-id="89355-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="89355-109">Создает цепочку mipmap с помощью определенного фильтра текстуры.</span><span class="sxs-lookup"><span data-stu-id="89355-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="89355-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89355-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="89355-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="89355-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89355-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="89355-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="89355-113">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="89355-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="89355-114">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="89355-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="89355-115">*птекстуре*</span><span class="sxs-lookup"><span data-stu-id="89355-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="89355-116">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="89355-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="89355-117">Объект текстуры для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="89355-117">The texture object to be filtered.</span></span> <span data-ttu-id="89355-118">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="89355-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="89355-119">*срклевел*</span><span class="sxs-lookup"><span data-stu-id="89355-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="89355-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="89355-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="89355-121">Уровень mipmap, данные которого используются для создания оставшейся части цепочки mipmap.</span><span class="sxs-lookup"><span data-stu-id="89355-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="89355-122">*мипфилтер*</span><span class="sxs-lookup"><span data-stu-id="89355-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="89355-123">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="89355-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="89355-124">Флаги, управляющие фильтрацией каждого миплевел (или D3DX11 \_ по умолчанию для \_ \_ линейного фильтра D3DX11).</span><span class="sxs-lookup"><span data-stu-id="89355-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="89355-125">См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="89355-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89355-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89355-126">Return value</span></span>

<span data-ttu-id="89355-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89355-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89355-128">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="89355-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89355-129">Требования</span><span class="sxs-lookup"><span data-stu-id="89355-129">Requirements</span></span>



| <span data-ttu-id="89355-130">Требование</span><span class="sxs-lookup"><span data-stu-id="89355-130">Requirement</span></span> | <span data-ttu-id="89355-131">Значение</span><span class="sxs-lookup"><span data-stu-id="89355-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89355-132">Header</span><span class="sxs-lookup"><span data-stu-id="89355-132">Header</span></span><br/>  | <dl> <span data-ttu-id="89355-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="89355-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="89355-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89355-134">Library</span></span><br/> | <dl> <span data-ttu-id="89355-135"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89355-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="89355-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89355-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89355-137">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="89355-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

