---
description: В следующем списке приводятся описания элементов свойств, поддерживаемых Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Описания элементов свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636126"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="76111-103">Описания элементов свойств</span><span class="sxs-lookup"><span data-stu-id="76111-103">Property Item Descriptions</span></span>

<span data-ttu-id="76111-104">В следующем списке приводятся описания элементов свойств, поддерживаемых Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="76111-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="76111-105">Описания являются краткими и общими, поэтому они применяются к различным форматам файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="76111-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="76111-106">Подробное описание того, как элемент свойства используется определенным форматом файла, см. в спецификации для этого формата файла.</span><span class="sxs-lookup"><span data-stu-id="76111-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="76111-107">Ссылки на некоторые спецификации файлов и другие документы, в которых подробно описаны метаданные, см. в разделе [спецификации формата файла изображения](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="76111-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="76111-108">Формат файла обмена изображениями (EXIF) — это японский стандарт ассоциации электронных отраслей (ЖЕИДА), измененный с 1998 июня по версии 2,1.</span><span class="sxs-lookup"><span data-stu-id="76111-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="76111-109">Части спецификации EXIF используются с разрешением ЖЕИДА.</span><span class="sxs-lookup"><span data-stu-id="76111-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="76111-110">пропертитаггпсвер</span><span class="sxs-lookup"><span data-stu-id="76111-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="76111-111">Версия системы управления глобальным позиционированием (GPS) IFD, заданная как 2.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="76111-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="76111-112">Этот тег является обязательным при наличии тега Пропертитаггпсифд.</span><span class="sxs-lookup"><span data-stu-id="76111-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="76111-113">Если версия — 2.0.0.0, значение тега — 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="76111-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="76111-114">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-114">Property info</span></span> | <span data-ttu-id="76111-115">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-116">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-116">Tag</span></span>   | <span data-ttu-id="76111-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="76111-117">0x0000</span></span>              |
| <span data-ttu-id="76111-118">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-118">Type</span></span>  | <span data-ttu-id="76111-119">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-120">Count</span><span class="sxs-lookup"><span data-stu-id="76111-120">Count</span></span> | <span data-ttu-id="76111-121">4</span><span class="sxs-lookup"><span data-stu-id="76111-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="76111-122">пропертитаггпслатитудереф</span><span class="sxs-lookup"><span data-stu-id="76111-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="76111-123">Строка символов, заканчивающаяся символом NULL, которая указывает, является ли Широта Севером или Юг.</span><span class="sxs-lookup"><span data-stu-id="76111-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="76111-124">`N` Указывает Север широты и `S` указывает Юго-Широта.</span><span class="sxs-lookup"><span data-stu-id="76111-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="76111-125">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-125">Property info</span></span> | <span data-ttu-id="76111-126">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-127">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-127">Tag</span></span>   | <span data-ttu-id="76111-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="76111-128">0x0001</span></span>                                     |
| <span data-ttu-id="76111-129">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-129">Type</span></span>  | <span data-ttu-id="76111-130">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-131">Count</span><span class="sxs-lookup"><span data-stu-id="76111-131">Count</span></span> | <span data-ttu-id="76111-132">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="76111-133">пропертитаггпслатитуде</span><span class="sxs-lookup"><span data-stu-id="76111-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="76111-134">Широта.</span><span class="sxs-lookup"><span data-stu-id="76111-134">Latitude.</span></span> <span data-ttu-id="76111-135">Широта выражается тремя рациональными значениями, предоставляющими градусы, минуты и секунды соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="76111-136">Если выражаются градусы, минуты и секунды, то используется формат ДД/1, мм/1, СС/1.</span><span class="sxs-lookup"><span data-stu-id="76111-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="76111-137">Если используются градусы и минуты и, например, доли минут получают до двух десятичных разрядов, форматом будет дд/1, мммм/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="76111-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="76111-138">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-138">Property info</span></span> | <span data-ttu-id="76111-139">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-140">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-140">Tag</span></span>   | <span data-ttu-id="76111-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="76111-141">0x0002</span></span>                  |
| <span data-ttu-id="76111-142">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-142">Type</span></span>  | <span data-ttu-id="76111-143">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-144">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-144">Count</span></span> | <span data-ttu-id="76111-145">3</span><span class="sxs-lookup"><span data-stu-id="76111-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="76111-146">пропертитаггпслонгитудереф</span><span class="sxs-lookup"><span data-stu-id="76111-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="76111-147">Строка символов, заканчивающаяся символом NULL, которая указывает, является ли Долгота восточная или Западной долготой.</span><span class="sxs-lookup"><span data-stu-id="76111-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="76111-148">`E` Задает "Восток" и " `W` Западная Долгота".</span><span class="sxs-lookup"><span data-stu-id="76111-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="76111-149">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-149">Property info</span></span> | <span data-ttu-id="76111-150">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-151">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-151">Tag</span></span>   | <span data-ttu-id="76111-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="76111-152">0x0003</span></span>                                     |
| <span data-ttu-id="76111-153">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-153">Type</span></span>  | <span data-ttu-id="76111-154">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-155">Count</span><span class="sxs-lookup"><span data-stu-id="76111-155">Count</span></span> | <span data-ttu-id="76111-156">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="76111-157">пропертитаггпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="76111-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="76111-158">Долгота.</span><span class="sxs-lookup"><span data-stu-id="76111-158">Longitude.</span></span> <span data-ttu-id="76111-159">Долгота выражается тремя рациональными значениями, предоставляющими градусы, минуты и секунды соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="76111-160">Если выражаются градусы, минуты и секунды, то используется формат DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="76111-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="76111-161">Если используются градусы и минуты, а, например, доли минут задаются до двух десятичных разрядов, используется формат DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="76111-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="76111-162">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-162">Property info</span></span> | <span data-ttu-id="76111-163">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-164">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-164">Tag</span></span>   | <span data-ttu-id="76111-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="76111-165">0x0004</span></span>                  |
| <span data-ttu-id="76111-166">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-166">Type</span></span>  | <span data-ttu-id="76111-167">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-168">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-168">Count</span></span> | <span data-ttu-id="76111-169">3</span><span class="sxs-lookup"><span data-stu-id="76111-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="76111-170">пропертитаггпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="76111-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="76111-171">Высота ссылки в метрах.</span><span class="sxs-lookup"><span data-stu-id="76111-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="76111-172">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-172">Property info</span></span> | <span data-ttu-id="76111-173">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-174">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-174">Tag</span></span>   | <span data-ttu-id="76111-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="76111-175">0x0005</span></span>              |
| <span data-ttu-id="76111-176">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-176">Type</span></span>  | <span data-ttu-id="76111-177">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-178">Count</span><span class="sxs-lookup"><span data-stu-id="76111-178">Count</span></span> | <span data-ttu-id="76111-179">1</span><span class="sxs-lookup"><span data-stu-id="76111-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="76111-180">пропертитаггпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="76111-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="76111-181">Высота в метрах, основанная на высоте ссылок, заданном параметром Пропертитаггпсалтитудереф.</span><span class="sxs-lookup"><span data-stu-id="76111-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="76111-182">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-182">Property info</span></span> | <span data-ttu-id="76111-183">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-184">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-184">Tag</span></span>   | <span data-ttu-id="76111-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="76111-185">0x0006</span></span>                  |
| <span data-ttu-id="76111-186">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-186">Type</span></span>  | <span data-ttu-id="76111-187">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-188">Count</span><span class="sxs-lookup"><span data-stu-id="76111-188">Count</span></span> | <span data-ttu-id="76111-189">1</span><span class="sxs-lookup"><span data-stu-id="76111-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="76111-190">пропертитаггпсгпстиме</span><span class="sxs-lookup"><span data-stu-id="76111-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="76111-191">Время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="76111-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="76111-192">Значение выражается тремя рациональными числами, которые дают час, минуту и секунду.</span><span class="sxs-lookup"><span data-stu-id="76111-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="76111-193">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-193">Property info</span></span> | <span data-ttu-id="76111-194">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-195">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-195">Tag</span></span>   | <span data-ttu-id="76111-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="76111-196">0x0007</span></span>                  |
| <span data-ttu-id="76111-197">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-197">Type</span></span>  | <span data-ttu-id="76111-198">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-199">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-199">Count</span></span> | <span data-ttu-id="76111-200">3</span><span class="sxs-lookup"><span data-stu-id="76111-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="76111-201">пропертитаггпсгпссателлитес</span><span class="sxs-lookup"><span data-stu-id="76111-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="76111-202">Строка символов, завершающаяся нулем, которая указывает вспомогательные спутники GPS, используемые для измерений.</span><span class="sxs-lookup"><span data-stu-id="76111-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="76111-203">С помощью этого тега можно указать ИДЕНТИФИКАЦИОНный номер, угол возвышения, азимус, СНР и другие сведения о каждой спутнике.</span><span class="sxs-lookup"><span data-stu-id="76111-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="76111-204">Формат не указан.</span><span class="sxs-lookup"><span data-stu-id="76111-204">The format is not specified.</span></span> <span data-ttu-id="76111-205">Если приемник GPS не поддерживает измерения, значение тега должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="76111-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="76111-206">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-206">Property info</span></span> | <span data-ttu-id="76111-207">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-208">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-208">Tag</span></span>   | <span data-ttu-id="76111-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="76111-209">0x0008</span></span>                                             |
| <span data-ttu-id="76111-210">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-210">Type</span></span>  | <span data-ttu-id="76111-211">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-212">Count</span><span class="sxs-lookup"><span data-stu-id="76111-212">Count</span></span> | <span data-ttu-id="76111-213">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="76111-214">пропертитаггпсгпсстатус</span><span class="sxs-lookup"><span data-stu-id="76111-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="76111-215">Строка символов, завершающаяся нулем, указывающая состояние приемника GPS при записи образа.</span><span class="sxs-lookup"><span data-stu-id="76111-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="76111-216">`A` означает, что измерение выполняется и `V` означает, что измерение является взаимодействием.</span><span class="sxs-lookup"><span data-stu-id="76111-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="76111-217">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-217">Property info</span></span> | <span data-ttu-id="76111-218">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-219">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-219">Tag</span></span>   | <span data-ttu-id="76111-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="76111-220">0x0009</span></span>                                     |
| <span data-ttu-id="76111-221">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-221">Type</span></span>  | <span data-ttu-id="76111-222">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-223">Count</span><span class="sxs-lookup"><span data-stu-id="76111-223">Count</span></span> | <span data-ttu-id="76111-224">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="76111-225">пропертитаггпсгпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="76111-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="76111-226">Строка символов, завершающаяся нулем, указывающая режим измерения GPS.</span><span class="sxs-lookup"><span data-stu-id="76111-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="76111-227">`2` Задает 2-D измерение и `3` задает Трехмерное измерение.</span><span class="sxs-lookup"><span data-stu-id="76111-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="76111-228">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-228">Property info</span></span> | <span data-ttu-id="76111-229">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-230">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-230">Tag</span></span>   | <span data-ttu-id="76111-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="76111-231">0x000A</span></span>                                     |
| <span data-ttu-id="76111-232">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-232">Type</span></span>  | <span data-ttu-id="76111-233">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-234">Count</span><span class="sxs-lookup"><span data-stu-id="76111-234">Count</span></span> | <span data-ttu-id="76111-235">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="76111-236">пропертитаггпсгпсдоп</span><span class="sxs-lookup"><span data-stu-id="76111-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="76111-237">GPS DOP (степень точности данных).</span><span class="sxs-lookup"><span data-stu-id="76111-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="76111-238">Значение ХДОП записывается во время двухмерного измерения, а значение ПДОП записывается при трехмерном измерении.</span><span class="sxs-lookup"><span data-stu-id="76111-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="76111-239">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-239">Property info</span></span> | <span data-ttu-id="76111-240">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-241">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-241">Tag</span></span>   | <span data-ttu-id="76111-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="76111-242">0x000B</span></span>                  |
| <span data-ttu-id="76111-243">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-243">Type</span></span>  | <span data-ttu-id="76111-244">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-245">Count</span><span class="sxs-lookup"><span data-stu-id="76111-245">Count</span></span> | <span data-ttu-id="76111-246">1</span><span class="sxs-lookup"><span data-stu-id="76111-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="76111-247">пропертитаггпсспидреф</span><span class="sxs-lookup"><span data-stu-id="76111-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="76111-248">Строка символов, завершающаяся нулем, указывающая единицу, используемую для выражения скорости перемещения GPS-приемника.</span><span class="sxs-lookup"><span data-stu-id="76111-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="76111-249">`K`, `M` и `N` представляют километры в час, миль в час и Кнотс соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="76111-250">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-250">Property info</span></span> | <span data-ttu-id="76111-251">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-252">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-252">Tag</span></span>   | <span data-ttu-id="76111-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="76111-253">0x000C</span></span>                                     |
| <span data-ttu-id="76111-254">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-254">Type</span></span>  | <span data-ttu-id="76111-255">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-256">Count</span><span class="sxs-lookup"><span data-stu-id="76111-256">Count</span></span> | <span data-ttu-id="76111-257">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="76111-258">пропертитаггпсспид</span><span class="sxs-lookup"><span data-stu-id="76111-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="76111-259">Скорость перемещения приемника GPS.</span><span class="sxs-lookup"><span data-stu-id="76111-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="76111-260">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-260">Property info</span></span> | <span data-ttu-id="76111-261">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-262">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-262">Tag</span></span>   | <span data-ttu-id="76111-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="76111-263">0x000D</span></span>                  |
| <span data-ttu-id="76111-264">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-264">Type</span></span>  | <span data-ttu-id="76111-265">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-266">Count</span><span class="sxs-lookup"><span data-stu-id="76111-266">Count</span></span> | <span data-ttu-id="76111-267">1</span><span class="sxs-lookup"><span data-stu-id="76111-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="76111-268">пропертитаггпстраккреф</span><span class="sxs-lookup"><span data-stu-id="76111-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="76111-269">Строка символов, завершающаяся нулем, указывающая ссылку для направления перемещения GPS-приемника.</span><span class="sxs-lookup"><span data-stu-id="76111-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="76111-270">`T` задает значение true Direction и `M` указывает направление магнитного потока.</span><span class="sxs-lookup"><span data-stu-id="76111-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="76111-271">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-271">Property info</span></span> | <span data-ttu-id="76111-272">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-273">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-273">Tag</span></span>   | <span data-ttu-id="76111-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="76111-274">0x000E</span></span>                                     |
| <span data-ttu-id="76111-275">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-275">Type</span></span>  | <span data-ttu-id="76111-276">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-277">Count</span><span class="sxs-lookup"><span data-stu-id="76111-277">Count</span></span> | <span data-ttu-id="76111-278">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="76111-279">пропертитаггпстракк</span><span class="sxs-lookup"><span data-stu-id="76111-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="76111-280">Направление перемещения GPS ресивер.</span><span class="sxs-lookup"><span data-stu-id="76111-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="76111-281">Диапазон значений — от 0,00 до 359,99.</span><span class="sxs-lookup"><span data-stu-id="76111-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="76111-282">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-282">Property info</span></span> | <span data-ttu-id="76111-283">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-284">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-284">Tag</span></span>   | <span data-ttu-id="76111-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="76111-285">0x000F</span></span>                  |
| <span data-ttu-id="76111-286">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-286">Type</span></span>  | <span data-ttu-id="76111-287">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-288">Count</span><span class="sxs-lookup"><span data-stu-id="76111-288">Count</span></span> | <span data-ttu-id="76111-289">1</span><span class="sxs-lookup"><span data-stu-id="76111-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="76111-290">пропертитаггпсимгдирреф</span><span class="sxs-lookup"><span data-stu-id="76111-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="76111-291">Строка символов, завершающаяся нулем, указывающая ссылку на направление изображения при его записи.</span><span class="sxs-lookup"><span data-stu-id="76111-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="76111-292">`T` задает значение true Direction и `M` указывает направление магнитного потока.</span><span class="sxs-lookup"><span data-stu-id="76111-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="76111-293">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-293">Property info</span></span> | <span data-ttu-id="76111-294">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-295">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-295">Tag</span></span>   | <span data-ttu-id="76111-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="76111-296">0x0010</span></span>                                     |
| <span data-ttu-id="76111-297">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-297">Type</span></span>  | <span data-ttu-id="76111-298">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-299">Count</span><span class="sxs-lookup"><span data-stu-id="76111-299">Count</span></span> | <span data-ttu-id="76111-300">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="76111-301">пропертитаггпсимгдир</span><span class="sxs-lookup"><span data-stu-id="76111-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="76111-302">Направление изображения, когда оно было захвачено.</span><span class="sxs-lookup"><span data-stu-id="76111-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="76111-303">Диапазон значений — от 0,00 до 359,99.</span><span class="sxs-lookup"><span data-stu-id="76111-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="76111-304">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-304">Property info</span></span> | <span data-ttu-id="76111-305">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-306">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-306">Tag</span></span>   | <span data-ttu-id="76111-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="76111-307">0x0011</span></span>                  |
| <span data-ttu-id="76111-308">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-308">Type</span></span>  | <span data-ttu-id="76111-309">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-310">Count</span><span class="sxs-lookup"><span data-stu-id="76111-310">Count</span></span> | <span data-ttu-id="76111-311">1</span><span class="sxs-lookup"><span data-stu-id="76111-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="76111-312">пропертитаггпсмапдатум</span><span class="sxs-lookup"><span data-stu-id="76111-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="76111-313">Строка символов, завершающаяся нулем, указывающая геодезический данные опроса, используемые приемником GPS.</span><span class="sxs-lookup"><span data-stu-id="76111-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="76111-314">Если данные опроса ограничены Япония, значение этого тега равно `TOKYO` или `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="76111-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="76111-315">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-315">Property info</span></span> | <span data-ttu-id="76111-316">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-317">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-317">Tag</span></span>   | <span data-ttu-id="76111-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="76111-318">0x0012</span></span>                                             |
| <span data-ttu-id="76111-319">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-319">Type</span></span>  | <span data-ttu-id="76111-320">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-321">Count</span><span class="sxs-lookup"><span data-stu-id="76111-321">Count</span></span> | <span data-ttu-id="76111-322">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="76111-323">пропертитаггпсдестлатреф</span><span class="sxs-lookup"><span data-stu-id="76111-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="76111-324">Строка символов, завершающаяся нулем, указывающая, является ли Широта точки назначения Севером или Юго-долготой.</span><span class="sxs-lookup"><span data-stu-id="76111-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="76111-325">`N` Указывает Север широты и `S` указывает Юго-Широта.</span><span class="sxs-lookup"><span data-stu-id="76111-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="76111-326">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-326">Property info</span></span> | <span data-ttu-id="76111-327">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-328">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-328">Tag</span></span>   | <span data-ttu-id="76111-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="76111-329">0x0013</span></span>                                     |
| <span data-ttu-id="76111-330">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-330">Type</span></span>  | <span data-ttu-id="76111-331">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-332">Count</span><span class="sxs-lookup"><span data-stu-id="76111-332">Count</span></span> | <span data-ttu-id="76111-333">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="76111-334">пропертитаггпсдестлат</span><span class="sxs-lookup"><span data-stu-id="76111-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="76111-335">Широта целевой точки.</span><span class="sxs-lookup"><span data-stu-id="76111-335">Latitude of the destination point.</span></span> <span data-ttu-id="76111-336">Широта выражается тремя рациональными значениями, предоставляющими градусы, минуты и секунды соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="76111-337">Если выражаются градусы, минуты и секунды, то используется формат ДД/1, мм/1, СС/1.</span><span class="sxs-lookup"><span data-stu-id="76111-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="76111-338">Если используются градусы и минуты и, например, доли минут получают до двух десятичных разрядов, форматом будет дд/1, мммм/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="76111-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="76111-339">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-339">Property info</span></span> | <span data-ttu-id="76111-340">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-341">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-341">Tag</span></span>   | <span data-ttu-id="76111-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="76111-342">0x0014</span></span>                  |
| <span data-ttu-id="76111-343">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-343">Type</span></span>  | <span data-ttu-id="76111-344">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-345">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-345">Count</span></span> | <span data-ttu-id="76111-346">3</span><span class="sxs-lookup"><span data-stu-id="76111-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="76111-347">пропертитаггпсдестлонгреф</span><span class="sxs-lookup"><span data-stu-id="76111-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="76111-348">Строка символов, завершающаяся нулем, указывающая, является ли Долгота точки назначения Восточная или Западной долготой.</span><span class="sxs-lookup"><span data-stu-id="76111-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="76111-349">`E` Задает "Восток" и " `W` Западная Долгота".</span><span class="sxs-lookup"><span data-stu-id="76111-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="76111-350">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-350">Property info</span></span> | <span data-ttu-id="76111-351">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-352">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-352">Tag</span></span>   | <span data-ttu-id="76111-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="76111-353">0x0015</span></span>                                     |
| <span data-ttu-id="76111-354">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-354">Type</span></span>  | <span data-ttu-id="76111-355">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-356">Count</span><span class="sxs-lookup"><span data-stu-id="76111-356">Count</span></span> | <span data-ttu-id="76111-357">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="76111-358">пропертитаггпсдестлонг</span><span class="sxs-lookup"><span data-stu-id="76111-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="76111-359">Долгота целевой точки.</span><span class="sxs-lookup"><span data-stu-id="76111-359">Longitude of the destination point.</span></span> <span data-ttu-id="76111-360">Долгота выражается тремя рациональными значениями, предоставляющими градусы, минуты и секунды соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="76111-361">Если выражаются градусы, минуты и секунды, то используется формат DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="76111-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="76111-362">Если используются градусы и минуты, а, например, доли минут задаются до двух десятичных разрядов, используется формат DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="76111-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="76111-363">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-363">Property info</span></span> | <span data-ttu-id="76111-364">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-365">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-365">Tag</span></span>   | <span data-ttu-id="76111-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="76111-366">0x0016</span></span>                  |
| <span data-ttu-id="76111-367">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-367">Type</span></span>  | <span data-ttu-id="76111-368">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-369">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-369">Count</span></span> | <span data-ttu-id="76111-370">3</span><span class="sxs-lookup"><span data-stu-id="76111-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="76111-371">пропертитаггпсдестбеарреф</span><span class="sxs-lookup"><span data-stu-id="76111-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="76111-372">Строка символов, завершающаяся нулем, указывающая ссылку, используемую для предоставления отношения к конечной точке.</span><span class="sxs-lookup"><span data-stu-id="76111-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="76111-373">`T` задает значение true Direction и `M` указывает направление магнитного потока.</span><span class="sxs-lookup"><span data-stu-id="76111-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="76111-374">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-374">Property info</span></span> | <span data-ttu-id="76111-375">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-376">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-376">Tag</span></span>   | <span data-ttu-id="76111-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="76111-377">0x0017</span></span>                                     |
| <span data-ttu-id="76111-378">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-378">Type</span></span>  | <span data-ttu-id="76111-379">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-380">Count</span><span class="sxs-lookup"><span data-stu-id="76111-380">Count</span></span> | <span data-ttu-id="76111-381">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="76111-382">пропертитаггпсдестбеар</span><span class="sxs-lookup"><span data-stu-id="76111-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="76111-383">Влияет на целевую точку.</span><span class="sxs-lookup"><span data-stu-id="76111-383">Bearing to the destination point.</span></span> <span data-ttu-id="76111-384">Диапазон значений — от 0,00 до 359,99.</span><span class="sxs-lookup"><span data-stu-id="76111-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="76111-385">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-385">Property info</span></span> | <span data-ttu-id="76111-386">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-387">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-387">Tag</span></span>   | <span data-ttu-id="76111-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="76111-388">0x0018</span></span>                  |
| <span data-ttu-id="76111-389">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-389">Type</span></span>  | <span data-ttu-id="76111-390">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-391">Count</span><span class="sxs-lookup"><span data-stu-id="76111-391">Count</span></span> | <span data-ttu-id="76111-392">1</span><span class="sxs-lookup"><span data-stu-id="76111-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="76111-393">пропертитаггпсдестдистреф</span><span class="sxs-lookup"><span data-stu-id="76111-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="76111-394">Строка символов, завершающаяся нулем, указывающая единицу, используемую для выражения расстояния до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="76111-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="76111-395">K, M и N представляют километры, мили и Кнотс соответственно.</span><span class="sxs-lookup"><span data-stu-id="76111-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="76111-396">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-396">Property info</span></span> | <span data-ttu-id="76111-397">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="76111-398">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-398">Tag</span></span>   | <span data-ttu-id="76111-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="76111-399">0x0019</span></span>                                     |
| <span data-ttu-id="76111-400">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-400">Type</span></span>  | <span data-ttu-id="76111-401">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="76111-402">Count</span><span class="sxs-lookup"><span data-stu-id="76111-402">Count</span></span> | <span data-ttu-id="76111-403">2 (один символ и знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="76111-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="76111-404">пропертитаггпсдестдист</span><span class="sxs-lookup"><span data-stu-id="76111-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="76111-405">Расстояние до конечной точки.</span><span class="sxs-lookup"><span data-stu-id="76111-405">Distance to the destination point.</span></span>



