---
description: Фильтр кодировщика Microsoft AC-3 кодирует аудио стерео PCM в Dolby Digital битовый поток.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Кодировщик Microsoft AC-3 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139998"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="adb9f-103">Кодировщик Microsoft AC-3</span><span class="sxs-lookup"><span data-stu-id="adb9f-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="adb9f-104">Фильтр кодировщика Microsoft AC-3 кодирует аудио стерео PCM в Dolby Digital битовый поток.</span><span class="sxs-lookup"><span data-stu-id="adb9f-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="adb9f-105">Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="adb9f-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="adb9f-106">Этот фильтр не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="adb9f-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="adb9f-107">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="adb9f-107">Filter Information</span></span>

<span data-ttu-id="adb9f-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="adb9f-108">Filter Interfaces</span></span>

[<span data-ttu-id="adb9f-109">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="adb9f-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="adb9f-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="adb9f-110">Input Pin Media Types</span></span>

<span data-ttu-id="adb9f-111">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="adb9f-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="adb9f-112">Тип входных данных должен составлять 48-кГц стерео, 16 бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="adb9f-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="adb9f-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="adb9f-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="adb9f-114">**имеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="adb9f-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="adb9f-115">**ипин**</span><span class="sxs-lookup"><span data-stu-id="adb9f-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="adb9f-116">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="adb9f-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="adb9f-117">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="adb9f-117">Output Pin Media Types</span></span>

<span data-ttu-id="adb9f-118">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="adb9f-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="adb9f-119">**MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="adb9f-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="adb9f-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="adb9f-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="adb9f-121">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="adb9f-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="adb9f-122">**ипин**</span><span class="sxs-lookup"><span data-stu-id="adb9f-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="adb9f-123">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="adb9f-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="adb9f-124">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="adb9f-124">Filter CLSID</span></span>

<span data-ttu-id="adb9f-125">**Идентификатор CLSID \_ CMSAC3Enc** (объявлено в вмкодекдсп. h)</span><span class="sxs-lookup"><span data-stu-id="adb9f-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="adb9f-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="adb9f-126">Executable</span></span>

<span data-ttu-id="adb9f-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="adb9f-127">msac3enc.dll</span></span>

[<span data-ttu-id="adb9f-128">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="adb9f-128">Merit</span></span>](merit.md)

<span data-ttu-id="adb9f-129">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="adb9f-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="adb9f-130">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="adb9f-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="adb9f-131">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="adb9f-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="adb9f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adb9f-132">Remarks</span></span>

<span data-ttu-id="adb9f-133">Этот фильтр недоступен для использования сторонними приложениями.</span><span class="sxs-lookup"><span data-stu-id="adb9f-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb9f-134">Требования</span><span class="sxs-lookup"><span data-stu-id="adb9f-134">Requirements</span></span>



| <span data-ttu-id="adb9f-135">Требование</span><span class="sxs-lookup"><span data-stu-id="adb9f-135">Requirement</span></span> | <span data-ttu-id="adb9f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="adb9f-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb9f-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb9f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="adb9f-138">Windows Vista Домашняя расширенная, Windows Vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="adb9f-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="adb9f-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb9f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="adb9f-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="adb9f-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="adb9f-141">Header</span><span class="sxs-lookup"><span data-stu-id="adb9f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb9f-142"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb9f-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="adb9f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb9f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb9f-144">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="adb9f-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




