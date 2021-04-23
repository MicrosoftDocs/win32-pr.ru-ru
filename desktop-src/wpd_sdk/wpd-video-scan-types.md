---
description: '\_ \_ Тип перечисления WPD Video Scan \_ types описывает, как кодируются поля в файле видео.'
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Перечисление WPD_VIDEO_SCAN_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647968"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="b265f-103">\_ \_ Перечисление типов сканирования видеороликов WPD \_</span><span class="sxs-lookup"><span data-stu-id="b265f-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="b265f-104">Тип перечисления **WPD \_ Video \_ Scan \_** Types описывает, как кодируются поля в файле видео.</span><span class="sxs-lookup"><span data-stu-id="b265f-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="b265f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b265f-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="b265f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b265f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b265f-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_Тип сканирования видеороликов WPD не \_ \_ \_ используется**</span><span class="sxs-lookup"><span data-stu-id="b265f-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-108">Тип сканирования не определен для этого видеофайла или неприменим.</span><span class="sxs-lookup"><span data-stu-id="b265f-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ прогрессивный**</span><span class="sxs-lookup"><span data-stu-id="b265f-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-110">Видеофайл последовательной проверки.</span><span class="sxs-lookup"><span data-stu-id="b265f-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_ \_ тип проверки видео WPD поле с \_ \_ \_ чередованием \_ сверху \_**</span><span class="sxs-lookup"><span data-stu-id="b265f-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-112">Сначала выводится файл с чередованием, в котором находятся альтернативные поля и верхнее поле (со строкой 1).</span><span class="sxs-lookup"><span data-stu-id="b265f-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="b265f-113">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="b265f-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_поле "тип сканирования видеороликов" (WPD) с \_ \_ \_ \_ чередованием \_ снизу \_**</span><span class="sxs-lookup"><span data-stu-id="b265f-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-115">Сначала выводится файл с чередованием, в котором находятся альтернативные поля и нижнее поле (со строкой 2).</span><span class="sxs-lookup"><span data-stu-id="b265f-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="b265f-116">Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="b265f-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ \_ \_ первое поле сверху \_**</span><span class="sxs-lookup"><span data-stu-id="b265f-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-118">Видеофайл с чередованием, в котором поля отправляются как смежные примеры, а верхнее поле (строка 1) рисуется первыми.</span><span class="sxs-lookup"><span data-stu-id="b265f-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="b265f-119">Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="b265f-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**\_ \_ поле типа сканирования видеороликов WPD \_ \_ \_ \_ \_ сначала**</span><span class="sxs-lookup"><span data-stu-id="b265f-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-121">Видеофайл с чередованием, в котором поля отправляются как смежные примеры, а в первую очередь отправляется нижнее поле (строка 2).</span><span class="sxs-lookup"><span data-stu-id="b265f-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_тип проверки видео WPD — \_ \_ \_ смешанная \_ развертка**</span><span class="sxs-lookup"><span data-stu-id="b265f-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-123">Видеофайл с смесью режимов чередования.</span><span class="sxs-lookup"><span data-stu-id="b265f-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="b265f-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ смешанные \_ \_ и \_ прогрессивные развертки**</span><span class="sxs-lookup"><span data-stu-id="b265f-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="b265f-125">Видеофайл с сочетанием чередующихся и прогрессивных режимов.</span><span class="sxs-lookup"><span data-stu-id="b265f-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b265f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b265f-126">Remarks</span></span>

<span data-ttu-id="b265f-127">Это перечисление используется свойством " [ \_ \_ \_ тип видеосканирования WPD](properties-and-attributes.md) ".</span><span class="sxs-lookup"><span data-stu-id="b265f-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="b265f-128">Существует два типа файлов с чередованием, которые задаются этим перечислением.</span><span class="sxs-lookup"><span data-stu-id="b265f-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="b265f-129">**WPD \_ \_Поле типа СКАНИРОВАНИЯ видео с \_ \_ \_ чередованием** относится к формату файла, в котором кадры доставляются по мере того, как они были проверены, а данные помещаются построчно, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b265f-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="b265f-130">**Кадр 1**</span><span class="sxs-lookup"><span data-stu-id="b265f-130">**Frame 1**</span></span>

