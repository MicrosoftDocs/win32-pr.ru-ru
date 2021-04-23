---
description: Загружает ряд символов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: 'ID3DXFont: метод:P Релоадчарактерс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713963"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="1206d-103">ID3DXFont: метод:P Релоадчарактерс</span><span class="sxs-lookup"><span data-stu-id="1206d-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="1206d-104">Загружает ряд символов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1206d-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1206d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1206d-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="1206d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1206d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1206d-107">*Сначала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1206d-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1206d-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1206d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1206d-109">Идентификатор первого символа, загружаемого в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="1206d-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="1206d-110">*Последний раз* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1206d-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1206d-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1206d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1206d-112">Идентификатор последнего символа, который должен быть загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="1206d-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1206d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1206d-113">Return value</span></span>

<span data-ttu-id="1206d-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1206d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1206d-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1206d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1206d-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1206d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1206d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1206d-117">Remarks</span></span>

<span data-ttu-id="1206d-118">Этот метод создает текстуры, содержащие глифы, представляющие входные символы.</span><span class="sxs-lookup"><span data-stu-id="1206d-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="1206d-119">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="1206d-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="1206d-120">Символы не будут подготавливаться к просмотру на устройстве; Для визуализации символов необходимо по-прежнему вызывать [**DrawText**](id3dxfont--drawtext.md) .</span><span class="sxs-lookup"><span data-stu-id="1206d-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="1206d-121">Однако при предварительной загрузке символов в видеопамять **DrawText** будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="1206d-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="1206d-122">Этот метод внутренне преобразует символы в глифы с помощью функции GDI [**жетчарактерплацемент**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="1206d-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="1206d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1206d-123">Requirements</span></span>



| <span data-ttu-id="1206d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1206d-124">Requirement</span></span> | <span data-ttu-id="1206d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1206d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1206d-126">Header</span><span class="sxs-lookup"><span data-stu-id="1206d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1206d-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1206d-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1206d-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1206d-128">Library</span></span><br/> | <dl> <span data-ttu-id="1206d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1206d-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1206d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1206d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1206d-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="1206d-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
