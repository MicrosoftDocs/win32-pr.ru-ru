---
title: Справочник по диспетчеру сжатия видео
description: Справочник по диспетчеру сжатия видео
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Видео для Windows (VFW), диспетчер сжатия видео (ВКМ)
- VFW (видео для Windows), диспетчер сжатия видео (ВКМ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252965"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="d2e95-105">Справочник по диспетчеру сжатия видео</span><span class="sxs-lookup"><span data-stu-id="d2e95-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="d2e95-106">В этом разделе описываются функции, структуры, сообщения и макросы, связанные с ВКМ.</span><span class="sxs-lookup"><span data-stu-id="d2e95-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="d2e95-107">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d2e95-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="d2e95-108">Установка и удаление программы сжатия</span><span class="sxs-lookup"><span data-stu-id="d2e95-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="d2e95-109">**иЦинсталл**</span><span class="sxs-lookup"><span data-stu-id="d2e95-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="d2e95-110">**иклокате**</span><span class="sxs-lookup"><span data-stu-id="d2e95-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="d2e95-111">**икопен**</span><span class="sxs-lookup"><span data-stu-id="d2e95-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="d2e95-112">**икклосе**</span><span class="sxs-lookup"><span data-stu-id="d2e95-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="d2e95-113">**икремове**</span><span class="sxs-lookup"><span data-stu-id="d2e95-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="d2e95-114">**икопенфунктион**</span><span class="sxs-lookup"><span data-stu-id="d2e95-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="d2e95-115">Поиск и открытие программы сжатия</span><span class="sxs-lookup"><span data-stu-id="d2e95-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="d2e95-116">**иклокате**</span><span class="sxs-lookup"><span data-stu-id="d2e95-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="d2e95-117">**икопен**</span><span class="sxs-lookup"><span data-stu-id="d2e95-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="d2e95-118">**икдекомпрессопен**</span><span class="sxs-lookup"><span data-stu-id="d2e95-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="d2e95-119">**икдравопен**</span><span class="sxs-lookup"><span data-stu-id="d2e95-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="d2e95-120">**иЦинфо**</span><span class="sxs-lookup"><span data-stu-id="d2e95-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="d2e95-121">**икклосе**</span><span class="sxs-lookup"><span data-stu-id="d2e95-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="d2e95-122">Выбор сжатия</span><span class="sxs-lookup"><span data-stu-id="d2e95-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="d2e95-123">**иккомпрессорчусе**</span><span class="sxs-lookup"><span data-stu-id="d2e95-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="d2e95-124">**иккомпрессорфри**</span><span class="sxs-lookup"><span data-stu-id="d2e95-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="d2e95-125">**компварс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="d2e95-126">Настройка компрессоров</span><span class="sxs-lookup"><span data-stu-id="d2e95-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="d2e95-127">**\_Настройка ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="d2e95-128">**ICM — \_ состояние**</span><span class="sxs-lookup"><span data-stu-id="d2e95-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="d2e95-129">**ICM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="d2e95-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="d2e95-130">**иксендмессаже**</span><span class="sxs-lookup"><span data-stu-id="d2e95-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="d2e95-131">Сведения о компрессоре</span><span class="sxs-lookup"><span data-stu-id="d2e95-131">Compressor Information</span></span>

-   [<span data-ttu-id="d2e95-132">**икжетинфо**</span><span class="sxs-lookup"><span data-stu-id="d2e95-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="d2e95-133">**иЦинфо**</span><span class="sxs-lookup"><span data-stu-id="d2e95-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="d2e95-134">**ICM \_ жетдефаулткэйфрамерате**</span><span class="sxs-lookup"><span data-stu-id="d2e95-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="d2e95-135">**икжетдисплайформат**</span><span class="sxs-lookup"><span data-stu-id="d2e95-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="d2e95-136">**ICM \_ жетдефаулткуалити**</span><span class="sxs-lookup"><span data-stu-id="d2e95-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="d2e95-137">**ICM \_ о**</span><span class="sxs-lookup"><span data-stu-id="d2e95-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="d2e95-138">Сжатие одного образа</span><span class="sxs-lookup"><span data-stu-id="d2e95-138">Single Image Compression</span></span>

-   [<span data-ttu-id="d2e95-139">**иЦимажекомпресс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="d2e95-140">Сжатие последовательностей</span><span class="sxs-lookup"><span data-stu-id="d2e95-140">Sequence Compression</span></span>

-   [<span data-ttu-id="d2e95-141">**иксеккомпрессфраме**</span><span class="sxs-lookup"><span data-stu-id="d2e95-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="d2e95-142">**иксеккомпрессфраместарт**</span><span class="sxs-lookup"><span data-stu-id="d2e95-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="d2e95-143">**иксеккомпрессфраминд**</span><span class="sxs-lookup"><span data-stu-id="d2e95-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="d2e95-144">компварс</span><span class="sxs-lookup"><span data-stu-id="d2e95-144">COMPVARS</span></span>

-   [<span data-ttu-id="d2e95-145">**иккомпрессорчусе**</span><span class="sxs-lookup"><span data-stu-id="d2e95-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="d2e95-146">Сжатие данных изображения</span><span class="sxs-lookup"><span data-stu-id="d2e95-146">Image Data Compression</span></span>

-   [<span data-ttu-id="d2e95-147">**иккомпресс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="d2e95-148">**\_ \_ \_ формат получения формата ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="d2e95-149">**\_запрос СЖАТИЯ \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="d2e95-150">**\_сжатие для \_ получения \_ размера ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="d2e95-151">**\_Начало СЖАТИЯ \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="d2e95-152">**\_ \_ Окончание сжатия ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="d2e95-153">Мониторинг сжатия</span><span class="sxs-lookup"><span data-stu-id="d2e95-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="d2e95-154">**иксетстатуспрок**</span><span class="sxs-lookup"><span data-stu-id="d2e95-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="d2e95-155">Распаковка отдельных образов</span><span class="sxs-lookup"><span data-stu-id="d2e95-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="d2e95-156">**иЦимажедекомпресс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="d2e95-157">Распаковка данных изображения</span><span class="sxs-lookup"><span data-stu-id="d2e95-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="d2e95-158">**икдекомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="d2e95-159">**икдекомпрессексбегин**</span><span class="sxs-lookup"><span data-stu-id="d2e95-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="d2e95-160">**\_ДЕКОМПРЕССЕКС ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="d2e95-161">**\_ \_ Получение формата для РАСПАКОВКи ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="d2e95-162">**\_ \_ извлечь ПАЛИТРУ ICM распаковки \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="d2e95-163">**икдекомпрессекскуери**</span><span class="sxs-lookup"><span data-stu-id="d2e95-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="d2e95-164">**икдекомпресс**</span><span class="sxs-lookup"><span data-stu-id="d2e95-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="d2e95-165">**\_Начало распаковки \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="d2e95-166">**\_Окончание распаковки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="d2e95-167">**\_распаковать \_ запрос ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="d2e95-168">Использование Hardware-Drawing возможностей</span><span class="sxs-lookup"><span data-stu-id="d2e95-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="d2e95-169">**икжетинфо**</span><span class="sxs-lookup"><span data-stu-id="d2e95-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="d2e95-170">**икдравбегин**</span><span class="sxs-lookup"><span data-stu-id="d2e95-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="d2e95-171">**\_Окончание прорисовки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="d2e95-172">**\_Вывод на \_ диск с ICM**</span><span class="sxs-lookup"><span data-stu-id="d2e95-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="d2e95-173">**\_запрос ICM Draw \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="d2e95-174">**икдравсугжестформат**</span><span class="sxs-lookup"><span data-stu-id="d2e95-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="d2e95-175">**\_Начало прорисовки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="d2e95-176">**\_Завершение прорисовки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="d2e95-177">**ICM \_ жетбуфферсвантед**</span><span class="sxs-lookup"><span data-stu-id="d2e95-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="d2e95-178">**\_выясняется прорисовка ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="d2e95-179">**икдравопен**</span><span class="sxs-lookup"><span data-stu-id="d2e95-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="d2e95-180">**икдрав**</span><span class="sxs-lookup"><span data-stu-id="d2e95-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="d2e95-181">**\_время прорисовки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="d2e95-182">**ICM \_ Draw \_ SETTIME**</span><span class="sxs-lookup"><span data-stu-id="d2e95-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="d2e95-183">**\_окно вырисовки ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="d2e95-184">**\_выясняется прорисовка ICM \_**</span><span class="sxs-lookup"><span data-stu-id="d2e95-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="d2e95-185">**ICM \_ Draw \_ чанжепалетте**</span><span class="sxs-lookup"><span data-stu-id="d2e95-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="d2e95-186">**ICM \_ Draw \_ рендербуффер**</span><span class="sxs-lookup"><span data-stu-id="d2e95-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="d2e95-187">См. также</span><span class="sxs-lookup"><span data-stu-id="d2e95-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e95-188">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="d2e95-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




