---
title: Идвритетекстанализер Жетгдикомпатиблеглифплацементс, метод
description: Поместите выходные данные глифов из метода "методы" в соответствии со шрифтами и правилами отрисовки системы записи.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Непосредственная запись метода Жетгдикомпатиблеглифплацементс
- Прямая запись метода Жетгдикомпатиблеглифплацементс, интерфейс Идвритетекстанализер
- Прямая запись интерфейса Идвритетекстанализер, метод Жетгдикомпатиблеглифплацементс
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665266"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="03588-106">Метод Идвритетекстанализер:: Жетгдикомпатиблеглифплацементс</span><span class="sxs-lookup"><span data-stu-id="03588-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="03588-107">Поместите выходные данные глифов [**из метода "методы" в соответствии**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) со шрифтами и правилами отрисовки системы записи.</span><span class="sxs-lookup"><span data-stu-id="03588-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="03588-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03588-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="03588-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="03588-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03588-110">*текстстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-111">Тип: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="03588-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="03588-112">Массив символов, содержащий исходную строку, из которой поступили глифы.</span><span class="sxs-lookup"><span data-stu-id="03588-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="03588-113">*клустермап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-114">Тип: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="03588-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="03588-115">Указатель на сопоставление между диапазонами символов и диапазонами глифов.</span><span class="sxs-lookup"><span data-stu-id="03588-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="03588-116">Он возвращается символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="03588-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="03588-117">*текстпропс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-118">Тип: **[ **дврите \_ изменение \_ \_ свойств текста**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="03588-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="03588-119">Указатель на массив структур, который содержит свойства формирования для каждого символа.</span><span class="sxs-lookup"><span data-stu-id="03588-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="03588-120">Эта структура возвращается символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="03588-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="03588-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="03588-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-122">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="03588-122">Type: **UINT32**</span></span>

<span data-ttu-id="03588-123">Длина текста *текстстринг*.</span><span class="sxs-lookup"><span data-stu-id="03588-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="03588-124">*глифиндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-125">Тип: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="03588-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="03588-126">Массив индексов глифов [**, возвращаемых символами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="03588-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="03588-127">*глифпропс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-128">Тип: **константа \* [**формирования дврите \_ \_ \_ свойств глифа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**</span><span class="sxs-lookup"><span data-stu-id="03588-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="03588-129">Указатель на массив структур, который содержит свойства формирования для каждого глифа, возвращаемого символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="03588-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="03588-130">*глифкаунт*</span><span class="sxs-lookup"><span data-stu-id="03588-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-131">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="03588-131">Type: **UINT32**</span></span>

