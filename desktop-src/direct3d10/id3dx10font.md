---
description: Интерфейс ID3DX10Font инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Интерфейс ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273798"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="4a7e1-103">Интерфейс ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="4a7e1-103">ID3DX10Font interface</span></span>

<span data-ttu-id="4a7e1-104">Интерфейс ID3DX10Font инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="4a7e1-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="4a7e1-105">Members</span></span>

<span data-ttu-id="4a7e1-106">Интерфейс **ID3DX10Font** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a7e1-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a7e1-107">**ID3DX10Font** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4a7e1-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="4a7e1-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4a7e1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a7e1-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4a7e1-109">Methods</span></span>

<span data-ttu-id="4a7e1-110">Интерфейс **ID3DX10Font** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="4a7e1-111">Метод</span><span class="sxs-lookup"><span data-stu-id="4a7e1-111">Method</span></span>                                                     | <span data-ttu-id="4a7e1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4a7e1-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a7e1-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="4a7e1-114">Рисование форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-114">Draw formatted text.</span></span> <span data-ttu-id="4a7e1-115">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="4a7e1-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="4a7e1-117">Возвращает маркер для контекста дисплея устройства (DC), для которого установлен шрифт.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="4a7e1-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="4a7e1-119">Получение описания текущего объекта Font.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4a7e1-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="4a7e1-121">Получите устройство Direct3D, связанное с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="4a7e1-122">**жетглифдата**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="4a7e1-123">Возвращает сведения о размещении и ориентации глифа в символьной ячейке.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="4a7e1-124">**жеттекстметрикс**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="4a7e1-125">Получение характеристик шрифта.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="4a7e1-126">**прелоадчарактерс**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="4a7e1-127">Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="4a7e1-128">**прелоадглифс**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="4a7e1-129">Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="4a7e1-130">**прелоадтекст**</span><span class="sxs-lookup"><span data-stu-id="4a7e1-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="4a7e1-131">Загрузка форматированного текста в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="4a7e1-132">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a7e1-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a7e1-133">Remarks</span></span>

<span data-ttu-id="4a7e1-134">Интерфейс ID3DX10Font получается путем вызова [**D3DX10CreateFont**](d3dx10createfont.md) или [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="4a7e1-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="4a7e1-135">Тип LPD3DX10FONT определяется как указатель на интерфейс ID3DX10Font.</span><span class="sxs-lookup"><span data-stu-id="4a7e1-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="4a7e1-136">Требования</span><span class="sxs-lookup"><span data-stu-id="4a7e1-136">Requirements</span></span>



| <span data-ttu-id="4a7e1-137">Требование</span><span class="sxs-lookup"><span data-stu-id="4a7e1-137">Requirement</span></span> | <span data-ttu-id="4a7e1-138">Значение</span><span class="sxs-lookup"><span data-stu-id="4a7e1-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7e1-139">Header</span><span class="sxs-lookup"><span data-stu-id="4a7e1-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4a7e1-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7e1-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a7e1-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a7e1-141">Library</span></span><br/> | <dl> <span data-ttu-id="4a7e1-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a7e1-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7e1-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a7e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7e1-144">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="4a7e1-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