| <span data-ttu-id="76111-406">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-406">Property info</span></span> | <span data-ttu-id="76111-407">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-408">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-408">Tag</span></span>   | <span data-ttu-id="76111-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="76111-409">0x001A</span></span>                  |
| <span data-ttu-id="76111-410">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-410">Type</span></span>  | <span data-ttu-id="76111-411">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-412">Count</span><span class="sxs-lookup"><span data-stu-id="76111-412">Count</span></span> | <span data-ttu-id="76111-413">1</span><span class="sxs-lookup"><span data-stu-id="76111-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="76111-414">пропертитагневсубфилетипе</span><span class="sxs-lookup"><span data-stu-id="76111-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="76111-415">Тип данных в подфайле.</span><span class="sxs-lookup"><span data-stu-id="76111-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="76111-416">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-416">Property info</span></span> | <span data-ttu-id="76111-417">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-418">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-418">Tag</span></span>   | <span data-ttu-id="76111-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="76111-419">0x00FE</span></span>              |
| <span data-ttu-id="76111-420">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-420">Type</span></span>  | <span data-ttu-id="76111-421">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-422">Count</span><span class="sxs-lookup"><span data-stu-id="76111-422">Count</span></span> | <span data-ttu-id="76111-423">1</span><span class="sxs-lookup"><span data-stu-id="76111-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="76111-424">пропертитагсубфилетипе</span><span class="sxs-lookup"><span data-stu-id="76111-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="76111-425">Тип данных в подфайле.</span><span class="sxs-lookup"><span data-stu-id="76111-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="76111-426">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-426">Property info</span></span> | <span data-ttu-id="76111-427">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-428">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-428">Tag</span></span>   | <span data-ttu-id="76111-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="76111-429">0x00FF</span></span>               |
| <span data-ttu-id="76111-430">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-430">Type</span></span>  | <span data-ttu-id="76111-431">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-432">Count</span><span class="sxs-lookup"><span data-stu-id="76111-432">Count</span></span> | <span data-ttu-id="76111-433">1</span><span class="sxs-lookup"><span data-stu-id="76111-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="76111-434">пропертитагимажевидс</span><span class="sxs-lookup"><span data-stu-id="76111-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="76111-435">Количество пикселей на строку.</span><span class="sxs-lookup"><span data-stu-id="76111-435">Number of pixels per row.</span></span>



| <span data-ttu-id="76111-436">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-436">Property info</span></span> | <span data-ttu-id="76111-437">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-438">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-438">Tag</span></span>   | <span data-ttu-id="76111-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="76111-439">0x0100</span></span>                                      |
| <span data-ttu-id="76111-440">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-440">Type</span></span>  | <span data-ttu-id="76111-441">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-442">Count</span><span class="sxs-lookup"><span data-stu-id="76111-442">Count</span></span> | <span data-ttu-id="76111-443">1</span><span class="sxs-lookup"><span data-stu-id="76111-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="76111-444">пропертитагимажехеигхт</span><span class="sxs-lookup"><span data-stu-id="76111-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="76111-445">Число строк в пикселях.</span><span class="sxs-lookup"><span data-stu-id="76111-445">Number of pixel rows.</span></span>



| <span data-ttu-id="76111-446">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-446">Property info</span></span> | <span data-ttu-id="76111-447">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-448">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-448">Tag</span></span>   | <span data-ttu-id="76111-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="76111-449">0x0101</span></span>                                      |
| <span data-ttu-id="76111-450">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-450">Type</span></span>  | <span data-ttu-id="76111-451">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-452">Count</span><span class="sxs-lookup"><span data-stu-id="76111-452">Count</span></span> | <span data-ttu-id="76111-453">1</span><span class="sxs-lookup"><span data-stu-id="76111-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="76111-454">пропертитагбитсперсампле</span><span class="sxs-lookup"><span data-stu-id="76111-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="76111-455">Число битов на компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="76111-455">Number of bits per color component.</span></span> <span data-ttu-id="76111-456">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-457">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-457">Property info</span></span> | <span data-ttu-id="76111-458">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-459">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-459">Tag</span></span>   | <span data-ttu-id="76111-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="76111-460">0x0102</span></span>                                   |
| <span data-ttu-id="76111-461">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-461">Type</span></span>  | <span data-ttu-id="76111-462">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-463">Count</span><span class="sxs-lookup"><span data-stu-id="76111-463">Count</span></span> | <span data-ttu-id="76111-464">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="76111-465">пропертитагкомпрессион</span><span class="sxs-lookup"><span data-stu-id="76111-465">PropertyTagCompression</span></span>

