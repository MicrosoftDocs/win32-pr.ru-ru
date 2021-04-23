---
description: Политика метаданных фотографии для свойства System. keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Политика метаданных фото в System. keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272094"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="00b24-103">Политика метаданных фото в System. keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="00b24-104">Политика метаданных фотографии для свойства [System. keywords](../properties/props-system-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="00b24-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="00b24-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="00b24-105">PKEY</span></span>

<span data-ttu-id="00b24-106">\_Ключевые слова PKEY</span><span class="sxs-lookup"><span data-stu-id="00b24-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="00b24-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="00b24-107">Containers</span></span>

<span data-ttu-id="00b24-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="00b24-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="00b24-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="00b24-109">Read-Only</span></span>

<span data-ttu-id="00b24-110">Нет</span><span class="sxs-lookup"><span data-stu-id="00b24-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="00b24-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="00b24-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="00b24-112">VT \_ Векторная \| \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="00b24-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="00b24-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="00b24-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="00b24-114">\_ \| \_ Предпочитаемый вектор VT LPWSTR является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="00b24-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="00b24-115">\_Также принимается VT LPWSTR, содержащий строку с разделителями-точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="00b24-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="00b24-116">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="00b24-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="00b24-117">Объединяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="00b24-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="00b24-118">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="00b24-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="00b24-119">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="00b24-119">Read Paths</span></span>



| <span data-ttu-id="00b24-120">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-120">Order</span></span> | <span data-ttu-id="00b24-121">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-121">Path</span></span>                              | <span data-ttu-id="00b24-122">Формат диска</span><span class="sxs-lookup"><span data-stu-id="00b24-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="00b24-123">1</span><span class="sxs-lookup"><span data-stu-id="00b24-123">1</span></span>     | <span data-ttu-id="00b24-124">/КСМП/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="00b24-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="00b24-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-125">unicode</span></span>        |
| <span data-ttu-id="00b24-126">2</span><span class="sxs-lookup"><span data-stu-id="00b24-126">2</span></span>     | <span data-ttu-id="00b24-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="00b24-128">3</span><span class="sxs-lookup"><span data-stu-id="00b24-128">3</span></span>     | <span data-ttu-id="00b24-129">/APP1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="00b24-130">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-130">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-131">4</span><span class="sxs-lookup"><span data-stu-id="00b24-131">4</span></span>     | <span data-ttu-id="00b24-132">/APP1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="00b24-133">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="00b24-134">Пути записи</span><span class="sxs-lookup"><span data-stu-id="00b24-134">Write Paths</span></span>



| <span data-ttu-id="00b24-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-135">Order</span></span> | <span data-ttu-id="00b24-136">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-136">Path</span></span>                                              | <span data-ttu-id="00b24-137">Формат диска</span><span class="sxs-lookup"><span data-stu-id="00b24-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="00b24-138">1</span><span class="sxs-lookup"><span data-stu-id="00b24-138">1</span></span>     | <span data-ttu-id="00b24-139">/КСМП/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="00b24-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="00b24-140">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-140">unicode</span></span>        |
| <span data-ttu-id="00b24-141">2</span><span class="sxs-lookup"><span data-stu-id="00b24-141">2</span></span>     | <span data-ttu-id="00b24-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="00b24-143">3</span><span class="sxs-lookup"><span data-stu-id="00b24-143">3</span></span>     | <span data-ttu-id="00b24-144">/APP1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="00b24-145">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-145">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-146">4</span><span class="sxs-lookup"><span data-stu-id="00b24-146">4</span></span>     | <span data-ttu-id="00b24-147">/APP1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="00b24-148">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-148">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-149">5</span><span class="sxs-lookup"><span data-stu-id="00b24-149">5</span></span>     | <span data-ttu-id="00b24-150">/КСМП/ <xmpbag> микрософтфото: ласткэйвордксмп</span><span class="sxs-lookup"><span data-stu-id="00b24-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="00b24-151">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-151">unicode</span></span>        |
| <span data-ttu-id="00b24-152">6</span><span class="sxs-lookup"><span data-stu-id="00b24-152">6</span></span>     | <span data-ttu-id="00b24-153">/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк</span><span class="sxs-lookup"><span data-stu-id="00b24-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="00b24-154">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="00b24-155">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="00b24-155">Remove Paths</span></span>



