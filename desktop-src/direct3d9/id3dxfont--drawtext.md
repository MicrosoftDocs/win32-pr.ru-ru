---
description: Рисует форматированный текст. Этот метод поддерживает строки ANSI и Юникод.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: 'ID3DXFont: метод:D Равтекст (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273770"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="3991a-104">ID3DXFont: метод:D Равтекст</span><span class="sxs-lookup"><span data-stu-id="3991a-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="3991a-105">Рисует форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="3991a-105">Draws formatted text.</span></span> <span data-ttu-id="3991a-106">Этот метод поддерживает строки ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="3991a-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="3991a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3991a-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="3991a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3991a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3991a-109">*псприте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-110">Тип: **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="3991a-111">Указатель на объект [**ID3DXSprite**](id3dxsprite.md) , содержащий строку.</span><span class="sxs-lookup"><span data-stu-id="3991a-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="3991a-112">Может иметь **значение NULL**, в этом случае Direct3D будет отображать строку с собственным объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="3991a-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="3991a-113">Чтобы повысить эффективность, необходимо указать объект Sprite, если **DrawText** должен быть вызван более одного раза в строке.</span><span class="sxs-lookup"><span data-stu-id="3991a-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-114">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3991a-116">Указатель на строку для рисования.</span><span class="sxs-lookup"><span data-stu-id="3991a-116">Pointer to a string to draw.</span></span> <span data-ttu-id="3991a-117">Если параметр count имеет значение-1, строка должна завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="3991a-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-119">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3991a-120">Указывает количество знаков в строке.</span><span class="sxs-lookup"><span data-stu-id="3991a-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="3991a-121">Если Count равно-1, то параметр Пстринг считается указателем на строку, завершающимся нулем, а **DrawText** автоматически выдает число символов.</span><span class="sxs-lookup"><span data-stu-id="3991a-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-122">*прект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-123">Тип: **[ **лпрект**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3991a-124">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую прямоугольник в логических координатах, в котором должен быть отформатирован текст.</span><span class="sxs-lookup"><span data-stu-id="3991a-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="3991a-125">Значение координаты правой стороны прямоугольника должно быть больше значения его левой стороны.</span><span class="sxs-lookup"><span data-stu-id="3991a-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="3991a-126">Аналогично, значение координаты нижнего значения должно быть больше верхнего.</span><span class="sxs-lookup"><span data-stu-id="3991a-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-127">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3991a-129">Задает метод форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="3991a-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="3991a-130">Это может быть любое сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3991a-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="3991a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3991a-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="3991a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3991a-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="3991a-133"><dt>**DT, \_ Нижний**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="3991a-134">Выравнивает текст по нижней части прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3991a-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="3991a-135">Это значение должно сочетаться с DT \_ SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="3991a-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="3991a-136"><dt>**DT \_ калкрект**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="3991a-137">Определяет ширину и высоту прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3991a-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="3991a-138">Если имеется несколько строк текста, **DrawText** использует ширину прямоугольника, на который указывает параметр прект, и расширяет основу прямоугольника, чтобы она была привязана к последней строке текста.</span><span class="sxs-lookup"><span data-stu-id="3991a-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="3991a-139">Если имеется только одна строка текста, **DrawText** изменяет правую часть прямоугольника таким образом, чтобы она была привязана к последнему символу в строке.</span><span class="sxs-lookup"><span data-stu-id="3991a-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="3991a-140">В любом случае **DrawText** Возвращает высоту форматированного текста, но не рисует текст.</span><span class="sxs-lookup"><span data-stu-id="3991a-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="3991a-141"><dt>**\_центр DT**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="3991a-142">Центрирование текста по горизонтали в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="3991a-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="3991a-143"><dt>**DT \_ експандтабс**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="3991a-144">Расширяет табуляцию.</span><span class="sxs-lookup"><span data-stu-id="3991a-144">Expands tab characters.</span></span> <span data-ttu-id="3991a-145">По умолчанию количество символов на шаг табуляции равно восьми.</span><span class="sxs-lookup"><span data-stu-id="3991a-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="3991a-146"><dt>**DT \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="3991a-147">Выровняйте текст по левому краю.</span><span class="sxs-lookup"><span data-stu-id="3991a-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="3991a-148"><dt>**DT — \_ Clip**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="3991a-149">Рисование без усечения.</span><span class="sxs-lookup"><span data-stu-id="3991a-149">Draws without clipping.</span></span> <span data-ttu-id="3991a-150">**DrawText** несколько быстрее при использовании "DT" \_ .</span><span class="sxs-lookup"><span data-stu-id="3991a-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="3991a-151"><dt>**DT, \_ вправо**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="3991a-152">Выровняйте текст по правому краю.</span><span class="sxs-lookup"><span data-stu-id="3991a-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="3991a-153"><dt>**DT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="3991a-154">Отображает текст в порядке чтения справа налево для двунаправленного текста при выборе шрифта для иврита или арабского языка.</span><span class="sxs-lookup"><span data-stu-id="3991a-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="3991a-155">По умолчанию для всех текстов используется порядок чтения слева направо.</span><span class="sxs-lookup"><span data-stu-id="3991a-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="3991a-156"><dt>**DT \_ SINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="3991a-157">Отображает текст только в одной строке.</span><span class="sxs-lookup"><span data-stu-id="3991a-157">Displays text on a single line only.</span></span> <span data-ttu-id="3991a-158">Возвраты каретки и перевода строки не нарушают линию.</span><span class="sxs-lookup"><span data-stu-id="3991a-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="3991a-159"><dt>**DT, \_ верхнее**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="3991a-160">Выравнивание текста по верхнему краю.</span><span class="sxs-lookup"><span data-stu-id="3991a-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="3991a-161"><dt>**DT \_ vCenter**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="3991a-162">Выравнивание текста по вертикали (только одна строка).</span><span class="sxs-lookup"><span data-stu-id="3991a-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="3991a-163"><dt>**DT \_ специализированные**</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="3991a-164">Разбивает слова.</span><span class="sxs-lookup"><span data-stu-id="3991a-164">Breaks words.</span></span> <span data-ttu-id="3991a-165">Строки автоматически прерываются между словами, если слово выходит за границы прямоугольника, заданного параметром прект.</span><span class="sxs-lookup"><span data-stu-id="3991a-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="3991a-166">Последовательность возврата каретки/перевода строки также прерывает линию.</span><span class="sxs-lookup"><span data-stu-id="3991a-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="3991a-167">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991a-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991a-168">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3991a-169">Цвет текста.</span><span class="sxs-lookup"><span data-stu-id="3991a-169">Color of the text.</span></span> <span data-ttu-id="3991a-170">Дополнительные сведения см. в разделе [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3991a-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3991a-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3991a-171">Return value</span></span>

