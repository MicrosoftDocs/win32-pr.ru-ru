---
description: Создает объект Font. Примечание. вместо использования этой функции рекомендуется использовать DirectWrite и библиотеку Директкстк, класс Спритефонт.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Функция D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354483"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="43cb6-103">Функция D3DX10CreateFontIndirect</span><span class="sxs-lookup"><span data-stu-id="43cb6-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="43cb6-104">Создает объект Font.</span><span class="sxs-lookup"><span data-stu-id="43cb6-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="43cb6-105">Вместо использования этой функции рекомендуется использовать [DirectWrite](../directwrite/direct-write-portal.md) и библиотеку [Директкстк](https://github.com/Microsoft/DirectXTK) , класс **спритефонт** .</span><span class="sxs-lookup"><span data-stu-id="43cb6-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="43cb6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43cb6-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="43cb6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43cb6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cb6-108">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43cb6-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cb6-109">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="43cb6-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="43cb6-110">Указатель на интерфейс интерфейса [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="43cb6-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="43cb6-111">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43cb6-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cb6-112">Тип: **const [**D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="43cb6-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="43cb6-113">Указатель на [**D3DX10 структуру \_ шрифта \_**](d3dx10-font-desc.md) с описанием атрибутов создаваемого объекта Font.</span><span class="sxs-lookup"><span data-stu-id="43cb6-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="43cb6-114">Если определен Юникод, вызов функции разрешается в D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="43cb6-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="43cb6-115">В противном случае вызов функции разрешается в D3DXCreateFontIndirectA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="43cb6-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="43cb6-116">*ппфонт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43cb6-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cb6-117">Тип: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="43cb6-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="43cb6-118">Возвращает указатель на [**интерфейс ID3DX10Font**](id3dx10font.md).</span><span class="sxs-lookup"><span data-stu-id="43cb6-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cb6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43cb6-119">Return value</span></span>

<span data-ttu-id="43cb6-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43cb6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43cb6-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="43cb6-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43cb6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="43cb6-122">Requirements</span></span>



| <span data-ttu-id="43cb6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="43cb6-123">Requirement</span></span> | <span data-ttu-id="43cb6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43cb6-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43cb6-125">Header</span><span class="sxs-lookup"><span data-stu-id="43cb6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="43cb6-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="43cb6-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="43cb6-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43cb6-127">Library</span></span><br/> | <dl> <span data-ttu-id="43cb6-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43cb6-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43cb6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43cb6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cb6-130">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="43cb6-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
