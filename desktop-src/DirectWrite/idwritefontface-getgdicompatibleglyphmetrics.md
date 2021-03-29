---
title: Идвритефонтфаце Жетгдикомпатиблеглифметрикс, метод
description: Получает метрики глифов в единицах дизайна шрифта с возвращаемыми значениями, совместимыми с тем, что создает GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Непосредственная запись метода Жетгдикомпатиблеглифметрикс
- Прямая запись метода Жетгдикомпатиблеглифметрикс, интерфейс Идвритефонтфаце
- Прямая запись интерфейса Идвритефонтфаце, метод Жетгдикомпатиблеглифметрикс
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668861"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="bac29-106">Метод Идвритефонтфаце:: Жетгдикомпатиблеглифметрикс</span><span class="sxs-lookup"><span data-stu-id="bac29-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="bac29-107">Получает метрики глифов в единицах дизайна шрифта с возвращаемыми значениями, совместимыми с тем, что создает GDI.</span><span class="sxs-lookup"><span data-stu-id="bac29-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac29-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bac29-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bac29-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bac29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac29-110">*емсизе*</span><span class="sxs-lookup"><span data-stu-id="bac29-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="bac29-111">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="bac29-111">Type: **FLOAT**</span></span>

<span data-ttu-id="bac29-112">Размер гическая шрифта в DIP.</span><span class="sxs-lookup"><span data-stu-id="bac29-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="bac29-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="bac29-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="bac29-114">Type: **FLOAT**</span></span>

<span data-ttu-id="bac29-115">Число физических пикселов на DIP.</span><span class="sxs-lookup"><span data-stu-id="bac29-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-116">*Преобразование* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="bac29-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bac29-117">Тип: **[**дврите \_ Матрица**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \* const**</span><span class="sxs-lookup"><span data-stu-id="bac29-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="bac29-118">Необязательное преобразование, применяемое к глифам и их позициям.</span><span class="sxs-lookup"><span data-stu-id="bac29-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="bac29-119">Это преобразование применяется после масштабирования, заданного размером шрифта и *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="bac29-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-120">*усегдинатурал*</span><span class="sxs-lookup"><span data-stu-id="bac29-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="bac29-121">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="bac29-121">Type: **BOOL**</span></span>

<span data-ttu-id="bac29-122">Если задано **значение false**, метрики совпадают с метриками текста с псевдонимами GDI.</span><span class="sxs-lookup"><span data-stu-id="bac29-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="bac29-123">Если задано **значение true**, метрики совпадают с метриками текста, ИЗМЕРЯЕМыми GDI, с использованием шрифта, созданного с помощью **технологии CLEARTYPE для \_ естественного \_ качества**.</span><span class="sxs-lookup"><span data-stu-id="bac29-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-124">*глифиндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bac29-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac29-125">Тип: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="bac29-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="bac29-126">Массив индексов глифов, для которых нужно вычислить метрики.</span><span class="sxs-lookup"><span data-stu-id="bac29-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-127">*глифкаунт*</span><span class="sxs-lookup"><span data-stu-id="bac29-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="bac29-128">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bac29-128">Type: **UINT32**</span></span>

<span data-ttu-id="bac29-129">Число элементов в массиве *глифиндицес* .</span><span class="sxs-lookup"><span data-stu-id="bac29-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-130">*глифметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bac29-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bac29-131">Тип: **[ **\_ \_ метрики глифов дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="bac29-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="bac29-132">Массив структур [**\_ \_ метрик глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) , заполняемый этой функцией.</span><span class="sxs-lookup"><span data-stu-id="bac29-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="bac29-133">Метрики находятся в единицах дизайна шрифта.</span><span class="sxs-lookup"><span data-stu-id="bac29-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="bac29-134">*в сторону*</span><span class="sxs-lookup"><span data-stu-id="bac29-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="bac29-135">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="bac29-135">Type: **BOOL**</span></span>

<span data-ttu-id="bac29-136">Логическое значение, указывающее, используется ли шрифт в параллельном исполнении.</span><span class="sxs-lookup"><span data-stu-id="bac29-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="bac29-137">Это может повлиять на метрики глифов, если шрифт имеет наклонное моделирование, поскольку имитация наклона в сторону отличается от ненаправленного наклонного моделирования.</span><span class="sxs-lookup"><span data-stu-id="bac29-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac29-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bac29-138">Return value</span></span>

<span data-ttu-id="bac29-139">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bac29-139">Type: **HRESULT**</span></span>

<span data-ttu-id="bac29-140">Стандартный код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bac29-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="bac29-141">Если любой из входных индексов глифов находится за пределами допустимого диапазона индекса глифа для текущего начертания шрифта, возвращается значение **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="bac29-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="bac29-142">Требования</span><span class="sxs-lookup"><span data-stu-id="bac29-142">Requirements</span></span>



| <span data-ttu-id="bac29-143">Требование</span><span class="sxs-lookup"><span data-stu-id="bac29-143">Requirement</span></span> | <span data-ttu-id="bac29-144">Значение</span><span class="sxs-lookup"><span data-stu-id="bac29-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bac29-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bac29-145">Library</span></span><br/> | <dl> <span data-ttu-id="bac29-146"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bac29-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="bac29-147">DLL</span><span class="sxs-lookup"><span data-stu-id="bac29-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="bac29-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bac29-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac29-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bac29-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac29-150">**идвритефонтфаце**</span><span class="sxs-lookup"><span data-stu-id="bac29-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="bac29-151">**идвритефонтфаце**</span><span class="sxs-lookup"><span data-stu-id="bac29-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

