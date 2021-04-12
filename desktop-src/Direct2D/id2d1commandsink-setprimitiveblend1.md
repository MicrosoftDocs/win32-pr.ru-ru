---
title: ID2D1CommandSink1 SetPrimitiveBlend1, метод
description: Задает новый режим простого смешения.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Метод SetPrimitiveBlend1 Direct2D
- Метод SetPrimitiveBlend1 Direct2D, интерфейс ID2D1CommandSink1
- Интерфейс ID2D1CommandSink1 Direct2D, метод SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135779"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="8c2ff-106">Метод ID2D1CommandSink1:: SetPrimitiveBlend1</span><span class="sxs-lookup"><span data-stu-id="8c2ff-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="8c2ff-107">Задает новый режим простого смешения.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2ff-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c2ff-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="8c2ff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c2ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2ff-110">*примитивебленд*</span><span class="sxs-lookup"><span data-stu-id="8c2ff-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="8c2ff-111">Тип: **[ **D2D1- \_ примитив \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="8c2ff-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="8c2ff-112">Примитивное смешение, которое будет применяться к последующим примитивам.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2ff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c2ff-113">Return value</span></span>

<span data-ttu-id="8c2ff-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c2ff-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8c2ff-115">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c2ff-116">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c2ff-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2ff-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c2ff-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="8c2ff-118">Режимы смешения</span><span class="sxs-lookup"><span data-stu-id="8c2ff-118">Blend modes</span></span>

<span data-ttu-id="8c2ff-119">Для отрисовки с псевдонимами (за исключением режима MIN) выходное значение O вычислено путем линейной интерполяции значения *Blend (S, D)* с целевым значением пикселя на основе величины, на которую примитив охватывает целевой пиксель.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="8c2ff-120">В таблице ниже показаны режимы простого смешения для наложения псевдонимов и сглаживания.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="8c2ff-121">В формулах, перечисленных в таблице, используются следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="8c2ff-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="8c2ff-122">O = выходные данные</span><span class="sxs-lookup"><span data-stu-id="8c2ff-122">O = Output</span></span>
-   <span data-ttu-id="8c2ff-123">S = источник</span><span class="sxs-lookup"><span data-stu-id="8c2ff-123">S = Source</span></span>
-   <span data-ttu-id="8c2ff-124">SA = источник альфа</span><span class="sxs-lookup"><span data-stu-id="8c2ff-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="8c2ff-125">D = назначение</span><span class="sxs-lookup"><span data-stu-id="8c2ff-125">D = Destination</span></span>
-   <span data-ttu-id="8c2ff-126">DA = альфа-канал назначения</span><span class="sxs-lookup"><span data-stu-id="8c2ff-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="8c2ff-127">C = покрытие пикселей</span><span class="sxs-lookup"><span data-stu-id="8c2ff-127">C = Pixel coverage</span></span>



| <span data-ttu-id="8c2ff-128">Режим "примитивный Blend"</span><span class="sxs-lookup"><span data-stu-id="8c2ff-128">Primitive blend mode</span></span>                 | <span data-ttu-id="8c2ff-129">Смешение с псевдонимами</span><span class="sxs-lookup"><span data-stu-id="8c2ff-129">Aliased blending</span></span>                            | <span data-ttu-id="8c2ff-130">Смешение с сглаживанием</span><span class="sxs-lookup"><span data-stu-id="8c2ff-130">Antialiased blending</span></span>            | <span data-ttu-id="8c2ff-131">Описание</span><span class="sxs-lookup"><span data-stu-id="8c2ff-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2ff-132">D2D1- \_ примитивный \_ \_ источник Blend \_</span><span class="sxs-lookup"><span data-stu-id="8c2ff-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="8c2ff-133">O = (S + (1 SA) \* D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="8c2ff-134">O = S \* C + D \* (1 SA \* C)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="8c2ff-135">Стандартный режим наложения «источник с назначением».</span><span class="sxs-lookup"><span data-stu-id="8c2ff-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="8c2ff-136">Копирование D2D1- \_ примитивного \_ смешения \_</span><span class="sxs-lookup"><span data-stu-id="8c2ff-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="8c2ff-137">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="8c2ff-138">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="8c2ff-139">Источник копируется в место назначения; целевые Пиксели игнорируются.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="8c2ff-140">D2D1- \_ примитивное \_ \_ минимальное смешение</span><span class="sxs-lookup"><span data-stu-id="8c2ff-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="8c2ff-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="8c2ff-142">O = min (S \* C + 1 SA \* c, D)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="8c2ff-143">Результирующие значения пикселей используют минимальное значение исходного и целевого пикселей.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="8c2ff-144">Доступно в Windows 8 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="8c2ff-145">D2D1- \_ примитивное \_ \_ Добавление</span><span class="sxs-lookup"><span data-stu-id="8c2ff-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="8c2ff-146">O = (S + D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="8c2ff-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="8c2ff-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="8c2ff-147">O = S \* C + D</span></span>                  | <span data-ttu-id="8c2ff-148">Результирующие значения пикселей — это сумма значений исходного и конечного пикселей.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="8c2ff-149">Доступно в Windows 8 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-149">Available in Windows 8 and later.</span></span>     |



 

![Иллюстрация Direct2D-примитивных режимов наложения с различной прозрачностью и фоновыми рисунками.](images/primblenddemo.png)

<span data-ttu-id="8c2ff-151">Иллюстрация примитивных режимов наложения с различной прозрачностью и фоновыми рисунками.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="8c2ff-152">Примитив Blend будет применяться ко всему примитиву, рисуемому в контексте, если это не переопределено с помощью параметра *компоситемоде* в API-интерфейсе [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .</span><span class="sxs-lookup"><span data-stu-id="8c2ff-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="8c2ff-153">Примитив Blend применяется к внутренней части всех примитивов, отображаемых в контексте.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="8c2ff-154">В случае с [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))это будет предприниматься прямоугольником изображения, смещением и универсальным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="8c2ff-155">Если примитив Blend является любым, отличным от **D2D1- \_ примитивного \_ смешения \_ по сравнению** с, то рендеринг ClearType будет отключен.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="8c2ff-156">Если приложение явно вызывает визуализацию ClearType в этих режимах, то контекст рисования будет помещен в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="8c2ff-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="8c2ff-157">D2DERR \_ \_ будет возвращено неправильное состояние: [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="8c2ff-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2ff-158">Требования</span><span class="sxs-lookup"><span data-stu-id="8c2ff-158">Requirements</span></span>



| <span data-ttu-id="8c2ff-159">Требование</span><span class="sxs-lookup"><span data-stu-id="8c2ff-159">Requirement</span></span> | <span data-ttu-id="8c2ff-160">Значение</span><span class="sxs-lookup"><span data-stu-id="8c2ff-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2ff-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c2ff-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2ff-162">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c2ff-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="8c2ff-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c2ff-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2ff-164">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c2ff-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="8c2ff-165">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="8c2ff-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="8c2ff-166">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c2ff-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c2ff-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c2ff-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2ff-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="8c2ff-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

