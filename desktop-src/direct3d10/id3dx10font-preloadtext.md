---
description: Загрузка форматированного текста в видеопамять для повышения эффективности отрисовки на устройстве. Этот метод поддерживает строки ANSI и Юникод.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: 'ID3DX10Font: метод:P Релоадтекст (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273797"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="c969d-104">ID3DX10Font: метод:P Релоадтекст</span><span class="sxs-lookup"><span data-stu-id="c969d-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="c969d-105">Загрузка форматированного текста в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="c969d-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="c969d-106">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="c969d-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="c969d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c969d-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="c969d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c969d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c969d-109">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c969d-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c969d-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c969d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c969d-111">Указатель на строку символов, которая должна быть загружена в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="c969d-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="c969d-112">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР; в противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c969d-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="c969d-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c969d-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c969d-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c969d-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c969d-115">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c969d-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c969d-116">Число символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="c969d-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c969d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c969d-117">Return value</span></span>

<span data-ttu-id="c969d-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c969d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c969d-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c969d-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c969d-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c969d-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c969d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c969d-121">Remarks</span></span>

<span data-ttu-id="c969d-122">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="c969d-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c969d-123">Если определен Юникод, вызов функции разрешается в Прелоадтекств.</span><span class="sxs-lookup"><span data-stu-id="c969d-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="c969d-124">В противном случае вызов функции разрешается в Прелоадтекста, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="c969d-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="c969d-125">Этот метод создает текстуры, которые содержат глифы, представляющие входной текст.</span><span class="sxs-lookup"><span data-stu-id="c969d-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="c969d-126">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="c969d-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="c969d-127">Текст не будет отображаться на устройстве; ID3DX10Font: для отрисовки текста необходимо по-прежнему вызывать метод:D Равтекст.</span><span class="sxs-lookup"><span data-stu-id="c969d-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="c969d-128">Однако при предварительной загрузке текста в видеопамять ID3DX10Font::D Равтекст будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="c969d-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="c969d-129">Этот метод внутренне преобразует символы в глифы с помощью функции GDI [жетчарактерплацемент](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c969d-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c969d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c969d-130">Requirements</span></span>



| <span data-ttu-id="c969d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c969d-131">Requirement</span></span> | <span data-ttu-id="c969d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c969d-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c969d-133">Header</span><span class="sxs-lookup"><span data-stu-id="c969d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c969d-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c969d-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c969d-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c969d-135">Library</span></span><br/> | <dl> <span data-ttu-id="c969d-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c969d-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c969d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c969d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c969d-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="c969d-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="c969d-139">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c969d-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
