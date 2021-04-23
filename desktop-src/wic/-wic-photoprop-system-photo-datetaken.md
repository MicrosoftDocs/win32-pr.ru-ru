---
description: Политика метаданных фотографии для свойства System. photo. Датетакен.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Политика метаданных фото для System. photo. Датетакен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713055"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="9517d-103">Политика метаданных фото для System. photo. Датетакен</span><span class="sxs-lookup"><span data-stu-id="9517d-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="9517d-104">Политика метаданных фотографии для свойства [System. photo. датетакен](../properties/props-system-photo-datetaken.md) .</span><span class="sxs-lookup"><span data-stu-id="9517d-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9517d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9517d-105">PKEY</span></span>

<span data-ttu-id="9517d-106">\_Датетакен фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="9517d-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="9517d-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="9517d-107">Containers</span></span>

<span data-ttu-id="9517d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9517d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9517d-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9517d-109">Read-Only</span></span>

<span data-ttu-id="9517d-110">Нет</span><span class="sxs-lookup"><span data-stu-id="9517d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9517d-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="9517d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9517d-112">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="9517d-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="9517d-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="9517d-113">Input Type</span></span>

<span data-ttu-id="9517d-114">Дата/время</span><span class="sxs-lookup"><span data-stu-id="9517d-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9517d-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="9517d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9517d-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="9517d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9517d-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="9517d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9517d-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9517d-118">Read Paths</span></span>



| <span data-ttu-id="9517d-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-119">Order</span></span> | <span data-ttu-id="9517d-120">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-120">Path</span></span>                                  | <span data-ttu-id="9517d-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="9517d-122">1</span><span class="sxs-lookup"><span data-stu-id="9517d-122">1</span></span>     | <span data-ttu-id="9517d-123">/APP1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="9517d-124">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-124">ascii</span></span>       |
| <span data-ttu-id="9517d-125">2</span><span class="sxs-lookup"><span data-stu-id="9517d-125">2</span></span>     | <span data-ttu-id="9517d-126">/APP13/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="9517d-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-127">unicode</span></span>     |
| <span data-ttu-id="9517d-128">3</span><span class="sxs-lookup"><span data-stu-id="9517d-128">3</span></span>     | <span data-ttu-id="9517d-129">/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="9517d-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-130">unicode</span></span>     |
| <span data-ttu-id="9517d-131">4</span><span class="sxs-lookup"><span data-stu-id="9517d-131">4</span></span>     | <span data-ttu-id="9517d-132">/APP1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="9517d-133">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-133">ascii</span></span>       |
| <span data-ttu-id="9517d-134">5</span><span class="sxs-lookup"><span data-stu-id="9517d-134">5</span></span>     | <span data-ttu-id="9517d-135">/APP13/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="9517d-136">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-136">unicode</span></span>     |
| <span data-ttu-id="9517d-137">6</span><span class="sxs-lookup"><span data-stu-id="9517d-137">6</span></span>     | <span data-ttu-id="9517d-138">/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="9517d-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9517d-140">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9517d-140">Write Paths</span></span>



| <span data-ttu-id="9517d-141">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-141">Order</span></span> | <span data-ttu-id="9517d-142">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-142">Path</span></span>                                  | <span data-ttu-id="9517d-143">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="9517d-144">1</span><span class="sxs-lookup"><span data-stu-id="9517d-144">1</span></span>     | <span data-ttu-id="9517d-145">/APP1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="9517d-146">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-146">ascii</span></span>       |
| <span data-ttu-id="9517d-147">2</span><span class="sxs-lookup"><span data-stu-id="9517d-147">2</span></span>     | <span data-ttu-id="9517d-148">/APP13/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="9517d-149">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-149">unicode</span></span>     |
| <span data-ttu-id="9517d-150">3</span><span class="sxs-lookup"><span data-stu-id="9517d-150">3</span></span>     | <span data-ttu-id="9517d-151">/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="9517d-152">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-152">unicode</span></span>     |
| <span data-ttu-id="9517d-153">4</span><span class="sxs-lookup"><span data-stu-id="9517d-153">4</span></span>     | <span data-ttu-id="9517d-154">/APP1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="9517d-155">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-155">ascii</span></span>       |
| <span data-ttu-id="9517d-156">5</span><span class="sxs-lookup"><span data-stu-id="9517d-156">5</span></span>     | <span data-ttu-id="9517d-157">/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="9517d-158">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9517d-159">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9517d-159">Remove Paths</span></span>



