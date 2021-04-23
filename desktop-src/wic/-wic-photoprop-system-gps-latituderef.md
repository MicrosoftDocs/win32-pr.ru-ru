---
description: Политика метаданных фотографии для свойства System. GPS. Латитудереф.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Политика метаданных фотографии System. GPS. Латитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265997"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="39f7a-103">Политика метаданных фотографии System. GPS. Латитудереф</span><span class="sxs-lookup"><span data-stu-id="39f7a-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="39f7a-104">Политика метаданных фотографии для свойства [System. GPS. латитудереф](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="39f7a-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="39f7a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="39f7a-105">PKEY</span></span>

<span data-ttu-id="39f7a-106">PKEY \_ GPS \_ латитудереф</span><span class="sxs-lookup"><span data-stu-id="39f7a-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="39f7a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="39f7a-107">Containers</span></span>

<span data-ttu-id="39f7a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="39f7a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="39f7a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="39f7a-109">Read-Only</span></span>

<span data-ttu-id="39f7a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="39f7a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="39f7a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="39f7a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="39f7a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="39f7a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="39f7a-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="39f7a-113">Input Type</span></span>

<span data-ttu-id="39f7a-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="39f7a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="39f7a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="39f7a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="39f7a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="39f7a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="39f7a-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="39f7a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="39f7a-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="39f7a-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="39f7a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="39f7a-119">Order</span></span> | <span data-ttu-id="39f7a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="39f7a-120">Path</span></span>                         | <span data-ttu-id="39f7a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="39f7a-121">Disk Format</span></span> | <span data-ttu-id="39f7a-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="39f7a-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="39f7a-123">1</span><span class="sxs-lookup"><span data-stu-id="39f7a-123">1</span></span>     | <span data-ttu-id="39f7a-124">/КСМП/ексиф: Гпслатитудереф</span><span class="sxs-lookup"><span data-stu-id="39f7a-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="39f7a-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="39f7a-125">Unicode</span></span>     | <span data-ttu-id="39f7a-126">Да</span><span class="sxs-lookup"><span data-stu-id="39f7a-126">Yes</span></span>      |
| <span data-ttu-id="39f7a-127">2</span><span class="sxs-lookup"><span data-stu-id="39f7a-127">2</span></span>     | <span data-ttu-id="39f7a-128">/APP1/IFD/GPS/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="39f7a-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="39f7a-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="39f7a-129">ASCII</span></span>       | <span data-ttu-id="39f7a-130">Нет</span><span class="sxs-lookup"><span data-stu-id="39f7a-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="39f7a-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="39f7a-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="39f7a-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="39f7a-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="39f7a-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="39f7a-133">Order</span></span> | <span data-ttu-id="39f7a-134">Путь</span><span class="sxs-lookup"><span data-stu-id="39f7a-134">Path</span></span>                         | <span data-ttu-id="39f7a-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="39f7a-135">Disk Format</span></span> | <span data-ttu-id="39f7a-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="39f7a-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="39f7a-137">1</span><span class="sxs-lookup"><span data-stu-id="39f7a-137">1</span></span>     | <span data-ttu-id="39f7a-138">/ИФД/КСМП/ексиф: Гпслатитудереф</span><span class="sxs-lookup"><span data-stu-id="39f7a-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="39f7a-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="39f7a-139">Unicode</span></span>     | <span data-ttu-id="39f7a-140">Да</span><span class="sxs-lookup"><span data-stu-id="39f7a-140">Yes</span></span>      |
| <span data-ttu-id="39f7a-141">2</span><span class="sxs-lookup"><span data-stu-id="39f7a-141">2</span></span>     | <span data-ttu-id="39f7a-142">/ИФД/ГПС/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="39f7a-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="39f7a-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="39f7a-143">ASCII</span></span>       | <span data-ttu-id="39f7a-144">Нет</span><span class="sxs-lookup"><span data-stu-id="39f7a-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="39f7a-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="39f7a-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="39f7a-146">См. также</span><span class="sxs-lookup"><span data-stu-id="39f7a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39f7a-147">System. GPS. Латитудереф</span><span class="sxs-lookup"><span data-stu-id="39f7a-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
