---
title: Функции DWM
description: В этом разделе содержатся сведения о функциях диспетчер окон рабочего стола (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), функции
- DWM (диспетчер окон рабочего стола), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339433"
---
# <a name="dwm-functions"></a><span data-ttu-id="674e6-107">Функции DWM</span><span class="sxs-lookup"><span data-stu-id="674e6-107">DWM Functions</span></span>

<span data-ttu-id="674e6-108">В этом разделе содержатся сведения о функциях диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="674e6-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="674e6-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="674e6-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="674e6-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="674e6-110">Topic</span></span></th>
<th><span data-ttu-id="674e6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="674e6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="674e6-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>двматтачмилконтент</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-113">Эта функция не реализована.</span><span class="sxs-lookup"><span data-stu-id="674e6-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>двмдефвиндовпрок</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-115">Процедура окна по умолчанию для проверки попадания DWM в области, не являющейся клиентской.</span><span class="sxs-lookup"><span data-stu-id="674e6-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="674e6-116">Также необходимо убедиться, что для <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> сообщения вызывается метод <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>двмдефвиндовпрок</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="674e6-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="674e6-117">Если <strong>двмдефвиндовпрок</strong> не вызывается для сообщения <strong>WM_NCMOUSELEAVE</strong> , DWM не удаляет выделение из кнопок <strong>развертывания</strong>, <strong>сворачивания</strong>и <strong>закрытия</strong> , когда курсор покидает окно.</span><span class="sxs-lookup"><span data-stu-id="674e6-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>двмдетачмилконтент</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-119">Эта функция не реализована.</span><span class="sxs-lookup"><span data-stu-id="674e6-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-121">Включает эффект размытия для указанного окна.</span><span class="sxs-lookup"><span data-stu-id="674e6-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="674e6-122">
<b>Примечание</b> . Начиная с Windows 8, вызов этой функции не приводит к эффекту размытия из-за изменения стиля в способе отрисовки окон.</span><span class="sxs-lookup"><span data-stu-id="674e6-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>двменаблекомпоситион</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-124">Включает или отключает композицию DWM.</span><span class="sxs-lookup"><span data-stu-id="674e6-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="674e6-125">Эта функция является устаревшей по отношению к Windows 8.</span><span class="sxs-lookup"><span data-stu-id="674e6-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="674e6-126">Диспетчер DWM больше не может быть отключен программным способом.</span><span class="sxs-lookup"><span data-stu-id="674e6-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>двменаблеммксс</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-128">Уведомляет DWM о необходимости отказаться от планирования службы обработки отказов (MMCSS) класса мультимедиа, пока вызывающий процесс активен.</span><span class="sxs-lookup"><span data-stu-id="674e6-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-130">Расширяет рамку окна в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="674e6-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>двмфлуш</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-132">Выдает вызов сброса, который блокирует вызывающий объект до следующего присутствия, когда все обновления Microsoft DirectX Surface, которые в настоящее время были выполнены.</span><span class="sxs-lookup"><span data-stu-id="674e6-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="674e6-133">Это компенсирует очень сложный монтажный кадр или вызов процессов с очень низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="674e6-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>двмжетколоризатионколор</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-135">Извлекает текущий цвет, используемый для композиции DWM с эффектом стекла.</span><span class="sxs-lookup"><span data-stu-id="674e6-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="674e6-136">Это значение основано на текущей цветовой схеме и может быть изменено пользователем.</span><span class="sxs-lookup"><span data-stu-id="674e6-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="674e6-137">Приложения могут прослушивать изменения цвета, обрабатывая уведомление <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="674e6-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>двмжеткомпоситионтимингинфо</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-139">Извлекает сведения о текущем времени композиции для указанного окна.</span><span class="sxs-lookup"><span data-stu-id="674e6-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>двмжетграфиксстреамклиент</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-141">Эта функция не реализована.</span><span class="sxs-lookup"><span data-stu-id="674e6-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>двмжетграфиксстреамтрансформхинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-143">Эта функция не реализована.</span><span class="sxs-lookup"><span data-stu-id="674e6-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>двмжеттранспортаттрибутес</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-145">Получает атрибуты транспорта.</span><span class="sxs-lookup"><span data-stu-id="674e6-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>двмжетунметтабрекуирементс</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="674e6-147">
<strong>Примечание</strong>  .  Эта функция является общедоступной, но нефункциональной для Windows 10, версии 1803.</span><span class="sxs-lookup"><span data-stu-id="674e6-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="674e6-148">Проверяет требования, необходимые для получения вкладок в строке заголовка приложения для указанного окна.</span><span class="sxs-lookup"><span data-stu-id="674e6-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>двмжетвиндоваттрибуте</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-150">Извлекает текущее значение указанного атрибута, примененного к окну.</span><span class="sxs-lookup"><span data-stu-id="674e6-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>двминвалидатеиконикбитмапс</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-152">Вызывается приложением для указания того, что все ранее предоставленные точечные рисунки из окна, как эскизы, так и Просмотр представлений, должны быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="674e6-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-154">Получает значение, указывающее, включена ли композиция DWM.</span><span class="sxs-lookup"><span data-stu-id="674e6-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="674e6-155">Приложения на компьютерах под управлением Windows 7 или более ранней версии могут прослушивать изменения состояния композиции, обрабатывая уведомление <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="674e6-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>двммодифипревиаусдксфрамедуратион</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-157">Изменяет число обновлений монитора, с помощью которых будет отображаться предыдущий кадр.</span><span class="sxs-lookup"><span data-stu-id="674e6-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="674e6-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Двммодифипревиаусдксфрамедуратион</strong></a> больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="674e6-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="674e6-159">Начиная с Windows 8.1, вызовы метода <strong>двммодифипревиаусдксфрамедуратион</strong> всегда возвращают E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="674e6-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>двмкуерисумбнаилсаурцесизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-161">Получает исходный размер эскиза DWM.</span><span class="sxs-lookup"><span data-stu-id="674e6-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-163">Создает отношение эскиза DWM между конечным и исходным окнами.</span><span class="sxs-lookup"><span data-stu-id="674e6-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>двмрендержестуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-165">Уведомляет DWM о том, что Контактное лицо было распознано как жест, и что DWM должен нарисовать отзыв для этого жеста.</span><span class="sxs-lookup"><span data-stu-id="674e6-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>двмсетдксфрамедуратион</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-167">Задает число обновлений монитора, по которым отображается отображаемый кадр.</span><span class="sxs-lookup"><span data-stu-id="674e6-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="674e6-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Двмсетдксфрамедуратион</strong></a> больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="674e6-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="674e6-169">Начиная с Windows 8.1, вызовы метода <strong>двмсетдксфрамедуратион</strong> всегда возвращают E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="674e6-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>двмсетиконикливепревиевбитмап</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-171">Задает статический точечный рисунок для отображения <em>динамического предварительного просмотра</em> (также известного как <em>Предварительный просмотр</em>) окна или вкладки. Панель задач может использовать это растровое изображение, чтобы отобразить полный предварительный просмотр окна или вкладки.</span><span class="sxs-lookup"><span data-stu-id="674e6-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>двмсетикониксумбнаил</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-173">Задает статический точечный рисунок на окне или вкладке для использования в качестве эскиза.</span><span class="sxs-lookup"><span data-stu-id="674e6-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="674e6-174">Панель задач может использовать это растровое изображение в качестве цели переключателя эскиза для окна или вкладки.</span><span class="sxs-lookup"><span data-stu-id="674e6-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>двмсетпресентпараметерс</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-176">Задает существующие параметры для компоновки кадра.</span><span class="sxs-lookup"><span data-stu-id="674e6-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="674e6-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Двмсетпресентпараметерс</strong></a> больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="674e6-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="674e6-178">Начиная с Windows 8.1, вызовы метода <strong>двмсетпресентпараметерс</strong> всегда возвращают E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="674e6-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>двмсетвиндоваттрибуте</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-180">Задает значение для атрибутов окна, не являющихся клиентским рендерингом.</span><span class="sxs-lookup"><span data-stu-id="674e6-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>двмшовконтакт</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-182">Вызывается приложением или платформой для указания типа визуальной обратной связи для отображения в ответ на конкретный контакт или связь с пером.</span><span class="sxs-lookup"><span data-stu-id="674e6-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>двмтесерконтакт</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-184">Позволяет выполнять графический отзыв о сенсорном взаимодействии и перетаскивать взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="674e6-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>двмтранситионовнедвиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-186">Координирует анимацию окон инструментов с помощью DWM.</span><span class="sxs-lookup"><span data-stu-id="674e6-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="674e6-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>двмунрегистерсумбнаил</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-188">Удаляет связь эскиза DWM, созданную функцией <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="674e6-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="674e6-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="674e6-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="674e6-190">Обновляет свойства эскиза DWM.</span><span class="sxs-lookup"><span data-stu-id="674e6-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

