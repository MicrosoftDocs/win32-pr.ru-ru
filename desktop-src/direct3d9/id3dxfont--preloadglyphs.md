---
description: Загружает ряд глифов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont: метод:P Релоадглифс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081940"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="3016a-103">ID3DXFont: метод:P Релоадглифс</span><span class="sxs-lookup"><span data-stu-id="3016a-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="3016a-104">Загружает ряд глифов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3016a-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3016a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3016a-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="3016a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3016a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3016a-107">*Сначала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3016a-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3016a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3016a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3016a-109">Идентификатор первого глифа, который будет загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="3016a-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="3016a-110">*Последний раз* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3016a-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3016a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3016a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3016a-112">Идентификатор последнего глифа, который будет загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="3016a-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3016a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3016a-113">Return value</span></span>

<span data-ttu-id="3016a-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3016a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3016a-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="3016a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3016a-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="3016a-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="3016a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3016a-117">Remarks</span></span>

<span data-ttu-id="3016a-118">Этот метод создает текстуры, которые содержат глифы входных данных.</span><span class="sxs-lookup"><span data-stu-id="3016a-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="3016a-119">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="3016a-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="3016a-120">Глифы не будут отображаться на устройстве; Для отрисовки глифов необходимо по-прежнему вызывать [**DrawText**](id3dxfont--drawtext.md) .</span><span class="sxs-lookup"><span data-stu-id="3016a-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="3016a-121">Однако предварительная загрузка глифов в видеопамять **DrawText** будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="3016a-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="3016a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3016a-122">Requirements</span></span>



| <span data-ttu-id="3016a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3016a-123">Requirement</span></span> | <span data-ttu-id="3016a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3016a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3016a-125">Header</span><span class="sxs-lookup"><span data-stu-id="3016a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3016a-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3016a-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3016a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3016a-127">Library</span></span><br/> | <dl> <span data-ttu-id="3016a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3016a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3016a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3016a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3016a-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="3016a-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
