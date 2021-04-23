---
title: Идвритефонтфаллбакк Мапчарактерс, метод
description: Определяет подходящий шрифт, используемый для отрисовки начального диапазона текста.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Непосредственная запись метода Мапчарактерс
- Прямая запись метода Мапчарактерс, интерфейс Идвритефонтфаллбакк
- Прямая запись интерфейса Идвритефонтфаллбакк, метод Мапчарактерс
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340835"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="c37dc-106">Метод Идвритефонтфаллбакк:: Мапчарактерс</span><span class="sxs-lookup"><span data-stu-id="c37dc-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="c37dc-107">Определяет подходящий шрифт, используемый для отрисовки начального диапазона текста.</span><span class="sxs-lookup"><span data-stu-id="c37dc-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c37dc-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="c37dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c37dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c37dc-110">*source*</span><span class="sxs-lookup"><span data-stu-id="c37dc-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-111">Тип: \**[**идвритетекстаналисиссаурце**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="c37dc-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="c37dc-112">В реализации источника текста содержатся текст и языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="c37dc-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="c37dc-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-114">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c37dc-114">Type: **UINT32**</span></span>

<span data-ttu-id="c37dc-115">Начальное расположение для анализа.</span><span class="sxs-lookup"><span data-stu-id="c37dc-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="c37dc-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-117">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c37dc-117">Type: **UINT32**</span></span>

<span data-ttu-id="c37dc-118">Длина анализируемого текста.</span><span class="sxs-lookup"><span data-stu-id="c37dc-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-119">*басефонтколлектион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c37dc-120">Тип: \**[**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="c37dc-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="c37dc-121">Используемая коллекция шрифтов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c37dc-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-122">_baseFamilyName \* \[ в, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c37dc-123">Тип: \**const WCHAR \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="c37dc-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="c37dc-124">Имя семейства базовых шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c37dc-124">Family name of the base font.</span></span> <span data-ttu-id="c37dc-125">Если передать значение null, для семейства не будет выполняться никаких соответствий.</span><span class="sxs-lookup"><span data-stu-id="c37dc-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="c37dc-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-127">Тип: **[ **\_ \_ плотность шрифта дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="c37dc-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="c37dc-128">Требуемый вес.</span><span class="sxs-lookup"><span data-stu-id="c37dc-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-129">*басестиле*</span><span class="sxs-lookup"><span data-stu-id="c37dc-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-130">Тип: Дврите начертание **[ **\_ шрифта \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="c37dc-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="c37dc-131">Нужный стиль.</span><span class="sxs-lookup"><span data-stu-id="c37dc-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-132">*басестретч*</span><span class="sxs-lookup"><span data-stu-id="c37dc-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="c37dc-133">Тип: **[ **дврите \_ Font \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="c37dc-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="c37dc-134">Требуемое растяжение.</span><span class="sxs-lookup"><span data-stu-id="c37dc-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-135">*маппедленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c37dc-136">Тип: \**UINT32 \** _</span><span class="sxs-lookup"><span data-stu-id="c37dc-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="c37dc-137">Длина текста, сопоставленного с сопоставленным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="c37dc-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="c37dc-138">Оно всегда будет меньше или равно длине текста и больше нуля (если длина текста не равна нулю), поэтому вызывающий объект перемещает по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="c37dc-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c37dc-140">Тип: **[ **идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="c37dc-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="c37dc-141">Шрифт, который должен использоваться для отрисовки первых *маппедленгс* символов текста.</span><span class="sxs-lookup"><span data-stu-id="c37dc-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="c37dc-142">Если он возвращает значение NULL, это означает, что ни один из шрифтов не может визуализировать текст, а *маппедленгс* — число пропускаемых символов (отображается с отсутствующим глифом).</span><span class="sxs-lookup"><span data-stu-id="c37dc-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="c37dc-143">*масштаб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c37dc-144">Тип: \**float \** _</span><span class="sxs-lookup"><span data-stu-id="c37dc-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="c37dc-145">Коэффициент масштабирования для умножения размера em возвращаемого шрифта на.</span><span class="sxs-lookup"><span data-stu-id="c37dc-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c37dc-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c37dc-146">Return value</span></span>

<span data-ttu-id="c37dc-147">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c37dc-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c37dc-148">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c37dc-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c37dc-149">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c37dc-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37dc-150">Требования</span><span class="sxs-lookup"><span data-stu-id="c37dc-150">Requirements</span></span>



| <span data-ttu-id="c37dc-151">Требование</span><span class="sxs-lookup"><span data-stu-id="c37dc-151">Requirement</span></span> | <span data-ttu-id="c37dc-152">Значение</span><span class="sxs-lookup"><span data-stu-id="c37dc-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c37dc-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c37dc-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c37dc-154">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c37dc-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c37dc-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c37dc-156">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c37dc-157">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="c37dc-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c37dc-158">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="c37dc-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c37dc-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c37dc-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="c37dc-160"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c37dc-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c37dc-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c37dc-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c37dc-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c37dc-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c37dc-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c37dc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37dc-164">**идвритефонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c37dc-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

