---
description: Создает цепочку mipmap с помощью определенного фильтра текстуры.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Функция D3DX10FilterTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703635"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="31bb5-103">Функция D3DX10FilterTexture</span><span class="sxs-lookup"><span data-stu-id="31bb5-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="31bb5-104">Создает цепочку mipmap с помощью определенного фильтра текстуры.</span><span class="sxs-lookup"><span data-stu-id="31bb5-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="31bb5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31bb5-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="31bb5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31bb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31bb5-107">*птекстуре*</span><span class="sxs-lookup"><span data-stu-id="31bb5-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="31bb5-108">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="31bb5-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="31bb5-109">Объект текстуры для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="31bb5-109">The texture object to be filtered.</span></span> <span data-ttu-id="31bb5-110">См. [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="31bb5-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="31bb5-111">*срклевел*</span><span class="sxs-lookup"><span data-stu-id="31bb5-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="31bb5-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31bb5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31bb5-113">Уровень mipmap, данные которого используются для создания оставшейся части цепочки mipmap.</span><span class="sxs-lookup"><span data-stu-id="31bb5-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="31bb5-114">*мипфилтер*</span><span class="sxs-lookup"><span data-stu-id="31bb5-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="31bb5-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31bb5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31bb5-116">Флаги, управляющие фильтрацией каждого миплевел (или D3DX10 \_ умолчанию для D3DX10 \_ \_ поле фильтра).</span><span class="sxs-lookup"><span data-stu-id="31bb5-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="31bb5-117">См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="31bb5-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31bb5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31bb5-118">Return value</span></span>

<span data-ttu-id="31bb5-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31bb5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31bb5-120">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="31bb5-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31bb5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="31bb5-121">Requirements</span></span>



| <span data-ttu-id="31bb5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="31bb5-122">Requirement</span></span> | <span data-ttu-id="31bb5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="31bb5-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bb5-124">Header</span><span class="sxs-lookup"><span data-stu-id="31bb5-124">Header</span></span><br/> | <dl> <span data-ttu-id="31bb5-125"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="31bb5-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31bb5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31bb5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bb5-127">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="31bb5-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