<span data-ttu-id="b265f-131">Поле 1. строка 1</span><span class="sxs-lookup"><span data-stu-id="b265f-131">Field 1: Line 1</span></span>

<span data-ttu-id="b265f-132">Поле 2. строка 1</span><span class="sxs-lookup"><span data-stu-id="b265f-132">Field 2: Line 1</span></span>

<span data-ttu-id="b265f-133">Поле 1. строка 2</span><span class="sxs-lookup"><span data-stu-id="b265f-133">Field 1: Line 2</span></span>

<span data-ttu-id="b265f-134">Поле 2. строка 2</span><span class="sxs-lookup"><span data-stu-id="b265f-134">Field 2: Line 2</span></span>

<span data-ttu-id="b265f-135">Поле 1. строка 3</span><span class="sxs-lookup"><span data-stu-id="b265f-135">Field 1: Line 3</span></span>

<span data-ttu-id="b265f-136">Поле 2. строка 3</span><span class="sxs-lookup"><span data-stu-id="b265f-136">Field 2: Line 3</span></span>

<span data-ttu-id="b265f-137">...</span><span class="sxs-lookup"><span data-stu-id="b265f-137">...</span></span>

<span data-ttu-id="b265f-138">**WPD \_ \_ \_ Поле типа сканирования \_ видео \_ Single** ссылается на формат файла, где каждое поле хранится в одном блоке строк сканирования, а поля хранятся последовательно, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b265f-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="b265f-139">**Кадр 1**</span><span class="sxs-lookup"><span data-stu-id="b265f-139">**Frame 1**</span></span>

<span data-ttu-id="b265f-140">Поле 1. строка 1</span><span class="sxs-lookup"><span data-stu-id="b265f-140">Field 1: Line 1</span></span>

<span data-ttu-id="b265f-141">Поле 1. строка 2</span><span class="sxs-lookup"><span data-stu-id="b265f-141">Field 1: Line 2</span></span>

<span data-ttu-id="b265f-142">Поле 1. строка 3</span><span class="sxs-lookup"><span data-stu-id="b265f-142">Field 1: Line 3</span></span>

<span data-ttu-id="b265f-143">...</span><span class="sxs-lookup"><span data-stu-id="b265f-143">...</span></span>

<span data-ttu-id="b265f-144">За которым следует</span><span class="sxs-lookup"><span data-stu-id="b265f-144">Followed by</span></span>

<span data-ttu-id="b265f-145">Поле 2. строка 1</span><span class="sxs-lookup"><span data-stu-id="b265f-145">Field 2: Line 1</span></span>

<span data-ttu-id="b265f-146">Поле 2. строка 2</span><span class="sxs-lookup"><span data-stu-id="b265f-146">Field 2: Line 2</span></span>

<span data-ttu-id="b265f-147">Поле 2. строка 3</span><span class="sxs-lookup"><span data-stu-id="b265f-147">Field 2: Line 3</span></span>

<span data-ttu-id="b265f-148">...</span><span class="sxs-lookup"><span data-stu-id="b265f-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="b265f-149">Требования</span><span class="sxs-lookup"><span data-stu-id="b265f-149">Requirements</span></span>



| <span data-ttu-id="b265f-150">Требование</span><span class="sxs-lookup"><span data-stu-id="b265f-150">Requirement</span></span> | <span data-ttu-id="b265f-151">Значение</span><span class="sxs-lookup"><span data-stu-id="b265f-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b265f-152">Header</span><span class="sxs-lookup"><span data-stu-id="b265f-152">Header</span></span><br/> | <dl> <span data-ttu-id="b265f-153"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="b265f-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b265f-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b265f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b265f-155">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="b265f-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




