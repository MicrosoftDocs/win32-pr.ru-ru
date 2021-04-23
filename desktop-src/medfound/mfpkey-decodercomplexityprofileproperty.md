---
description: Указывает профиль сложности закодированного содержимого.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Свойство MFPKEY_DECODERCOMPLEXITYPROFILE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908792"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="e65f4-103">МФПКЭЙ \_ декодеркомплекситипрофиле, свойство</span><span class="sxs-lookup"><span data-stu-id="e65f4-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="e65f4-104">Указывает профиль сложности закодированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="e65f4-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e65f4-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="e65f4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e65f4-106">g \_ всзвмвкдекодеркомплекситипрофиле</span><span class="sxs-lookup"><span data-stu-id="e65f4-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="e65f4-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e65f4-107">Data Type</span></span>

<span data-ttu-id="e65f4-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="e65f4-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="e65f4-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e65f4-109">Remarks</span></span>

<span data-ttu-id="e65f4-110">Это значение можно прочитать только после завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="e65f4-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="e65f4-111">Для звука это свойство имеет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e65f4-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="e65f4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e65f4-112">Value</span></span> | <span data-ttu-id="e65f4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e65f4-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e65f4-114">L1</span><span class="sxs-lookup"><span data-stu-id="e65f4-114">"L1"</span></span>  | <span data-ttu-id="e65f4-115">Стандартная кодировка с частотой выборки 44,1 кГц и максимальной скоростью в 161 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="e65f4-116">L2</span><span class="sxs-lookup"><span data-stu-id="e65f4-116">"L2"</span></span>  | <span data-ttu-id="e65f4-117">Стандартная кодировка с частотой выборки до 48 кГц и максимальной скоростью в 161 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="e65f4-118">Индекс</span><span class="sxs-lookup"><span data-stu-id="e65f4-118">"L3"</span></span>  | <span data-ttu-id="e65f4-119">Стандартная кодировка с частотой выборки до 48 кГц и максимальной скоростью в 385 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="e65f4-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="e65f4-120">"M0a"</span></span> | <span data-ttu-id="e65f4-121">Профессиональная кодировка с частотой выборки до 48 кГц и скоростью между 48 и 192 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="e65f4-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="e65f4-122">"M0b"</span></span> | <span data-ttu-id="e65f4-123">Профессиональная кодировка с частотой выборки до 48 кГц и максимальной скоростью в 192 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="e65f4-124">M1</span><span class="sxs-lookup"><span data-stu-id="e65f4-124">"M1"</span></span>  | <span data-ttu-id="e65f4-125">Профессиональная кодировка с частотой выборки до 48 кГц и максимальной скоростью в 384 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="e65f4-126">M2</span><span class="sxs-lookup"><span data-stu-id="e65f4-126">"M2"</span></span>  | <span data-ttu-id="e65f4-127">Профессиональная кодировка с частотой выборки до 96 кГц и максимальной скоростью в 768 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="e65f4-128">M3</span><span class="sxs-lookup"><span data-stu-id="e65f4-128">"M3"</span></span>  | <span data-ttu-id="e65f4-129">Профессиональная кодировка с частотой выборки до 96 кГц и максимальной скоростью в 1,5 Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="e65f4-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="e65f4-130">N1</span><span class="sxs-lookup"><span data-stu-id="e65f4-130">"N1"</span></span>  | <span data-ttu-id="e65f4-131">Кодирование без потерь с частотой выборки до 48 кГц и максимум 2 канала.</span><span class="sxs-lookup"><span data-stu-id="e65f4-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="e65f4-132">N2</span><span class="sxs-lookup"><span data-stu-id="e65f4-132">"N2"</span></span>  | <span data-ttu-id="e65f4-133">Кодирование без потерь с частотой выборки до 96 кГц и максимум 6 каналов (5,1 вокруг).</span><span class="sxs-lookup"><span data-stu-id="e65f4-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="e65f4-134">N3</span><span class="sxs-lookup"><span data-stu-id="e65f4-134">"N3"</span></span>  | <span data-ttu-id="e65f4-135">Кодирование без потерь с частотой выборки до 96 кГц и максимум 8 каналов (7,1 вокруг).</span><span class="sxs-lookup"><span data-stu-id="e65f4-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="e65f4-136">Для видео это свойство имеет одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e65f4-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="e65f4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e65f4-137">Value</span></span> | <span data-ttu-id="e65f4-138">Описание</span><span class="sxs-lookup"><span data-stu-id="e65f4-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e65f4-139">ПРОФИЛЯ</span><span class="sxs-lookup"><span data-stu-id="e65f4-139">"AP"</span></span>  | <span data-ttu-id="e65f4-140">Расширенный профиль (доступен только для кодека расширенного профиля Windows Media видео 9)</span><span class="sxs-lookup"><span data-stu-id="e65f4-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="e65f4-141">CP</span><span class="sxs-lookup"><span data-stu-id="e65f4-141">"CP"</span></span>  | <span data-ttu-id="e65f4-142">больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e65f4-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="e65f4-143">МВ</span><span class="sxs-lookup"><span data-stu-id="e65f4-143">"MP"</span></span>  | <span data-ttu-id="e65f4-144">Основной профиль</span><span class="sxs-lookup"><span data-stu-id="e65f4-144">main profile</span></span>                                                                      |
| <span data-ttu-id="e65f4-145">ПОРТОВ</span><span class="sxs-lookup"><span data-stu-id="e65f4-145">"SP"</span></span>  | <span data-ttu-id="e65f4-146">простой профиль</span><span class="sxs-lookup"><span data-stu-id="e65f4-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="e65f4-147">Для видеоматериала можно запросить уровень профиля, установив [мфпкэй \_ декодеркомплекситирекуестед](mfpkey-decodercomplexityrequestedproperty.md) перед началом кодирования.</span><span class="sxs-lookup"><span data-stu-id="e65f4-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="e65f4-148">Кодек попытается выполнить кодирование в параметрах запрошенного уровня сложности, но другие настроенные параметры будут иметь приоритет.</span><span class="sxs-lookup"><span data-stu-id="e65f4-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="e65f4-149">Следует всегда проверять фактическое значение профиля сложности после кодирования в случае, если запрос не может быть обработан.</span><span class="sxs-lookup"><span data-stu-id="e65f4-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e65f4-150">Требования</span><span class="sxs-lookup"><span data-stu-id="e65f4-150">Requirements</span></span>



| <span data-ttu-id="e65f4-151">Требование</span><span class="sxs-lookup"><span data-stu-id="e65f4-151">Requirement</span></span> | <span data-ttu-id="e65f4-152">Значение</span><span class="sxs-lookup"><span data-stu-id="e65f4-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e65f4-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e65f4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e65f4-154">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e65f4-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e65f4-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e65f4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e65f4-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e65f4-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e65f4-157">Header</span><span class="sxs-lookup"><span data-stu-id="e65f4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e65f4-158"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e65f4-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e65f4-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e65f4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65f4-160">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e65f4-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




