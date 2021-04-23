---
title: Справочник по диспетчеру аудиосжатия
description: Справочник по диспетчеру аудиосжатия
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Мультимедиа Windows, Справочник по ACM
- мультимедиа, Справочник по ACM
- мультимедиа аудио, Справочник по ACM
- аудио, Справочник по ACM)
- Диспетчер аудиосжатия (ACM), Справочник
- ACM (диспетчер аудиосжатия), справочные материалы
- Справочник по ACM, сведения
- Справочник по ACM, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533107"
---
# <a name="audio-compression-manager-reference"></a><span data-ttu-id="539ec-111">Справочник по диспетчеру аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="539ec-111">Audio Compression Manager Reference</span></span>

<span data-ttu-id="539ec-112">В этом разделе описываются функции, структуры и сообщения, связанные с ACM.</span><span class="sxs-lookup"><span data-stu-id="539ec-112">This section describes the functions, structures, and messages associated with the ACM.</span></span> <span data-ttu-id="539ec-113">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="539ec-113">These elements are grouped as follows.</span></span>

## <a name="drivers"></a><span data-ttu-id="539ec-114">драйверы,</span><span class="sxs-lookup"><span data-stu-id="539ec-114">Drivers</span></span>

-   [<span data-ttu-id="539ec-115">**акмдриверадд**</span><span class="sxs-lookup"><span data-stu-id="539ec-115">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="539ec-116">**акмдриверклосе**</span><span class="sxs-lookup"><span data-stu-id="539ec-116">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="539ec-117">**акмдривердетаилс**</span><span class="sxs-lookup"><span data-stu-id="539ec-117">**ACMDRIVERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [<span data-ttu-id="539ec-118">**акмдриверенум**</span><span class="sxs-lookup"><span data-stu-id="539ec-118">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="539ec-119">**акмдриверенумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="539ec-119">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="539ec-120">**акмдриверид**</span><span class="sxs-lookup"><span data-stu-id="539ec-120">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="539ec-121">**акмдривермессаже**</span><span class="sxs-lookup"><span data-stu-id="539ec-121">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="539ec-122">**акмдриверопен**</span><span class="sxs-lookup"><span data-stu-id="539ec-122">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="539ec-123">**акмдриверприорити**</span><span class="sxs-lookup"><span data-stu-id="539ec-123">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="539ec-124">**акмдриверпрок**</span><span class="sxs-lookup"><span data-stu-id="539ec-124">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="539ec-125">**акмдриверремове**</span><span class="sxs-lookup"><span data-stu-id="539ec-125">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a><span data-ttu-id="539ec-126">фильтры;</span><span class="sxs-lookup"><span data-stu-id="539ec-126">Filters</span></span>

-   [<span data-ttu-id="539ec-127">**акмфилтерчусе**</span><span class="sxs-lookup"><span data-stu-id="539ec-127">**ACMFILTERCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [<span data-ttu-id="539ec-128">**акмфилтерчусехукпрок**</span><span class="sxs-lookup"><span data-stu-id="539ec-128">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="539ec-129">**акмфилтердетаилс**</span><span class="sxs-lookup"><span data-stu-id="539ec-129">**ACMFILTERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [<span data-ttu-id="539ec-130">**акмфилтеренум**</span><span class="sxs-lookup"><span data-stu-id="539ec-130">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="539ec-131">**акмфилтеренумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="539ec-131">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="539ec-132">**акмфилтертагдетаилс**</span><span class="sxs-lookup"><span data-stu-id="539ec-132">**ACMFILTERTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="539ec-133">**акмфилтертаженум**</span><span class="sxs-lookup"><span data-stu-id="539ec-133">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="539ec-134">**акмфилтертаженумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="539ec-134">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a><span data-ttu-id="539ec-135">Форматы</span><span class="sxs-lookup"><span data-stu-id="539ec-135">Formats</span></span>

-   [<span data-ttu-id="539ec-136">**акмформатчусе**</span><span class="sxs-lookup"><span data-stu-id="539ec-136">**ACMFORMATCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [<span data-ttu-id="539ec-137">**акмформатчусехукпрок**</span><span class="sxs-lookup"><span data-stu-id="539ec-137">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="539ec-138">**акмформатдетаилс**</span><span class="sxs-lookup"><span data-stu-id="539ec-138">**ACMFORMATDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [<span data-ttu-id="539ec-139">**акмформатенум**</span><span class="sxs-lookup"><span data-stu-id="539ec-139">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="539ec-140">**акмформатенумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="539ec-140">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="539ec-141">**акмформатсугжест**</span><span class="sxs-lookup"><span data-stu-id="539ec-141">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="539ec-142">**акмформаттагдетаилс**</span><span class="sxs-lookup"><span data-stu-id="539ec-142">**ACMFORMATTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [<span data-ttu-id="539ec-143">**акмформаттаженум**</span><span class="sxs-lookup"><span data-stu-id="539ec-143">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="539ec-144">**акмформаттаженумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="539ec-144">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a><span data-ttu-id="539ec-145">Сообщения</span><span class="sxs-lookup"><span data-stu-id="539ec-145">Messages</span></span>

-   [<span data-ttu-id="539ec-146">**MM \_ ACM \_ филтерчусе**</span><span class="sxs-lookup"><span data-stu-id="539ec-146">**MM\_ACM\_FILTERCHOOSE**</span></span>](mm-acm-filterchoose.md)
-   [<span data-ttu-id="539ec-147">**MM \_ ACM \_ форматчусе**</span><span class="sxs-lookup"><span data-stu-id="539ec-147">**MM\_ACM\_FORMATCHOOSE**</span></span>](mm-acm-formatchoose.md)

## <a name="streams"></a><span data-ttu-id="539ec-148">Потоки</span><span class="sxs-lookup"><span data-stu-id="539ec-148">Streams</span></span>

-   [<span data-ttu-id="539ec-149">**акмстреамклосе**</span><span class="sxs-lookup"><span data-stu-id="539ec-149">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="539ec-150">**акмстреамконверт**</span><span class="sxs-lookup"><span data-stu-id="539ec-150">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="539ec-151">[**акмстреамконверткаллбакк**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="539ec-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="539ec-152">**акмстреамхеадер**</span><span class="sxs-lookup"><span data-stu-id="539ec-152">**ACMSTREAMHEADER**</span></span>](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [<span data-ttu-id="539ec-153">**акмстреаммессаже**</span><span class="sxs-lookup"><span data-stu-id="539ec-153">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="539ec-154">**акмстреамопен**</span><span class="sxs-lookup"><span data-stu-id="539ec-154">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="539ec-155">**акмстреампрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="539ec-155">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="539ec-156">**акмстреамресет**</span><span class="sxs-lookup"><span data-stu-id="539ec-156">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="539ec-157">**акмстреамсизе**</span><span class="sxs-lookup"><span data-stu-id="539ec-157">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="539ec-158">**акмстреамунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="539ec-158">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a><span data-ttu-id="539ec-159">Разное</span><span class="sxs-lookup"><span data-stu-id="539ec-159">Miscellaneous</span></span>

-   [<span data-ttu-id="539ec-160">**акмжетверсион**</span><span class="sxs-lookup"><span data-stu-id="539ec-160">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="539ec-161">**акмметрикс**</span><span class="sxs-lookup"><span data-stu-id="539ec-161">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a><span data-ttu-id="539ec-162">См. также</span><span class="sxs-lookup"><span data-stu-id="539ec-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="539ec-163">Диспетчер аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="539ec-163">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> </dl>

 

 