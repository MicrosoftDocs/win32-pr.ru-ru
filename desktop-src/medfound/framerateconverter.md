---
description: Изменяет частоту кадров потока видео.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Средство преобразования частоты кадров DSP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808074"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="2a206-103">Средство преобразования частоты кадров DSP</span><span class="sxs-lookup"><span data-stu-id="2a206-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="2a206-104">Изменяет частоту кадров потока видео.</span><span class="sxs-lookup"><span data-stu-id="2a206-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="2a206-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="2a206-105">CLSID</span></span>

<span data-ttu-id="2a206-106">\_КФРАМЕРАТЕКОНВЕРТДМО CLSID</span><span class="sxs-lookup"><span data-stu-id="2a206-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="2a206-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="2a206-107">Interfaces</span></span>

-   <span data-ttu-id="2a206-108">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="2a206-108">**IMediaObject**</span></span>
-   <span data-ttu-id="2a206-109">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="2a206-109">**IMFTransform**</span></span>
-   <span data-ttu-id="2a206-110">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="2a206-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="2a206-111">Форматы</span><span class="sxs-lookup"><span data-stu-id="2a206-111">Formats</span></span>

-   <span data-ttu-id="2a206-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="2a206-112">ARGB 32</span></span>
-   <span data-ttu-id="2a206-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="2a206-113">RGB 24</span></span>
-   <span data-ttu-id="2a206-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="2a206-114">RGB 32</span></span>
-   <span data-ttu-id="2a206-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="2a206-115">RGB 555</span></span>
-   <span data-ttu-id="2a206-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="2a206-116">RGB 565</span></span>
-   <span data-ttu-id="2a206-117">айув</span><span class="sxs-lookup"><span data-stu-id="2a206-117">AYUV</span></span>
-   <span data-ttu-id="2a206-118">ийув</span><span class="sxs-lookup"><span data-stu-id="2a206-118">IYUV</span></span>
-   <span data-ttu-id="2a206-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="2a206-119">UYVY</span></span>
-   <span data-ttu-id="2a206-120">Y211</span><span class="sxs-lookup"><span data-stu-id="2a206-120">Y211</span></span>
-   <span data-ttu-id="2a206-121">Y411</span><span class="sxs-lookup"><span data-stu-id="2a206-121">Y411</span></span>
-   <span data-ttu-id="2a206-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="2a206-122">Y41P</span></span>
-   <span data-ttu-id="2a206-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="2a206-123">YUY2</span></span>
-   <span data-ttu-id="2a206-124">юив</span><span class="sxs-lookup"><span data-stu-id="2a206-124">YUYV</span></span>
-   <span data-ttu-id="2a206-125">YV12</span><span class="sxs-lookup"><span data-stu-id="2a206-125">YV12</span></span>
-   <span data-ttu-id="2a206-126">ивю</span><span class="sxs-lookup"><span data-stu-id="2a206-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="2a206-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a206-127">Properties</span></span>

-   [<span data-ttu-id="2a206-128">МФПКЭЙ \_ , \_ инпутфрамерате</span><span class="sxs-lookup"><span data-stu-id="2a206-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="2a206-129">МФПКЭЙ \_ , \_ аутпутфрамерате</span><span class="sxs-lookup"><span data-stu-id="2a206-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="2a206-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a206-130">Remarks</span></span>

<span data-ttu-id="2a206-131">Этот DSP изменяет частоту кадров путем повторения или удаления кадров.</span><span class="sxs-lookup"><span data-stu-id="2a206-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="2a206-132">По умолчанию DSP получает частоту кадров из типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a206-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="2a206-133">Кроме того, можно указать частоту кадров, задав свойства МФПКЭЙ, \_ \_ ИНПУТФРАМЕРАТЕ и мфпкэй \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a206-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="2a206-134">Эти значения переопределяют частоту кадров, заданную в типе носителя.</span><span class="sxs-lookup"><span data-stu-id="2a206-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="2a206-135">Однако при использовании этого DSP в конвейере Media Foundation не следует задавать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2a206-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a206-136">Требования</span><span class="sxs-lookup"><span data-stu-id="2a206-136">Requirements</span></span>



| <span data-ttu-id="2a206-137">Требование</span><span class="sxs-lookup"><span data-stu-id="2a206-137">Requirement</span></span> | <span data-ttu-id="2a206-138">Значение</span><span class="sxs-lookup"><span data-stu-id="2a206-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a206-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a206-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2a206-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a206-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2a206-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a206-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2a206-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a206-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a206-143">Header</span><span class="sxs-lookup"><span data-stu-id="2a206-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a206-144"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a206-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="2a206-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2a206-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a206-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a206-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a206-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a206-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a206-148">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="2a206-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




