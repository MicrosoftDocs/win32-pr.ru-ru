---
title: Справочник по Авифиле
description: Справочник по Авифиле
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068527"
---
# <a name="avifile-reference"></a><span data-ttu-id="701f4-103">Справочник по Авифиле</span><span class="sxs-lookup"><span data-stu-id="701f4-103">AVIFile Reference</span></span>

<span data-ttu-id="701f4-104">В этом разделе описываются функции, структуры и макросы для приложений, использующих службы Авифиле Services.</span><span class="sxs-lookup"><span data-stu-id="701f4-104">This section describes the functions, structures, and macros for applications using the AVIFile services.</span></span> <span data-ttu-id="701f4-105">Эти элементы группируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="701f4-105">These elements are grouped as follows:</span></span>

## <a name="avifile-library-operations"></a><span data-ttu-id="701f4-106">Операции с библиотекой Авифиле</span><span class="sxs-lookup"><span data-stu-id="701f4-106">AVIFile Library Operations</span></span>

-   [<span data-ttu-id="701f4-107">**авифилеинит**</span><span class="sxs-lookup"><span data-stu-id="701f4-107">**AVIFileInit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [<span data-ttu-id="701f4-108">**авифиликсит**</span><span class="sxs-lookup"><span data-stu-id="701f4-108">**AVIFileExit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a><span data-ttu-id="701f4-109">Открытие и закрытие AVI файлов</span><span class="sxs-lookup"><span data-stu-id="701f4-109">Opening and Closing AVI Files</span></span>

-   [<span data-ttu-id="701f4-110">**авифилеопен**</span><span class="sxs-lookup"><span data-stu-id="701f4-110">**AVIFileOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [<span data-ttu-id="701f4-111">**авифилеаддреф**</span><span class="sxs-lookup"><span data-stu-id="701f4-111">**AVIFileAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [<span data-ttu-id="701f4-112">**авифилерелеасе**</span><span class="sxs-lookup"><span data-stu-id="701f4-112">**AVIFileRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [<span data-ttu-id="701f4-113">**жетопенфиленамепревиев**</span><span class="sxs-lookup"><span data-stu-id="701f4-113">**GetOpenFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a><span data-ttu-id="701f4-114">Чтение из файла</span><span class="sxs-lookup"><span data-stu-id="701f4-114">Reading from a File</span></span>

-   [<span data-ttu-id="701f4-115">**авифилеинфо**</span><span class="sxs-lookup"><span data-stu-id="701f4-115">**AVIFileInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [<span data-ttu-id="701f4-116">**авифилеинфо**</span><span class="sxs-lookup"><span data-stu-id="701f4-116">**AVIFILEINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [<span data-ttu-id="701f4-117">**авифилереаддата**</span><span class="sxs-lookup"><span data-stu-id="701f4-117">**AVIFileReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a><span data-ttu-id="701f4-118">Запись в файл</span><span class="sxs-lookup"><span data-stu-id="701f4-118">Writing to a File</span></span>

-   [<span data-ttu-id="701f4-119">**авифилевритедата**</span><span class="sxs-lookup"><span data-stu-id="701f4-119">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a><span data-ttu-id="701f4-120">Использование буфера обмена</span><span class="sxs-lookup"><span data-stu-id="701f4-120">Using the Clipboard</span></span>

-   [<span data-ttu-id="701f4-121">**авипутфилеонклипбоард**</span><span class="sxs-lookup"><span data-stu-id="701f4-121">**AVIPutFileOnClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [<span data-ttu-id="701f4-122">**авижетфромклипбоард**</span><span class="sxs-lookup"><span data-stu-id="701f4-122">**AVIGetFromClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [<span data-ttu-id="701f4-123">**авиклеарклипбоард**</span><span class="sxs-lookup"><span data-stu-id="701f4-123">**AVIClearClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a><span data-ttu-id="701f4-124">Открытие и закрытие потоков</span><span class="sxs-lookup"><span data-stu-id="701f4-124">Opening and Closing Streams</span></span>

-   [<span data-ttu-id="701f4-125">**авифилежетстреам**</span><span class="sxs-lookup"><span data-stu-id="701f4-125">**AVIFileGetStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [<span data-ttu-id="701f4-126">**авистреамопенфромфиле**</span><span class="sxs-lookup"><span data-stu-id="701f4-126">**AVIStreamOpenFromFile**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [<span data-ttu-id="701f4-127">**авистреамаддреф**</span><span class="sxs-lookup"><span data-stu-id="701f4-127">**AVIStreamAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [<span data-ttu-id="701f4-128">**авистреамрелеасе**</span><span class="sxs-lookup"><span data-stu-id="701f4-128">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a><span data-ttu-id="701f4-129">Чтение сведений о потоке</span><span class="sxs-lookup"><span data-stu-id="701f4-129">Reading Stream Information</span></span>

-   [<span data-ttu-id="701f4-130">**авистреаминфо**</span><span class="sxs-lookup"><span data-stu-id="701f4-130">**AVISTREAMINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [<span data-ttu-id="701f4-131">**авистреамреаддата**</span><span class="sxs-lookup"><span data-stu-id="701f4-131">**AVIStreamReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [<span data-ttu-id="701f4-132">**авистреамдатасизе**</span><span class="sxs-lookup"><span data-stu-id="701f4-132">**AVIStreamDataSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [<span data-ttu-id="701f4-133">**авистреамреадформат**</span><span class="sxs-lookup"><span data-stu-id="701f4-133">**AVIStreamReadFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [<span data-ttu-id="701f4-134">**авистреамформатсизе**</span><span class="sxs-lookup"><span data-stu-id="701f4-134">**AVIStreamFormatSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [<span data-ttu-id="701f4-135">**авистреамреад**</span><span class="sxs-lookup"><span data-stu-id="701f4-135">**AVIStreamRead**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [<span data-ttu-id="701f4-136">**авистреамсамплесизе**</span><span class="sxs-lookup"><span data-stu-id="701f4-136">**AVIStreamSampleSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [<span data-ttu-id="701f4-137">**авистреамбегинстреаминг**</span><span class="sxs-lookup"><span data-stu-id="701f4-137">**AVIStreamBeginStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [<span data-ttu-id="701f4-138">**авистреамендстреаминг**</span><span class="sxs-lookup"><span data-stu-id="701f4-138">**AVIStreamEndStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a><span data-ttu-id="701f4-139">Распаковка данных видео в потоке</span><span class="sxs-lookup"><span data-stu-id="701f4-139">Decompressing Video Data in a Stream</span></span>

-   [<span data-ttu-id="701f4-140">**авистреамжетфрамеопен**</span><span class="sxs-lookup"><span data-stu-id="701f4-140">**AVIStreamGetFrameOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [<span data-ttu-id="701f4-141">**авистреамжетфраме**</span><span class="sxs-lookup"><span data-stu-id="701f4-141">**AVIStreamGetFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [<span data-ttu-id="701f4-142">**авистреамжетфрамеклосе**</span><span class="sxs-lookup"><span data-stu-id="701f4-142">**AVIStreamGetFrameClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="701f4-143">Создание файла из существующих потоков</span><span class="sxs-lookup"><span data-stu-id="701f4-143">Creating a File from Existing Streams</span></span>

-   [<span data-ttu-id="701f4-144">**ависаве**</span><span class="sxs-lookup"><span data-stu-id="701f4-144">**AVISave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [<span data-ttu-id="701f4-145">**ависавев**</span><span class="sxs-lookup"><span data-stu-id="701f4-145">**AVISaveV**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [<span data-ttu-id="701f4-146">**ависавеоптионс**</span><span class="sxs-lookup"><span data-stu-id="701f4-146">**AVISaveOptions**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [<span data-ttu-id="701f4-147">**жетсавефиленамепревиев**</span><span class="sxs-lookup"><span data-stu-id="701f4-147">**GetSaveFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [<span data-ttu-id="701f4-148">**авимакефилефромстреамс**</span><span class="sxs-lookup"><span data-stu-id="701f4-148">**AVIMakeFileFromStreams**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a><span data-ttu-id="701f4-149">Запись отдельных потоков</span><span class="sxs-lookup"><span data-stu-id="701f4-149">Writing Individual Streams</span></span>

-   [<span data-ttu-id="701f4-150">**авифилекреатестреам**</span><span class="sxs-lookup"><span data-stu-id="701f4-150">**AVIFileCreateStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [<span data-ttu-id="701f4-151">**авистреамсетформат**</span><span class="sxs-lookup"><span data-stu-id="701f4-151">**AVIStreamSetFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [<span data-ttu-id="701f4-152">**авистреамврите**</span><span class="sxs-lookup"><span data-stu-id="701f4-152">**AVIStreamWrite**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [<span data-ttu-id="701f4-153">**авифилевритедата**</span><span class="sxs-lookup"><span data-stu-id="701f4-153">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [<span data-ttu-id="701f4-154">**авистреамвритедата**</span><span class="sxs-lookup"><span data-stu-id="701f4-154">**AVIStreamWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [<span data-ttu-id="701f4-155">**авистреамрелеасе**</span><span class="sxs-lookup"><span data-stu-id="701f4-155">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a><span data-ttu-id="701f4-156">Поиск начальной положения в потоке</span><span class="sxs-lookup"><span data-stu-id="701f4-156">Finding the Starting Position in a Stream</span></span>

-   [<span data-ttu-id="701f4-157">**авистреамстарт**</span><span class="sxs-lookup"><span data-stu-id="701f4-157">**AVIStreamStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [<span data-ttu-id="701f4-158">**авистреамстарттиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-158">**AVIStreamStartTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [<span data-ttu-id="701f4-159">**авистреамленгс**</span><span class="sxs-lookup"><span data-stu-id="701f4-159">**AVIStreamLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [<span data-ttu-id="701f4-160">**авистреамленгстиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-160">**AVIStreamLengthTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [<span data-ttu-id="701f4-161">**авистреамфиндсампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-161">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="701f4-162">**авистреаменд**</span><span class="sxs-lookup"><span data-stu-id="701f4-162">**AVIStreamEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [<span data-ttu-id="701f4-163">**авистреамендтиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-163">**AVIStreamEndTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a><span data-ttu-id="701f4-164">Поиск образца и ключевых кадров</span><span class="sxs-lookup"><span data-stu-id="701f4-164">Finding Sample and Key Frames</span></span>

-   [<span data-ttu-id="701f4-165">**авистреамфиндсампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-165">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="701f4-166">**авистреамискэйфраме**</span><span class="sxs-lookup"><span data-stu-id="701f4-166">**AVIStreamIsKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [<span data-ttu-id="701f4-167">**авистреамнеаресткэйфраме**</span><span class="sxs-lookup"><span data-stu-id="701f4-167">**AVIStreamNearestKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [<span data-ttu-id="701f4-168">**авистреамнеаресткэйфраметиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-168">**AVIStreamNearestKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [<span data-ttu-id="701f4-169">**авистреамнеарестсампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-169">**AVIStreamNearestSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [<span data-ttu-id="701f4-170">**авистреамнеарестсамплетиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-170">**AVIStreamNearestSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [<span data-ttu-id="701f4-171">**авистреамнексткэйфраме**</span><span class="sxs-lookup"><span data-stu-id="701f4-171">**AVIStreamNextKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [<span data-ttu-id="701f4-172">**авистреамнексткэйфраметиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-172">**AVIStreamNextKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [<span data-ttu-id="701f4-173">**авистреамнекстсампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-173">**AVIStreamNextSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [<span data-ttu-id="701f4-174">**авистреамнекстсамплетиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-174">**AVIStreamNextSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [<span data-ttu-id="701f4-175">**авистреампревкэйфраме**</span><span class="sxs-lookup"><span data-stu-id="701f4-175">**AVIStreamPrevKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [<span data-ttu-id="701f4-176">**авистреампревкэйфраметиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-176">**AVIStreamPrevKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [<span data-ttu-id="701f4-177">**авистреампревсампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-177">**AVIStreamPrevSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [<span data-ttu-id="701f4-178">**авистреампревсамплетиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-178">**AVIStreamPrevSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [<span data-ttu-id="701f4-179">**авистреамсамплетосампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-179">**AVIStreamSampleToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a><span data-ttu-id="701f4-180">Переключение между образцами и временем</span><span class="sxs-lookup"><span data-stu-id="701f4-180">Switching Between Samples and Time</span></span>

-   [<span data-ttu-id="701f4-181">**авистреамсамплетотиме**</span><span class="sxs-lookup"><span data-stu-id="701f4-181">**AVIStreamSampleToTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [<span data-ttu-id="701f4-182">**авистреамтиметосампле**</span><span class="sxs-lookup"><span data-stu-id="701f4-182">**AVIStreamTimeToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a><span data-ttu-id="701f4-183">Создание временных потоков</span><span class="sxs-lookup"><span data-stu-id="701f4-183">Creating Temporary Streams</span></span>

-   [<span data-ttu-id="701f4-184">**авистреамкреате**</span><span class="sxs-lookup"><span data-stu-id="701f4-184">**AVIStreamCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [<span data-ttu-id="701f4-185">**авимакекомпресседстреам**</span><span class="sxs-lookup"><span data-stu-id="701f4-185">**AVIMakeCompressedStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [<span data-ttu-id="701f4-186">**авистреамрелеасе**</span><span class="sxs-lookup"><span data-stu-id="701f4-186">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a><span data-ttu-id="701f4-187">Редактирование потоков AVI</span><span class="sxs-lookup"><span data-stu-id="701f4-187">Editing AVI Streams</span></span>

-   [<span data-ttu-id="701f4-188">**креатидитаблестреам**</span><span class="sxs-lookup"><span data-stu-id="701f4-188">**CreateEditableStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [<span data-ttu-id="701f4-189">**едитстреамкут**</span><span class="sxs-lookup"><span data-stu-id="701f4-189">**EditStreamCut**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [<span data-ttu-id="701f4-190">**едитстреамкопи**</span><span class="sxs-lookup"><span data-stu-id="701f4-190">**EditStreamCopy**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [<span data-ttu-id="701f4-191">**едитстреампасте**</span><span class="sxs-lookup"><span data-stu-id="701f4-191">**EditStreamPaste**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [<span data-ttu-id="701f4-192">**едитстреамклоне**</span><span class="sxs-lookup"><span data-stu-id="701f4-192">**EditStreamClone**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [<span data-ttu-id="701f4-193">**едитстреамсетинфо**</span><span class="sxs-lookup"><span data-stu-id="701f4-193">**EditStreamSetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [<span data-ttu-id="701f4-194">**едитстреамсетнаме**</span><span class="sxs-lookup"><span data-stu-id="701f4-194">**EditStreamSetName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a><span data-ttu-id="701f4-195">См. также</span><span class="sxs-lookup"><span data-stu-id="701f4-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="701f4-196">Функции и макросы Авифиле</span><span class="sxs-lookup"><span data-stu-id="701f4-196">AVIFile Functions and Macros</span></span>](avifile-functions-and-macros.md)
</dt> </dl>

 

 




