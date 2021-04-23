---
description: Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: 'ID3DX10Font: метод:P Релоадглифс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703800"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="585c1-103">ID3DX10Font: метод:P Релоадглифс</span><span class="sxs-lookup"><span data-stu-id="585c1-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="585c1-104">Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="585c1-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="585c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="585c1-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="585c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="585c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585c1-107">*Сначала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="585c1-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="585c1-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585c1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="585c1-109">Идентификатор первого глифа, который будет загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="585c1-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="585c1-110">*Последний раз* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="585c1-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="585c1-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585c1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="585c1-112">Идентификатор последнего глифа, который будет загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="585c1-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="585c1-113">Return value</span></span>

<span data-ttu-id="585c1-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="585c1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="585c1-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="585c1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="585c1-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="585c1-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="585c1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="585c1-117">Remarks</span></span>

<span data-ttu-id="585c1-118">Этот метод создает текстуры, которые содержат глифы входных данных.</span><span class="sxs-lookup"><span data-stu-id="585c1-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="585c1-119">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="585c1-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="585c1-120">Глифы не будут отображаться на устройстве; ID3DX10Font: для отрисовки глифов необходимо по-прежнему вызывать метод:D Равтекст.</span><span class="sxs-lookup"><span data-stu-id="585c1-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="585c1-121">Однако предварительная загрузка глифов в видеопамять ID3DX10Font::D Равтекст будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="585c1-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="585c1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="585c1-122">Requirements</span></span>



| <span data-ttu-id="585c1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="585c1-123">Requirement</span></span> | <span data-ttu-id="585c1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="585c1-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="585c1-125">Header</span><span class="sxs-lookup"><span data-stu-id="585c1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="585c1-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="585c1-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="585c1-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="585c1-127">Library</span></span><br/> | <dl> <span data-ttu-id="585c1-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="585c1-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="585c1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="585c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585c1-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="585c1-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="585c1-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="585c1-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
