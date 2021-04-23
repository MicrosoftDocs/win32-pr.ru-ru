---
description: Рисование форматированного текста. Этот метод поддерживает строки ANSI и Юникод.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: 'ID3DX10Font: метод:D Равтекст (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694172"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="ed1d8-104">ID3DX10Font: метод:D Равтекст</span><span class="sxs-lookup"><span data-stu-id="ed1d8-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="ed1d8-105">Рисование форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-105">Draw formatted text.</span></span> <span data-ttu-id="ed1d8-106">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed1d8-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="ed1d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed1d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1d8-109">*псприте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-110">Тип: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="ed1d8-111">Указатель на объект ID3DX10Sprite, содержащий строку, которую необходимо нарисовать.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="ed1d8-112">Может иметь **значение NULL**, в этом случае Direct3D будет отображать строку с собственным объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="ed1d8-113">Чтобы повысить эффективность, необходимо указать объект Sprite, если ID3DX10Font::D Равтекст будет вызываться более одного раза в строке.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d8-114">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed1d8-116">Указатель на строку для рисования.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-116">Pointer to a string to draw.</span></span> <span data-ttu-id="ed1d8-117">Если определен Юникод, этот тип параметра разрешается в ЛПКВСТР, в противном случае тип разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="ed1d8-118">Если параметр count имеет значение-1, строка **должна завершаться нулем.**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d8-119">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-120">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed1d8-121">Количество знаков в строке.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-121">The number of characters in the string.</span></span> <span data-ttu-id="ed1d8-122">Если аргумент count имеет значение-1, то предполагается, что параметр Пстринг является указателем на спрайт, содержащий строку, завершающуюся нулем, и ID3DX10Font::D Равтекст автоматически вычислит число символов.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d8-123">*прект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-124">Тип: **лпрект**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-124">Type: **LPRECT**</span></span>