| <span data-ttu-id="00b24-156">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-156">Order</span></span> | <span data-ttu-id="00b24-157">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="00b24-158">1</span><span class="sxs-lookup"><span data-stu-id="00b24-158">1</span></span>     | <span data-ttu-id="00b24-159">/КСМП/ДК: Тема</span><span class="sxs-lookup"><span data-stu-id="00b24-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="00b24-160">2</span><span class="sxs-lookup"><span data-stu-id="00b24-160">2</span></span>     | <span data-ttu-id="00b24-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="00b24-162">3</span><span class="sxs-lookup"><span data-stu-id="00b24-162">3</span></span>     | <span data-ttu-id="00b24-163">/APP1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="00b24-164">4</span><span class="sxs-lookup"><span data-stu-id="00b24-164">4</span></span>     | <span data-ttu-id="00b24-165">/APP1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="00b24-166">5</span><span class="sxs-lookup"><span data-stu-id="00b24-166">5</span></span>     | <span data-ttu-id="00b24-167">/КСМП/ <xmpbag> микрософтфото: ласткэйвордксмп</span><span class="sxs-lookup"><span data-stu-id="00b24-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="00b24-168">6</span><span class="sxs-lookup"><span data-stu-id="00b24-168">6</span></span>     | <span data-ttu-id="00b24-169">/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк</span><span class="sxs-lookup"><span data-stu-id="00b24-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="00b24-170">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="00b24-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="00b24-171">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="00b24-171">Read Paths</span></span>



| <span data-ttu-id="00b24-172">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-172">Order</span></span> | <span data-ttu-id="00b24-173">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-173">Path</span></span>                              | <span data-ttu-id="00b24-174">Формат диска</span><span class="sxs-lookup"><span data-stu-id="00b24-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="00b24-175">1</span><span class="sxs-lookup"><span data-stu-id="00b24-175">1</span></span>     | <span data-ttu-id="00b24-176">/ИФД/КСМП/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="00b24-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="00b24-177">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-177">unicode</span></span>        |
| <span data-ttu-id="00b24-178">2</span><span class="sxs-lookup"><span data-stu-id="00b24-178">2</span></span>     | <span data-ttu-id="00b24-179">/ифд/иптк/кэйвордс</span><span class="sxs-lookup"><span data-stu-id="00b24-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="00b24-180">3</span><span class="sxs-lookup"><span data-stu-id="00b24-180">3</span></span>     | <span data-ttu-id="00b24-181">/ИФД/{ушорт = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="00b24-182">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-182">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-183">4</span><span class="sxs-lookup"><span data-stu-id="00b24-183">4</span></span>     | <span data-ttu-id="00b24-184">/ИФД/{ушорт = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="00b24-185">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-185">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-186">5</span><span class="sxs-lookup"><span data-stu-id="00b24-186">5</span></span>     | <span data-ttu-id="00b24-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="00b24-188">Пути записи</span><span class="sxs-lookup"><span data-stu-id="00b24-188">Write Paths</span></span>



