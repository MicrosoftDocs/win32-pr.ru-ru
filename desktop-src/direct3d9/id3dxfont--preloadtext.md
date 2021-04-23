---
description: Загружает форматированный текст в видеопамять для повышения эффективности отрисовки на устройстве. Этот метод поддерживает строки ANSI и Юникод.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: 'ID3DXFont: метод:P Релоадтекст (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157247"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="392e3-104">ID3DXFont: метод:P Релоадтекст</span><span class="sxs-lookup"><span data-stu-id="392e3-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="392e3-105">Загружает форматированный текст в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="392e3-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="392e3-106">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="392e3-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="392e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="392e3-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="392e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="392e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="392e3-109">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="392e3-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="392e3-110">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="392e3-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="392e3-111">Указатель на строку символов, которая должна быть загружена в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="392e3-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="392e3-112">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР; в противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="392e3-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="392e3-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="392e3-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="392e3-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="392e3-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="392e3-115">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="392e3-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="392e3-116">Число символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="392e3-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="392e3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="392e3-117">Return value</span></span>

<span data-ttu-id="392e3-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="392e3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="392e3-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="392e3-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="392e3-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="392e3-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="392e3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="392e3-121">Remarks</span></span>

<span data-ttu-id="392e3-122">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="392e3-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="392e3-123">Если определен Юникод, вызов функции разрешается в Прелоадтекств.</span><span class="sxs-lookup"><span data-stu-id="392e3-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="392e3-124">В противном случае вызов функции разрешается в Прелоадтекста, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="392e3-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="392e3-125">Этот метод создает текстуры, которые содержат глифы, представляющие входной текст.</span><span class="sxs-lookup"><span data-stu-id="392e3-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="392e3-126">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="392e3-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="392e3-127">Текст не будет отображаться на устройстве; Для отрисовки текста необходимо по-прежнему вызывать [**DrawText**](id3dxfont--drawtext.md) .</span><span class="sxs-lookup"><span data-stu-id="392e3-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="392e3-128">Однако при предварительной загрузке текста в видеопамять **DrawText** будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="392e3-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="392e3-129">Этот метод внутренне преобразует символы в глифы с помощью функции GDI [**жетчарактерплацемент**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="392e3-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="392e3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="392e3-130">Requirements</span></span>



| <span data-ttu-id="392e3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="392e3-131">Requirement</span></span> | <span data-ttu-id="392e3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="392e3-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="392e3-133">Header</span><span class="sxs-lookup"><span data-stu-id="392e3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="392e3-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="392e3-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="392e3-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="392e3-135">Library</span></span><br/> | <dl> <span data-ttu-id="392e3-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="392e3-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="392e3-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="392e3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392e3-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="392e3-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