<span data-ttu-id="ed1d8-125">Указатель на структуру [Rect](/previous-versions//ms536136(v=vs.85)) , содержащую прямоугольник в логических координатах, в котором должен быть отформатирован текст.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="ed1d8-126">Как и в случае с любым объектом RECT, значение координаты правой стороны прямоугольника должно быть больше значения его левой стороны.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="ed1d8-127">Аналогично, значение координаты нижнего значения должно быть больше верхнего.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d8-128">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed1d8-130">Укажите метод форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="ed1d8-131">Это может быть любое сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ed1d8-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="ed1d8-132">Элемент</span><span class="sxs-lookup"><span data-stu-id="ed1d8-132">Item</span></span>                                                                                      | <span data-ttu-id="ed1d8-133">Описание</span><span class="sxs-lookup"><span data-stu-id="ed1d8-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1d8-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT, \_ Нижний</span><span class="sxs-lookup"><span data-stu-id="ed1d8-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="ed1d8-135">Выровнять текст по нижнему краю прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="ed1d8-136">Это значение должно сочетаться с DT \_ SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ed1d8-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ калкрект</span><span class="sxs-lookup"><span data-stu-id="ed1d8-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="ed1d8-138">Укажите DrawText, чтобы автоматически вычислить ширину и высоту прямоугольника на основе длины строки, которую он нарисует.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="ed1d8-139">Если имеется несколько строк текста, ID3DX10Font::D Равтекст использует ширину прямоугольника, на который указывает параметр прект, и расширяет основу прямоугольника, чтобы она была привязана к последней строке текста.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="ed1d8-140">Если имеется только одна строка текста, ID3DX10Font::D Равтекст изменяет правую часть прямоугольника таким образом, чтобы она была привязана к последнему символу в строке.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="ed1d8-141">В любом случае ID3DX10Font::D Равтекст Возвращает высоту форматированного текста, но не рисует текст.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="ed1d8-142"><span id="DT_CENTER"></span><span id="dt_center"></span>\_центр DT</span><span class="sxs-lookup"><span data-stu-id="ed1d8-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="ed1d8-143">Центрирование текста по горизонтали в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ed1d8-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ експандтабс</span><span class="sxs-lookup"><span data-stu-id="ed1d8-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="ed1d8-145">Развернуть символы табуляции.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-145">Expand tab characters.</span></span> <span data-ttu-id="ed1d8-146">По умолчанию количество символов на шаг табуляции равно восьми.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ed1d8-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ слева</span><span class="sxs-lookup"><span data-stu-id="ed1d8-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="ed1d8-148">Выровняйте текст по левому краю.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ed1d8-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT — \_ Clip</span><span class="sxs-lookup"><span data-stu-id="ed1d8-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="ed1d8-150">Рисование без усечения.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-150">Draw without clipping.</span></span> <span data-ttu-id="ed1d8-151">ID3DX10Font::D Равтекст несколько быстрее, когда используется "DT" \_ .</span><span class="sxs-lookup"><span data-stu-id="ed1d8-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ed1d8-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT, \_ вправо</span><span class="sxs-lookup"><span data-stu-id="ed1d8-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="ed1d8-153">Выровняйте текст по правому краю.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ed1d8-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING</span><span class="sxs-lookup"><span data-stu-id="ed1d8-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="ed1d8-155">Отображение текста в порядке чтения справа налево для двунаправленного текста при выборе шрифта для иврита или арабского языка.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="ed1d8-156">По умолчанию для всех текстов используется порядок чтения слева направо.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ed1d8-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE</span><span class="sxs-lookup"><span data-stu-id="ed1d8-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="ed1d8-158">Отображать текст только в одной строке.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-158">Display text on a single line only.</span></span> <span data-ttu-id="ed1d8-159">Возвраты каретки и перевода строки не нарушают линию.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ed1d8-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT, \_ верхнее</span><span class="sxs-lookup"><span data-stu-id="ed1d8-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="ed1d8-161">Текст сверху по ширине.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ed1d8-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ vCenter</span><span class="sxs-lookup"><span data-stu-id="ed1d8-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="ed1d8-163">Центрировать текст по вертикали (только одна строка).</span><span class="sxs-lookup"><span data-stu-id="ed1d8-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ed1d8-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ специализированные</span><span class="sxs-lookup"><span data-stu-id="ed1d8-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="ed1d8-165">Разбейте слова.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-165">Break words.</span></span> <span data-ttu-id="ed1d8-166">Строки автоматически прерываются между словами, если слово выходит за границы прямоугольника, заданного параметром прект.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="ed1d8-167">Последовательность возврата каретки/перевода строки также прерывает линию.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="ed1d8-168">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed1d8-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1d8-169">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="ed1d8-170">Цвет текста.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-170">Color of the text.</span></span> <span data-ttu-id="ed1d8-171">См. [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="ed1d8-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1d8-172">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed1d8-172">Return value</span></span>

<span data-ttu-id="ed1d8-173">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed1d8-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed1d8-174">Если функция выполнена удачно, возвращаемое значение является высотой текста в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="ed1d8-175">Если \_ указан параметр DT vCenter или DT \_ Bottom, возвращаемое значение является смещением от прект (сверху вниз) отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="ed1d8-176">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1d8-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed1d8-177">Remarks</span></span>

<span data-ttu-id="ed1d8-178">Параметры этого метода очень похожи на функции [GDI DrawText](/previous-versions//ms533909(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ed1d8-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="ed1d8-179">Этот метод поддерживает строки как в ANSI, так и в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="ed1d8-180">Если не \_ используется формат DT, этот метод вырезает текст таким образом, чтобы он не выходил за пределы указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="ed1d8-181">Предполагается, что все форматирование имеет несколько строк, если не \_ указан формат DT SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="ed1d8-182">Если выбранный шрифт слишком велик для прямоугольника, этот метод не пытается заменить шрифт меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="ed1d8-183">Этот метод поддерживает только шрифты, для которых в качестве escape-последовательности и ориентации заданы нулевые значения.</span><span class="sxs-lookup"><span data-stu-id="ed1d8-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1d8-184">Требования</span><span class="sxs-lookup"><span data-stu-id="ed1d8-184">Requirements</span></span>



| <span data-ttu-id="ed1d8-185">Требование</span><span class="sxs-lookup"><span data-stu-id="ed1d8-185">Requirement</span></span> | <span data-ttu-id="ed1d8-186">Значение</span><span class="sxs-lookup"><span data-stu-id="ed1d8-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1d8-187">Header</span><span class="sxs-lookup"><span data-stu-id="ed1d8-187">Header</span></span><br/>  | <dl> <span data-ttu-id="ed1d8-188"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1d8-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed1d8-189">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed1d8-189">Library</span></span><br/> | <dl> <span data-ttu-id="ed1d8-190"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed1d8-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1d8-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed1d8-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1d8-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="ed1d8-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="ed1d8-193">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ed1d8-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
