---
title: Идвритефонтфаце Жетгдикомпатиблеметрикс, метод
description: Получает единицы проектирования и общие метрики для начертания шрифта. Эти метрики применимы ко всем глифам в фонтфаце и используются приложениями для вычисления макета.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Непосредственная запись метода Жетгдикомпатиблеметрикс
- Прямая запись метода Жетгдикомпатиблеметрикс, интерфейс Идвритефонтфаце
- Прямая запись интерфейса Идвритефонтфаце, метод Жетгдикомпатиблеметрикс
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685254"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="d5f8f-107">Метод Идвритефонтфаце:: Жетгдикомпатиблеметрикс</span><span class="sxs-lookup"><span data-stu-id="d5f8f-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="d5f8f-108">Получает единицы проектирования и общие метрики для начертания шрифта.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="d5f8f-109">Эти метрики применимы ко всем глифам в фонтфаце и используются приложениями для вычисления макета.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f8f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5f8f-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d5f8f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5f8f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f8f-112">*емсизе*</span><span class="sxs-lookup"><span data-stu-id="d5f8f-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f8f-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-113">Type: **FLOAT**</span></span>

<span data-ttu-id="d5f8f-114">Логический размер шрифта в единицах DIP.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="d5f8f-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="d5f8f-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f8f-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-116">Type: **FLOAT**</span></span>

<span data-ttu-id="d5f8f-117">Число физических пикселов на DIP.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="d5f8f-118">*Преобразование* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d5f8f-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f8f-119">Тип: **[**дврите \_ Матрица**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \* const**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="d5f8f-120">Необязательное преобразование, применяемое к глифам и их позициям.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="d5f8f-121">Это преобразование применяется после масштабирования, заданного размером шрифта и *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f8f-122">*фонтфацеметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d5f8f-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f8f-123">Тип: **[ **дврите \_ . \_ метрики шрифта**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="d5f8f-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="d5f8f-124">Указатель на структуру [**\_ \_ метрики шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)для заполнения.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="d5f8f-125">Метрики, возвращаемые этой функцией, находятся в единицах дизайна шрифта.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f8f-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5f8f-126">Return value</span></span>

<span data-ttu-id="d5f8f-127">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-127">Type: **HRESULT**</span></span>

<span data-ttu-id="d5f8f-128">Стандартный код ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d5f8f-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f8f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d5f8f-129">Requirements</span></span>



| <span data-ttu-id="d5f8f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d5f8f-130">Requirement</span></span> | <span data-ttu-id="d5f8f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d5f8f-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f8f-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5f8f-132">Library</span></span><br/> | <dl> <span data-ttu-id="d5f8f-133"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f8f-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5f8f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f8f-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5f8f-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f8f-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f8f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5f8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f8f-137">**идвритефонтфаце**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="d5f8f-138">**идвритефонтфаце**</span><span class="sxs-lookup"><span data-stu-id="d5f8f-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