<span data-ttu-id="76111-466">Схема сжатия, используемая для данных изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="76111-467">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-467">Property info</span></span> | <span data-ttu-id="76111-468">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-469">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-469">Tag</span></span>   | <span data-ttu-id="76111-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="76111-470">0x0103</span></span>               |
| <span data-ttu-id="76111-471">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-471">Type</span></span>  | <span data-ttu-id="76111-472">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-473">Count</span><span class="sxs-lookup"><span data-stu-id="76111-473">Count</span></span> | <span data-ttu-id="76111-474">1</span><span class="sxs-lookup"><span data-stu-id="76111-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="76111-475">пропертитагфотометриЦинтерп</span><span class="sxs-lookup"><span data-stu-id="76111-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="76111-476">Как будут интерпретироваться данные в пикселях.</span><span class="sxs-lookup"><span data-stu-id="76111-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="76111-477">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-477">Property info</span></span> | <span data-ttu-id="76111-478">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-479">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-479">Tag</span></span>   | <span data-ttu-id="76111-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="76111-480">0x0106</span></span>               |
| <span data-ttu-id="76111-481">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-481">Type</span></span>  | <span data-ttu-id="76111-482">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-483">Count</span><span class="sxs-lookup"><span data-stu-id="76111-483">Count</span></span> | <span data-ttu-id="76111-484">1</span><span class="sxs-lookup"><span data-stu-id="76111-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="76111-485">пропертитагсрешхолдинг</span><span class="sxs-lookup"><span data-stu-id="76111-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="76111-486">Метод, используемый для преобразования серых пикселей в черные и белые пиксели.</span><span class="sxs-lookup"><span data-stu-id="76111-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="76111-487">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-487">Property info</span></span> | <span data-ttu-id="76111-488">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-489">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-489">Tag</span></span>   | <span data-ttu-id="76111-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="76111-490">0x0107</span></span>               |
| <span data-ttu-id="76111-491">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-491">Type</span></span>  | <span data-ttu-id="76111-492">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-493">Count</span><span class="sxs-lookup"><span data-stu-id="76111-493">Count</span></span> | <span data-ttu-id="76111-494">1</span><span class="sxs-lookup"><span data-stu-id="76111-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="76111-495">пропертитагцеллвидс</span><span class="sxs-lookup"><span data-stu-id="76111-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="76111-496">Ширина матрицы сглаживания или передачи полутонов.</span><span class="sxs-lookup"><span data-stu-id="76111-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="76111-497">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-497">Property info</span></span> | <span data-ttu-id="76111-498">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-499">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-499">Tag</span></span>   | <span data-ttu-id="76111-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="76111-500">0x0108</span></span>               |
| <span data-ttu-id="76111-501">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-501">Type</span></span>  | <span data-ttu-id="76111-502">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-503">Count</span><span class="sxs-lookup"><span data-stu-id="76111-503">Count</span></span> | <span data-ttu-id="76111-504">1</span><span class="sxs-lookup"><span data-stu-id="76111-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="76111-505">пропертитагцеллхеигхт</span><span class="sxs-lookup"><span data-stu-id="76111-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="76111-506">Высота матрицы сглаживания или передачи полутонов.</span><span class="sxs-lookup"><span data-stu-id="76111-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="76111-507">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-507">Property info</span></span> | <span data-ttu-id="76111-508">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-509">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-509">Tag</span></span>   | <span data-ttu-id="76111-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="76111-510">0x0109</span></span>               |
| <span data-ttu-id="76111-511">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-511">Type</span></span>  | <span data-ttu-id="76111-512">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-513">Count</span><span class="sxs-lookup"><span data-stu-id="76111-513">Count</span></span> | <span data-ttu-id="76111-514">1</span><span class="sxs-lookup"><span data-stu-id="76111-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="76111-515">пропертитагфиллордер</span><span class="sxs-lookup"><span data-stu-id="76111-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="76111-516">Логический порядок битов в байте.</span><span class="sxs-lookup"><span data-stu-id="76111-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="76111-517">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-517">Property info</span></span> | <span data-ttu-id="76111-518">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-519">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-519">Tag</span></span>   | <span data-ttu-id="76111-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="76111-520">0x010A</span></span>               |
| <span data-ttu-id="76111-521">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-521">Type</span></span>  | <span data-ttu-id="76111-522">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-523">Count</span><span class="sxs-lookup"><span data-stu-id="76111-523">Count</span></span> | <span data-ttu-id="76111-524">1</span><span class="sxs-lookup"><span data-stu-id="76111-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="76111-525">пропертитагдокументнаме</span><span class="sxs-lookup"><span data-stu-id="76111-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="76111-526">Строка символов, завершающаяся нулем, указывающая имя документа, из которого было выполнено сканирование изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="76111-527">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-527">Property info</span></span> | <span data-ttu-id="76111-528">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-529">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-529">Tag</span></span>   | <span data-ttu-id="76111-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="76111-530">0x010D</span></span>                                             |
| <span data-ttu-id="76111-531">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-531">Type</span></span>  | <span data-ttu-id="76111-532">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-533">Count</span><span class="sxs-lookup"><span data-stu-id="76111-533">Count</span></span> | <span data-ttu-id="76111-534">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="76111-535">пропертитагимажедескриптион</span><span class="sxs-lookup"><span data-stu-id="76111-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="76111-536">Строка символов, завершающаяся нулем, указывающая название изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="76111-537">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-537">Property info</span></span> | <span data-ttu-id="76111-538">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-539">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-539">Tag</span></span>   | <span data-ttu-id="76111-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="76111-540">0x010E</span></span>                                             |
| <span data-ttu-id="76111-541">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-541">Type</span></span>  | <span data-ttu-id="76111-542">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-543">Count</span><span class="sxs-lookup"><span data-stu-id="76111-543">Count</span></span> | <span data-ttu-id="76111-544">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="76111-545">пропертитажекуипмаке</span><span class="sxs-lookup"><span data-stu-id="76111-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="76111-546">Строка символов, завершающаяся нулем, которая указывает изготовителя оборудования, используемого для записи образа.</span><span class="sxs-lookup"><span data-stu-id="76111-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="76111-547">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-547">Property info</span></span> | <span data-ttu-id="76111-548">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-549">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-549">Tag</span></span>   | <span data-ttu-id="76111-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="76111-550">0x010F</span></span>                                             |
| <span data-ttu-id="76111-551">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-551">Type</span></span>  | <span data-ttu-id="76111-552">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-553">Count</span><span class="sxs-lookup"><span data-stu-id="76111-553">Count</span></span> | <span data-ttu-id="76111-554">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="76111-555">пропертитажекуипмодел</span><span class="sxs-lookup"><span data-stu-id="76111-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="76111-556">Строка символов, завершающаяся нулем, которая указывает имя модели или номер модели оборудования, используемого для записи образа.</span><span class="sxs-lookup"><span data-stu-id="76111-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="76111-557">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-557">Property info</span></span> | <span data-ttu-id="76111-558">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-559">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-559">Tag</span></span>   | <span data-ttu-id="76111-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="76111-560">0x0110</span></span>                                             |
| <span data-ttu-id="76111-561">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-561">Type</span></span>  | <span data-ttu-id="76111-562">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-563">Count</span><span class="sxs-lookup"><span data-stu-id="76111-563">Count</span></span> | <span data-ttu-id="76111-564">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="76111-565">пропертитагстрипоффсетс</span><span class="sxs-lookup"><span data-stu-id="76111-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="76111-566">Для каждой полосы — смещение в байтах для этой полосы.</span><span class="sxs-lookup"><span data-stu-id="76111-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="76111-567">См. также [пропертитагровсперстрип](#propertytagrowsperstrip) и [пропертитагстрипбитескаунт](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="76111-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="76111-568">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-568">Property info</span></span> | <span data-ttu-id="76111-569">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-570">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-570">Tag</span></span>   | <span data-ttu-id="76111-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="76111-571">0x0111</span></span>                                      |
| <span data-ttu-id="76111-572">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-572">Type</span></span>  | <span data-ttu-id="76111-573">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-574">Count</span><span class="sxs-lookup"><span data-stu-id="76111-574">Count</span></span> | <span data-ttu-id="76111-575">Число полос</span><span class="sxs-lookup"><span data-stu-id="76111-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="76111-576">пропертитагориентатион</span><span class="sxs-lookup"><span data-stu-id="76111-576">PropertyTagOrientation</span></span>

<span data-ttu-id="76111-577">Ориентация изображения, просматриваемая с точки зрения строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="76111-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="76111-578">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-578">Tag</span></span>

<span data-ttu-id="76111-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="76111-579">0x0112</span></span>

<span data-ttu-id="76111-580">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-580">Type</span></span>

<span data-ttu-id="76111-581">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-582">Count</span><span class="sxs-lookup"><span data-stu-id="76111-582">Count</span></span>

<span data-ttu-id="76111-583">1</span><span class="sxs-lookup"><span data-stu-id="76111-583">1</span></span>

<span data-ttu-id="76111-584">1 — 0-я строка находится в верхней части визуального изображения, а 0-ом столбец — визуальная левая часть.</span><span class="sxs-lookup"><span data-stu-id="76111-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="76111-585">2 — 0-я строка находится на визуальном элементе изображения, а 0 — на визуальной правой стороне.</span><span class="sxs-lookup"><span data-stu-id="76111-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="76111-586">3 — 0-я строка находится в визуальной нижней части изображения, а 0 — на визуальной правой стороне.</span><span class="sxs-lookup"><span data-stu-id="76111-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="76111-587">4.0-я строка находится в нижней части изображения, а 0-ом является видимой левой стороной.</span><span class="sxs-lookup"><span data-stu-id="76111-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="76111-588">5 — 0-я строка — это визуальная левая сторона изображения, а 0-ом столбец — визуальный элемент.</span><span class="sxs-lookup"><span data-stu-id="76111-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="76111-589">6 — 0-я строка — это визуальная правая сторона изображения, а 0-ом — визуальный элемент.</span><span class="sxs-lookup"><span data-stu-id="76111-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="76111-590">7 — 0-я строка — это визуальная правая сторона изображения, а 0-ом столбец — это визуальная Нижняя.</span><span class="sxs-lookup"><span data-stu-id="76111-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="76111-591">8 — 0-я строка — это визуальная левая сторона изображения, а 0-ом столбец — это визуальная Нижняя.</span><span class="sxs-lookup"><span data-stu-id="76111-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="76111-592">пропертитагсамплесперпиксел</span><span class="sxs-lookup"><span data-stu-id="76111-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="76111-593">Число цветовых компонентов на пиксель.</span><span class="sxs-lookup"><span data-stu-id="76111-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="76111-594">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-594">Property info</span></span> | <span data-ttu-id="76111-595">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-596">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-596">Tag</span></span>   | <span data-ttu-id="76111-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="76111-597">0x0115</span></span>               |
| <span data-ttu-id="76111-598">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-598">Type</span></span>  | <span data-ttu-id="76111-599">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-600">Count</span><span class="sxs-lookup"><span data-stu-id="76111-600">Count</span></span> | <span data-ttu-id="76111-601">1</span><span class="sxs-lookup"><span data-stu-id="76111-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="76111-602">пропертитагровсперстрип</span><span class="sxs-lookup"><span data-stu-id="76111-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="76111-603">Число строк на ленту.</span><span class="sxs-lookup"><span data-stu-id="76111-603">Number of rows per strip.</span></span> <span data-ttu-id="76111-604">См. также [пропертитагстрипбитескаунт](#propertytagstripbytescount) и [пропертитагстрипоффсетс](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="76111-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="76111-605">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-605">Property info</span></span> | <span data-ttu-id="76111-606">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-607">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-607">Tag</span></span>   | <span data-ttu-id="76111-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="76111-608">0x0116</span></span>                                      |
| <span data-ttu-id="76111-609">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-609">Type</span></span>  | <span data-ttu-id="76111-610">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-611">Count</span><span class="sxs-lookup"><span data-stu-id="76111-611">Count</span></span> | <span data-ttu-id="76111-612">1</span><span class="sxs-lookup"><span data-stu-id="76111-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="76111-613">пропертитагстрипбитескаунт</span><span class="sxs-lookup"><span data-stu-id="76111-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="76111-614">Для каждой полосы — общее число байтов в этой полосе.</span><span class="sxs-lookup"><span data-stu-id="76111-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="76111-615">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-615">Property info</span></span> | <span data-ttu-id="76111-616">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-617">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-617">Tag</span></span>   | <span data-ttu-id="76111-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="76111-618">0x0117</span></span>                                      |
| <span data-ttu-id="76111-619">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-619">Type</span></span>  | <span data-ttu-id="76111-620">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-621">Count</span><span class="sxs-lookup"><span data-stu-id="76111-621">Count</span></span> | <span data-ttu-id="76111-622">Число полос</span><span class="sxs-lookup"><span data-stu-id="76111-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="76111-623">пропертитагминсамплевалуе</span><span class="sxs-lookup"><span data-stu-id="76111-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="76111-624">Для каждого компонента цвета — минимальное значение, присвоенное этому компоненту.</span><span class="sxs-lookup"><span data-stu-id="76111-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="76111-625">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-626">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-626">Property info</span></span> | <span data-ttu-id="76111-627">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-628">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-628">Tag</span></span>   | <span data-ttu-id="76111-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="76111-629">0x0118</span></span>                                   |
| <span data-ttu-id="76111-630">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-630">Type</span></span>  | <span data-ttu-id="76111-631">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-632">Count</span><span class="sxs-lookup"><span data-stu-id="76111-632">Count</span></span> | <span data-ttu-id="76111-633">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="76111-634">пропертитагмакссамплевалуе</span><span class="sxs-lookup"><span data-stu-id="76111-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="76111-635">Для каждого компонента цвета — максимальное значение, присвоенное этому компоненту.</span><span class="sxs-lookup"><span data-stu-id="76111-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="76111-636">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-637">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-637">Property info</span></span> | <span data-ttu-id="76111-638">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-639">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-639">Tag</span></span>   | <span data-ttu-id="76111-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="76111-640">0x0119</span></span>                                   |
| <span data-ttu-id="76111-641">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-641">Type</span></span>  | <span data-ttu-id="76111-642">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-643">Count</span><span class="sxs-lookup"><span data-stu-id="76111-643">Count</span></span> | <span data-ttu-id="76111-644">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="76111-645">пропертитагксресолутион</span><span class="sxs-lookup"><span data-stu-id="76111-645">PropertyTagXResolution</span></span>

<span data-ttu-id="76111-646">Число пикселей на единицу в направлении ширины изображения (x).</span><span class="sxs-lookup"><span data-stu-id="76111-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="76111-647">Единица задается параметром [пропертитагресолутионунит](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="76111-648">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-648">Property info</span></span> | <span data-ttu-id="76111-649">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-650">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-650">Tag</span></span>   | <span data-ttu-id="76111-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="76111-651">0x011A</span></span>                  |
| <span data-ttu-id="76111-652">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-652">Type</span></span>  | <span data-ttu-id="76111-653">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-654">Count</span><span class="sxs-lookup"><span data-stu-id="76111-654">Count</span></span> | <span data-ttu-id="76111-655">1</span><span class="sxs-lookup"><span data-stu-id="76111-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="76111-656">пропертитагиресолутион</span><span class="sxs-lookup"><span data-stu-id="76111-656">PropertyTagYResolution</span></span>

<span data-ttu-id="76111-657">Число пикселей на единицу в направлении высоты (y) изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="76111-658">Единица задается параметром [пропертитагресолутионунит](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="76111-659">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-659">Property info</span></span> | <span data-ttu-id="76111-660">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-661">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-661">Tag</span></span>   | <span data-ttu-id="76111-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="76111-662">0x011B</span></span>                  |
| <span data-ttu-id="76111-663">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-663">Type</span></span>  | <span data-ttu-id="76111-664">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-665">Count</span><span class="sxs-lookup"><span data-stu-id="76111-665">Count</span></span> | <span data-ttu-id="76111-666">1</span><span class="sxs-lookup"><span data-stu-id="76111-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="76111-667">пропертитагпланарконфиг</span><span class="sxs-lookup"><span data-stu-id="76111-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="76111-668">Записываются ли компоненты пикселей в больших или плоском формате.</span><span class="sxs-lookup"><span data-stu-id="76111-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="76111-669">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-669">Property info</span></span> | <span data-ttu-id="76111-670">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-671">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-671">Tag</span></span>   | <span data-ttu-id="76111-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="76111-672">0x011C</span></span>               |
| <span data-ttu-id="76111-673">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-673">Type</span></span>  | <span data-ttu-id="76111-674">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-675">Count</span><span class="sxs-lookup"><span data-stu-id="76111-675">Count</span></span> | <span data-ttu-id="76111-676">1</span><span class="sxs-lookup"><span data-stu-id="76111-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="76111-677">пропертитагпаженаме</span><span class="sxs-lookup"><span data-stu-id="76111-677">PropertyTagPageName</span></span>

<span data-ttu-id="76111-678">Строка символов, завершающаяся нулем, указывающая имя страницы, из которой было выполнено сканирование изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="76111-679">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-679">Property info</span></span> | <span data-ttu-id="76111-680">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-681">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-681">Tag</span></span>   | <span data-ttu-id="76111-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="76111-682">0x011D</span></span>                                             |
| <span data-ttu-id="76111-683">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-683">Type</span></span>  | <span data-ttu-id="76111-684">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-685">Count</span><span class="sxs-lookup"><span data-stu-id="76111-685">Count</span></span> | <span data-ttu-id="76111-686">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="76111-687">пропертитагкспоситион</span><span class="sxs-lookup"><span data-stu-id="76111-687">PropertyTagXPosition</span></span>

<span data-ttu-id="76111-688">Смещение от левой части страницы до левой части изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="76111-689">Единица измерения задается параметром [пропертитагресолутионунит](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="76111-690">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-690">Property info</span></span> | <span data-ttu-id="76111-691">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-692">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-692">Tag</span></span>   | <span data-ttu-id="76111-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="76111-693">0x011E</span></span>                  |
| <span data-ttu-id="76111-694">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-694">Type</span></span>  | <span data-ttu-id="76111-695">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-696">Count</span><span class="sxs-lookup"><span data-stu-id="76111-696">Count</span></span> | <span data-ttu-id="76111-697">1</span><span class="sxs-lookup"><span data-stu-id="76111-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="76111-698">пропертитагипоситион</span><span class="sxs-lookup"><span data-stu-id="76111-698">PropertyTagYPosition</span></span>

<span data-ttu-id="76111-699">Смещение от верхнего края страницы до верхней части изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="76111-700">Единица измерения задается параметром [пропертитагресолутионунит](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="76111-701">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-701">Property info</span></span> | <span data-ttu-id="76111-702">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-703">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-703">Tag</span></span>   | <span data-ttu-id="76111-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="76111-704">0x011F</span></span>                  |
| <span data-ttu-id="76111-705">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-705">Type</span></span>  | <span data-ttu-id="76111-706">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-707">Count</span><span class="sxs-lookup"><span data-stu-id="76111-707">Count</span></span> | <span data-ttu-id="76111-708">1</span><span class="sxs-lookup"><span data-stu-id="76111-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="76111-709">пропертитагфриоффсет</span><span class="sxs-lookup"><span data-stu-id="76111-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="76111-710">Для каждой строки непрерывных неиспользуемых байтов смещение строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="76111-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="76111-711">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-711">Property info</span></span> | <span data-ttu-id="76111-712">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="76111-713">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-713">Tag</span></span>  | <span data-ttu-id="76111-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="76111-714">0x0120</span></span>              |
| <span data-ttu-id="76111-715">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-715">Type</span></span> | <span data-ttu-id="76111-716">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="76111-717">пропертитагфрибитекаунтс</span><span class="sxs-lookup"><span data-stu-id="76111-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="76111-718">Для каждой строки смежных неиспользуемых байтов — число байтов в этой строке.</span><span class="sxs-lookup"><span data-stu-id="76111-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="76111-719">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-719">Property info</span></span> | <span data-ttu-id="76111-720">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="76111-721">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-721">Tag</span></span>   | <span data-ttu-id="76111-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="76111-722">0x0121</span></span>                                        |
| <span data-ttu-id="76111-723">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-723">Type</span></span>  | <span data-ttu-id="76111-724">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="76111-725">Count</span><span class="sxs-lookup"><span data-stu-id="76111-725">Count</span></span> | <span data-ttu-id="76111-726">Число строк смежных неиспользуемых байтов.</span><span class="sxs-lookup"><span data-stu-id="76111-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="76111-727">пропертитагграйреспонсеунит</span><span class="sxs-lookup"><span data-stu-id="76111-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="76111-728">Точность числа, заданного параметром Пропертитагграйреспонсекурве.</span><span class="sxs-lookup"><span data-stu-id="76111-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="76111-729">1 указывает десятые доли, 2 — сотые, 3 — доли секунды и т. д.</span><span class="sxs-lookup"><span data-stu-id="76111-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="76111-730">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-730">Property info</span></span> | <span data-ttu-id="76111-731">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-732">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-732">Tag</span></span>   | <span data-ttu-id="76111-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="76111-733">0x0122</span></span>               |
| <span data-ttu-id="76111-734">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-734">Type</span></span>  | <span data-ttu-id="76111-735">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-736">Count</span><span class="sxs-lookup"><span data-stu-id="76111-736">Count</span></span> | <span data-ttu-id="76111-737">1</span><span class="sxs-lookup"><span data-stu-id="76111-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="76111-738">пропертитагграйреспонсекурве</span><span class="sxs-lookup"><span data-stu-id="76111-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="76111-739">Для каждого возможного значения пикселя в изображении в градациях серого это значение пикселя оптической плотности.</span><span class="sxs-lookup"><span data-stu-id="76111-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="76111-740">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-740">Property info</span></span> | <span data-ttu-id="76111-741">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="76111-742">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-742">Tag</span></span>   | <span data-ttu-id="76111-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="76111-743">0x0123</span></span>                          |
| <span data-ttu-id="76111-744">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-744">Type</span></span>  | <span data-ttu-id="76111-745">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="76111-746">Count</span><span class="sxs-lookup"><span data-stu-id="76111-746">Count</span></span> | <span data-ttu-id="76111-747">Число возможных значений пикселей</span><span class="sxs-lookup"><span data-stu-id="76111-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="76111-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="76111-748">PropertyTagT4Option</span></span>

<span data-ttu-id="76111-749">Набор флагов, связанных с кодировкой T4.</span><span class="sxs-lookup"><span data-stu-id="76111-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="76111-750">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-750">Property info</span></span> | <span data-ttu-id="76111-751">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-752">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-752">Tag</span></span>   | <span data-ttu-id="76111-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="76111-753">0x0124</span></span>              |
| <span data-ttu-id="76111-754">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-754">Type</span></span>  | <span data-ttu-id="76111-755">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-756">Count</span><span class="sxs-lookup"><span data-stu-id="76111-756">Count</span></span> | <span data-ttu-id="76111-757">1</span><span class="sxs-lookup"><span data-stu-id="76111-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="76111-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="76111-758">PropertyTagT6Option</span></span>

<span data-ttu-id="76111-759">Набор флагов, связанных с кодировкой T6.</span><span class="sxs-lookup"><span data-stu-id="76111-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="76111-760">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-760">Property info</span></span> | <span data-ttu-id="76111-761">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-762">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-762">Tag</span></span>   | <span data-ttu-id="76111-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="76111-763">0x0125</span></span>              |
| <span data-ttu-id="76111-764">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-764">Type</span></span>  | <span data-ttu-id="76111-765">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-766">Count</span><span class="sxs-lookup"><span data-stu-id="76111-766">Count</span></span> | <span data-ttu-id="76111-767">1</span><span class="sxs-lookup"><span data-stu-id="76111-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="76111-768">пропертитагресолутионунит</span><span class="sxs-lookup"><span data-stu-id="76111-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="76111-769">Единица измерения для разрешения по горизонтали и разрешения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="76111-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="76111-770">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-770">Tag</span></span>

<span data-ttu-id="76111-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="76111-771">0x0128</span></span>

<span data-ttu-id="76111-772">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-772">Type</span></span>

<span data-ttu-id="76111-773">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-774">Count</span><span class="sxs-lookup"><span data-stu-id="76111-774">Count</span></span>

<span data-ttu-id="76111-775">1</span><span class="sxs-lookup"><span data-stu-id="76111-775">1</span></span>

<span data-ttu-id="76111-776">2-дюймовый 3-сантиметр</span><span class="sxs-lookup"><span data-stu-id="76111-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="76111-777">пропертитагпаженумбер</span><span class="sxs-lookup"><span data-stu-id="76111-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="76111-778">Номер страницы страницы, с которой было выполнено сканирование изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="76111-779">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-779">Property info</span></span> | <span data-ttu-id="76111-780">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-781">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-781">Tag</span></span>   | <span data-ttu-id="76111-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="76111-782">0x0129</span></span>               |
| <span data-ttu-id="76111-783">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-783">Type</span></span>  | <span data-ttu-id="76111-784">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-785">Count</span><span class="sxs-lookup"><span data-stu-id="76111-785">Count</span></span> | <span data-ttu-id="76111-786">1</span><span class="sxs-lookup"><span data-stu-id="76111-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="76111-787">пропертитагтрансферфунктион</span><span class="sxs-lookup"><span data-stu-id="76111-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="76111-788">Таблицы, указывающие функции перемещения для изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="76111-789">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-789">Property info</span></span> | <span data-ttu-id="76111-790">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="76111-791">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-791">Tag</span></span>   | <span data-ttu-id="76111-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="76111-792">0x012D</span></span>                                               |
| <span data-ttu-id="76111-793">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-793">Type</span></span>  | <span data-ttu-id="76111-794">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="76111-795">Count</span><span class="sxs-lookup"><span data-stu-id="76111-795">Count</span></span> | <span data-ttu-id="76111-796">Общее число 16-разрядных слов, необходимых для таблиц</span><span class="sxs-lookup"><span data-stu-id="76111-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="76111-797">пропертитагсофтвареусед</span><span class="sxs-lookup"><span data-stu-id="76111-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="76111-798">Строка символов, завершающаяся нулем, которая указывает имя и версию программного обеспечения или микропрограммы устройства, используемого для создания образа.</span><span class="sxs-lookup"><span data-stu-id="76111-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="76111-799">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-799">Property info</span></span> | <span data-ttu-id="76111-800">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-801">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-801">Tag</span></span>   | <span data-ttu-id="76111-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="76111-802">0x0131</span></span>                                             |
| <span data-ttu-id="76111-803">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-803">Type</span></span>  | <span data-ttu-id="76111-804">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-805">Count</span><span class="sxs-lookup"><span data-stu-id="76111-805">Count</span></span> | <span data-ttu-id="76111-806">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="76111-807">пропертитагдатетиме</span><span class="sxs-lookup"><span data-stu-id="76111-807">PropertyTagDateTime</span></span>

<span data-ttu-id="76111-808">Дата и время создания образа.</span><span class="sxs-lookup"><span data-stu-id="76111-808">Date and time the image was created.</span></span>



| <span data-ttu-id="76111-809">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-809">Property info</span></span> | <span data-ttu-id="76111-810">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-811">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-811">Tag</span></span>   | <span data-ttu-id="76111-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="76111-812">0x0132</span></span>               |
| <span data-ttu-id="76111-813">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-813">Type</span></span>  | <span data-ttu-id="76111-814">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-815">Count</span><span class="sxs-lookup"><span data-stu-id="76111-815">Count</span></span> | <span data-ttu-id="76111-816">20</span><span class="sxs-lookup"><span data-stu-id="76111-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="76111-817">пропертитагартист</span><span class="sxs-lookup"><span data-stu-id="76111-817">PropertyTagArtist</span></span>

<span data-ttu-id="76111-818">Строка символов, завершающаяся нулем, указывающая имя пользователя, создавшего изображение.</span><span class="sxs-lookup"><span data-stu-id="76111-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="76111-819">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-819">Property info</span></span> | <span data-ttu-id="76111-820">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-821">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-821">Tag</span></span>   | <span data-ttu-id="76111-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="76111-822">0x013B</span></span>                                             |
| <span data-ttu-id="76111-823">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-823">Type</span></span>  | <span data-ttu-id="76111-824">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-825">Count</span><span class="sxs-lookup"><span data-stu-id="76111-825">Count</span></span> | <span data-ttu-id="76111-826">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="76111-827">пропертитагхосткомпутер</span><span class="sxs-lookup"><span data-stu-id="76111-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="76111-828">Строка символов, завершающаяся нулем, которая указывает компьютер и (или) операционную систему, используемую для создания образа.</span><span class="sxs-lookup"><span data-stu-id="76111-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="76111-829">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-829">Property info</span></span> | <span data-ttu-id="76111-830">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-831">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-831">Tag</span></span>   | <span data-ttu-id="76111-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="76111-832">0x013C</span></span>                                             |
| <span data-ttu-id="76111-833">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-833">Type</span></span>  | <span data-ttu-id="76111-834">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-835">Count</span><span class="sxs-lookup"><span data-stu-id="76111-835">Count</span></span> | <span data-ttu-id="76111-836">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="76111-837">пропертитагпредиктор</span><span class="sxs-lookup"><span data-stu-id="76111-837">PropertyTagPredictor</span></span>

<span data-ttu-id="76111-838">Тип схемы прогнозирования, которая была применена к данным изображения до применения схемы кодировки.</span><span class="sxs-lookup"><span data-stu-id="76111-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="76111-839">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-839">Property info</span></span> | <span data-ttu-id="76111-840">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-841">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-841">Tag</span></span>   | <span data-ttu-id="76111-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="76111-842">0x013D</span></span>               |
| <span data-ttu-id="76111-843">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-843">Type</span></span>  | <span data-ttu-id="76111-844">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-845">Count</span><span class="sxs-lookup"><span data-stu-id="76111-845">Count</span></span> | <span data-ttu-id="76111-846">1</span><span class="sxs-lookup"><span data-stu-id="76111-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="76111-847">пропертитагвхитепоинт</span><span class="sxs-lookup"><span data-stu-id="76111-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="76111-848">Цветная точка белого изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="76111-849">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-849">Property info</span></span> | <span data-ttu-id="76111-850">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-851">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-851">Tag</span></span>   | <span data-ttu-id="76111-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="76111-852">0x013E</span></span>                  |
| <span data-ttu-id="76111-853">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-853">Type</span></span>  | <span data-ttu-id="76111-854">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-855">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-855">Count</span></span> | <span data-ttu-id="76111-856">2</span><span class="sxs-lookup"><span data-stu-id="76111-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="76111-857">пропертитагпримаричроматиЦитиес</span><span class="sxs-lookup"><span data-stu-id="76111-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="76111-858">Для каждого из трех основных цветов изображения это цвет.</span><span class="sxs-lookup"><span data-stu-id="76111-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="76111-859">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-859">Property info</span></span> | <span data-ttu-id="76111-860">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-861">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-861">Tag</span></span>   | <span data-ttu-id="76111-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="76111-862">0x013F</span></span>                  |
| <span data-ttu-id="76111-863">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-863">Type</span></span>  | <span data-ttu-id="76111-864">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-865">Count</span><span class="sxs-lookup"><span data-stu-id="76111-865">Count</span></span> | <span data-ttu-id="76111-866">6</span><span class="sxs-lookup"><span data-stu-id="76111-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="76111-867">пропертитагколормап</span><span class="sxs-lookup"><span data-stu-id="76111-867">PropertyTagColorMap</span></span>

<span data-ttu-id="76111-868">Цветовая палитра (таблица подстановки) для изображения, индексированного по палитре.</span><span class="sxs-lookup"><span data-stu-id="76111-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="76111-869">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-869">Property info</span></span> | <span data-ttu-id="76111-870">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="76111-871">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-871">Tag</span></span>   | <span data-ttu-id="76111-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="76111-872">0x0140</span></span>                                          |
| <span data-ttu-id="76111-873">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-873">Type</span></span>  | <span data-ttu-id="76111-874">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="76111-875">Count</span><span class="sxs-lookup"><span data-stu-id="76111-875">Count</span></span> | <span data-ttu-id="76111-876">Число 16-разрядных слов, необходимых для палитры</span><span class="sxs-lookup"><span data-stu-id="76111-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="76111-877">пропертитагхалфтонехинтс</span><span class="sxs-lookup"><span data-stu-id="76111-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="76111-878">Сведения, используемые функцией передачи полутонов</span><span class="sxs-lookup"><span data-stu-id="76111-878">Information used by the halftone function</span></span>



| <span data-ttu-id="76111-879">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-879">Property info</span></span> | <span data-ttu-id="76111-880">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-881">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-881">Tag</span></span>   | <span data-ttu-id="76111-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="76111-882">0x0141</span></span>               |
| <span data-ttu-id="76111-883">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-883">Type</span></span>  | <span data-ttu-id="76111-884">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-885">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-885">Count</span></span> | <span data-ttu-id="76111-886">2</span><span class="sxs-lookup"><span data-stu-id="76111-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="76111-887">пропертитагтилевидс</span><span class="sxs-lookup"><span data-stu-id="76111-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="76111-888">Число столбцов пикселей в каждой плитке.</span><span class="sxs-lookup"><span data-stu-id="76111-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="76111-889">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-889">Property info</span></span> | <span data-ttu-id="76111-890">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-891">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-891">Tag</span></span>   | <span data-ttu-id="76111-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="76111-892">0x0142</span></span>                                      |
| <span data-ttu-id="76111-893">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-893">Type</span></span>  | <span data-ttu-id="76111-894">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-895">Count</span><span class="sxs-lookup"><span data-stu-id="76111-895">Count</span></span> | <span data-ttu-id="76111-896">1</span><span class="sxs-lookup"><span data-stu-id="76111-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="76111-897">пропертитагтилеленгс</span><span class="sxs-lookup"><span data-stu-id="76111-897">PropertyTagTileLength</span></span>

<span data-ttu-id="76111-898">Число строк пикселей в каждой плитке.</span><span class="sxs-lookup"><span data-stu-id="76111-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="76111-899">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-899">Property info</span></span> | <span data-ttu-id="76111-900">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-901">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-901">Tag</span></span>   | <span data-ttu-id="76111-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="76111-902">0x0143</span></span>                                      |
| <span data-ttu-id="76111-903">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-903">Type</span></span>  | <span data-ttu-id="76111-904">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-905">Count</span><span class="sxs-lookup"><span data-stu-id="76111-905">Count</span></span> | <span data-ttu-id="76111-906">1</span><span class="sxs-lookup"><span data-stu-id="76111-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="76111-907">пропертитагтилеоффсет</span><span class="sxs-lookup"><span data-stu-id="76111-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="76111-908">Для каждой плитки — смещение в байтах для этой плитки.</span><span class="sxs-lookup"><span data-stu-id="76111-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="76111-909">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-909">Property info</span></span> | <span data-ttu-id="76111-910">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-911">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-911">Tag</span></span>   | <span data-ttu-id="76111-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="76111-912">0x0144</span></span>              |
| <span data-ttu-id="76111-913">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-913">Type</span></span>  | <span data-ttu-id="76111-914">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-915">Count</span><span class="sxs-lookup"><span data-stu-id="76111-915">Count</span></span> | <span data-ttu-id="76111-916">Число плиток</span><span class="sxs-lookup"><span data-stu-id="76111-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="76111-917">пропертитагтилебитекаунтс</span><span class="sxs-lookup"><span data-stu-id="76111-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="76111-918">Для каждой плитки — число байтов в этой плитке.</span><span class="sxs-lookup"><span data-stu-id="76111-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="76111-919">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-919">Property info</span></span> | <span data-ttu-id="76111-920">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-921">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-921">Tag</span></span>   | <span data-ttu-id="76111-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="76111-922">0x0145</span></span>                                      |
| <span data-ttu-id="76111-923">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-923">Type</span></span>  | <span data-ttu-id="76111-924">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-925">Count</span><span class="sxs-lookup"><span data-stu-id="76111-925">Count</span></span> | <span data-ttu-id="76111-926">Число плиток</span><span class="sxs-lookup"><span data-stu-id="76111-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="76111-927">пропертитагинксет</span><span class="sxs-lookup"><span data-stu-id="76111-927">PropertyTagInkSet</span></span>

<span data-ttu-id="76111-928">Набор красок, используемых в отдельном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="76111-929">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-929">Property info</span></span> | <span data-ttu-id="76111-930">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-931">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-931">Tag</span></span>   | <span data-ttu-id="76111-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="76111-932">0x014C</span></span>               |
| <span data-ttu-id="76111-933">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-933">Type</span></span>  | <span data-ttu-id="76111-934">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-935">Count</span><span class="sxs-lookup"><span data-stu-id="76111-935">Count</span></span> | <span data-ttu-id="76111-936">1</span><span class="sxs-lookup"><span data-stu-id="76111-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="76111-937">пропертитагинкнамес</span><span class="sxs-lookup"><span data-stu-id="76111-937">PropertyTagInkNames</span></span>

<span data-ttu-id="76111-938">Последовательность сцепленных строк, заканчивающихся символом NULL, которые указывают имена красок, используемых в отдельном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="76111-939">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-939">Property info</span></span> | <span data-ttu-id="76111-940">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="76111-941">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-941">Tag</span></span>   | <span data-ttu-id="76111-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="76111-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="76111-943">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-943">Type</span></span>  | <span data-ttu-id="76111-944">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="76111-945">Count</span><span class="sxs-lookup"><span data-stu-id="76111-945">Count</span></span> | <span data-ttu-id="76111-946">Общая длина последовательности строк, включая признаки конца строки</span><span class="sxs-lookup"><span data-stu-id="76111-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="76111-947">пропертитагнумберофинкс</span><span class="sxs-lookup"><span data-stu-id="76111-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="76111-948">Число красок.</span><span class="sxs-lookup"><span data-stu-id="76111-948">Number of inks.</span></span>



| <span data-ttu-id="76111-949">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-949">Property info</span></span> | <span data-ttu-id="76111-950">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-951">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-951">Tag</span></span>   | <span data-ttu-id="76111-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="76111-952">0x014E</span></span>               |
| <span data-ttu-id="76111-953">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-953">Type</span></span>  | <span data-ttu-id="76111-954">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-955">Count</span><span class="sxs-lookup"><span data-stu-id="76111-955">Count</span></span> | <span data-ttu-id="76111-956">1</span><span class="sxs-lookup"><span data-stu-id="76111-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="76111-957">пропертитагдотранже</span><span class="sxs-lookup"><span data-stu-id="76111-957">PropertyTagDotRange</span></span>

<span data-ttu-id="76111-958">Значения компонентов цвета, которые соответствуют 0-процентной точке и точке 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="76111-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="76111-959">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-959">Property info</span></span> | <span data-ttu-id="76111-960">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-961">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-961">Tag</span></span>   | <span data-ttu-id="76111-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="76111-962">0x0150</span></span>                                      |
| <span data-ttu-id="76111-963">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-963">Type</span></span>  | <span data-ttu-id="76111-964">Пропертитагтипебите или Пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-965">Count</span><span class="sxs-lookup"><span data-stu-id="76111-965">Count</span></span> | <span data-ttu-id="76111-966">2 или 2 х Пропертитагсамплесперпиксел</span><span class="sxs-lookup"><span data-stu-id="76111-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="76111-967">пропертитагтаржетпринтер</span><span class="sxs-lookup"><span data-stu-id="76111-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="76111-968">Строка символов, завершающаяся нулем, которая описывает предполагаемую среду печати.</span><span class="sxs-lookup"><span data-stu-id="76111-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="76111-969">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-969">Property info</span></span> | <span data-ttu-id="76111-970">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-971">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-971">Tag</span></span>   | <span data-ttu-id="76111-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="76111-972">0x0151</span></span>                                             |
| <span data-ttu-id="76111-973">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-973">Type</span></span>  | <span data-ttu-id="76111-974">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-975">Count</span><span class="sxs-lookup"><span data-stu-id="76111-975">Count</span></span> | <span data-ttu-id="76111-976">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="76111-977">пропертитажекстрасамплес</span><span class="sxs-lookup"><span data-stu-id="76111-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="76111-978">Число дополнительных компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="76111-978">Number of extra color components.</span></span> <span data-ttu-id="76111-979">Например, один дополнительный компонент может содержать альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="76111-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="76111-980">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-980">Property info</span></span> | <span data-ttu-id="76111-981">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-982">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-982">Tag</span></span>   | <span data-ttu-id="76111-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="76111-983">0x0152</span></span>               |
| <span data-ttu-id="76111-984">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-984">Type</span></span>  | <span data-ttu-id="76111-985">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-986">Count</span><span class="sxs-lookup"><span data-stu-id="76111-986">Count</span></span> | <span data-ttu-id="76111-987">1</span><span class="sxs-lookup"><span data-stu-id="76111-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="76111-988">пропертитагсамплеформат</span><span class="sxs-lookup"><span data-stu-id="76111-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="76111-989">Для каждого компонента цвета — числовой формат (без знака, со знаком, с плавающей запятой) этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="76111-990">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-991">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-991">Property info</span></span> | <span data-ttu-id="76111-992">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-993">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-993">Tag</span></span>   | <span data-ttu-id="76111-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="76111-994">0x0153</span></span>                                   |
| <span data-ttu-id="76111-995">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-995">Type</span></span>  | <span data-ttu-id="76111-996">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-997">Count</span><span class="sxs-lookup"><span data-stu-id="76111-997">Count</span></span> | <span data-ttu-id="76111-998">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="76111-999">пропертитагсминсамплевалуе</span><span class="sxs-lookup"><span data-stu-id="76111-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="76111-1000">Для каждого компонента цвета — минимальное значение этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="76111-1001">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1002">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1002">Property info</span></span> | <span data-ttu-id="76111-1003">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="76111-1004">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1004">Tag</span></span>   | <span data-ttu-id="76111-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="76111-1005">0x0154</span></span>                                              |
| <span data-ttu-id="76111-1006">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1006">Type</span></span>  | <span data-ttu-id="76111-1007">Тип, который наилучшим образом соответствует данным компонента пикселей</span><span class="sxs-lookup"><span data-stu-id="76111-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="76111-1008">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1008">Count</span></span> | <span data-ttu-id="76111-1009">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="76111-1010">пропертитагсмакссамплевалуе</span><span class="sxs-lookup"><span data-stu-id="76111-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="76111-1011">Для каждого компонента цвета — максимальное значение этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="76111-1012">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1013">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1013">Property info</span></span> | <span data-ttu-id="76111-1014">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="76111-1015">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1015">Tag</span></span>   | <span data-ttu-id="76111-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="76111-1016">0x0155</span></span>                                              |
| <span data-ttu-id="76111-1017">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1017">Type</span></span>  | <span data-ttu-id="76111-1018">Тип, который наилучшим образом соответствует данным компонента пикселей</span><span class="sxs-lookup"><span data-stu-id="76111-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="76111-1019">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1019">Count</span></span> | <span data-ttu-id="76111-1020">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="76111-1021">пропертитагтрансферранже</span><span class="sxs-lookup"><span data-stu-id="76111-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="76111-1022">Таблица значений, которая расширяет диапазон функции перемещения.</span><span class="sxs-lookup"><span data-stu-id="76111-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="76111-1023">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1023">Property info</span></span> | <span data-ttu-id="76111-1024">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1025">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1025">Tag</span></span>   | <span data-ttu-id="76111-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="76111-1026">0x0156</span></span>               |
| <span data-ttu-id="76111-1027">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1027">Type</span></span>  | <span data-ttu-id="76111-1028">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1029">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1029">Count</span></span> | <span data-ttu-id="76111-1030">6</span><span class="sxs-lookup"><span data-stu-id="76111-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="76111-1031">пропертитагжпегпрок</span><span class="sxs-lookup"><span data-stu-id="76111-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="76111-1032">Процесс сжатия JPEG.</span><span class="sxs-lookup"><span data-stu-id="76111-1032">JPEG compression process.</span></span>



| <span data-ttu-id="76111-1033">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1033">Property info</span></span> | <span data-ttu-id="76111-1034">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1035">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1035">Tag</span></span>   | <span data-ttu-id="76111-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="76111-1036">0x0200</span></span>               |
| <span data-ttu-id="76111-1037">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1037">Type</span></span>  | <span data-ttu-id="76111-1038">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1039">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1039">Count</span></span> | <span data-ttu-id="76111-1040">1</span><span class="sxs-lookup"><span data-stu-id="76111-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="76111-1041">пропертитагжпегинтерформат</span><span class="sxs-lookup"><span data-stu-id="76111-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="76111-1042">Смещение до начала JPEG битовый поток.</span><span class="sxs-lookup"><span data-stu-id="76111-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="76111-1043">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1043">Property info</span></span> | <span data-ttu-id="76111-1044">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1045">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1045">Tag</span></span>   | <span data-ttu-id="76111-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="76111-1046">0x0201</span></span>              |
| <span data-ttu-id="76111-1047">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1047">Type</span></span>  | <span data-ttu-id="76111-1048">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1049">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1049">Count</span></span> | <span data-ttu-id="76111-1050">1</span><span class="sxs-lookup"><span data-stu-id="76111-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="76111-1051">пропертитагжпегинтерленгс</span><span class="sxs-lookup"><span data-stu-id="76111-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="76111-1052">Длина (в байтах) битовый поток JPEG.</span><span class="sxs-lookup"><span data-stu-id="76111-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="76111-1053">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1053">Property info</span></span> | <span data-ttu-id="76111-1054">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1055">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1055">Tag</span></span>   | <span data-ttu-id="76111-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="76111-1056">0x0202</span></span>              |
| <span data-ttu-id="76111-1057">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1057">Type</span></span>  | <span data-ttu-id="76111-1058">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1059">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1059">Count</span></span> | <span data-ttu-id="76111-1060">1</span><span class="sxs-lookup"><span data-stu-id="76111-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="76111-1061">пропертитагжпегрестартинтервал</span><span class="sxs-lookup"><span data-stu-id="76111-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="76111-1062">Длина интервала перезапуска.</span><span class="sxs-lookup"><span data-stu-id="76111-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="76111-1063">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1063">Property info</span></span> | <span data-ttu-id="76111-1064">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1065">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1065">Tag</span></span>   | <span data-ttu-id="76111-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="76111-1066">0x0203</span></span>               |
| <span data-ttu-id="76111-1067">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1067">Type</span></span>  | <span data-ttu-id="76111-1068">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1069">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1069">Count</span></span> | <span data-ttu-id="76111-1070">1</span><span class="sxs-lookup"><span data-stu-id="76111-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="76111-1071">пропертитагжпеглосслесспредикторс</span><span class="sxs-lookup"><span data-stu-id="76111-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="76111-1072">Для каждого компонента цвета — значение выбора прогноза без потерь для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="76111-1073">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1074">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1074">Property info</span></span> | <span data-ttu-id="76111-1075">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-1076">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1076">Tag</span></span>   | <span data-ttu-id="76111-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="76111-1077">0x0205</span></span>                                   |
| <span data-ttu-id="76111-1078">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1078">Type</span></span>  | <span data-ttu-id="76111-1079">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-1080">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1080">Count</span></span> | <span data-ttu-id="76111-1081">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="76111-1082">пропертитагжпегпоинттрансформс</span><span class="sxs-lookup"><span data-stu-id="76111-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="76111-1083">Для каждого компонента цвета это значение преобразования «точка» для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="76111-1084">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1085">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1085">Property info</span></span> | <span data-ttu-id="76111-1086">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-1087">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1087">Tag</span></span>   | <span data-ttu-id="76111-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="76111-1088">0x0206</span></span>                                   |
| <span data-ttu-id="76111-1089">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1089">Type</span></span>  | <span data-ttu-id="76111-1090">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="76111-1091">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1091">Count</span></span> | <span data-ttu-id="76111-1092">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="76111-1093">пропертитагжпегктаблес</span><span class="sxs-lookup"><span data-stu-id="76111-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="76111-1094">Для каждого компонента цвета смещение таблицы дискретизация для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="76111-1095">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1096">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1096">Property info</span></span> | <span data-ttu-id="76111-1097">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-1098">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1098">Tag</span></span>   | <span data-ttu-id="76111-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="76111-1099">0x0207</span></span>                                   |
| <span data-ttu-id="76111-1100">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1100">Type</span></span>  | <span data-ttu-id="76111-1101">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="76111-1102">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1102">Count</span></span> | <span data-ttu-id="76111-1103">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="76111-1104">пропертитагжпегдктаблес</span><span class="sxs-lookup"><span data-stu-id="76111-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="76111-1105">Для каждого компонента цвета смещение таблицы DC Хаффмана (или таблицы Хаффмана без потерь) для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="76111-1106">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1107">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1107">Property info</span></span> | <span data-ttu-id="76111-1108">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-1109">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1109">Tag</span></span>   | <span data-ttu-id="76111-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="76111-1110">0x0208</span></span>                                   |
| <span data-ttu-id="76111-1111">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1111">Type</span></span>  | <span data-ttu-id="76111-1112">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="76111-1113">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1113">Count</span></span> | <span data-ttu-id="76111-1114">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="76111-1115">пропертитагжпегактаблес</span><span class="sxs-lookup"><span data-stu-id="76111-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="76111-1116">Для каждого компонента цвета смещение таблицы AC Хаффмана для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="76111-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="76111-1117">См. также [пропертитагсамплесперпиксел](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1118">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1118">Property info</span></span> | <span data-ttu-id="76111-1119">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="76111-1120">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1120">Tag</span></span>   | <span data-ttu-id="76111-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="76111-1121">0x0209</span></span>                                   |
| <span data-ttu-id="76111-1122">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1122">Type</span></span>  | <span data-ttu-id="76111-1123">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="76111-1124">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1124">Count</span></span> | <span data-ttu-id="76111-1125">Число выборок (компонентов) на пиксель</span><span class="sxs-lookup"><span data-stu-id="76111-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="76111-1126">пропертитагикбкркоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="76111-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="76111-1127">Коэффициенты преобразования из RGB в Икбкр Image Data.</span><span class="sxs-lookup"><span data-stu-id="76111-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="76111-1128">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1128">Property info</span></span> | <span data-ttu-id="76111-1129">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1130">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1130">Tag</span></span>   | <span data-ttu-id="76111-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="76111-1131">0x0211</span></span>                  |
| <span data-ttu-id="76111-1132">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1132">Type</span></span>  | <span data-ttu-id="76111-1133">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1134">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-1134">Count</span></span> | <span data-ttu-id="76111-1135">3</span><span class="sxs-lookup"><span data-stu-id="76111-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="76111-1136">пропертитагикбкрсубсамплинг</span><span class="sxs-lookup"><span data-stu-id="76111-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="76111-1137">Коэффициент выборки компонентов чроминанце относительно компонента светимости.</span><span class="sxs-lookup"><span data-stu-id="76111-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="76111-1138">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1138">Property info</span></span> | <span data-ttu-id="76111-1139">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1140">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1140">Tag</span></span>   | <span data-ttu-id="76111-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="76111-1141">0x0212</span></span>               |
| <span data-ttu-id="76111-1142">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1142">Type</span></span>  | <span data-ttu-id="76111-1143">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1144">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-1144">Count</span></span> | <span data-ttu-id="76111-1145">2</span><span class="sxs-lookup"><span data-stu-id="76111-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="76111-1146">пропертитагикбкрпоситионинг</span><span class="sxs-lookup"><span data-stu-id="76111-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="76111-1147">Расположение компонентов чроминанце относительно компонента светимости.</span><span class="sxs-lookup"><span data-stu-id="76111-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="76111-1148">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1148">Property info</span></span> | <span data-ttu-id="76111-1149">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1150">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1150">Tag</span></span>   | <span data-ttu-id="76111-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="76111-1151">0x0213</span></span>               |
| <span data-ttu-id="76111-1152">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1152">Type</span></span>  | <span data-ttu-id="76111-1153">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1154">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1154">Count</span></span> | <span data-ttu-id="76111-1155">1</span><span class="sxs-lookup"><span data-stu-id="76111-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="76111-1156">пропертитагрефблакквхите</span><span class="sxs-lookup"><span data-stu-id="76111-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="76111-1157">Ссылка на значение черной точки и ссылка на значение белого пункта.</span><span class="sxs-lookup"><span data-stu-id="76111-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="76111-1158">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1158">Property info</span></span> | <span data-ttu-id="76111-1159">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1160">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1160">Tag</span></span>   | <span data-ttu-id="76111-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="76111-1161">0x0214</span></span>                  |
| <span data-ttu-id="76111-1162">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1162">Type</span></span>  | <span data-ttu-id="76111-1163">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1164">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1164">Count</span></span> | <span data-ttu-id="76111-1165">6</span><span class="sxs-lookup"><span data-stu-id="76111-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="76111-1166">пропертитаггамма</span><span class="sxs-lookup"><span data-stu-id="76111-1166">PropertyTagGamma</span></span>

<span data-ttu-id="76111-1167">Значение гаммы, прикрепленное к изображению.</span><span class="sxs-lookup"><span data-stu-id="76111-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="76111-1168">Значение гаммы хранится в виде рационального числа (пары **Long**) с числителем 100000.</span><span class="sxs-lookup"><span data-stu-id="76111-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="76111-1169">Например, значение гаммы 2,2 хранится в виде пары (100000, 45455).</span><span class="sxs-lookup"><span data-stu-id="76111-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="76111-1170">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1170">Property info</span></span> | <span data-ttu-id="76111-1171">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1172">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1172">Tag</span></span>   | <span data-ttu-id="76111-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="76111-1173">0x0301</span></span>                  |
| <span data-ttu-id="76111-1174">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1174">Type</span></span>  | <span data-ttu-id="76111-1175">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1176">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1176">Count</span></span> | <span data-ttu-id="76111-1177">1</span><span class="sxs-lookup"><span data-stu-id="76111-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="76111-1178">пропертитагиккпрофиледескриптор</span><span class="sxs-lookup"><span data-stu-id="76111-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="76111-1179">Строка символов, завершающаяся нулем, которая определяет профиль ICC.</span><span class="sxs-lookup"><span data-stu-id="76111-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="76111-1180">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1180">Property info</span></span> | <span data-ttu-id="76111-1181">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1182">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1182">Tag</span></span>   | <span data-ttu-id="76111-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="76111-1183">0x0302</span></span>                                             |
| <span data-ttu-id="76111-1184">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1184">Type</span></span>  | <span data-ttu-id="76111-1185">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1186">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1186">Count</span></span> | <span data-ttu-id="76111-1187">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="76111-1188">пропертитагсргбрендерингинтент</span><span class="sxs-lookup"><span data-stu-id="76111-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="76111-1189">Как изображение должно отображаться в соответствии с определением языка ICC.</span><span class="sxs-lookup"><span data-stu-id="76111-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="76111-1190">Если объект  [**изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ создан с параметром *усимбеддедколорманажемент* , для которого установлено значение **true**, то GDI+ визуализирует изображение в соответствии с заданным намерением визуализации.</span><span class="sxs-lookup"><span data-stu-id="76111-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="76111-1191">Для цели можно задать значение искусственного, относительный контраст, насыщенность или абсолютный.</span><span class="sxs-lookup"><span data-stu-id="76111-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="76111-1192">Искусственного намерение, которое подходит для фотографий, обеспечивает хорошую адаптацию к охвату видеоустройства за счет повышения точности.</span><span class="sxs-lookup"><span data-stu-id="76111-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="76111-1193">Относительная цель подходит для изображений (например, логотипов), для которых требуется соответствие цветового оформления относительно белого пункта устройства отображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="76111-1194">Намерение насыщенности, которое подходит для диаграмм и графиков, сохраняет насыщенность за счет оттенок и яркости.</span><span class="sxs-lookup"><span data-stu-id="76111-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="76111-1195">Абсолютная цель подходит для подтверждения (предварительный просмотр образов, предназначенных для другого устройства отображения), требующих сохранения абсолютного колориметри.</span><span class="sxs-lookup"><span data-stu-id="76111-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="76111-1196">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1196">Tag</span></span>

<span data-ttu-id="76111-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="76111-1197">0x0303</span></span>

<span data-ttu-id="76111-1198">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1198">Type</span></span>

<span data-ttu-id="76111-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="76111-1199">BYTE</span></span>

<span data-ttu-id="76111-1200">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1200">Count</span></span>

<span data-ttu-id="76111-1201">1</span><span class="sxs-lookup"><span data-stu-id="76111-1201">1</span></span>

<span data-ttu-id="76111-1202">0-искусственного 1 — относительный контраст 2 — насыщенность 3 — абсолютный</span><span class="sxs-lookup"><span data-stu-id="76111-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="76111-1203">пропертитагимажетитле</span><span class="sxs-lookup"><span data-stu-id="76111-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="76111-1204">Строка символов, завершающаяся нулем, указывающая название изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="76111-1205">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1205">Property info</span></span> | <span data-ttu-id="76111-1206">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1207">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1207">Tag</span></span>   | <span data-ttu-id="76111-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="76111-1208">0x0320</span></span>                                             |
| <span data-ttu-id="76111-1209">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1209">Type</span></span>  | <span data-ttu-id="76111-1210">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1211">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1211">Count</span></span> | <span data-ttu-id="76111-1212">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="76111-1213">пропертитагресолутионксунит</span><span class="sxs-lookup"><span data-stu-id="76111-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="76111-1214">Единицы, в которых отображается разрешение по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="76111-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="76111-1215">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1215">Tag</span></span>

<span data-ttu-id="76111-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="76111-1216">0x5001</span></span>

<span data-ttu-id="76111-1217">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1217">Type</span></span>

<span data-ttu-id="76111-1218">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1219">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1219">Count</span></span>

<span data-ttu-id="76111-1220">1</span><span class="sxs-lookup"><span data-stu-id="76111-1220">1</span></span>

<span data-ttu-id="76111-1221">1 пиксел на дюйм (2 пиксела на сантиметр)</span><span class="sxs-lookup"><span data-stu-id="76111-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="76111-1222">пропертитагресолутионюнит</span><span class="sxs-lookup"><span data-stu-id="76111-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="76111-1223">Единицы, в которых отображается разрешение по вертикали.</span><span class="sxs-lookup"><span data-stu-id="76111-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="76111-1224">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1224">Tag</span></span>

<span data-ttu-id="76111-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="76111-1225">0x5002</span></span>

<span data-ttu-id="76111-1226">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1226">Type</span></span>

<span data-ttu-id="76111-1227">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1228">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1228">Count</span></span>

<span data-ttu-id="76111-1229">1</span><span class="sxs-lookup"><span data-stu-id="76111-1229">1</span></span>

<span data-ttu-id="76111-1230">1 пиксел на дюйм (2 пиксела на сантиметр)</span><span class="sxs-lookup"><span data-stu-id="76111-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="76111-1231">пропертитагресолутионксленгсунит</span><span class="sxs-lookup"><span data-stu-id="76111-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="76111-1232">Единицы, в которых отображается ширина изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="76111-1233">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1233">Tag</span></span>

<span data-ttu-id="76111-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="76111-1234">0x5003</span></span>

<span data-ttu-id="76111-1235">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1235">Type</span></span>

<span data-ttu-id="76111-1236">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1237">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1237">Count</span></span>

<span data-ttu-id="76111-1238">1</span><span class="sxs-lookup"><span data-stu-id="76111-1238">1</span></span>

<span data-ttu-id="76111-1239">1-дюймовые 2-сантиметры 3-точки 4-пика 5-столбцы</span><span class="sxs-lookup"><span data-stu-id="76111-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="76111-1240">пропертитагресолутиониленгсунит</span><span class="sxs-lookup"><span data-stu-id="76111-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="76111-1241">Единицы, в которых отображается высота изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="76111-1242">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1242">Tag</span></span>

<span data-ttu-id="76111-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="76111-1243">0x5004</span></span>

<span data-ttu-id="76111-1244">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1244">Type</span></span>

<span data-ttu-id="76111-1245">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1246">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1246">Count</span></span>

<span data-ttu-id="76111-1247">1</span><span class="sxs-lookup"><span data-stu-id="76111-1247">1</span></span>

<span data-ttu-id="76111-1248">1-дюймовые 2-сантиметры 3-точки 4-пика 5-столбцы</span><span class="sxs-lookup"><span data-stu-id="76111-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="76111-1249">пропертитагпринтфлагс</span><span class="sxs-lookup"><span data-stu-id="76111-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="76111-1250">Последовательность однобайтовых логических значений, задающих параметры печати.</span><span class="sxs-lookup"><span data-stu-id="76111-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="76111-1251">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1251">Property info</span></span> | <span data-ttu-id="76111-1252">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1253">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1253">Tag</span></span>   | <span data-ttu-id="76111-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="76111-1254">0x5005</span></span>               |
| <span data-ttu-id="76111-1255">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1255">Type</span></span>  | <span data-ttu-id="76111-1256">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-1257">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1257">Count</span></span> | <span data-ttu-id="76111-1258">Число флагов</span><span class="sxs-lookup"><span data-stu-id="76111-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="76111-1259">пропертитагпринтфлагсверсион</span><span class="sxs-lookup"><span data-stu-id="76111-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="76111-1260">Версия флагов печати.</span><span class="sxs-lookup"><span data-stu-id="76111-1260">Print flags version.</span></span>



| <span data-ttu-id="76111-1261">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1261">Property info</span></span> | <span data-ttu-id="76111-1262">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1263">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1263">Tag</span></span>   | <span data-ttu-id="76111-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="76111-1264">0x5006</span></span>               |
| <span data-ttu-id="76111-1265">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1265">Type</span></span>  | <span data-ttu-id="76111-1266">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1267">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1267">Count</span></span> | <span data-ttu-id="76111-1268">1</span><span class="sxs-lookup"><span data-stu-id="76111-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="76111-1269">пропертитагпринтфлагскроп</span><span class="sxs-lookup"><span data-stu-id="76111-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="76111-1270">Печать флагов обрезные метки.</span><span class="sxs-lookup"><span data-stu-id="76111-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="76111-1271">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1271">Property info</span></span> | <span data-ttu-id="76111-1272">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1273">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1273">Tag</span></span>   | <span data-ttu-id="76111-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="76111-1274">0x5007</span></span>              |
| <span data-ttu-id="76111-1275">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1275">Type</span></span>  | <span data-ttu-id="76111-1276">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-1277">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1277">Count</span></span> | <span data-ttu-id="76111-1278">1</span><span class="sxs-lookup"><span data-stu-id="76111-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="76111-1279">пропертитагпринтфлагсблидвидс</span><span class="sxs-lookup"><span data-stu-id="76111-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="76111-1280">Печать флагов для ширины выхода.</span><span class="sxs-lookup"><span data-stu-id="76111-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="76111-1281">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1281">Property info</span></span> | <span data-ttu-id="76111-1282">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1283">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1283">Tag</span></span>   | <span data-ttu-id="76111-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="76111-1284">0x5008</span></span>              |
| <span data-ttu-id="76111-1285">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1285">Type</span></span>  | <span data-ttu-id="76111-1286">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1287">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1287">Count</span></span> | <span data-ttu-id="76111-1288">1</span><span class="sxs-lookup"><span data-stu-id="76111-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="76111-1289">пропертитагпринтфлагсблидвидсскале</span><span class="sxs-lookup"><span data-stu-id="76111-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="76111-1290">Печать флагов, ширина которых уменьшена.</span><span class="sxs-lookup"><span data-stu-id="76111-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="76111-1291">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1291">Property info</span></span> | <span data-ttu-id="76111-1292">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1293">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1293">Tag</span></span>   | <span data-ttu-id="76111-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="76111-1294">0x5009</span></span>               |
| <span data-ttu-id="76111-1295">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1295">Type</span></span>  | <span data-ttu-id="76111-1296">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1297">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1297">Count</span></span> | <span data-ttu-id="76111-1298">1</span><span class="sxs-lookup"><span data-stu-id="76111-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="76111-1299">пропертитагхалфтонелпи</span><span class="sxs-lookup"><span data-stu-id="76111-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="76111-1300">Частота отображения рукописного ввода в строках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="76111-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="76111-1301">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1301">Property info</span></span> | <span data-ttu-id="76111-1302">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1303">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1303">Tag</span></span>   | <span data-ttu-id="76111-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="76111-1304">0x500A</span></span>                  |
| <span data-ttu-id="76111-1305">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1305">Type</span></span>  | <span data-ttu-id="76111-1306">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1307">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1307">Count</span></span> | <span data-ttu-id="76111-1308">1</span><span class="sxs-lookup"><span data-stu-id="76111-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="76111-1309">пропертитагхалфтонелпиунит</span><span class="sxs-lookup"><span data-stu-id="76111-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="76111-1310">Единицы измерения частоты растра.</span><span class="sxs-lookup"><span data-stu-id="76111-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="76111-1311">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1311">Tag</span></span>

<span data-ttu-id="76111-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="76111-1312">0x500B</span></span>

<span data-ttu-id="76111-1313">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1313">Type</span></span>

<span data-ttu-id="76111-1314">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1315">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1315">Count</span></span>

<span data-ttu-id="76111-1316">1</span><span class="sxs-lookup"><span data-stu-id="76111-1316">1</span></span>

<span data-ttu-id="76111-1317">1-линии на дюйм 2-линии на сантиметр</span><span class="sxs-lookup"><span data-stu-id="76111-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="76111-1318">пропертитагхалфтонедегри</span><span class="sxs-lookup"><span data-stu-id="76111-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="76111-1319">Угол для экрана.</span><span class="sxs-lookup"><span data-stu-id="76111-1319">Angle for screen.</span></span>



| <span data-ttu-id="76111-1320">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1320">Property info</span></span> | <span data-ttu-id="76111-1321">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1322">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1322">Tag</span></span>   | <span data-ttu-id="76111-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="76111-1323">0x500C</span></span>                  |
| <span data-ttu-id="76111-1324">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1324">Type</span></span>  | <span data-ttu-id="76111-1325">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1326">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1326">Count</span></span> | <span data-ttu-id="76111-1327">1</span><span class="sxs-lookup"><span data-stu-id="76111-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="76111-1328">пропертитагхалфтонешапе</span><span class="sxs-lookup"><span data-stu-id="76111-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="76111-1329">Форма точек полутонов.</span><span class="sxs-lookup"><span data-stu-id="76111-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="76111-1330">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1330">Tag</span></span>

<span data-ttu-id="76111-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="76111-1331">0x500D</span></span>

<span data-ttu-id="76111-1332">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1332">Type</span></span>

<span data-ttu-id="76111-1333">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-1334">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1334">Count</span></span>

<span data-ttu-id="76111-1335">1</span><span class="sxs-lookup"><span data-stu-id="76111-1335">1</span></span>

<span data-ttu-id="76111-1336">0-округлить 1-эллипс 2-line 3-квадрат 4-Cross 6-ромб</span><span class="sxs-lookup"><span data-stu-id="76111-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="76111-1337">пропертитагхалфтонемиск</span><span class="sxs-lookup"><span data-stu-id="76111-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="76111-1338">Различные сведения о полутонах.</span><span class="sxs-lookup"><span data-stu-id="76111-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="76111-1339">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1339">Property info</span></span> | <span data-ttu-id="76111-1340">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1341">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1341">Tag</span></span>   | <span data-ttu-id="76111-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="76111-1342">0x500E</span></span>              |
| <span data-ttu-id="76111-1343">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1343">Type</span></span>  | <span data-ttu-id="76111-1344">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1345">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1345">Count</span></span> | <span data-ttu-id="76111-1346">1</span><span class="sxs-lookup"><span data-stu-id="76111-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="76111-1347">пропертитагхалфтонескрин</span><span class="sxs-lookup"><span data-stu-id="76111-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="76111-1348">Логическое значение, указывающее, следует ли использовать экраны принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76111-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="76111-1349">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1349">Tag</span></span>

<span data-ttu-id="76111-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="76111-1350">0x500F</span></span>

<span data-ttu-id="76111-1351">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1351">Type</span></span>

<span data-ttu-id="76111-1352">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="76111-1353">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1353">Count</span></span>

<span data-ttu-id="76111-1354">1</span><span class="sxs-lookup"><span data-stu-id="76111-1354">1</span></span>

<span data-ttu-id="76111-1355">1 — использовать экраны принтера по умолчанию 2 — другие</span><span class="sxs-lookup"><span data-stu-id="76111-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="76111-1356">пропертитагжпегкуалити</span><span class="sxs-lookup"><span data-stu-id="76111-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="76111-1357">Закрытый тег, используемый форматом Adobe Photoshop.</span><span class="sxs-lookup"><span data-stu-id="76111-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="76111-1358">Не для свободного использования.</span><span class="sxs-lookup"><span data-stu-id="76111-1358">Not for public use.</span></span>



| <span data-ttu-id="76111-1359">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1359">Property info</span></span> | <span data-ttu-id="76111-1360">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1361">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1361">Tag</span></span>   | <span data-ttu-id="76111-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="76111-1362">0x5010</span></span>               |
| <span data-ttu-id="76111-1363">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1363">Type</span></span>  | <span data-ttu-id="76111-1364">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1365">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1365">Count</span></span> | <span data-ttu-id="76111-1366">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="76111-1367">пропертитаггридсизе</span><span class="sxs-lookup"><span data-stu-id="76111-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="76111-1368">Блок сведений о сетках и направляющих.</span><span class="sxs-lookup"><span data-stu-id="76111-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="76111-1369">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1369">Property info</span></span> | <span data-ttu-id="76111-1370">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-1371">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1371">Tag</span></span>   | <span data-ttu-id="76111-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="76111-1372">0x5011</span></span>                   |
| <span data-ttu-id="76111-1373">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1373">Type</span></span>  | <span data-ttu-id="76111-1374">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-1375">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1375">Count</span></span> | <span data-ttu-id="76111-1376">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="76111-1377">пропертитагсумбнаилформат</span><span class="sxs-lookup"><span data-stu-id="76111-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="76111-1378">Формат эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="76111-1379">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1379">Tag</span></span>

<span data-ttu-id="76111-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="76111-1380">0x5012</span></span>

<span data-ttu-id="76111-1381">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1381">Type</span></span>

<span data-ttu-id="76111-1382">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="76111-1383">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1383">Count</span></span>

<span data-ttu-id="76111-1384">1</span><span class="sxs-lookup"><span data-stu-id="76111-1384">1</span></span>

<span data-ttu-id="76111-1385">0-необработанный RGB 1 — JPEG</span><span class="sxs-lookup"><span data-stu-id="76111-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="76111-1386">пропертитагсумбнаилвидс</span><span class="sxs-lookup"><span data-stu-id="76111-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="76111-1387">Ширина (в пикселях) эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="76111-1388">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1388">Property info</span></span> | <span data-ttu-id="76111-1389">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1390">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1390">Tag</span></span>   | <span data-ttu-id="76111-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="76111-1391">0x5013</span></span>              |
| <span data-ttu-id="76111-1392">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1392">Type</span></span>  | <span data-ttu-id="76111-1393">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1394">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1394">Count</span></span> | <span data-ttu-id="76111-1395">1</span><span class="sxs-lookup"><span data-stu-id="76111-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="76111-1396">пропертитагсумбнаилхеигхт</span><span class="sxs-lookup"><span data-stu-id="76111-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="76111-1397">Высота эскиза изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="76111-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="76111-1398">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1398">Property info</span></span> | <span data-ttu-id="76111-1399">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1400">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1400">Tag</span></span>   | <span data-ttu-id="76111-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="76111-1401">0x5014</span></span>              |
| <span data-ttu-id="76111-1402">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1402">Type</span></span>  | <span data-ttu-id="76111-1403">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1404">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1404">Count</span></span> | <span data-ttu-id="76111-1405">1</span><span class="sxs-lookup"><span data-stu-id="76111-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="76111-1406">пропертитагсумбнаилколордепс</span><span class="sxs-lookup"><span data-stu-id="76111-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="76111-1407">бит на пиксель (в бит) для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="76111-1408">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1408">Property info</span></span> | <span data-ttu-id="76111-1409">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1410">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1410">Tag</span></span>   | <span data-ttu-id="76111-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="76111-1411">0x5015</span></span>               |
| <span data-ttu-id="76111-1412">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1412">Type</span></span>  | <span data-ttu-id="76111-1413">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1414">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1414">Count</span></span> | <span data-ttu-id="76111-1415">1</span><span class="sxs-lookup"><span data-stu-id="76111-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="76111-1416">пропертитагсумбнаилпланес</span><span class="sxs-lookup"><span data-stu-id="76111-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="76111-1417">Число цветовых плоскостей для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="76111-1418">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1418">Property info</span></span> | <span data-ttu-id="76111-1419">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1420">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1420">Tag</span></span>   | <span data-ttu-id="76111-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="76111-1421">0x5016</span></span>               |
| <span data-ttu-id="76111-1422">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1422">Type</span></span>  | <span data-ttu-id="76111-1423">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1424">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1424">Count</span></span> | <span data-ttu-id="76111-1425">1</span><span class="sxs-lookup"><span data-stu-id="76111-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="76111-1426">пропертитагсумбнаилравбитес</span><span class="sxs-lookup"><span data-stu-id="76111-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="76111-1427">Смещение в байтах между строками данных в пикселях.</span><span class="sxs-lookup"><span data-stu-id="76111-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="76111-1428">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1428">Property info</span></span> | <span data-ttu-id="76111-1429">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1430">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1430">Tag</span></span>   | <span data-ttu-id="76111-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="76111-1431">0x5017</span></span>              |
| <span data-ttu-id="76111-1432">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1432">Type</span></span>  | <span data-ttu-id="76111-1433">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1434">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1434">Count</span></span> | <span data-ttu-id="76111-1435">1</span><span class="sxs-lookup"><span data-stu-id="76111-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="76111-1436">пропертитагсумбнаилсизе</span><span class="sxs-lookup"><span data-stu-id="76111-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="76111-1437">Общий размер эскизного изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="76111-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="76111-1438">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1438">Property info</span></span> | <span data-ttu-id="76111-1439">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1440">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1440">Tag</span></span>   | <span data-ttu-id="76111-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="76111-1441">0x5018</span></span>              |
| <span data-ttu-id="76111-1442">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1442">Type</span></span>  | <span data-ttu-id="76111-1443">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1444">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1444">Count</span></span> | <span data-ttu-id="76111-1445">1</span><span class="sxs-lookup"><span data-stu-id="76111-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="76111-1446">пропертитагсумбнаилкомпресседсизе</span><span class="sxs-lookup"><span data-stu-id="76111-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="76111-1447">Сжатый размер эскиза изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="76111-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="76111-1448">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1448">Property info</span></span> | <span data-ttu-id="76111-1449">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1450">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1450">Tag</span></span>   | <span data-ttu-id="76111-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="76111-1451">0x5019</span></span>              |
| <span data-ttu-id="76111-1452">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1452">Type</span></span>  | <span data-ttu-id="76111-1453">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1454">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1454">Count</span></span> | <span data-ttu-id="76111-1455">1</span><span class="sxs-lookup"><span data-stu-id="76111-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="76111-1456">пропертитагколортрансферфунктион</span><span class="sxs-lookup"><span data-stu-id="76111-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="76111-1457">Таблица значений, задающих функции цветовой пересылки.</span><span class="sxs-lookup"><span data-stu-id="76111-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="76111-1458">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1458">Property info</span></span> | <span data-ttu-id="76111-1459">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-1460">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1460">Tag</span></span>   | <span data-ttu-id="76111-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="76111-1461">0x501A</span></span>                   |
| <span data-ttu-id="76111-1462">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1462">Type</span></span>  | <span data-ttu-id="76111-1463">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-1464">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1464">Count</span></span> | <span data-ttu-id="76111-1465">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="76111-1466">пропертитагсумбнаилдата</span><span class="sxs-lookup"><span data-stu-id="76111-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="76111-1467">Необработанные миниатюрные биты в формате JPEG или RGB.</span><span class="sxs-lookup"><span data-stu-id="76111-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="76111-1468">Зависит от Пропертитагсумбнаилформат.</span><span class="sxs-lookup"><span data-stu-id="76111-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="76111-1469">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1469">Property info</span></span> | <span data-ttu-id="76111-1470">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1471">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1471">Tag</span></span>   | <span data-ttu-id="76111-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="76111-1472">0x501B</span></span>              |
| <span data-ttu-id="76111-1473">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1473">Type</span></span>  | <span data-ttu-id="76111-1474">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-1475">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1475">Count</span></span> | <span data-ttu-id="76111-1476">Переменная</span><span class="sxs-lookup"><span data-stu-id="76111-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="76111-1477">пропертитагсумбнаилимажевидс</span><span class="sxs-lookup"><span data-stu-id="76111-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="76111-1478">Количество пикселей на строку в миниатюрном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="76111-1479">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1479">Property info</span></span> | <span data-ttu-id="76111-1480">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-1481">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1481">Tag</span></span>   | <span data-ttu-id="76111-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="76111-1482">0x5020</span></span>                                      |
| <span data-ttu-id="76111-1483">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1483">Type</span></span>  | <span data-ttu-id="76111-1484">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1485">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1485">Count</span></span> | <span data-ttu-id="76111-1486">1</span><span class="sxs-lookup"><span data-stu-id="76111-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="76111-1487">пропертитагсумбнаилимажехеигхт</span><span class="sxs-lookup"><span data-stu-id="76111-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="76111-1488">Число точек в миниатюрном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="76111-1489">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1489">Property info</span></span> | <span data-ttu-id="76111-1490">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-1491">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1491">Tag</span></span>   | <span data-ttu-id="76111-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="76111-1492">0x5021</span></span>                                      |
| <span data-ttu-id="76111-1493">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1493">Type</span></span>  | <span data-ttu-id="76111-1494">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1495">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1495">Count</span></span> | <span data-ttu-id="76111-1496">1</span><span class="sxs-lookup"><span data-stu-id="76111-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="76111-1497">пропертитагсумбнаилбитсперсампле</span><span class="sxs-lookup"><span data-stu-id="76111-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="76111-1498">Число битов на компонент цвета в миниатюрном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="76111-1499">См. также [пропертитагсумбнаилсамплесперпиксел](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="76111-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="76111-1500">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1500">Property info</span></span> | <span data-ttu-id="76111-1501">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="76111-1502">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1502">Tag</span></span>   | <span data-ttu-id="76111-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="76111-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="76111-1504">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1504">Type</span></span>  | <span data-ttu-id="76111-1505">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="76111-1506">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1506">Count</span></span> | <span data-ttu-id="76111-1507">Число выборок (компонентов) на пиксель в миниатюрном изображении</span><span class="sxs-lookup"><span data-stu-id="76111-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="76111-1508">пропертитагсумбнаилкомпрессион</span><span class="sxs-lookup"><span data-stu-id="76111-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="76111-1509">Схема сжатия, используемая для данных эскиза.</span><span class="sxs-lookup"><span data-stu-id="76111-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="76111-1510">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1510">Property info</span></span> | <span data-ttu-id="76111-1511">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1512">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1512">Tag</span></span>   | <span data-ttu-id="76111-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="76111-1513">0x5023</span></span>               |
| <span data-ttu-id="76111-1514">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1514">Type</span></span>  | <span data-ttu-id="76111-1515">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1516">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1516">Count</span></span> | <span data-ttu-id="76111-1517">1</span><span class="sxs-lookup"><span data-stu-id="76111-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="76111-1518">пропертитагсумбнаилфотометриЦинтерп</span><span class="sxs-lookup"><span data-stu-id="76111-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="76111-1519">Как будут интерпретироваться эскизы данных в пикселях.</span><span class="sxs-lookup"><span data-stu-id="76111-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="76111-1520">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1520">Property info</span></span> | <span data-ttu-id="76111-1521">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1522">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1522">Tag</span></span>   | <span data-ttu-id="76111-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="76111-1523">0x5024</span></span>               |
| <span data-ttu-id="76111-1524">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1524">Type</span></span>  | <span data-ttu-id="76111-1525">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1526">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1526">Count</span></span> | <span data-ttu-id="76111-1527">1</span><span class="sxs-lookup"><span data-stu-id="76111-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="76111-1528">пропертитагсумбнаилимажедескриптион</span><span class="sxs-lookup"><span data-stu-id="76111-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="76111-1529">Строка символов, завершающаяся нулем, указывающая название изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="76111-1530">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1530">Property info</span></span> | <span data-ttu-id="76111-1531">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1532">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1532">Tag</span></span>   | <span data-ttu-id="76111-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="76111-1533">0x5025</span></span>                                             |
| <span data-ttu-id="76111-1534">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1534">Type</span></span>  | <span data-ttu-id="76111-1535">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1536">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1536">Count</span></span> | <span data-ttu-id="76111-1537">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="76111-1538">пропертитагсумбнаилекуипмаке</span><span class="sxs-lookup"><span data-stu-id="76111-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="76111-1539">Строка символов, завершающаяся нулем, которая указывает изготовителя оборудования, используемого для записи эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="76111-1540">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1540">Property info</span></span> | <span data-ttu-id="76111-1541">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1542">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1542">Tag</span></span>   | <span data-ttu-id="76111-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="76111-1543">0x5026</span></span>                                             |
| <span data-ttu-id="76111-1544">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1544">Type</span></span>  | <span data-ttu-id="76111-1545">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1546">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1546">Count</span></span> | <span data-ttu-id="76111-1547">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="76111-1548">пропертитагсумбнаилекуипмодел</span><span class="sxs-lookup"><span data-stu-id="76111-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="76111-1549">Строка символов, завершающаяся нулем, которая указывает имя модели или номер модели оборудования, используемого для записи эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="76111-1550">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1550">Property info</span></span> | <span data-ttu-id="76111-1551">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1552">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1552">Tag</span></span>   | <span data-ttu-id="76111-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="76111-1553">0x5027</span></span>                                             |
| <span data-ttu-id="76111-1554">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1554">Type</span></span>  | <span data-ttu-id="76111-1555">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1556">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1556">Count</span></span> | <span data-ttu-id="76111-1557">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="76111-1558">пропертитагсумбнаилстрипоффсетс</span><span class="sxs-lookup"><span data-stu-id="76111-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="76111-1559">Для каждой полосы в миниатюрном изображении смещение в байтах для этой полосы.</span><span class="sxs-lookup"><span data-stu-id="76111-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="76111-1560">См. также [пропертитагсумбнаилровсперстрип](#propertytagthumbnailrowsperstrip) и [пропертитагсумбнаилстрипбитескаунт](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="76111-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="76111-1561">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1561">Property info</span></span> | <span data-ttu-id="76111-1562">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-1563">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1563">Tag</span></span>   | <span data-ttu-id="76111-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="76111-1564">0x5028</span></span>                                      |
| <span data-ttu-id="76111-1565">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1565">Type</span></span>  | <span data-ttu-id="76111-1566">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1567">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1567">Count</span></span> | <span data-ttu-id="76111-1568">Число полос</span><span class="sxs-lookup"><span data-stu-id="76111-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="76111-1569">пропертитагсумбнаилориентатион</span><span class="sxs-lookup"><span data-stu-id="76111-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="76111-1570">Ориентация изображения в виде строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="76111-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="76111-1571">См. также [пропертитагориентатион](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="76111-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="76111-1572">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1572">Property info</span></span> | <span data-ttu-id="76111-1573">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1574">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1574">Tag</span></span>   | <span data-ttu-id="76111-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="76111-1575">0x5029</span></span>               |
| <span data-ttu-id="76111-1576">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1576">Type</span></span>  | <span data-ttu-id="76111-1577">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1578">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1578">Count</span></span> | <span data-ttu-id="76111-1579">1</span><span class="sxs-lookup"><span data-stu-id="76111-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="76111-1580">пропертитагсумбнаилсамплесперпиксел</span><span class="sxs-lookup"><span data-stu-id="76111-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="76111-1581">Число цветовых компонентов на пиксель эскиза.</span><span class="sxs-lookup"><span data-stu-id="76111-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="76111-1582">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1582">Property info</span></span> | <span data-ttu-id="76111-1583">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1584">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1584">Tag</span></span>   | <span data-ttu-id="76111-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="76111-1585">0x502A</span></span>               |
| <span data-ttu-id="76111-1586">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1586">Type</span></span>  | <span data-ttu-id="76111-1587">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1588">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1588">Count</span></span> | <span data-ttu-id="76111-1589">1</span><span class="sxs-lookup"><span data-stu-id="76111-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="76111-1590">пропертитагсумбнаилровсперстрип</span><span class="sxs-lookup"><span data-stu-id="76111-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="76111-1591">Число строк на ленту в миниатюрном изображении.</span><span class="sxs-lookup"><span data-stu-id="76111-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="76111-1592">См. также [пропертитагсумбнаилстрипбитескаунт](#propertytagthumbnailstripbytescount) и [пропертитагсумбнаилстрипоффсетс](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="76111-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="76111-1593">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1593">Property info</span></span> | <span data-ttu-id="76111-1594">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-1595">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1595">Tag</span></span>   | <span data-ttu-id="76111-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="76111-1596">0x502B</span></span>                                      |
| <span data-ttu-id="76111-1597">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1597">Type</span></span>  | <span data-ttu-id="76111-1598">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1599">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1599">Count</span></span> | <span data-ttu-id="76111-1600">1</span><span class="sxs-lookup"><span data-stu-id="76111-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="76111-1601">пропертитагсумбнаилстрипбитескаунт</span><span class="sxs-lookup"><span data-stu-id="76111-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="76111-1602">Для каждой полосы эскиза изображения — общее число байтов в этой полосе.</span><span class="sxs-lookup"><span data-stu-id="76111-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="76111-1603">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1603">Property info</span></span> | <span data-ttu-id="76111-1604">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-1605">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1605">Tag</span></span>   | <span data-ttu-id="76111-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="76111-1606">0x502C</span></span>                                      |
| <span data-ttu-id="76111-1607">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1607">Type</span></span>  | <span data-ttu-id="76111-1608">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1609">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1609">Count</span></span> | <span data-ttu-id="76111-1610">Число полос в миниатюрном изображении</span><span class="sxs-lookup"><span data-stu-id="76111-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="76111-1611">пропертитагсумбнаилресолутионкс</span><span class="sxs-lookup"><span data-stu-id="76111-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="76111-1612">Разрешение эскиза в направлении ширины.</span><span class="sxs-lookup"><span data-stu-id="76111-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="76111-1613">Единица разрешения указывается в [пропертитагсумбнаилресолутионунит](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="76111-1614">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1614">Property info</span></span> | <span data-ttu-id="76111-1615">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="76111-1616">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1616">Tag</span></span> | <span data-ttu-id="76111-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="76111-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="76111-1618">пропертитагсумбнаилресолутиони</span><span class="sxs-lookup"><span data-stu-id="76111-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="76111-1619">Разрешение эскиза в направлении высоты.</span><span class="sxs-lookup"><span data-stu-id="76111-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="76111-1620">Единица разрешения указывается в [пропертитагсумбнаилресолутионунит](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="76111-1621">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1621">Property info</span></span> | <span data-ttu-id="76111-1622">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="76111-1623">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1623">Tag</span></span> | <span data-ttu-id="76111-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="76111-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="76111-1625">пропертитагсумбнаилпланарконфиг</span><span class="sxs-lookup"><span data-stu-id="76111-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="76111-1626">Записываются ли компоненты пикселей в эскизе в формате больших или плоского изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="76111-1627">См. также [пропертитагпланарконфиг](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="76111-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="76111-1628">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1628">Property info</span></span> | <span data-ttu-id="76111-1629">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1630">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1630">Tag</span></span>   | <span data-ttu-id="76111-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="76111-1631">0x502F</span></span>               |
| <span data-ttu-id="76111-1632">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1632">Type</span></span>  | <span data-ttu-id="76111-1633">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1634">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1634">Count</span></span> | <span data-ttu-id="76111-1635">1</span><span class="sxs-lookup"><span data-stu-id="76111-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="76111-1636">пропертитагсумбнаилресолутионунит</span><span class="sxs-lookup"><span data-stu-id="76111-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="76111-1637">Единица измерения для горизонтального разрешения и вертикальное разрешение эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="76111-1638">См. также [пропертитагресолутионунит](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="76111-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="76111-1639">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1639">Property info</span></span> | <span data-ttu-id="76111-1640">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1641">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1641">Tag</span></span>   | <span data-ttu-id="76111-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="76111-1642">0x5030</span></span>               |
| <span data-ttu-id="76111-1643">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1643">Type</span></span>  | <span data-ttu-id="76111-1644">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1645">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1645">Count</span></span> | <span data-ttu-id="76111-1646">1</span><span class="sxs-lookup"><span data-stu-id="76111-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="76111-1647">пропертитагсумбнаилтрансферфунктион</span><span class="sxs-lookup"><span data-stu-id="76111-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="76111-1648">Таблицы, указывающие функции перемещения для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="76111-1649">См. также [пропертитагтрансферфунктион](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="76111-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="76111-1650">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1650">Property info</span></span> | <span data-ttu-id="76111-1651">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="76111-1652">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1652">Tag</span></span>   | <span data-ttu-id="76111-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="76111-1653">0x5031</span></span>                                               |
| <span data-ttu-id="76111-1654">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1654">Type</span></span>  | <span data-ttu-id="76111-1655">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="76111-1656">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1656">Count</span></span> | <span data-ttu-id="76111-1657">Общее число 16-разрядных слов, необходимых для таблиц</span><span class="sxs-lookup"><span data-stu-id="76111-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="76111-1658">пропертитагсумбнаилсофтвареусед</span><span class="sxs-lookup"><span data-stu-id="76111-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="76111-1659">Строка символов, заканчивающаяся символом NULL, которая указывает имя и версию программного обеспечения или микропрограммы устройства, используемого для создания эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="76111-1660">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1660">Property info</span></span> | <span data-ttu-id="76111-1661">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1662">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1662">Tag</span></span>   | <span data-ttu-id="76111-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="76111-1663">0x5032</span></span>                                             |
| <span data-ttu-id="76111-1664">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1664">Type</span></span>  | <span data-ttu-id="76111-1665">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1666">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1666">Count</span></span> | <span data-ttu-id="76111-1667">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="76111-1668">пропертитагсумбнаилдатетиме</span><span class="sxs-lookup"><span data-stu-id="76111-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="76111-1669">Дата и время создания эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="76111-1670">См. также [пропертитагдатетиме](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="76111-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="76111-1671">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1671">Property info</span></span> | <span data-ttu-id="76111-1672">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1673">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1673">Tag</span></span>   | <span data-ttu-id="76111-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="76111-1674">0x5033</span></span>               |
| <span data-ttu-id="76111-1675">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1675">Type</span></span>  | <span data-ttu-id="76111-1676">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-1677">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1677">Count</span></span> | <span data-ttu-id="76111-1678">20</span><span class="sxs-lookup"><span data-stu-id="76111-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="76111-1679">пропертитагсумбнаилартист</span><span class="sxs-lookup"><span data-stu-id="76111-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="76111-1680">Строка символов, завершающаяся нулем, указывающая имя пользователя, создавшего эскиз изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="76111-1681">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1681">Property info</span></span> | <span data-ttu-id="76111-1682">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1683">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1683">Tag</span></span>   | <span data-ttu-id="76111-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="76111-1684">0x5034</span></span>                                             |
| <span data-ttu-id="76111-1685">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1685">Type</span></span>  | <span data-ttu-id="76111-1686">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1687">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1687">Count</span></span> | <span data-ttu-id="76111-1688">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="76111-1689">пропертитагсумбнаилвхитепоинт</span><span class="sxs-lookup"><span data-stu-id="76111-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="76111-1690">Цветная точка белого изображения эскиза.</span><span class="sxs-lookup"><span data-stu-id="76111-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="76111-1691">См. также [пропертитагвхитепоинт](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="76111-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="76111-1692">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1692">Property info</span></span> | <span data-ttu-id="76111-1693">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1694">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1694">Tag</span></span>   | <span data-ttu-id="76111-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="76111-1695">0x5035</span></span>                  |
| <span data-ttu-id="76111-1696">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1696">Type</span></span>  | <span data-ttu-id="76111-1697">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1698">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-1698">Count</span></span> | <span data-ttu-id="76111-1699">2</span><span class="sxs-lookup"><span data-stu-id="76111-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="76111-1700">пропертитагсумбнаилпримаричроматиЦитиес</span><span class="sxs-lookup"><span data-stu-id="76111-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="76111-1701">Для каждого из трех основных цветов в эскизе цвет изображения цвета.</span><span class="sxs-lookup"><span data-stu-id="76111-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="76111-1702">См. также [пропертитагпримаричроматиЦитиес](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="76111-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="76111-1703">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1703">Property info</span></span> | <span data-ttu-id="76111-1704">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1705">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1705">Tag</span></span>   | <span data-ttu-id="76111-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="76111-1706">0x5036</span></span>                  |
| <span data-ttu-id="76111-1707">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1707">Type</span></span>  | <span data-ttu-id="76111-1708">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1709">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1709">Count</span></span> | <span data-ttu-id="76111-1710">6</span><span class="sxs-lookup"><span data-stu-id="76111-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="76111-1711">пропертитагсумбнаиликбкркоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="76111-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="76111-1712">Коэффициенты преобразования из RGB в Икбкр данные для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="76111-1713">См. также [пропертитагикбкркоеффиЦиентс](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="76111-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="76111-1714">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1714">Property info</span></span> | <span data-ttu-id="76111-1715">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1716">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1716">Tag</span></span>   | <span data-ttu-id="76111-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="76111-1717">0x5037</span></span>                  |
| <span data-ttu-id="76111-1718">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1718">Type</span></span>  | <span data-ttu-id="76111-1719">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1720">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-1720">Count</span></span> | <span data-ttu-id="76111-1721">3</span><span class="sxs-lookup"><span data-stu-id="76111-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="76111-1722">пропертитагсумбнаиликбкрсубсамплинг</span><span class="sxs-lookup"><span data-stu-id="76111-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="76111-1723">Коэффициент выборки компонентов чроминанце относительно компонента светимости для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="76111-1724">См. также [пропертитагикбкрсубсамплинг](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="76111-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="76111-1725">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1725">Property info</span></span> | <span data-ttu-id="76111-1726">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1727">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1727">Tag</span></span>   | <span data-ttu-id="76111-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="76111-1728">0x5038</span></span>               |
| <span data-ttu-id="76111-1729">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1729">Type</span></span>  | <span data-ttu-id="76111-1730">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1731">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-1731">Count</span></span> | <span data-ttu-id="76111-1732">2</span><span class="sxs-lookup"><span data-stu-id="76111-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="76111-1733">пропертитагсумбнаиликбкрпоситионинг</span><span class="sxs-lookup"><span data-stu-id="76111-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="76111-1734">Расположение компонентов чроминанце относительно компонента освещенности для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="76111-1735">См. также [пропертитагикбкрпоситионинг](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="76111-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="76111-1736">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1736">Property info</span></span> | <span data-ttu-id="76111-1737">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1738">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1738">Tag</span></span>   | <span data-ttu-id="76111-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="76111-1739">0x5039</span></span>               |
| <span data-ttu-id="76111-1740">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1740">Type</span></span>  | <span data-ttu-id="76111-1741">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1742">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1742">Count</span></span> | <span data-ttu-id="76111-1743">1</span><span class="sxs-lookup"><span data-stu-id="76111-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="76111-1744">пропертитагсумбнаилрефблакквхите</span><span class="sxs-lookup"><span data-stu-id="76111-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="76111-1745">Ссылка на значение черной точки и ссылка на значение белой точки для эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="76111-1746">См. также [пропертитагрефблакквхите](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="76111-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="76111-1747">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1747">Property info</span></span> | <span data-ttu-id="76111-1748">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1749">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1749">Tag</span></span>   | <span data-ttu-id="76111-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="76111-1750">0x503A</span></span>                  |
| <span data-ttu-id="76111-1751">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1751">Type</span></span>  | <span data-ttu-id="76111-1752">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1753">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1753">Count</span></span> | <span data-ttu-id="76111-1754">6</span><span class="sxs-lookup"><span data-stu-id="76111-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="76111-1755">пропертитагсумбнаилкопиригхт</span><span class="sxs-lookup"><span data-stu-id="76111-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="76111-1756">Строка символов, завершающаяся символом NULL, содержащая сведения об авторских правах на эскиз изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="76111-1757">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1757">Property info</span></span> | <span data-ttu-id="76111-1758">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1759">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1759">Tag</span></span>   | <span data-ttu-id="76111-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="76111-1760">0x503B</span></span>                                             |
| <span data-ttu-id="76111-1761">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1761">Type</span></span>  | <span data-ttu-id="76111-1762">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1763">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1763">Count</span></span> | <span data-ttu-id="76111-1764">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="76111-1765">пропертитаглуминанцетабле</span><span class="sxs-lookup"><span data-stu-id="76111-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="76111-1766">Таблица освещенности.</span><span class="sxs-lookup"><span data-stu-id="76111-1766">Luminance table.</span></span> <span data-ttu-id="76111-1767">Таблица светимости и таблица чроминанце используются для управления качеством JPEG.</span><span class="sxs-lookup"><span data-stu-id="76111-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="76111-1768">Допустимая светимость или чроминанценая таблица содержит 64 записей типа Пропертитагтипешорт.</span><span class="sxs-lookup"><span data-stu-id="76111-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="76111-1769">Если в изображении есть таблица светимости или таблица чроминанце, то она должна содержать обе таблицы.</span><span class="sxs-lookup"><span data-stu-id="76111-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="76111-1770">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1770">Property info</span></span> | <span data-ttu-id="76111-1771">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1772">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1772">Tag</span></span>   | <span data-ttu-id="76111-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="76111-1773">0x5090</span></span>               |
| <span data-ttu-id="76111-1774">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1774">Type</span></span>  | <span data-ttu-id="76111-1775">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1776">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1776">Count</span></span> | <span data-ttu-id="76111-1777">64</span><span class="sxs-lookup"><span data-stu-id="76111-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="76111-1778">пропертитагчроминанцетабле</span><span class="sxs-lookup"><span data-stu-id="76111-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="76111-1779">Таблица чроминанце.</span><span class="sxs-lookup"><span data-stu-id="76111-1779">Chrominance table.</span></span> <span data-ttu-id="76111-1780">Таблица светимости и таблица чроминанце используются для управления качеством JPEG.</span><span class="sxs-lookup"><span data-stu-id="76111-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="76111-1781">Допустимая светимость или чроминанценая таблица содержит 64 записей типа Пропертитагтипешорт.</span><span class="sxs-lookup"><span data-stu-id="76111-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="76111-1782">Если в изображении есть таблица светимости или таблица чроминанце, то она должна содержать обе таблицы.</span><span class="sxs-lookup"><span data-stu-id="76111-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="76111-1783">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1783">Property info</span></span> | <span data-ttu-id="76111-1784">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1785">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1785">Tag</span></span>   | <span data-ttu-id="76111-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="76111-1786">0x5091</span></span>               |
| <span data-ttu-id="76111-1787">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1787">Type</span></span>  | <span data-ttu-id="76111-1788">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1789">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1789">Count</span></span> | <span data-ttu-id="76111-1790">64</span><span class="sxs-lookup"><span data-stu-id="76111-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="76111-1791">пропертитагфрамеделай</span><span class="sxs-lookup"><span data-stu-id="76111-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="76111-1792">Время задержки в сотых долях секунды между двумя кадрами в анимированном изображении GIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="76111-1793">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1793">Property info</span></span> | <span data-ttu-id="76111-1794">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="76111-1795">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1795">Tag</span></span>   | <span data-ttu-id="76111-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="76111-1796">0x5100</span></span>                        |
| <span data-ttu-id="76111-1797">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1797">Type</span></span>  | <span data-ttu-id="76111-1798">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="76111-1799">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1799">Count</span></span> | <span data-ttu-id="76111-1800">Число кадров в изображении</span><span class="sxs-lookup"><span data-stu-id="76111-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="76111-1801">пропертитаглупкаунт</span><span class="sxs-lookup"><span data-stu-id="76111-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="76111-1802">Для анимированного изображения GIF количество отображаемых анимаций.</span><span class="sxs-lookup"><span data-stu-id="76111-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="76111-1803">Значение 0 указывает, что анимация должна отображаться бесконечно.</span><span class="sxs-lookup"><span data-stu-id="76111-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="76111-1804">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1804">Property info</span></span> | <span data-ttu-id="76111-1805">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1806">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1806">Tag</span></span>   | <span data-ttu-id="76111-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="76111-1807">0x5101</span></span>               |
| <span data-ttu-id="76111-1808">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1808">Type</span></span>  | <span data-ttu-id="76111-1809">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1810">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1810">Count</span></span> | <span data-ttu-id="76111-1811">1</span><span class="sxs-lookup"><span data-stu-id="76111-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="76111-1812">пропертитагглобалпалетте</span><span class="sxs-lookup"><span data-stu-id="76111-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="76111-1813">Цветовая палитра для индексированного растрового изображения в изображении в формате GIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="76111-1814">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1814">Property info</span></span> | <span data-ttu-id="76111-1815">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="76111-1816">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1816">Tag</span></span>   | <span data-ttu-id="76111-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="76111-1817">0x5102</span></span>                        |
| <span data-ttu-id="76111-1818">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1818">Type</span></span>  | <span data-ttu-id="76111-1819">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="76111-1820">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1820">Count</span></span> | <span data-ttu-id="76111-1821">3 x число записей в палитре</span><span class="sxs-lookup"><span data-stu-id="76111-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="76111-1822">пропертитагиндексбаккграунд</span><span class="sxs-lookup"><span data-stu-id="76111-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="76111-1823">Индекс цвета фона в палитре изображения GIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="76111-1824">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1824">Property info</span></span> | <span data-ttu-id="76111-1825">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1826">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1826">Tag</span></span>   | <span data-ttu-id="76111-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="76111-1827">0x5103</span></span>              |
| <span data-ttu-id="76111-1828">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1828">Type</span></span>  | <span data-ttu-id="76111-1829">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-1830">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1830">Count</span></span> | <span data-ttu-id="76111-1831">1</span><span class="sxs-lookup"><span data-stu-id="76111-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="76111-1832">пропертитагиндекстранспарент</span><span class="sxs-lookup"><span data-stu-id="76111-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="76111-1833">Индекс прозрачного цвета в палитре изображения GIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="76111-1834">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1834">Property info</span></span> | <span data-ttu-id="76111-1835">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1836">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1836">Tag</span></span>   | <span data-ttu-id="76111-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="76111-1837">0x5104</span></span>              |
| <span data-ttu-id="76111-1838">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1838">Type</span></span>  | <span data-ttu-id="76111-1839">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="76111-1840">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1840">Count</span></span> | <span data-ttu-id="76111-1841">1</span><span class="sxs-lookup"><span data-stu-id="76111-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="76111-1842">пропертитагпикселунит</span><span class="sxs-lookup"><span data-stu-id="76111-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="76111-1843">Единица измерения для Пропертитагпикселперуниткс и Пропертитагпикселперунити.</span><span class="sxs-lookup"><span data-stu-id="76111-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="76111-1844">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1844">Tag</span></span>

<span data-ttu-id="76111-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="76111-1845">0x5110</span></span>

<span data-ttu-id="76111-1846">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1846">Type</span></span>

<span data-ttu-id="76111-1847">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="76111-1848">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1848">Count</span></span>

<span data-ttu-id="76111-1849">1</span><span class="sxs-lookup"><span data-stu-id="76111-1849">1</span></span>

<span data-ttu-id="76111-1850">0 — неизвестно</span><span class="sxs-lookup"><span data-stu-id="76111-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="76111-1851">пропертитагпикселперуниткс</span><span class="sxs-lookup"><span data-stu-id="76111-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="76111-1852">Пикселей на единицу в направлении x.</span><span class="sxs-lookup"><span data-stu-id="76111-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="76111-1853">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1853">Property info</span></span> | <span data-ttu-id="76111-1854">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1855">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1855">Tag</span></span>   | <span data-ttu-id="76111-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="76111-1856">0x5111</span></span>              |
| <span data-ttu-id="76111-1857">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1857">Type</span></span>  | <span data-ttu-id="76111-1858">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1859">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1859">Count</span></span> | <span data-ttu-id="76111-1860">1</span><span class="sxs-lookup"><span data-stu-id="76111-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="76111-1861">пропертитагпикселперунити</span><span class="sxs-lookup"><span data-stu-id="76111-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="76111-1862">Пикселей на единицу в направлении y.</span><span class="sxs-lookup"><span data-stu-id="76111-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="76111-1863">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1863">Property info</span></span> | <span data-ttu-id="76111-1864">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1865">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1865">Tag</span></span>   | <span data-ttu-id="76111-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="76111-1866">0x5112</span></span>              |
| <span data-ttu-id="76111-1867">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1867">Type</span></span>  | <span data-ttu-id="76111-1868">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1869">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1869">Count</span></span> | <span data-ttu-id="76111-1870">1</span><span class="sxs-lookup"><span data-stu-id="76111-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="76111-1871">пропертитагпалеттехистограм</span><span class="sxs-lookup"><span data-stu-id="76111-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="76111-1872">Гистограмма палитры.</span><span class="sxs-lookup"><span data-stu-id="76111-1872">Palette histogram.</span></span>



| <span data-ttu-id="76111-1873">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1873">Property info</span></span> | <span data-ttu-id="76111-1874">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1875">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1875">Tag</span></span>   | <span data-ttu-id="76111-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="76111-1876">0x5113</span></span>                  |
| <span data-ttu-id="76111-1877">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1877">Type</span></span>  | <span data-ttu-id="76111-1878">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="76111-1879">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1879">Count</span></span> | <span data-ttu-id="76111-1880">Длина гистограммы</span><span class="sxs-lookup"><span data-stu-id="76111-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="76111-1881">пропертитагкопиригхт</span><span class="sxs-lookup"><span data-stu-id="76111-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="76111-1882">Строка символов, завершающаяся нулем, содержащая сведения об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="76111-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="76111-1883">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1883">Property info</span></span> | <span data-ttu-id="76111-1884">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1885">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1885">Tag</span></span>   | <span data-ttu-id="76111-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="76111-1886">0x8298</span></span>                                             |
| <span data-ttu-id="76111-1887">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1887">Type</span></span>  | <span data-ttu-id="76111-1888">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1889">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1889">Count</span></span> | <span data-ttu-id="76111-1890">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="76111-1891">пропертитажексифекспосуретиме</span><span class="sxs-lookup"><span data-stu-id="76111-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="76111-1892">Время выдержки, измеряемое в секундах.</span><span class="sxs-lookup"><span data-stu-id="76111-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="76111-1893">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1893">Property info</span></span> | <span data-ttu-id="76111-1894">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-1895">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1895">Tag</span></span>   | <span data-ttu-id="76111-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="76111-1896">0x829A</span></span>                  |
| <span data-ttu-id="76111-1897">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1897">Type</span></span>  | <span data-ttu-id="76111-1898">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-1899">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1899">Count</span></span> | <span data-ttu-id="76111-1900">1</span><span class="sxs-lookup"><span data-stu-id="76111-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="76111-1901">пропертитажексиффнумбер</span><span class="sxs-lookup"><span data-stu-id="76111-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="76111-1902">Номер F.</span><span class="sxs-lookup"><span data-stu-id="76111-1902">F number.</span></span>



| <span data-ttu-id="76111-1903">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1903">Property info</span></span> | <span data-ttu-id="76111-1904">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="76111-1905">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1905">Tag</span></span>   | <span data-ttu-id="76111-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="76111-1906">0x829D</span></span>   |
| <span data-ttu-id="76111-1907">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1907">Type</span></span>  | <span data-ttu-id="76111-1908">ОСНОВНОЙ</span><span class="sxs-lookup"><span data-stu-id="76111-1908">RATIONAL</span></span> |
| <span data-ttu-id="76111-1909">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1909">Count</span></span> | <span data-ttu-id="76111-1910">1</span><span class="sxs-lookup"><span data-stu-id="76111-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="76111-1911">пропертитажексифифд</span><span class="sxs-lookup"><span data-stu-id="76111-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="76111-1912">Закрытый тег, используемый GDI+.</span><span class="sxs-lookup"><span data-stu-id="76111-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="76111-1913">Не для свободного использования.</span><span class="sxs-lookup"><span data-stu-id="76111-1913">Not for public use.</span></span> <span data-ttu-id="76111-1914">GDI+ использует этот тег для нахождение сведений, относящихся к EXIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="76111-1915">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1915">Property info</span></span> | <span data-ttu-id="76111-1916">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1917">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1917">Tag</span></span>   | <span data-ttu-id="76111-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="76111-1918">0x8769</span></span>              |
| <span data-ttu-id="76111-1919">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1919">Type</span></span>  | <span data-ttu-id="76111-1920">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1921">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1921">Count</span></span> | <span data-ttu-id="76111-1922">1</span><span class="sxs-lookup"><span data-stu-id="76111-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="76111-1923">пропертитагиккпрофиле</span><span class="sxs-lookup"><span data-stu-id="76111-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="76111-1924">Профиль ICC, внедренный в изображение.</span><span class="sxs-lookup"><span data-stu-id="76111-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="76111-1925">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1925">Property info</span></span> | <span data-ttu-id="76111-1926">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="76111-1927">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1927">Tag</span></span>   | <span data-ttu-id="76111-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="76111-1928">0x8773</span></span>                |
| <span data-ttu-id="76111-1929">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1929">Type</span></span>  | <span data-ttu-id="76111-1930">пропертитагтипебите</span><span class="sxs-lookup"><span data-stu-id="76111-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="76111-1931">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1931">Count</span></span> | <span data-ttu-id="76111-1932">Длина профиля</span><span class="sxs-lookup"><span data-stu-id="76111-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="76111-1933">пропертитажексифекспосурепрог</span><span class="sxs-lookup"><span data-stu-id="76111-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="76111-1934">Класс программы, используемой камерой для установки экспозиции при съемке.</span><span class="sxs-lookup"><span data-stu-id="76111-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="76111-1935">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1935">Tag</span></span>

<span data-ttu-id="76111-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="76111-1936">0x8822</span></span>

<span data-ttu-id="76111-1937">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1937">Type</span></span>

<span data-ttu-id="76111-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="76111-1938">SHORT</span></span>

<span data-ttu-id="76111-1939">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1939">Count</span></span>

<span data-ttu-id="76111-1940">1</span><span class="sxs-lookup"><span data-stu-id="76111-1940">1</span></span>

<span data-ttu-id="76111-1941">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-1941">Default</span></span>

<span data-ttu-id="76111-1942">0</span><span class="sxs-lookup"><span data-stu-id="76111-1942">0</span></span>

<span data-ttu-id="76111-1943">0 — не определено 1-ручное 2-обычная программа 3-, приоритет 4 — Выдержка 5-творческая программа (смещенная к глубине поля) 6-действий (смещенная в сторону быстрого скорость затвора) 7 — книжная ориентация (для закрываемых фотографий с фоновым изображением) в 8-альбомном режиме (для альбомных фотографий с фоном в фокусе) с 9 до 255 — зарезервировано</span><span class="sxs-lookup"><span data-stu-id="76111-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="76111-1944">пропертитажексифспектралсенсе</span><span class="sxs-lookup"><span data-stu-id="76111-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="76111-1945">Строка символов, завершающаяся нулем, которая указывает Спектрал чувствительность каждого канала используемой камеры.</span><span class="sxs-lookup"><span data-stu-id="76111-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="76111-1946">Строка совместима со стандартом, разработанным техническим комитетом АСТМ.</span><span class="sxs-lookup"><span data-stu-id="76111-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="76111-1947">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1947">Property info</span></span> | <span data-ttu-id="76111-1948">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-1949">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1949">Tag</span></span>   | <span data-ttu-id="76111-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="76111-1950">0x8824</span></span>                                             |
| <span data-ttu-id="76111-1951">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1951">Type</span></span>  | <span data-ttu-id="76111-1952">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-1953">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1953">Count</span></span> | <span data-ttu-id="76111-1954">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="76111-1955">пропертитаггпсифд</span><span class="sxs-lookup"><span data-stu-id="76111-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="76111-1956">Смещение к блоку элементов свойств GPS.</span><span class="sxs-lookup"><span data-stu-id="76111-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="76111-1957">Элементы свойств, теги которых имеют префикс Пропертитаггпс, хранятся в блоке GPS.</span><span class="sxs-lookup"><span data-stu-id="76111-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="76111-1958">Элементы свойств GPS определяются в спецификации EXIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="76111-1959">GDI+ использует этот тег для нахождение сведений GPS, но GDI+ не предоставляет этот тег для общего использования.</span><span class="sxs-lookup"><span data-stu-id="76111-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="76111-1960">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1960">Property info</span></span> | <span data-ttu-id="76111-1961">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-1962">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1962">Tag</span></span>   | <span data-ttu-id="76111-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="76111-1963">0x8825</span></span>              |
| <span data-ttu-id="76111-1964">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1964">Type</span></span>  | <span data-ttu-id="76111-1965">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-1966">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1966">Count</span></span> | <span data-ttu-id="76111-1967">1</span><span class="sxs-lookup"><span data-stu-id="76111-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="76111-1968">пропертитажексифисоспид</span><span class="sxs-lookup"><span data-stu-id="76111-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="76111-1969">Скорость ISO и широту ISO для камеры или устройства ввода, как указано в стандарте ISO 12232.</span><span class="sxs-lookup"><span data-stu-id="76111-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="76111-1970">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1970">Property info</span></span> | <span data-ttu-id="76111-1971">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-1972">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1972">Tag</span></span>   | <span data-ttu-id="76111-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="76111-1973">0x8827</span></span>               |
| <span data-ttu-id="76111-1974">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1974">Type</span></span>  | <span data-ttu-id="76111-1975">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-1976">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1976">Count</span></span> | <span data-ttu-id="76111-1977">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="76111-1978">пропертитажексифоекф</span><span class="sxs-lookup"><span data-stu-id="76111-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="76111-1979">Функция преобразования оптоелектроник (ОЕКФ), указанная в стандарте ISO 14524.</span><span class="sxs-lookup"><span data-stu-id="76111-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="76111-1980">ОЕКФ — это связь между оптическим входом камеры и значениями изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="76111-1981">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1981">Property info</span></span> | <span data-ttu-id="76111-1982">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-1983">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1983">Tag</span></span>   | <span data-ttu-id="76111-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="76111-1984">0x8828</span></span>                   |
| <span data-ttu-id="76111-1985">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1985">Type</span></span>  | <span data-ttu-id="76111-1986">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-1987">Count</span><span class="sxs-lookup"><span data-stu-id="76111-1987">Count</span></span> | <span data-ttu-id="76111-1988">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="76111-1989">пропертитажексифвер</span><span class="sxs-lookup"><span data-stu-id="76111-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="76111-1990">Поддерживаемая версия стандартного EXIF.</span><span class="sxs-lookup"><span data-stu-id="76111-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="76111-1991">Несуществование этого поля означает, что это значение не соответствует стандарту.</span><span class="sxs-lookup"><span data-stu-id="76111-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="76111-1992">Соответствие стандарту определяется записью 0210 в виде строки ASCII размером 4 байта.</span><span class="sxs-lookup"><span data-stu-id="76111-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="76111-1993">Поскольку тип — Пропертитагтипеундефинед, завершающий символ NULL отсутствует.</span><span class="sxs-lookup"><span data-stu-id="76111-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="76111-1994">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-1994">Property info</span></span> | <span data-ttu-id="76111-1995">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="76111-1996">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-1996">Tag</span></span>     | <span data-ttu-id="76111-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="76111-1997">0x9000</span></span>                   |
| <span data-ttu-id="76111-1998">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-1998">Type</span></span>    | <span data-ttu-id="76111-1999">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2000">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2000">Count</span></span>   | <span data-ttu-id="76111-2001">4</span><span class="sxs-lookup"><span data-stu-id="76111-2001">4</span></span>                        |
| <span data-ttu-id="76111-2002">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-2002">Default</span></span> | <span data-ttu-id="76111-2003">0210</span><span class="sxs-lookup"><span data-stu-id="76111-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="76111-2004">пропертитажексифдториг</span><span class="sxs-lookup"><span data-stu-id="76111-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="76111-2005">Дата и время создания исходных данных изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="76111-2006">Для DSC Дата и время съемки изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="76111-2007">Формат — гггг: мм: дд чч: мм: СС с временем, указанным в 24-часовом формате, и Дата и время, разделенные одним пустым символом (0x2000).</span><span class="sxs-lookup"><span data-stu-id="76111-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="76111-2008">Длина строки символов равна 20 байтам, включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="76111-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="76111-2009">Если поле пустое, оно считается неизвестным.</span><span class="sxs-lookup"><span data-stu-id="76111-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="76111-2010">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2010">Property info</span></span> | <span data-ttu-id="76111-2011">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-2012">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2012">Tag</span></span>   | <span data-ttu-id="76111-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="76111-2013">0x9003</span></span>               |
| <span data-ttu-id="76111-2014">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2014">Type</span></span>  | <span data-ttu-id="76111-2015">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-2016">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2016">Count</span></span> | <span data-ttu-id="76111-2017">20</span><span class="sxs-lookup"><span data-stu-id="76111-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="76111-2018">пропертитажексифдтдигитизед</span><span class="sxs-lookup"><span data-stu-id="76111-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="76111-2019">Дата и время хранения образа в виде цифровых данных.</span><span class="sxs-lookup"><span data-stu-id="76111-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="76111-2020">Если, например, изображение было захвачено DSC и в то же время, когда файл был записан, то Датетимеоригинал и Датетимедигитизед будут иметь одинаковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="76111-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="76111-2021">Формат — гггг: мм: дд чч: мм: СС с временем, указанным в 24-часовом формате, и Дата и время, разделенные одним пустым символом (0x2000).</span><span class="sxs-lookup"><span data-stu-id="76111-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="76111-2022">Длина строки символов равна 20 байтам, включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="76111-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="76111-2023">Если поле пустое, оно считается неизвестным.</span><span class="sxs-lookup"><span data-stu-id="76111-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="76111-2024">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2024">Property info</span></span> | <span data-ttu-id="76111-2025">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-2026">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2026">Tag</span></span>   | <span data-ttu-id="76111-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="76111-2027">0x9004</span></span>               |
| <span data-ttu-id="76111-2028">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2028">Type</span></span>  | <span data-ttu-id="76111-2029">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-2030">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2030">Count</span></span> | <span data-ttu-id="76111-2031">20</span><span class="sxs-lookup"><span data-stu-id="76111-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="76111-2032">пропертитажексифкомпконфиг</span><span class="sxs-lookup"><span data-stu-id="76111-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="76111-2033">Сведения, относящиеся к сжатым данным.</span><span class="sxs-lookup"><span data-stu-id="76111-2033">Information specific to compressed data.</span></span> <span data-ttu-id="76111-2034">Каналы каждого компонента упорядочиваются по порядку от первого компонента до четвертого.</span><span class="sxs-lookup"><span data-stu-id="76111-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="76111-2035">Для несжатых данных расположение данных указывается в теге ПропертитагфотометриЦинтерп.</span><span class="sxs-lookup"><span data-stu-id="76111-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="76111-2036">Однако, поскольку ПропертитагфотометриЦинтерп может выразить только порядок значений Y, CB и CR, этот тег предоставляется в случаях, когда в сжатых данных используются компоненты, отличные от Y, CB и CR, а также для поддержки других последовательностей.</span><span class="sxs-lookup"><span data-stu-id="76111-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="76111-2037">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2037">Tag</span></span>

<span data-ttu-id="76111-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="76111-2038">0x9101</span></span>

<span data-ttu-id="76111-2039">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2039">Type</span></span>

<span data-ttu-id="76111-2040">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="76111-2041">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2041">Count</span></span>

<span data-ttu-id="76111-2042">4</span><span class="sxs-lookup"><span data-stu-id="76111-2042">4</span></span>

<span data-ttu-id="76111-2043">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-2043">Default</span></span>

<span data-ttu-id="76111-2044">4 5 6 0 (если RGB без сжатия) 1 2 3 0 (другие случаи)</span><span class="sxs-lookup"><span data-stu-id="76111-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="76111-2045">0 — не существует 1-Y 2-CB 3-CR 4-R 5-G 6-B другой зарезервированный</span><span class="sxs-lookup"><span data-stu-id="76111-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="76111-2046">пропертитажексифкомпбпп</span><span class="sxs-lookup"><span data-stu-id="76111-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="76111-2047">Сведения, относящиеся к сжатым данным.</span><span class="sxs-lookup"><span data-stu-id="76111-2047">Information specific to compressed data.</span></span> <span data-ttu-id="76111-2048">Режим сжатия, используемый для сжатого изображения, обозначается в единицах измерения бит.</span><span class="sxs-lookup"><span data-stu-id="76111-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="76111-2049">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2049">Property info</span></span> | <span data-ttu-id="76111-2050">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2051">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2051">Tag</span></span>   | <span data-ttu-id="76111-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="76111-2052">0x9102</span></span>                  |
| <span data-ttu-id="76111-2053">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2053">Type</span></span>  | <span data-ttu-id="76111-2054">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2055">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2055">Count</span></span> | <span data-ttu-id="76111-2056">1</span><span class="sxs-lookup"><span data-stu-id="76111-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="76111-2057">пропертитажексифшуттерспид</span><span class="sxs-lookup"><span data-stu-id="76111-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="76111-2058">Скорость затвора.</span><span class="sxs-lookup"><span data-stu-id="76111-2058">Shutter speed.</span></span> <span data-ttu-id="76111-2059">Единицей является добавочная система для значения экспозиции фотографа (ВЕРШИНЕ).</span><span class="sxs-lookup"><span data-stu-id="76111-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="76111-2060">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2060">Property info</span></span> | <span data-ttu-id="76111-2061">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2062">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2062">Tag</span></span>   | <span data-ttu-id="76111-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="76111-2063">0x9201</span></span>                   |
| <span data-ttu-id="76111-2064">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2064">Type</span></span>  | <span data-ttu-id="76111-2065">пропертитагтипесратионал</span><span class="sxs-lookup"><span data-stu-id="76111-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="76111-2066">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2066">Count</span></span> | <span data-ttu-id="76111-2067">1</span><span class="sxs-lookup"><span data-stu-id="76111-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="76111-2068">пропертитажексифапертуре</span><span class="sxs-lookup"><span data-stu-id="76111-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="76111-2069">Апертура линзы.</span><span class="sxs-lookup"><span data-stu-id="76111-2069">Lens aperture.</span></span> <span data-ttu-id="76111-2070">Единицей является значение ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="76111-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="76111-2071">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2071">Property info</span></span> | <span data-ttu-id="76111-2072">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2073">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2073">Tag</span></span>   | <span data-ttu-id="76111-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="76111-2074">0x9202</span></span>                  |
| <span data-ttu-id="76111-2075">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2075">Type</span></span>  | <span data-ttu-id="76111-2076">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2077">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2077">Count</span></span> | <span data-ttu-id="76111-2078">1</span><span class="sxs-lookup"><span data-stu-id="76111-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="76111-2079">пропертитажексифбригхтнесс</span><span class="sxs-lookup"><span data-stu-id="76111-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="76111-2080">Значение яркости.</span><span class="sxs-lookup"><span data-stu-id="76111-2080">Brightness value.</span></span> <span data-ttu-id="76111-2081">Единицей является значение ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="76111-2081">The unit is the APEX value.</span></span> <span data-ttu-id="76111-2082">Обычно он указывается в диапазоне от-99,99 до 99,99.</span><span class="sxs-lookup"><span data-stu-id="76111-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="76111-2083">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2083">Property info</span></span> | <span data-ttu-id="76111-2084">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2085">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2085">Tag</span></span>   | <span data-ttu-id="76111-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="76111-2086">0x9203</span></span>                   |
| <span data-ttu-id="76111-2087">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2087">Type</span></span>  | <span data-ttu-id="76111-2088">пропертитагтипесратионал</span><span class="sxs-lookup"><span data-stu-id="76111-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="76111-2089">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2089">Count</span></span> | <span data-ttu-id="76111-2090">1</span><span class="sxs-lookup"><span data-stu-id="76111-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="76111-2091">пропертитажексифекспосуребиас</span><span class="sxs-lookup"><span data-stu-id="76111-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="76111-2092">Сдвиг экспозиции.</span><span class="sxs-lookup"><span data-stu-id="76111-2092">Exposure bias.</span></span> <span data-ttu-id="76111-2093">Единицей является значение ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="76111-2093">The unit is the APEX value.</span></span> <span data-ttu-id="76111-2094">Обычно он указывается в диапазоне от-99,99 до 99,99.</span><span class="sxs-lookup"><span data-stu-id="76111-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="76111-2095">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2095">Property info</span></span> | <span data-ttu-id="76111-2096">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2097">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2097">Tag</span></span>   | <span data-ttu-id="76111-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="76111-2098">0x9204</span></span>                   |
| <span data-ttu-id="76111-2099">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2099">Type</span></span>  | <span data-ttu-id="76111-2100">пропертитагтипесратионал</span><span class="sxs-lookup"><span data-stu-id="76111-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="76111-2101">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2101">Count</span></span> | <span data-ttu-id="76111-2102">1</span><span class="sxs-lookup"><span data-stu-id="76111-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="76111-2103">пропертитажексифмаксапертуре</span><span class="sxs-lookup"><span data-stu-id="76111-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="76111-2104">Наименьший F номер линзы.</span><span class="sxs-lookup"><span data-stu-id="76111-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="76111-2105">Единицей является значение ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="76111-2105">The unit is the APEX value.</span></span> <span data-ttu-id="76111-2106">Обычно это значение указывается в диапазоне от 00,00 до 99,99, но не ограничивается этим диапазоном.</span><span class="sxs-lookup"><span data-stu-id="76111-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="76111-2107">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2107">Property info</span></span> | <span data-ttu-id="76111-2108">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2109">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2109">Tag</span></span>   | <span data-ttu-id="76111-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="76111-2110">0x9205</span></span>                  |
| <span data-ttu-id="76111-2111">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2111">Type</span></span>  | <span data-ttu-id="76111-2112">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2113">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2113">Count</span></span> | <span data-ttu-id="76111-2114">1</span><span class="sxs-lookup"><span data-stu-id="76111-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="76111-2115">пропертитажексифсубжектдист</span><span class="sxs-lookup"><span data-stu-id="76111-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="76111-2116">Расстояние до субъекта, измеряемое в метрах.</span><span class="sxs-lookup"><span data-stu-id="76111-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="76111-2117">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2117">Property info</span></span> | <span data-ttu-id="76111-2118">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2119">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2119">Tag</span></span>   | <span data-ttu-id="76111-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="76111-2120">0x9206</span></span>                  |
| <span data-ttu-id="76111-2121">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2121">Type</span></span>  | <span data-ttu-id="76111-2122">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2123">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2123">Count</span></span> | <span data-ttu-id="76111-2124">1</span><span class="sxs-lookup"><span data-stu-id="76111-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="76111-2125">пропертитажексифметерингмоде</span><span class="sxs-lookup"><span data-stu-id="76111-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="76111-2126">Режим измерения.</span><span class="sxs-lookup"><span data-stu-id="76111-2126">Metering mode.</span></span>



<span data-ttu-id="76111-2127">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2127">Tag</span></span>

<span data-ttu-id="76111-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="76111-2128">0x9207</span></span>

<span data-ttu-id="76111-2129">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2129">Type</span></span>

<span data-ttu-id="76111-2130">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2131">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2131">Count</span></span>

<span data-ttu-id="76111-2132">1</span><span class="sxs-lookup"><span data-stu-id="76111-2132">1</span></span>

<span data-ttu-id="76111-2133">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-2133">Default</span></span>

<span data-ttu-id="76111-2134">0</span><span class="sxs-lookup"><span data-stu-id="76111-2134">0</span></span>

<span data-ttu-id="76111-2135">0-неизвестное 1-среднее 2-Центервеигхтедавераже 3-точечный 4-многоточечный 5-шаблон 6-частичный 7 – 254-зарезервированный 255 — другой</span><span class="sxs-lookup"><span data-stu-id="76111-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="76111-2136">пропертитажексифлигхтсаурце</span><span class="sxs-lookup"><span data-stu-id="76111-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="76111-2137">Тип источника освещения.</span><span class="sxs-lookup"><span data-stu-id="76111-2137">Type of light source.</span></span>



<span data-ttu-id="76111-2138">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2138">Tag</span></span>

<span data-ttu-id="76111-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="76111-2139">0x9208</span></span>

<span data-ttu-id="76111-2140">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2140">Type</span></span>

<span data-ttu-id="76111-2141">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2142">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2142">Count</span></span>

<span data-ttu-id="76111-2143">1</span><span class="sxs-lookup"><span data-stu-id="76111-2143">1</span></span>

<span data-ttu-id="76111-2144">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-2144">Default</span></span>

<span data-ttu-id="76111-2145">0</span><span class="sxs-lookup"><span data-stu-id="76111-2145">0</span></span>

<span data-ttu-id="76111-2146">0 — неизвестная 1-летная 2-флуоресцентные 3-Тунгстен 17-Standard Light A 18-Standard светло B 19-Standard Light C 20-D55 21-D65 22-D75 23 – 254-reserved 255 — other</span><span class="sxs-lookup"><span data-stu-id="76111-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="76111-2147">пропертитажексиффлаш</span><span class="sxs-lookup"><span data-stu-id="76111-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="76111-2148">Состояние флэш-памяти.</span><span class="sxs-lookup"><span data-stu-id="76111-2148">Flash status.</span></span> <span data-ttu-id="76111-2149">Этот тег записывается, когда изображение берется с помощью света (Flash).</span><span class="sxs-lookup"><span data-stu-id="76111-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="76111-2150">Бит 0 указывает состояние обработки флэш-памяти, а биты 1 и 2 указывают состояние возврата Flash.</span><span class="sxs-lookup"><span data-stu-id="76111-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="76111-2151">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2151">Tag</span></span>

<span data-ttu-id="76111-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="76111-2152">0x9209</span></span>

<span data-ttu-id="76111-2153">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2153">Type</span></span>

<span data-ttu-id="76111-2154">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2155">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2155">Count</span></span>

<span data-ttu-id="76111-2156">1</span><span class="sxs-lookup"><span data-stu-id="76111-2156">1</span></span>

<span data-ttu-id="76111-2157">Значения для бита 0, указывающие, активировалась ли вспышка: 0b-Flash не активировал 1B-Flash.</span><span class="sxs-lookup"><span data-stu-id="76111-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="76111-2158">Значения бит 1 и 2, указывающие состояние возвращенного света: 00b-No функция обнаружения возврата с помощью отраженного света 01b — зарезервированный 10b — индикатор возврата с помощью отраженного света не обнаружен 11b — обнаружен индикатор возврата с освещением</span><span class="sxs-lookup"><span data-stu-id="76111-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="76111-2159">Итоговые значения тега Flash: Символ 0x0000-Flash не активировал 0x0001-Flash, запущенный 0x0005-вспышка с освещением не обнаружено</span><span class="sxs-lookup"><span data-stu-id="76111-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="76111-2160">пропертитажексиффокалленгс</span><span class="sxs-lookup"><span data-stu-id="76111-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="76111-2161">Фактическая Длина фокуса (в миллиметрах) линзы.</span><span class="sxs-lookup"><span data-stu-id="76111-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="76111-2162">Преобразование не выполняется для фокусной длины камеры 35 миллиметра.</span><span class="sxs-lookup"><span data-stu-id="76111-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="76111-2163">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2163">Property info</span></span> | <span data-ttu-id="76111-2164">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2165">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2165">Tag</span></span>   | <span data-ttu-id="76111-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="76111-2166">0x920A</span></span>                  |
| <span data-ttu-id="76111-2167">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2167">Type</span></span>  | <span data-ttu-id="76111-2168">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2169">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2169">Count</span></span> | <span data-ttu-id="76111-2170">1</span><span class="sxs-lookup"><span data-stu-id="76111-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="76111-2171">пропертитажексифмакерноте</span><span class="sxs-lookup"><span data-stu-id="76111-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="76111-2172">Тег примечания.</span><span class="sxs-lookup"><span data-stu-id="76111-2172">Note tag.</span></span> <span data-ttu-id="76111-2173">Тег, используемый производителями составителей EXIF для записи информации.</span><span class="sxs-lookup"><span data-stu-id="76111-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="76111-2174">Содержимое имеет изготовитель.</span><span class="sxs-lookup"><span data-stu-id="76111-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="76111-2175">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2175">Property info</span></span> | <span data-ttu-id="76111-2176">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2177">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2177">Tag</span></span>   | <span data-ttu-id="76111-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="76111-2178">0x927C</span></span>                   |
| <span data-ttu-id="76111-2179">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2179">Type</span></span>  | <span data-ttu-id="76111-2180">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2181">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2181">Count</span></span> | <span data-ttu-id="76111-2182">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="76111-2183">пропертитажексифусеркоммент</span><span class="sxs-lookup"><span data-stu-id="76111-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="76111-2184">Тег комментария.</span><span class="sxs-lookup"><span data-stu-id="76111-2184">Comment tag.</span></span> <span data-ttu-id="76111-2185">Тег, используемый пользователями EXIF для написания ключевых слов или комментариев к изображению, помимо тех, которые находятся в Пропертитагимажедескриптион и без ограничений на символы кода тега Пропертитагимажедескриптион.</span><span class="sxs-lookup"><span data-stu-id="76111-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="76111-2186">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2186">Property info</span></span> | <span data-ttu-id="76111-2187">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2188">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2188">Tag</span></span>   | <span data-ttu-id="76111-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="76111-2189">0x9286</span></span>                   |
| <span data-ttu-id="76111-2190">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2190">Type</span></span>  | <span data-ttu-id="76111-2191">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2192">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2192">Count</span></span> | <span data-ttu-id="76111-2193">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-2193">Any</span></span>                      |



 

<span data-ttu-id="76111-2194">Код символа, используемый в теге Пропертитажексифусеркоммент, определяется на основе кода идентификатора в фиксированной 8-байтовой области в начале области данных тега.</span><span class="sxs-lookup"><span data-stu-id="76111-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="76111-2195">Неиспользуемая часть области дополнена символами NULL (0).</span><span class="sxs-lookup"><span data-stu-id="76111-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="76111-2196">Коды ИДЕНТИФИКАТОРов назначаются средствами регистрации.</span><span class="sxs-lookup"><span data-stu-id="76111-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="76111-2197">Поскольку тип не является ASCII, нет необходимости использовать завершающий символ NULL.</span><span class="sxs-lookup"><span data-stu-id="76111-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="76111-2198">пропертитажексифдтсубсек</span><span class="sxs-lookup"><span data-stu-id="76111-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="76111-2199">Строка символов, завершающаяся нулем, которая указывает долю секунды для тега Пропертитагдатетиме.</span><span class="sxs-lookup"><span data-stu-id="76111-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="76111-2200">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2200">Property info</span></span> | <span data-ttu-id="76111-2201">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="76111-2202">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2202">Tag</span></span>   | <span data-ttu-id="76111-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="76111-2203">0x9290</span></span>                                             |
| <span data-ttu-id="76111-2204">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2204">Type</span></span>  | <span data-ttu-id="76111-2205">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-2206">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2206">Count</span></span> | <span data-ttu-id="76111-2207">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="76111-2208">пропертитажексифдторигсс</span><span class="sxs-lookup"><span data-stu-id="76111-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="76111-2209">Строка символов, завершающаяся нулем, которая указывает долю секунды для тега Пропертитажексифдториг.</span><span class="sxs-lookup"><span data-stu-id="76111-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="76111-2210">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2210">Property info</span></span> | <span data-ttu-id="76111-2211">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="76111-2212">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2212">Tag</span></span>  | <span data-ttu-id="76111-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="76111-2213">0x9291</span></span>                                             |
| <span data-ttu-id="76111-2214">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2214">Type</span></span> | <span data-ttu-id="76111-2215">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="76111-2216">Нет</span><span class="sxs-lookup"><span data-stu-id="76111-2216">N</span></span>    | <span data-ttu-id="76111-2217">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="76111-2218">пропертитажексифдтдигсс</span><span class="sxs-lookup"><span data-stu-id="76111-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="76111-2219">Строка символов, завершающаяся нулем, которая указывает долю секунды для тега Пропертитажексифдтдигитизед.</span><span class="sxs-lookup"><span data-stu-id="76111-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="76111-2220">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2220">Property info</span></span> | <span data-ttu-id="76111-2221">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="76111-2222">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2222">Tag</span></span>  | <span data-ttu-id="76111-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="76111-2223">0x9292</span></span>                                             |
| <span data-ttu-id="76111-2224">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2224">Type</span></span> | <span data-ttu-id="76111-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="76111-2225">ASCII</span></span>                                              |
| <span data-ttu-id="76111-2226">Нет</span><span class="sxs-lookup"><span data-stu-id="76111-2226">N</span></span>    | <span data-ttu-id="76111-2227">Длина строки, включая знак завершения NULL</span><span class="sxs-lookup"><span data-stu-id="76111-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="76111-2228">пропертитажексиффпксвер</span><span class="sxs-lookup"><span data-stu-id="76111-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="76111-2229">Версия формата Флашпикс, поддерживаемая файлом ФПКСР.</span><span class="sxs-lookup"><span data-stu-id="76111-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="76111-2230">Если функция ФПКСР поддерживает формат Флашпикс версии 1,0, это указывается аналогично Пропертитажексифвер путем записи 0100 в виде 4-байтовой строки ASCII.</span><span class="sxs-lookup"><span data-stu-id="76111-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="76111-2231">Поскольку тип — Пропертитагтипеундефинед, завершающий символ NULL отсутствует.</span><span class="sxs-lookup"><span data-stu-id="76111-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="76111-2232">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2232">Tag</span></span>

<span data-ttu-id="76111-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="76111-2233">0xA000</span></span>

<span data-ttu-id="76111-2234">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2234">Type</span></span>

<span data-ttu-id="76111-2235">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="76111-2236">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2236">Count</span></span>

<span data-ttu-id="76111-2237">4</span><span class="sxs-lookup"><span data-stu-id="76111-2237">4</span></span>

<span data-ttu-id="76111-2238">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="76111-2238">Default</span></span>

<span data-ttu-id="76111-2239">0100</span><span class="sxs-lookup"><span data-stu-id="76111-2239">0100</span></span>

<span data-ttu-id="76111-2240">0100-Флашпикс формат версии 1,0, другой-зарезервированный</span><span class="sxs-lookup"><span data-stu-id="76111-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="76111-2241">пропертитажексифколорспаце</span><span class="sxs-lookup"><span data-stu-id="76111-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="76111-2242">Описатель цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="76111-2242">Color space specifier.</span></span> <span data-ttu-id="76111-2243">Обычно sRGB (= 1) используется для определения цветового пространства на основе условий и среды монитора ПК.</span><span class="sxs-lookup"><span data-stu-id="76111-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="76111-2244">При использовании цветового пространства, отличного от sRGB, задается некалиброванная (= 0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="76111-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="76111-2245">Данные изображения, записанные как некалиброванные, можно рассматривать как sRGB при преобразовании в Флашпикс.</span><span class="sxs-lookup"><span data-stu-id="76111-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="76111-2246">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2246">Tag</span></span>

<span data-ttu-id="76111-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="76111-2247">0xA001</span></span>

<span data-ttu-id="76111-2248">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2248">Type</span></span>

<span data-ttu-id="76111-2249">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2250">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2250">Count</span></span>

<span data-ttu-id="76111-2251">1</span><span class="sxs-lookup"><span data-stu-id="76111-2251">1</span></span>

<span data-ttu-id="76111-2252">0x1 — sRGB 0xFFFF — некалибровка другой — зарезервированный</span><span class="sxs-lookup"><span data-stu-id="76111-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="76111-2253">пропертитажексифпиксксдим</span><span class="sxs-lookup"><span data-stu-id="76111-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="76111-2254">Сведения, относящиеся к сжатым данным.</span><span class="sxs-lookup"><span data-stu-id="76111-2254">Information specific to compressed data.</span></span> <span data-ttu-id="76111-2255">При записи сжатого файла допустимая ширина осмысленного изображения должна быть записана в этот тег, независимо от того, есть ли заполненные данные или маркер перезапуска.</span><span class="sxs-lookup"><span data-stu-id="76111-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="76111-2256">Этот тег не должен существовать в несжатом файле.</span><span class="sxs-lookup"><span data-stu-id="76111-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="76111-2257">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2257">Property info</span></span> | <span data-ttu-id="76111-2258">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-2259">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2259">Tag</span></span>   | <span data-ttu-id="76111-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="76111-2260">0xA002</span></span>                                      |
| <span data-ttu-id="76111-2261">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2261">Type</span></span>  | <span data-ttu-id="76111-2262">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-2263">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2263">Count</span></span> | <span data-ttu-id="76111-2264">1</span><span class="sxs-lookup"><span data-stu-id="76111-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="76111-2265">пропертитажексифпиксидим</span><span class="sxs-lookup"><span data-stu-id="76111-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="76111-2266">Сведения, относящиеся к сжатым данным.</span><span class="sxs-lookup"><span data-stu-id="76111-2266">Information specific to compressed data.</span></span> <span data-ttu-id="76111-2267">При записи сжатого файла допустимая высота осмысленного изображения должна быть записана в этом теге независимо от того, имеются ли заполненные данные или маркер перезапуска.</span><span class="sxs-lookup"><span data-stu-id="76111-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="76111-2268">Этот тег не должен существовать в несжатом файле.</span><span class="sxs-lookup"><span data-stu-id="76111-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="76111-2269">Поскольку заполнение данных не требуется в вертикальном направлении, число строк, записанных в этом теге допустимой высоты, будет таким же, как и записано в S из.</span><span class="sxs-lookup"><span data-stu-id="76111-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="76111-2270">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2270">Property info</span></span> | <span data-ttu-id="76111-2271">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="76111-2272">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2272">Tag</span></span>   | <span data-ttu-id="76111-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="76111-2273">0xA003</span></span>                                      |
| <span data-ttu-id="76111-2274">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2274">Type</span></span>  | <span data-ttu-id="76111-2275">Пропертитагтипешорт или Пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-2276">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2276">Count</span></span> | <span data-ttu-id="76111-2277">1</span><span class="sxs-lookup"><span data-stu-id="76111-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="76111-2278">пропертитажексифрелатедвав</span><span class="sxs-lookup"><span data-stu-id="76111-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="76111-2279">Имя звукового файла, связанного с данными изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="76111-2280">Единственная зарегистрированная реляционная информация — это имя и расширение файла EXIF (строка ASCII, состоящая из 8 символов плюс точка (.) и 3 символа).</span><span class="sxs-lookup"><span data-stu-id="76111-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="76111-2281">Путь не записан.</span><span class="sxs-lookup"><span data-stu-id="76111-2281">The path is not recorded.</span></span> <span data-ttu-id="76111-2282">При использовании этого тега звуковые файлы должны быть записаны в соответствие с аудио форматом EXIF.</span><span class="sxs-lookup"><span data-stu-id="76111-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="76111-2283">Кроме того, модули записи могут хранить аудиоданные в Флашпикс в виде потоковых данных расширения.</span><span class="sxs-lookup"><span data-stu-id="76111-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="76111-2284">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2284">Property info</span></span> | <span data-ttu-id="76111-2285">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-2286">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2286">Tag</span></span>   | <span data-ttu-id="76111-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="76111-2287">0xA004</span></span>               |
| <span data-ttu-id="76111-2288">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2288">Type</span></span>  | <span data-ttu-id="76111-2289">пропертитагтипеасЦии</span><span class="sxs-lookup"><span data-stu-id="76111-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="76111-2290">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2290">Count</span></span> | <span data-ttu-id="76111-2291">13</span><span class="sxs-lookup"><span data-stu-id="76111-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="76111-2292">пропертитажексифинтероп</span><span class="sxs-lookup"><span data-stu-id="76111-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="76111-2293">Смещение к блоку элементов свойств, содержащих сведения о взаимодействии.</span><span class="sxs-lookup"><span data-stu-id="76111-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="76111-2294">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2294">Property info</span></span> | <span data-ttu-id="76111-2295">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="76111-2296">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2296">Tag</span></span>   | <span data-ttu-id="76111-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="76111-2297">0xA005</span></span>              |
| <span data-ttu-id="76111-2298">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2298">Type</span></span>  | <span data-ttu-id="76111-2299">пропертитагтипелонг</span><span class="sxs-lookup"><span data-stu-id="76111-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="76111-2300">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2300">Count</span></span> | <span data-ttu-id="76111-2301">1</span><span class="sxs-lookup"><span data-stu-id="76111-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="76111-2302">пропертитажексиффлашенерги</span><span class="sxs-lookup"><span data-stu-id="76111-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="76111-2303">Энергия с предвспышкой, в образе свечи (БКПС), на момент захвата образа.</span><span class="sxs-lookup"><span data-stu-id="76111-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="76111-2304">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2304">Property info</span></span> | <span data-ttu-id="76111-2305">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2306">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2306">Tag</span></span>   | <span data-ttu-id="76111-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="76111-2307">0xA20B</span></span>                  |
| <span data-ttu-id="76111-2308">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2308">Type</span></span>  | <span data-ttu-id="76111-2309">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2310">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2310">Count</span></span> | <span data-ttu-id="76111-2311">1</span><span class="sxs-lookup"><span data-stu-id="76111-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="76111-2312">пропертитажексифспатиалфр</span><span class="sxs-lookup"><span data-stu-id="76111-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="76111-2313">Таблица с пространственными частотой камеры или устройства ввода и SFR значения в ширину изображения, высоту изображения и диагональное направление, как указано в стандарте ISO 12233.</span><span class="sxs-lookup"><span data-stu-id="76111-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="76111-2314">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2314">Property info</span></span> | <span data-ttu-id="76111-2315">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2316">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2316">Tag</span></span>   | <span data-ttu-id="76111-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="76111-2317">0xA20C</span></span>                   |
| <span data-ttu-id="76111-2318">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2318">Type</span></span>  | <span data-ttu-id="76111-2319">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2320">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2320">Count</span></span> | <span data-ttu-id="76111-2321">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="76111-2322">пропертитажексиффокалксрес</span><span class="sxs-lookup"><span data-stu-id="76111-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="76111-2323">Количество пикселов в ширине изображения (x) на единицу в фокальной плоскости камеры.</span><span class="sxs-lookup"><span data-stu-id="76111-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="76111-2324">Единица указывается в Пропертитажексиффокалресунит.</span><span class="sxs-lookup"><span data-stu-id="76111-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="76111-2325">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2325">Property info</span></span> | <span data-ttu-id="76111-2326">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2327">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2327">Tag</span></span>   | <span data-ttu-id="76111-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="76111-2328">0xA20E</span></span>                  |
| <span data-ttu-id="76111-2329">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2329">Type</span></span>  | <span data-ttu-id="76111-2330">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2331">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2331">Count</span></span> | <span data-ttu-id="76111-2332">1</span><span class="sxs-lookup"><span data-stu-id="76111-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="76111-2333">пропертитажексиффокалирес</span><span class="sxs-lookup"><span data-stu-id="76111-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="76111-2334">Число пикселей в значении высоты (y) на единицу в плоскости, направляющей камеру.</span><span class="sxs-lookup"><span data-stu-id="76111-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="76111-2335">Единица указывается в Пропертитажексиффокалресунит.</span><span class="sxs-lookup"><span data-stu-id="76111-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="76111-2336">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2336">Property info</span></span> | <span data-ttu-id="76111-2337">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2338">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2338">Tag</span></span>   | <span data-ttu-id="76111-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="76111-2339">0xA20F</span></span>                  |
| <span data-ttu-id="76111-2340">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2340">Type</span></span>  | <span data-ttu-id="76111-2341">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2342">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2342">Count</span></span> | <span data-ttu-id="76111-2343">1</span><span class="sxs-lookup"><span data-stu-id="76111-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="76111-2344">пропертитажексиффокалресунит</span><span class="sxs-lookup"><span data-stu-id="76111-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="76111-2345">Единица измерения для Пропертитажексиффокалксрес и Пропертитажексиффокалирес.</span><span class="sxs-lookup"><span data-stu-id="76111-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="76111-2346">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2346">Tag</span></span>

<span data-ttu-id="76111-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="76111-2347">0xA210</span></span>

<span data-ttu-id="76111-2348">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2348">Type</span></span>

<span data-ttu-id="76111-2349">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2350">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2350">Count</span></span>

<span data-ttu-id="76111-2351">1</span><span class="sxs-lookup"><span data-stu-id="76111-2351">1</span></span>

<span data-ttu-id="76111-2352">2-дюймовый 3-сантиметр</span><span class="sxs-lookup"><span data-stu-id="76111-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="76111-2353">пропертитажексифсубжектлок</span><span class="sxs-lookup"><span data-stu-id="76111-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="76111-2354">Расположение основной темы в сцене.</span><span class="sxs-lookup"><span data-stu-id="76111-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="76111-2355">Значение этого тега представляет точку в центре основной темы относительно левого края.</span><span class="sxs-lookup"><span data-stu-id="76111-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="76111-2356">Первое значение указывает номер столбца, а второе значение — номер строки.</span><span class="sxs-lookup"><span data-stu-id="76111-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="76111-2357">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2357">Property info</span></span> | <span data-ttu-id="76111-2358">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="76111-2359">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2359">Tag</span></span>   | <span data-ttu-id="76111-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="76111-2360">0xA214</span></span>               |
| <span data-ttu-id="76111-2361">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2361">Type</span></span>  | <span data-ttu-id="76111-2362">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="76111-2363">Счетчик</span><span class="sxs-lookup"><span data-stu-id="76111-2363">Count</span></span> | <span data-ttu-id="76111-2364">2</span><span class="sxs-lookup"><span data-stu-id="76111-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="76111-2365">пропертитажексифекспосуреиндекс</span><span class="sxs-lookup"><span data-stu-id="76111-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="76111-2366">Индекс экспозиции, выбранный на камере или устройстве ввода на момент записи образа.</span><span class="sxs-lookup"><span data-stu-id="76111-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="76111-2367">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2367">Property info</span></span> | <span data-ttu-id="76111-2368">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="76111-2369">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2369">Tag</span></span>   | <span data-ttu-id="76111-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="76111-2370">0xA215</span></span>                  |
| <span data-ttu-id="76111-2371">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2371">Type</span></span>  | <span data-ttu-id="76111-2372">пропертитагтиператионал</span><span class="sxs-lookup"><span data-stu-id="76111-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="76111-2373">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2373">Count</span></span> | <span data-ttu-id="76111-2374">1</span><span class="sxs-lookup"><span data-stu-id="76111-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="76111-2375">пропертитажексифсенсингмесод</span><span class="sxs-lookup"><span data-stu-id="76111-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="76111-2376">Тип датчика изображения на камере или устройстве ввода.</span><span class="sxs-lookup"><span data-stu-id="76111-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="76111-2377">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2377">Tag</span></span>

<span data-ttu-id="76111-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="76111-2378">0xA217</span></span>

<span data-ttu-id="76111-2379">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2379">Type</span></span>

<span data-ttu-id="76111-2380">пропертитагтипешорт</span><span class="sxs-lookup"><span data-stu-id="76111-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="76111-2381">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2381">Count</span></span>

<span data-ttu-id="76111-2382">1</span><span class="sxs-lookup"><span data-stu-id="76111-2382">1</span></span>

<span data-ttu-id="76111-2383">1 — не определен 2-один микрофактор цветовой области 3 — Датчик цветовой области с двумя микросхемами 4 — датчик цветовой области с тремя микроцветами 5 — датчик трилинейной 8 — цвет последовательного линейного датчика с другим зарезервированным</span><span class="sxs-lookup"><span data-stu-id="76111-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="76111-2384">пропертитажексиффилесаурце</span><span class="sxs-lookup"><span data-stu-id="76111-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="76111-2385">Источник изображения.</span><span class="sxs-lookup"><span data-stu-id="76111-2385">The image source.</span></span> <span data-ttu-id="76111-2386">Если в DSC записано изображение, значение этого тега равно 3.</span><span class="sxs-lookup"><span data-stu-id="76111-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="76111-2387">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2387">Property info</span></span> | <span data-ttu-id="76111-2388">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2389">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2389">Tag</span></span>   | <span data-ttu-id="76111-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="76111-2390">0xA300</span></span>                   |
| <span data-ttu-id="76111-2391">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2391">Type</span></span>  | <span data-ttu-id="76111-2392">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2393">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2393">Count</span></span> | <span data-ttu-id="76111-2394">1</span><span class="sxs-lookup"><span data-stu-id="76111-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="76111-2395">пропертитажексифсценетипе</span><span class="sxs-lookup"><span data-stu-id="76111-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="76111-2396">Тип сцены.</span><span class="sxs-lookup"><span data-stu-id="76111-2396">The type of scene.</span></span> <span data-ttu-id="76111-2397">Если в DSC записано изображение, значение этого тега должно быть равно 1, что указывает на то, что изображение было непосредственно расграфическим графиком.</span><span class="sxs-lookup"><span data-stu-id="76111-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="76111-2398">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2398">Property info</span></span> | <span data-ttu-id="76111-2399">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2400">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2400">Tag</span></span>   | <span data-ttu-id="76111-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="76111-2401">0xA301</span></span>                   |
| <span data-ttu-id="76111-2402">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2402">Type</span></span>  | <span data-ttu-id="76111-2403">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2404">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2404">Count</span></span> | <span data-ttu-id="76111-2405">1</span><span class="sxs-lookup"><span data-stu-id="76111-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="76111-2406">пропертитажексифкфапаттерн</span><span class="sxs-lookup"><span data-stu-id="76111-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="76111-2407">Геометрический шаблон массива цветовых фильтров (КФА) датчика изображения при использовании датчика цветовой области с одним набором микросхем.</span><span class="sxs-lookup"><span data-stu-id="76111-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="76111-2408">Он не применяется ко всем методам с поддатчикими.</span><span class="sxs-lookup"><span data-stu-id="76111-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="76111-2409">Сведения о свойстве</span><span class="sxs-lookup"><span data-stu-id="76111-2409">Property info</span></span> | <span data-ttu-id="76111-2410">Значение</span><span class="sxs-lookup"><span data-stu-id="76111-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="76111-2411">Тег</span><span class="sxs-lookup"><span data-stu-id="76111-2411">Tag</span></span>   | <span data-ttu-id="76111-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="76111-2412">0xA302</span></span>                   |
| <span data-ttu-id="76111-2413">Тип</span><span class="sxs-lookup"><span data-stu-id="76111-2413">Type</span></span>  | <span data-ttu-id="76111-2414">пропертитагтипеундефинед</span><span class="sxs-lookup"><span data-stu-id="76111-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="76111-2415">Count</span><span class="sxs-lookup"><span data-stu-id="76111-2415">Count</span></span> | <span data-ttu-id="76111-2416">Любой</span><span class="sxs-lookup"><span data-stu-id="76111-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="76111-2417">См. также</span><span class="sxs-lookup"><span data-stu-id="76111-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76111-2418">Спецификации форматов файлов изображений</span><span class="sxs-lookup"><span data-stu-id="76111-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="76111-2419">Константы тега свойства Image</span><span class="sxs-lookup"><span data-stu-id="76111-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="76111-2420">**Константы типа тега свойства Image**</span><span class="sxs-lookup"><span data-stu-id="76111-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="76111-2421">Теги свойств в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="76111-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="76111-2422">Теги свойств в числовом порядке</span><span class="sxs-lookup"><span data-stu-id="76111-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="76111-2423">Чтение и запись метаданных</span><span class="sxs-lookup"><span data-stu-id="76111-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