| <span data-ttu-id="9517d-160">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-160">Order</span></span> | <span data-ttu-id="9517d-161">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="9517d-162">1</span><span class="sxs-lookup"><span data-stu-id="9517d-162">1</span></span>     | <span data-ttu-id="9517d-163">/APP1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="9517d-164">2</span><span class="sxs-lookup"><span data-stu-id="9517d-164">2</span></span>     | <span data-ttu-id="9517d-165">/APP1/IFD/EXIF/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="9517d-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="9517d-166">3</span><span class="sxs-lookup"><span data-stu-id="9517d-166">3</span></span>     | <span data-ttu-id="9517d-167">/APP1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="9517d-168">4</span><span class="sxs-lookup"><span data-stu-id="9517d-168">4</span></span>     | <span data-ttu-id="9517d-169">/APP1/IFD/EXIF/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="9517d-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="9517d-170">5</span><span class="sxs-lookup"><span data-stu-id="9517d-170">5</span></span>     | <span data-ttu-id="9517d-171">/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="9517d-172">6</span><span class="sxs-lookup"><span data-stu-id="9517d-172">6</span></span>     | <span data-ttu-id="9517d-173">/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="9517d-174">7</span><span class="sxs-lookup"><span data-stu-id="9517d-174">7</span></span>     | <span data-ttu-id="9517d-175">/APP13/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="9517d-176">8</span><span class="sxs-lookup"><span data-stu-id="9517d-176">8</span></span>     | <span data-ttu-id="9517d-177">/APP13/IRB/8bimiptc/IPTC/Time создан</span><span class="sxs-lookup"><span data-stu-id="9517d-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="9517d-178">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="9517d-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9517d-179">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9517d-179">Read Paths</span></span>



