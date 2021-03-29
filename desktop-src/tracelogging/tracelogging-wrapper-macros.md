---
title: Макросы оболочки Трацелоггинг
description: Содержит список макросов-оболочек для поставщиков Трацелоггинг.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779688"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="783d9-103">Макросы оболочки Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="783d9-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="783d9-104">Содержит список макросов-оболочек для поставщиков Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="783d9-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="783d9-105">Для записи событий с помощью поставщиков Трацелоггинг необходимо использовать макросы записи Трацелоггинг [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) или [**трацелоггингвритеактивити**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span><span class="sxs-lookup"><span data-stu-id="783d9-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="783d9-106">Для обоих этих макросов требуется заключить данные событий в макрос оболочки.</span><span class="sxs-lookup"><span data-stu-id="783d9-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="783d9-107">Существует несколько различных макросов-оболочек для различных типов данных.</span><span class="sxs-lookup"><span data-stu-id="783d9-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="783d9-108">Полный список макросов Трацелоггинг см. в разделе [макросы трацелоггинг](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="783d9-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="783d9-109">Помимо макросов оболочки, приведенных выше, для отдельных типов данных доступны несколько макросов.</span><span class="sxs-lookup"><span data-stu-id="783d9-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="783d9-110">Все эти макросы имеют тот же формат, что и макрос [трацелоггингвалуе](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) .</span><span class="sxs-lookup"><span data-stu-id="783d9-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="783d9-111">Можно использовать макрос Трацелоггингвалуе для автоматического определения нужного макроса-оболочки или непосредственного использования конкретного макроса.</span><span class="sxs-lookup"><span data-stu-id="783d9-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="783d9-112">**трацелоггингбинари**</span><span class="sxs-lookup"><span data-stu-id="783d9-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="783d9-113">**трацелоггингчаннел**</span><span class="sxs-lookup"><span data-stu-id="783d9-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="783d9-114">**трацелоггингкустоматтрибуте**</span><span class="sxs-lookup"><span data-stu-id="783d9-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="783d9-115">**трацелоггингдескриптион**</span><span class="sxs-lookup"><span data-stu-id="783d9-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="783d9-116">**трацелоггинжевенттаг**</span><span class="sxs-lookup"><span data-stu-id="783d9-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="783d9-117">**трацелоггингкэйворд**</span><span class="sxs-lookup"><span data-stu-id="783d9-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="783d9-118">**трацелоггинглевел**</span><span class="sxs-lookup"><span data-stu-id="783d9-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="783d9-119">**трацелоггингопкоде**</span><span class="sxs-lookup"><span data-stu-id="783d9-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="783d9-120">**трацелоггингсоккетаддресс**</span><span class="sxs-lookup"><span data-stu-id="783d9-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="783d9-121">**трацелоггингструкт**</span><span class="sxs-lookup"><span data-stu-id="783d9-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="783d9-122">**трацелоггингвалуе**</span><span class="sxs-lookup"><span data-stu-id="783d9-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="783d9-123">**Трацелоггингоптионграуп** специально предназначен для использования внутри трацелоггинг \_ определения \_ поставщика.</span><span class="sxs-lookup"><span data-stu-id="783d9-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="783d9-124">**трацелоггингоптионграуп**</span><span class="sxs-lookup"><span data-stu-id="783d9-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="783d9-125">Ниже приведены отдельные макросы-оболочки.</span><span class="sxs-lookup"><span data-stu-id="783d9-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="783d9-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="783d9-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="783d9-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="783d9-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="783d9-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="783d9-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="783d9-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="783d9-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="783d9-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="783d9-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="783d9-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="783d9-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="783d9-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="783d9-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="783d9-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="783d9-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="783d9-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="783d9-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="783d9-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="783d9-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="783d9-136">трацелоггингбул</span><span class="sxs-lookup"><span data-stu-id="783d9-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="783d9-137">трацелоггингфилетиме</span><span class="sxs-lookup"><span data-stu-id="783d9-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="783d9-138">трацелоггинггуид</span><span class="sxs-lookup"><span data-stu-id="783d9-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="783d9-139">трацелоггингпоинтер</span><span class="sxs-lookup"><span data-stu-id="783d9-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="783d9-140">трацелоггингсистемтиме</span><span class="sxs-lookup"><span data-stu-id="783d9-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="783d9-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="783d9-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="783d9-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="783d9-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="783d9-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="783d9-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="783d9-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="783d9-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="783d9-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="783d9-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="783d9-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="783d9-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="783d9-147">трацелоггингвчар</span><span class="sxs-lookup"><span data-stu-id="783d9-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="783d9-148">трацелоггингчар</span><span class="sxs-lookup"><span data-stu-id="783d9-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="783d9-149">трацелоггингинтптр</span><span class="sxs-lookup"><span data-stu-id="783d9-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="783d9-150">трацелоггингуинтптр</span><span class="sxs-lookup"><span data-stu-id="783d9-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="783d9-151">трацелоггингбулеан</span><span class="sxs-lookup"><span data-stu-id="783d9-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="783d9-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="783d9-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="783d9-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="783d9-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="783d9-154">трацелоггингпид</span><span class="sxs-lookup"><span data-stu-id="783d9-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="783d9-155">трацелоггингтид</span><span class="sxs-lookup"><span data-stu-id="783d9-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="783d9-156">трацелоггингпорт</span><span class="sxs-lookup"><span data-stu-id="783d9-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="783d9-157">трацелоггингвинеррор</span><span class="sxs-lookup"><span data-stu-id="783d9-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="783d9-158">трацелоггингнтстатус</span><span class="sxs-lookup"><span data-stu-id="783d9-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="783d9-159">трацелоггингхресулт</span><span class="sxs-lookup"><span data-stu-id="783d9-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="783d9-160">трацелоггингсоккетаддресс</span><span class="sxs-lookup"><span data-stu-id="783d9-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="783d9-161">трацелоггингсид</span><span class="sxs-lookup"><span data-stu-id="783d9-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="783d9-162">трацелоггингстринг</span><span class="sxs-lookup"><span data-stu-id="783d9-162">TraceLoggingString</span></span>

-   <span data-ttu-id="783d9-163">трацелоггингвидестринг</span><span class="sxs-lookup"><span data-stu-id="783d9-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="783d9-164">трацелоггингкаунтедстринг</span><span class="sxs-lookup"><span data-stu-id="783d9-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="783d9-165">трацелоггингкаунтедвидестринг</span><span class="sxs-lookup"><span data-stu-id="783d9-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="783d9-166">трацелоггингансистринг</span><span class="sxs-lookup"><span data-stu-id="783d9-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="783d9-167">трацелоггингуникодестринг</span><span class="sxs-lookup"><span data-stu-id="783d9-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="783d9-168">Трацелоггингбинари (пустые \* данные, размер данных в байтах, \[ необязательное \] имя) параметры этого макроса отличаются от указанных выше.</span><span class="sxs-lookup"><span data-stu-id="783d9-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="783d9-169">Если указан параметр *Name* , он должен быть строковым литералом (а не переменной) и не может содержать внедренные символы NULL.</span><span class="sxs-lookup"><span data-stu-id="783d9-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="783d9-170">Если параметр *Name* не указан, имя создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="783d9-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="783d9-171">API Трацелоггинг также делает несколько макросов доступными для массивов.</span><span class="sxs-lookup"><span data-stu-id="783d9-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="783d9-172">Эти массивы могут иметь фиксированную длину или иметь переменную длину в зависимости от того, какой макрос оболочки вы решили использовать.</span><span class="sxs-lookup"><span data-stu-id="783d9-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="783d9-173">Все эти макросы-оболочки соответствуют этому формату.</span><span class="sxs-lookup"><span data-stu-id="783d9-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="783d9-174">Параметр *пвалс* указывает на массив данных, а *квалс* указывает количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="783d9-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="783d9-175">*квалс* должен быть константой и не может быть переменной.</span><span class="sxs-lookup"><span data-stu-id="783d9-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="783d9-176">Как и в случае с макросами одного значения, *Name*, **DESC** и *Tags* являются необязательными параметрами и должны следовать тем же ограничениям, которые описаны в макросе **трацелоггингвалуе** .</span><span class="sxs-lookup"><span data-stu-id="783d9-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="783d9-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="783d9-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="783d9-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="783d9-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="783d9-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="783d9-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="783d9-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="783d9-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="783d9-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="783d9-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="783d9-187">трацелоггингбулфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="783d9-188">трацелоггинггуидфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="783d9-189">трацелоггингпоинтерфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="783d9-190">трацелоггингфилетимефикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="783d9-191">трацелоггингсистемтимефикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="783d9-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="783d9-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="783d9-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="783d9-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="783d9-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="783d9-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="783d9-198">трацелоггингвчарфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="783d9-199">трацелоггингчарфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="783d9-200">трацелоггингинтптрфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="783d9-201">трацелоггингуинтптрфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="783d9-202">трацелоггингбулеанфикседаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="783d9-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="783d9-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="783d9-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="783d9-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="783d9-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="783d9-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="783d9-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="783d9-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="783d9-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="783d9-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="783d9-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="783d9-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="783d9-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="783d9-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="783d9-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="783d9-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="783d9-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="783d9-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="783d9-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="783d9-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="783d9-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="783d9-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="783d9-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="783d9-215">трацелоггингбуларрай</span><span class="sxs-lookup"><span data-stu-id="783d9-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="783d9-216">трацелоггинггуидаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="783d9-217">трацелоггингпоинтераррай</span><span class="sxs-lookup"><span data-stu-id="783d9-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="783d9-218">трацелоггингфилетимеаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="783d9-219">трацелоггингсистемтимеаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="783d9-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="783d9-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="783d9-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="783d9-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="783d9-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="783d9-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="783d9-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="783d9-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="783d9-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="783d9-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="783d9-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="783d9-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="783d9-226">трацелоггингвчараррай</span><span class="sxs-lookup"><span data-stu-id="783d9-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="783d9-227">трацелоггингчараррай</span><span class="sxs-lookup"><span data-stu-id="783d9-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="783d9-228">трацелоггингинтптраррай</span><span class="sxs-lookup"><span data-stu-id="783d9-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="783d9-229">трацелоггингуинтптраррай</span><span class="sxs-lookup"><span data-stu-id="783d9-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="783d9-230">трацелоггингбулеанаррай</span><span class="sxs-lookup"><span data-stu-id="783d9-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="783d9-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="783d9-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="783d9-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="783d9-232">TraceLoggingHexUInt16Array</span></span>

 

 




