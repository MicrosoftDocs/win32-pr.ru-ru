---
title: IDWriteFactory2 Креатеглифрунаналисис, метод
description: Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Непосредственная запись метода Креатеглифрунаналисис
- Прямая запись метода Креатеглифрунаналисис, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Креатеглифрунаналисис
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415801"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="9a340-106">Метод IDWriteFactory2:: Креатеглифрунаналисис</span><span class="sxs-lookup"><span data-stu-id="9a340-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="9a340-107">Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.</span><span class="sxs-lookup"><span data-stu-id="9a340-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a340-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a340-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="9a340-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a340-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a340-110">*glyphRun* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a340-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a340-111">Тип: \**const константа \* [**дврите \_ \_ Запуск**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)* _</span><span class="sxs-lookup"><span data-stu-id="9a340-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="9a340-112">Структура, указывающая свойства запуска глифа.</span><span class="sxs-lookup"><span data-stu-id="9a340-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-113">_transform \* \[ в, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="9a340-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a340-114">Тип: \**const [**дврите \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="9a340-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="9a340-115">Необязательное преобразование, применяемое к глифам и их позициям.</span><span class="sxs-lookup"><span data-stu-id="9a340-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="9a340-116">Это преобразование применяется после масштабирования, указанного в параметре Емсизе и pixelsPerDip.</span><span class="sxs-lookup"><span data-stu-id="9a340-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="9a340-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-118">Тип: **\_ \_ режим рендеринга дврите**</span><span class="sxs-lookup"><span data-stu-id="9a340-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="9a340-119">Задает режим рендеринга, который должен быть одним из режимов растровой отрисовки (т. е. не является значением по умолчанию и не структурным).</span><span class="sxs-lookup"><span data-stu-id="9a340-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="9a340-120">*меасурингмоде*</span><span class="sxs-lookup"><span data-stu-id="9a340-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-121">Тип: **[ **дврите \_ измерение \_ режим**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="9a340-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="9a340-122">Задает метод для измерения глифов.</span><span class="sxs-lookup"><span data-stu-id="9a340-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-123">*гридфитмоде*</span><span class="sxs-lookup"><span data-stu-id="9a340-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-124">Тип: **[ **дврите \_ \_ \_ режим вписывания в сетку**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="9a340-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="9a340-125">Как поместить контур глифа в сетку.</span><span class="sxs-lookup"><span data-stu-id="9a340-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="9a340-126">Это значение должно быть не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a340-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-127">*антиалиасмоде*</span><span class="sxs-lookup"><span data-stu-id="9a340-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-128">Тип: **[ **дврите \_ \_ \_ режим сглаживания текста**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="9a340-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="9a340-129">Задает режим сглаживания.</span><span class="sxs-lookup"><span data-stu-id="9a340-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-130">*баселинеоригинкс*</span><span class="sxs-lookup"><span data-stu-id="9a340-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-131">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9a340-131">Type: **FLOAT**</span></span>

<span data-ttu-id="9a340-132">Горизонтальное положение исходного плана в DIP.</span><span class="sxs-lookup"><span data-stu-id="9a340-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-133">*баселинеоригини*</span><span class="sxs-lookup"><span data-stu-id="9a340-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="9a340-134">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9a340-134">Type: **FLOAT**</span></span>

<span data-ttu-id="9a340-135">Вертикальное положение исходного плана в DIP.</span><span class="sxs-lookup"><span data-stu-id="9a340-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="9a340-136">*глифрунаналисис* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9a340-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a340-137">Тип: **[ **идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a340-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="9a340-138">Получает указатель на только что созданный объект.</span><span class="sxs-lookup"><span data-stu-id="9a340-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a340-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a340-139">Return value</span></span>

<span data-ttu-id="9a340-140">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a340-140">Type: **HRESULT**</span></span>

<span data-ttu-id="9a340-141">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9a340-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a340-142">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a340-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a340-143">Требования</span><span class="sxs-lookup"><span data-stu-id="9a340-143">Requirements</span></span>



| <span data-ttu-id="9a340-144">Требование</span><span class="sxs-lookup"><span data-stu-id="9a340-144">Requirement</span></span> | <span data-ttu-id="9a340-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9a340-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a340-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a340-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9a340-147">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a340-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="9a340-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a340-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9a340-149">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a340-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9a340-150">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="9a340-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9a340-151">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a340-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="9a340-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a340-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a340-153"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a340-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9a340-154">DLL</span><span class="sxs-lookup"><span data-stu-id="9a340-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a340-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a340-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a340-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a340-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a340-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="9a340-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

