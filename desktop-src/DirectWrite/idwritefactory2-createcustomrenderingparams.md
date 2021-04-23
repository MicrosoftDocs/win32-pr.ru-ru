---
title: IDWriteFactory2 Креатекустомрендерингпарамс, метод
description: Создает объект параметров отрисовки с указанными свойствами.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Непосредственная запись метода Креатекустомрендерингпарамс
- Прямая запись метода Креатекустомрендерингпарамс, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Креатекустомрендерингпарамс
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415804"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="f0682-106">Метод IDWriteFactory2:: Креатекустомрендерингпарамс</span><span class="sxs-lookup"><span data-stu-id="f0682-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="f0682-107">Создает объект параметров отрисовки с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f0682-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0682-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0682-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f0682-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0682-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0682-110">*цвет*</span><span class="sxs-lookup"><span data-stu-id="f0682-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-111">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f0682-111">Type: **FLOAT**</span></span>

<span data-ttu-id="f0682-112">Значение гаммы, используемое для гамма-коррекции, которое должно быть больше нуля и не может превышать 256.</span><span class="sxs-lookup"><span data-stu-id="f0682-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-113">*енханцедконтраст*</span><span class="sxs-lookup"><span data-stu-id="f0682-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f0682-114">Type: **FLOAT**</span></span>

<span data-ttu-id="f0682-115">Степень контрастности, ноль или больше.</span><span class="sxs-lookup"><span data-stu-id="f0682-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-116">*грайскалинханцедконтраст*</span><span class="sxs-lookup"><span data-stu-id="f0682-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-117">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f0682-117">Type: **FLOAT**</span></span>

<span data-ttu-id="f0682-118">Степень контрастности, ноль или больше.</span><span class="sxs-lookup"><span data-stu-id="f0682-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-119">*клеартипелевел*</span><span class="sxs-lookup"><span data-stu-id="f0682-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-120">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f0682-120">Type: **FLOAT**</span></span>

<span data-ttu-id="f0682-121">Степень уровня ClearType, от 0,0 f (без ClearType) до 1,0 f (Полная технология ClearType).</span><span class="sxs-lookup"><span data-stu-id="f0682-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="f0682-122">*пикселжеометри*</span><span class="sxs-lookup"><span data-stu-id="f0682-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-123">Тип: **[ **дврите \_ пиксель \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="f0682-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="f0682-124">Геометрия точки устройства.</span><span class="sxs-lookup"><span data-stu-id="f0682-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-125">*рендерингмоде*</span><span class="sxs-lookup"><span data-stu-id="f0682-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-126">Тип: **[ **\_ \_ режим рендеринга дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="f0682-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="f0682-127">Метод отрисовки глифов.</span><span class="sxs-lookup"><span data-stu-id="f0682-127">Method of rendering glyphs.</span></span> <span data-ttu-id="f0682-128">В большинстве случаев это должен быть ДВРИТЕ \_ \_ режим рендеринга \_ по умолчанию для автоматического использования соответствующего режима.</span><span class="sxs-lookup"><span data-stu-id="f0682-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-129">*гридфитмоде*</span><span class="sxs-lookup"><span data-stu-id="f0682-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="f0682-130">Тип: **[ **дврите \_ \_ \_ режим вписывания в сетку**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="f0682-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="f0682-131">Как поместить контур глифа в сетку.</span><span class="sxs-lookup"><span data-stu-id="f0682-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="f0682-132">В большинстве случаев это должно быть ДВРИТЕ \_ Сетка \_ \_ по умолчанию для автоматического выбора соответствующего режима.</span><span class="sxs-lookup"><span data-stu-id="f0682-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="f0682-133">*рендерингпарамс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0682-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0682-134">Тип: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0682-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="f0682-135">Содержит только что созданный объект параметров отрисовки или значение NULL в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="f0682-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0682-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0682-136">Return value</span></span>

<span data-ttu-id="f0682-137">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0682-137">Type: **HRESULT**</span></span>

<span data-ttu-id="f0682-138">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0682-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0682-139">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0682-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0682-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f0682-140">Requirements</span></span>



| <span data-ttu-id="f0682-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f0682-141">Requirement</span></span> | <span data-ttu-id="f0682-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f0682-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0682-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0682-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f0682-144">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="f0682-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f0682-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0682-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f0682-146">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f0682-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f0682-147">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="f0682-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f0682-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0682-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="f0682-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f0682-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0682-150"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0682-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f0682-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f0682-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0682-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0682-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0682-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0682-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0682-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="f0682-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

