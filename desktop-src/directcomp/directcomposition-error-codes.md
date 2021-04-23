---
title: Коды ошибок DirectComposition (Дкомп. h)
description: В этом разделе описываются коды ошибок, которые относятся к DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136707"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="9b604-103">Коды ошибок DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9b604-103">DirectComposition error codes</span></span>

<span data-ttu-id="9b604-104">При возникновении ошибки Microsoft DirectComposition возвращает код в виде значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b604-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="9b604-105">В этом разделе описываются коды ошибок, которые относятся к DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9b604-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="9b604-106">Список общих кодов ошибок модели COM см. в разделе [коды ошибок COM](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9b604-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9b604-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_доступ к ошибке дкомпоситион \_ \_ запрещен**</span><span class="sxs-lookup"><span data-stu-id="9b604-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="9b604-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9b604-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="9b604-109">Обработчик окна, указанный в вызове метода [**идкомпоситиондевице:: креатетаржетфорхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) , принадлежит другому процессу, создавшему объект устройства.</span><span class="sxs-lookup"><span data-stu-id="9b604-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9b604-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="9b604-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9b604-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="9b604-112">Поверхность уже была отображена, когда приложение вызвало метод [**идкомпоситионсурфаце:: бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**Идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)или [**идкомпоситионсурфаце:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) .</span><span class="sxs-lookup"><span data-stu-id="9b604-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="9b604-113">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="9b604-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9b604-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ готовится к просмотру**</span><span class="sxs-lookup"><span data-stu-id="9b604-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="9b604-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9b604-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="9b604-116">Приложение вызвало метод [**идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**Идкомпоситионсурфаце:: ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)или [**идкомпоситионсурфаце:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) для поверхности, которая не подготавливается к просмотру.</span><span class="sxs-lookup"><span data-stu-id="9b604-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="9b604-117">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="9b604-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9b604-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**ДКОМПОСИТИОН \_ \_ окно ошибок \_ уже \_ состояло**</span><span class="sxs-lookup"><span data-stu-id="9b604-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="9b604-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9b604-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="9b604-120">Метод [**идкомпоситиондевице:: креатетаржетфорхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) был вызван с *HWND* и *верхними* параметрами, для которых уже существует визуальное дерево.</span><span class="sxs-lookup"><span data-stu-id="9b604-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b604-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b604-121">Remarks</span></span>

<span data-ttu-id="9b604-122">Если вызов [**идкомпоситионсурфаце:: бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) был последним действием:</span><span class="sxs-lookup"><span data-stu-id="9b604-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="9b604-123">Вызов этого метода:</span><span class="sxs-lookup"><span data-stu-id="9b604-123">Calling this method:</span></span>                                    | <span data-ttu-id="9b604-124">Возвращает это значение:</span><span class="sxs-lookup"><span data-stu-id="9b604-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="9b604-125">**бегиндрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="9b604-126">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="9b604-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="9b604-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="9b604-128">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="9b604-129">**суспенддрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="9b604-130">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="9b604-131">**ресумедрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="9b604-132">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="9b604-133">Если вызов [**идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) был последним действием:</span><span class="sxs-lookup"><span data-stu-id="9b604-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="9b604-134">Вызов этого метода:</span><span class="sxs-lookup"><span data-stu-id="9b604-134">Calling this method:</span></span>                                    | <span data-ttu-id="9b604-135">Возвращает это значение:</span><span class="sxs-lookup"><span data-stu-id="9b604-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="9b604-136">**бегиндрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="9b604-137">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="9b604-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="9b604-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="9b604-139">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="9b604-140">**суспенддрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="9b604-141">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="9b604-142">**ресумедрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="9b604-143">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="9b604-144">Если вызов [**идкомпоситионсурфаце:: ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) был последним действием:</span><span class="sxs-lookup"><span data-stu-id="9b604-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="9b604-145">Вызов этого метода:</span><span class="sxs-lookup"><span data-stu-id="9b604-145">Calling this method:</span></span>                                    | <span data-ttu-id="9b604-146">Возвращает это значение:</span><span class="sxs-lookup"><span data-stu-id="9b604-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9b604-147">**бегиндрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="9b604-148">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**</span><span class="sxs-lookup"><span data-stu-id="9b604-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="9b604-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="9b604-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="9b604-150">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="9b604-151">**суспенддрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="9b604-152">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="9b604-153">**ресумедрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="9b604-154">**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_ .**</span><span class="sxs-lookup"><span data-stu-id="9b604-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="9b604-155">Если вызов [**идкомпоситионсурфаце:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) был последним действием:</span><span class="sxs-lookup"><span data-stu-id="9b604-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="9b604-156">Вызов этого метода:</span><span class="sxs-lookup"><span data-stu-id="9b604-156">Calling this method:</span></span>                                    | <span data-ttu-id="9b604-157">Возвращает это значение:</span><span class="sxs-lookup"><span data-stu-id="9b604-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="9b604-158">**бегиндрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="9b604-159">\_ОК</span><span class="sxs-lookup"><span data-stu-id="9b604-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="9b604-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="9b604-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="9b604-161">**\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.**</span><span class="sxs-lookup"><span data-stu-id="9b604-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="9b604-162">**суспенддрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="9b604-163">**\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.**</span><span class="sxs-lookup"><span data-stu-id="9b604-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="9b604-164">**ресумедрав**</span><span class="sxs-lookup"><span data-stu-id="9b604-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="9b604-165">**\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.**</span><span class="sxs-lookup"><span data-stu-id="9b604-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9b604-166">Требования</span><span class="sxs-lookup"><span data-stu-id="9b604-166">Requirements</span></span>



| <span data-ttu-id="9b604-167">Требование</span><span class="sxs-lookup"><span data-stu-id="9b604-167">Requirement</span></span> | <span data-ttu-id="9b604-168">Значение</span><span class="sxs-lookup"><span data-stu-id="9b604-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b604-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b604-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9b604-170">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9b604-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9b604-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b604-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9b604-172">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9b604-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9b604-173">Header</span><span class="sxs-lookup"><span data-stu-id="9b604-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b604-174"><dt>Дкомп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b604-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b604-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b604-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b604-176">Справочник по DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9b604-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