| <span data-ttu-id="00b24-189">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-189">Order</span></span> | <span data-ttu-id="00b24-190">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-190">Path</span></span>                                                             | <span data-ttu-id="00b24-191">Формат диска</span><span class="sxs-lookup"><span data-stu-id="00b24-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="00b24-192">1</span><span class="sxs-lookup"><span data-stu-id="00b24-192">1</span></span>     | <span data-ttu-id="00b24-193">/ИФД/КСМП/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="00b24-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="00b24-194">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-194">unicode</span></span>        |
| <span data-ttu-id="00b24-195">2</span><span class="sxs-lookup"><span data-stu-id="00b24-195">2</span></span>     | <span data-ttu-id="00b24-196">/ифд/иптк/кэйвордс</span><span class="sxs-lookup"><span data-stu-id="00b24-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="00b24-197">3</span><span class="sxs-lookup"><span data-stu-id="00b24-197">3</span></span>     | <span data-ttu-id="00b24-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="00b24-199">4</span><span class="sxs-lookup"><span data-stu-id="00b24-199">4</span></span>     | <span data-ttu-id="00b24-200">/ИФД/{ушорт = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="00b24-201">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-201">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-202">5</span><span class="sxs-lookup"><span data-stu-id="00b24-202">5</span></span>     | <span data-ttu-id="00b24-203">/ИФД/{ушорт = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="00b24-204">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="00b24-204">unicode\_bytes</span></span> |
| <span data-ttu-id="00b24-205">6</span><span class="sxs-lookup"><span data-stu-id="00b24-205">6</span></span>     | <span data-ttu-id="00b24-206">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордксмп</span><span class="sxs-lookup"><span data-stu-id="00b24-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="00b24-207">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-207">unicode</span></span>        |
| <span data-ttu-id="00b24-208">7</span><span class="sxs-lookup"><span data-stu-id="00b24-208">7</span></span>     | <span data-ttu-id="00b24-209">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк</span><span class="sxs-lookup"><span data-stu-id="00b24-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="00b24-210">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-210">unicode</span></span>        |
| <span data-ttu-id="00b24-211">8</span><span class="sxs-lookup"><span data-stu-id="00b24-211">8</span></span>     | <span data-ttu-id="00b24-212">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк \_ TIFF \_ ИРБ</span><span class="sxs-lookup"><span data-stu-id="00b24-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="00b24-213">Юникод</span><span class="sxs-lookup"><span data-stu-id="00b24-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="00b24-214">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="00b24-214">Remove Paths</span></span>



| <span data-ttu-id="00b24-215">Заказ</span><span class="sxs-lookup"><span data-stu-id="00b24-215">Order</span></span> | <span data-ttu-id="00b24-216">Путь</span><span class="sxs-lookup"><span data-stu-id="00b24-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="00b24-217">1</span><span class="sxs-lookup"><span data-stu-id="00b24-217">1</span></span>     | <span data-ttu-id="00b24-218">/ИФД/КСМП/ДК: Тема</span><span class="sxs-lookup"><span data-stu-id="00b24-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="00b24-219">2</span><span class="sxs-lookup"><span data-stu-id="00b24-219">2</span></span>     | <span data-ttu-id="00b24-220">/ифд/иптк/кэйвордс</span><span class="sxs-lookup"><span data-stu-id="00b24-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="00b24-221">3</span><span class="sxs-lookup"><span data-stu-id="00b24-221">3</span></span>     | <span data-ttu-id="00b24-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="00b24-223">4</span><span class="sxs-lookup"><span data-stu-id="00b24-223">4</span></span>     | <span data-ttu-id="00b24-224">/ИФД/{ушорт = 18247}</span><span class="sxs-lookup"><span data-stu-id="00b24-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="00b24-225">5</span><span class="sxs-lookup"><span data-stu-id="00b24-225">5</span></span>     | <span data-ttu-id="00b24-226">/ИФД/{ушорт = 40094}</span><span class="sxs-lookup"><span data-stu-id="00b24-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="00b24-227">6</span><span class="sxs-lookup"><span data-stu-id="00b24-227">6</span></span>     | <span data-ttu-id="00b24-228">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордксмп</span><span class="sxs-lookup"><span data-stu-id="00b24-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="00b24-229">7</span><span class="sxs-lookup"><span data-stu-id="00b24-229">7</span></span>     | <span data-ttu-id="00b24-230">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк</span><span class="sxs-lookup"><span data-stu-id="00b24-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="00b24-231">8</span><span class="sxs-lookup"><span data-stu-id="00b24-231">8</span></span>     | <span data-ttu-id="00b24-232">/ИФД/КСМП/ <xmpbag> микрософтфото: ласткэйвордиптк \_ TIFF \_ ИРБ</span><span class="sxs-lookup"><span data-stu-id="00b24-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="00b24-233">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00b24-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b24-234">См. также</span><span class="sxs-lookup"><span data-stu-id="00b24-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b24-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="00b24-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