<span data-ttu-id="3991a-172">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3991a-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3991a-173">Если функция выполнена удачно, возвращаемое значение является высотой текста в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="3991a-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="3991a-174">Если \_ указан параметр DT vCenter или DT \_ Bottom, возвращаемое значение является смещением от прект (сверху вниз) отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="3991a-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="3991a-175">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3991a-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3991a-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3991a-176">Remarks</span></span>

<span data-ttu-id="3991a-177">Параметры этого метода очень похожи на функции GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="3991a-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="3991a-178">Этот метод поддерживает строки как в ANSI, так и в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3991a-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="3991a-179">Этот метод должен вызываться внутри [**бегинсцене**](/windows/desktop/api) ... Блок [**ендсцене**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="3991a-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="3991a-180">Единственным исключением является то, что приложение вызывает **DrawText** с DT \_ калкрект для вычисления размера данного блока текста.</span><span class="sxs-lookup"><span data-stu-id="3991a-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="3991a-181">Если не \_ используется формат DT, этот метод вырезает текст таким образом, чтобы он не выходил за пределы указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3991a-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="3991a-182">Предполагается, что все форматирование имеет несколько строк, если не \_ указан формат DT SINGLELINE.</span><span class="sxs-lookup"><span data-stu-id="3991a-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="3991a-183">Если выбранный шрифт слишком велик для прямоугольника, этот метод не пытается заменить шрифт меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="3991a-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="3991a-184">Этот метод поддерживает только шрифты, для которых в качестве escape-последовательности и ориентации заданы нулевые значения.</span><span class="sxs-lookup"><span data-stu-id="3991a-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3991a-185">Требования</span><span class="sxs-lookup"><span data-stu-id="3991a-185">Requirements</span></span>



| <span data-ttu-id="3991a-186">Требование</span><span class="sxs-lookup"><span data-stu-id="3991a-186">Requirement</span></span> | <span data-ttu-id="3991a-187">Значение</span><span class="sxs-lookup"><span data-stu-id="3991a-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3991a-188">Header</span><span class="sxs-lookup"><span data-stu-id="3991a-188">Header</span></span><br/>  | <dl> <span data-ttu-id="3991a-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3991a-190">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3991a-190">Library</span></span><br/> | <dl> <span data-ttu-id="3991a-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3991a-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3991a-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3991a-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="3991a-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
