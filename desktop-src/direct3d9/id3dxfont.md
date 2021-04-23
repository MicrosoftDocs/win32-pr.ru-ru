---
description: Интерфейс ID3DXFont инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Интерфейс ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694302"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="879a0-103">Интерфейс ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="879a0-103">ID3DXFont interface</span></span>

<span data-ttu-id="879a0-104">Интерфейс ID3DXFont инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="879a0-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="879a0-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="879a0-105">Members</span></span>

<span data-ttu-id="879a0-106">Интерфейс **ID3DXFont** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="879a0-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="879a0-107">**ID3DXFont** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="879a0-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="879a0-108">Методы</span><span class="sxs-lookup"><span data-stu-id="879a0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="879a0-109">Методы</span><span class="sxs-lookup"><span data-stu-id="879a0-109">Methods</span></span>

<span data-ttu-id="879a0-110">Интерфейс **ID3DXFont** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="879a0-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="879a0-111">Метод</span><span class="sxs-lookup"><span data-stu-id="879a0-111">Method</span></span>                                                    | <span data-ttu-id="879a0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="879a0-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="879a0-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="879a0-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="879a0-114">Рисует форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="879a0-114">Draws formatted text.</span></span> <span data-ttu-id="879a0-115">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="879a0-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="879a0-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="879a0-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="879a0-117">Возвращает маркер для контекста дисплея устройства (DC) с набором шрифтов.</span><span class="sxs-lookup"><span data-stu-id="879a0-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="879a0-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="879a0-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="879a0-119">Возвращает описание текущего объекта Font.</span><span class="sxs-lookup"><span data-stu-id="879a0-119">Gets a description of the current font object.</span></span> <span data-ttu-id="879a0-120">Жетдескв и DESC идентичны этому методу, за исключением того, что указатель возвращается в структуру [**D3DXFONT \_ Дескв**](d3dxfont-desc.md) или **D3DXFONT \_ DESC** соответственно.</span><span class="sxs-lookup"><span data-stu-id="879a0-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="879a0-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="879a0-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="879a0-122">Извлекает устройство Direct3D, связанное с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="879a0-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="879a0-123">**жетглифдата**</span><span class="sxs-lookup"><span data-stu-id="879a0-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="879a0-124">Возвращает сведения о размещении и ориентации глифа в ячейке символов.</span><span class="sxs-lookup"><span data-stu-id="879a0-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="879a0-125">**жеттекстметрикс**</span><span class="sxs-lookup"><span data-stu-id="879a0-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="879a0-126">Получает характеристики шрифта, определенные в структуре [**текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="879a0-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="879a0-127">Этот метод поддерживает параметры компилятора ANSI и Unicode.</span><span class="sxs-lookup"><span data-stu-id="879a0-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="879a0-128">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="879a0-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="879a0-129">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="879a0-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="879a0-130">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="879a0-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="879a0-131">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="879a0-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="879a0-132">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="879a0-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="879a0-133">**прелоадчарактерс**</span><span class="sxs-lookup"><span data-stu-id="879a0-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="879a0-134">Загружает ряд символов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="879a0-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="879a0-135">**прелоадглифс**</span><span class="sxs-lookup"><span data-stu-id="879a0-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="879a0-136">Загружает ряд глифов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="879a0-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="879a0-137">**прелоадтекст**</span><span class="sxs-lookup"><span data-stu-id="879a0-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="879a0-138">Загружает форматированный текст в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="879a0-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="879a0-139">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="879a0-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="879a0-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="879a0-140">Remarks</span></span>

<span data-ttu-id="879a0-141">Интерфейс **ID3DXFont** получается путем вызова [**D3DXCreateFont**](d3dxcreatefont.md) или [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="879a0-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="879a0-142">Тип LPD3DXFONT определяется как указатель на интерфейс **ID3DXFont** .</span><span class="sxs-lookup"><span data-stu-id="879a0-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="879a0-143">Требования</span><span class="sxs-lookup"><span data-stu-id="879a0-143">Requirements</span></span>



| <span data-ttu-id="879a0-144">Требование</span><span class="sxs-lookup"><span data-stu-id="879a0-144">Requirement</span></span> | <span data-ttu-id="879a0-145">Значение</span><span class="sxs-lookup"><span data-stu-id="879a0-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="879a0-146">Header</span><span class="sxs-lookup"><span data-stu-id="879a0-146">Header</span></span><br/>  | <dl> <span data-ttu-id="879a0-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="879a0-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="879a0-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="879a0-148">Library</span></span><br/> | <dl> <span data-ttu-id="879a0-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="879a0-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="879a0-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="879a0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879a0-151">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="879a0-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