| <span data-ttu-id="9517d-180">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-180">Order</span></span> | <span data-ttu-id="9517d-181">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-181">Path</span></span>                                | <span data-ttu-id="9517d-182">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="9517d-183">1</span><span class="sxs-lookup"><span data-stu-id="9517d-183">1</span></span>     | <span data-ttu-id="9517d-184">/ИФД/ексиф/{ушорт = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="9517d-185">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-185">ascii</span></span>       |
| <span data-ttu-id="9517d-186">2</span><span class="sxs-lookup"><span data-stu-id="9517d-186">2</span></span>     | <span data-ttu-id="9517d-187">/ИФД/иптк/дате создан</span><span class="sxs-lookup"><span data-stu-id="9517d-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="9517d-188">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-188">unicode</span></span>     |
| <span data-ttu-id="9517d-189">3</span><span class="sxs-lookup"><span data-stu-id="9517d-189">3</span></span>     | <span data-ttu-id="9517d-190">/ИФД/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="9517d-191">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-191">unicode</span></span>     |
| <span data-ttu-id="9517d-192">4</span><span class="sxs-lookup"><span data-stu-id="9517d-192">4</span></span>     | <span data-ttu-id="9517d-193">/ИФД/ексиф/{ушорт = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="9517d-194">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-194">ascii</span></span>       |
| <span data-ttu-id="9517d-195">5</span><span class="sxs-lookup"><span data-stu-id="9517d-195">5</span></span>     | <span data-ttu-id="9517d-196">/ИФД/иптк/дате создан</span><span class="sxs-lookup"><span data-stu-id="9517d-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="9517d-197">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-197">unicode</span></span>     |
| <span data-ttu-id="9517d-198">6</span><span class="sxs-lookup"><span data-stu-id="9517d-198">6</span></span>     | <span data-ttu-id="9517d-199">/IFD/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="9517d-200">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-200">unicode</span></span>     |
| <span data-ttu-id="9517d-201">7</span><span class="sxs-lookup"><span data-stu-id="9517d-201">7</span></span>     | <span data-ttu-id="9517d-202">/ИФД/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="9517d-203">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9517d-204">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9517d-204">Write Paths</span></span>



| <span data-ttu-id="9517d-205">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-205">Order</span></span> | <span data-ttu-id="9517d-206">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-206">Path</span></span>                                | <span data-ttu-id="9517d-207">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="9517d-208">1</span><span class="sxs-lookup"><span data-stu-id="9517d-208">1</span></span>     | <span data-ttu-id="9517d-209">/ИФД/ексиф/{ушорт = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="9517d-210">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-210">ascii</span></span>       |
| <span data-ttu-id="9517d-211">2</span><span class="sxs-lookup"><span data-stu-id="9517d-211">2</span></span>     | <span data-ttu-id="9517d-212">/ИФД/иптк/дате создан</span><span class="sxs-lookup"><span data-stu-id="9517d-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="9517d-213">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-213">unicode</span></span>     |
| <span data-ttu-id="9517d-214">3</span><span class="sxs-lookup"><span data-stu-id="9517d-214">3</span></span>     | <span data-ttu-id="9517d-215">/ИФД/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="9517d-216">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-216">unicode</span></span>     |
| <span data-ttu-id="9517d-217">4</span><span class="sxs-lookup"><span data-stu-id="9517d-217">4</span></span>     | <span data-ttu-id="9517d-218">/ИФД/ексиф/{ушорт = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="9517d-219">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-219">ascii</span></span>       |
| <span data-ttu-id="9517d-220">5</span><span class="sxs-lookup"><span data-stu-id="9517d-220">5</span></span>     | <span data-ttu-id="9517d-221">/IFD/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="9517d-222">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-222">unicode</span></span>     |
| <span data-ttu-id="9517d-223">6</span><span class="sxs-lookup"><span data-stu-id="9517d-223">6</span></span>     | <span data-ttu-id="9517d-224">/ИФД/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="9517d-225">Юникод</span><span class="sxs-lookup"><span data-stu-id="9517d-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9517d-226">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9517d-226">Remove Paths</span></span>



| <span data-ttu-id="9517d-227">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-227">Order</span></span> | <span data-ttu-id="9517d-228">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="9517d-229">1</span><span class="sxs-lookup"><span data-stu-id="9517d-229">1</span></span>     | <span data-ttu-id="9517d-230">/ИФД/ексиф/{ушорт = 36867}</span><span class="sxs-lookup"><span data-stu-id="9517d-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="9517d-231">2</span><span class="sxs-lookup"><span data-stu-id="9517d-231">2</span></span>     | <span data-ttu-id="9517d-232">/ИФД/ексиф/{ушорт = 37521}</span><span class="sxs-lookup"><span data-stu-id="9517d-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="9517d-233">3</span><span class="sxs-lookup"><span data-stu-id="9517d-233">3</span></span>     | <span data-ttu-id="9517d-234">/ИФД/ексиф/{ушорт = 36868}</span><span class="sxs-lookup"><span data-stu-id="9517d-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="9517d-235">4</span><span class="sxs-lookup"><span data-stu-id="9517d-235">4</span></span>     | <span data-ttu-id="9517d-236">/ИФД/ексиф/{ушорт = 37522}</span><span class="sxs-lookup"><span data-stu-id="9517d-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="9517d-237">5</span><span class="sxs-lookup"><span data-stu-id="9517d-237">5</span></span>     | <span data-ttu-id="9517d-238">/ИФД/КСМП/ексиф: Датетимеоригинал</span><span class="sxs-lookup"><span data-stu-id="9517d-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="9517d-239">6</span><span class="sxs-lookup"><span data-stu-id="9517d-239">6</span></span>     | <span data-ttu-id="9517d-240">/ИФД/КСМП/КСМП: Креатедате</span><span class="sxs-lookup"><span data-stu-id="9517d-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="9517d-241">7</span><span class="sxs-lookup"><span data-stu-id="9517d-241">7</span></span>     | <span data-ttu-id="9517d-242">/ИФД/иптк/дате создан</span><span class="sxs-lookup"><span data-stu-id="9517d-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="9517d-243">8</span><span class="sxs-lookup"><span data-stu-id="9517d-243">8</span></span>     | <span data-ttu-id="9517d-244">/ИФД/иптк/Тиме создан</span><span class="sxs-lookup"><span data-stu-id="9517d-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="9517d-245">9</span><span class="sxs-lookup"><span data-stu-id="9517d-245">9</span></span>     | <span data-ttu-id="9517d-246">/IFD/IRB/8bimiptc/IPTC/Date создан</span><span class="sxs-lookup"><span data-stu-id="9517d-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="9517d-247">10</span><span class="sxs-lookup"><span data-stu-id="9517d-247">10</span></span>    | <span data-ttu-id="9517d-248">/IFD/IRB/8bimiptc/IPTC/Time создан</span><span class="sxs-lookup"><span data-stu-id="9517d-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="9517d-249">Политика PNG</span><span class="sxs-lookup"><span data-stu-id="9517d-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9517d-250">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9517d-250">Read Paths</span></span>



| <span data-ttu-id="9517d-251">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-251">Order</span></span> | <span data-ttu-id="9517d-252">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-252">Path</span></span>                      | <span data-ttu-id="9517d-253">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9517d-254">1</span><span class="sxs-lookup"><span data-stu-id="9517d-254">1</span></span>     | <span data-ttu-id="9517d-255">/\[\*\]Время текста и создания</span><span class="sxs-lookup"><span data-stu-id="9517d-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="9517d-256">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="9517d-257">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9517d-257">Write Paths</span></span>



| <span data-ttu-id="9517d-258">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-258">Order</span></span> | <span data-ttu-id="9517d-259">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-259">Path</span></span>                      | <span data-ttu-id="9517d-260">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9517d-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9517d-261">2</span><span class="sxs-lookup"><span data-stu-id="9517d-261">2</span></span>     | <span data-ttu-id="9517d-262">/\[\*\]Время текста и создания</span><span class="sxs-lookup"><span data-stu-id="9517d-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="9517d-263">ascii</span><span class="sxs-lookup"><span data-stu-id="9517d-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="9517d-264">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9517d-264">Remove Paths</span></span>



| <span data-ttu-id="9517d-265">Заказ</span><span class="sxs-lookup"><span data-stu-id="9517d-265">Order</span></span> | <span data-ttu-id="9517d-266">Путь</span><span class="sxs-lookup"><span data-stu-id="9517d-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9517d-267">3</span><span class="sxs-lookup"><span data-stu-id="9517d-267">3</span></span>     | <span data-ttu-id="9517d-268">/\[\*\]Время текста и создания</span><span class="sxs-lookup"><span data-stu-id="9517d-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9517d-269">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9517d-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9517d-270">См. также</span><span class="sxs-lookup"><span data-stu-id="9517d-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9517d-271">System. photo. Датетакен</span><span class="sxs-lookup"><span data-stu-id="9517d-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