<span data-ttu-id="03588-132">Число глифов, возвращаемых из [**Подглифов**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="03588-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="03588-133">*фонтфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-134">Тип: **[ **идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="03588-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="03588-135">Указатель на начертание шрифта, которое является источником для выходных глифов.</span><span class="sxs-lookup"><span data-stu-id="03588-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="03588-136">*фонтемсизе*</span><span class="sxs-lookup"><span data-stu-id="03588-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-137">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="03588-137">Type: **FLOAT**</span></span>

<span data-ttu-id="03588-138">Логический размер шрифта в DIP.</span><span class="sxs-lookup"><span data-stu-id="03588-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="03588-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="03588-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-140">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="03588-140">Type: **FLOAT**</span></span>

<span data-ttu-id="03588-141">Число физических пикселов на DIP.</span><span class="sxs-lookup"><span data-stu-id="03588-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="03588-142">*Преобразование* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="03588-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-143">Тип: **[**дврите \_ Матрица**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \* const**</span><span class="sxs-lookup"><span data-stu-id="03588-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="03588-144">Необязательное преобразование, применяемое к глифам и их позициям.</span><span class="sxs-lookup"><span data-stu-id="03588-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="03588-145">Это преобразование применяется после масштабирования, заданного размером шрифта и *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="03588-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="03588-146">*усегдинатурал*</span><span class="sxs-lookup"><span data-stu-id="03588-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-147">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="03588-147">Type: **BOOL**</span></span>

<span data-ttu-id="03588-148">Если задано **значение false**, метрики совпадают с метриками текста с псевдонимами GDI.</span><span class="sxs-lookup"><span data-stu-id="03588-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="03588-149">Если задано **значение true**, метрики совпадают с метриками текста, ИЗМЕРЯЕМыми GDI, с использованием шрифта, созданного с помощью **технологии CLEARTYPE для \_ естественного \_ качества**.</span><span class="sxs-lookup"><span data-stu-id="03588-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-150">*в сторону*</span><span class="sxs-lookup"><span data-stu-id="03588-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-151">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="03588-151">Type: **BOOL**</span></span>

<span data-ttu-id="03588-152">Логический флаг, установленный в **значение true** , если текст должен отображаться вертикально.</span><span class="sxs-lookup"><span data-stu-id="03588-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-153">*исригхттолефт*</span><span class="sxs-lookup"><span data-stu-id="03588-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-154">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="03588-154">Type: **BOOL**</span></span>

<span data-ttu-id="03588-155">Логический флаг, установленный в **значение true** для текста справа налево.</span><span class="sxs-lookup"><span data-stu-id="03588-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-156">*скриптаналисис* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03588-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-157">Тип: " **const [**дврите" \_ \_ анализ скриптов**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="03588-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="03588-158">Указатель на результат анализа скрипта из вызова [**анализескрипт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .</span><span class="sxs-lookup"><span data-stu-id="03588-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-159">*localeName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="03588-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-160">Тип: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="03588-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="03588-161">Массив символов, содержащий языковой стандарт, используемый при выборе глифов.</span><span class="sxs-lookup"><span data-stu-id="03588-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="03588-162">Например, один и тот же символ может сопоставляться с разными глифами для ja-JP и zh-CHS.</span><span class="sxs-lookup"><span data-stu-id="03588-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="03588-163">Если это **значение равно NULL**, используется сопоставление по умолчанию, основанное на скрипте.</span><span class="sxs-lookup"><span data-stu-id="03588-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-164">*функции* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="03588-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-165">Тип: **const [**дврите \_ типографские \_ функции**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***</span><span class="sxs-lookup"><span data-stu-id="03588-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="03588-166">Массив указателей на наборы типографских функций для использования в каждом диапазоне функций.</span><span class="sxs-lookup"><span data-stu-id="03588-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-167">*феатуреранжеленгсс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="03588-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-168">Тип: **const UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="03588-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="03588-169">Длина каждого диапазона компонентов в символах.</span><span class="sxs-lookup"><span data-stu-id="03588-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="03588-170">Сумма всех значений длины должна быть равна *TextLength*.</span><span class="sxs-lookup"><span data-stu-id="03588-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-171">*феатуреранжес*</span><span class="sxs-lookup"><span data-stu-id="03588-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="03588-172">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="03588-172">Type: **UINT32**</span></span>

<span data-ttu-id="03588-173">Число диапазонов функций.</span><span class="sxs-lookup"><span data-stu-id="03588-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-174">*глифадванцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03588-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-175">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="03588-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="03588-176">При возврате из этого метода содержит предварительную ширину каждого глифа.</span><span class="sxs-lookup"><span data-stu-id="03588-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="03588-177">*глифоффсетс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03588-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03588-178">Тип: **[ **\_ \_ смещение глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="03588-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="03588-179">При возврате из этого метода содержит смещение начала каждого глифа.</span><span class="sxs-lookup"><span data-stu-id="03588-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03588-180">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03588-180">Return value</span></span>

<span data-ttu-id="03588-181">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03588-181">Type: **HRESULT**</span></span>

<span data-ttu-id="03588-182">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="03588-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03588-183">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03588-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03588-184">Требования</span><span class="sxs-lookup"><span data-stu-id="03588-184">Requirements</span></span>



| <span data-ttu-id="03588-185">Требование</span><span class="sxs-lookup"><span data-stu-id="03588-185">Requirement</span></span> | <span data-ttu-id="03588-186">Значение</span><span class="sxs-lookup"><span data-stu-id="03588-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03588-187">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03588-187">Library</span></span><br/> | <dl> <span data-ttu-id="03588-188"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03588-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="03588-189">DLL</span><span class="sxs-lookup"><span data-stu-id="03588-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="03588-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03588-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03588-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03588-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03588-192">**идвритетекстанализер**</span><span class="sxs-lookup"><span data-stu-id="03588-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

