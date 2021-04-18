---
description: Политика метаданных фотографии для свойства System. GPS. Дестлонгитудереф.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Политика метаданных фотографии System. GPS. Дестлонгитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712691"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="73d82-103">Политика метаданных фотографии System. GPS. Дестлонгитудереф</span><span class="sxs-lookup"><span data-stu-id="73d82-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="73d82-104">Политика метаданных фотографии для свойства [System. GPS. дестлонгитудереф](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="73d82-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="73d82-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="73d82-105">PKEY</span></span>

<span data-ttu-id="73d82-106">PKEY \_ , GPS. дестлонгитудереф</span><span class="sxs-lookup"><span data-stu-id="73d82-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="73d82-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="73d82-107">Containers</span></span>

<span data-ttu-id="73d82-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="73d82-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="73d82-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="73d82-109">Read-Only</span></span>

<span data-ttu-id="73d82-110">Нет</span><span class="sxs-lookup"><span data-stu-id="73d82-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="73d82-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="73d82-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="73d82-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="73d82-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="73d82-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="73d82-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="73d82-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="73d82-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="73d82-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="73d82-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="73d82-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="73d82-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="73d82-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="73d82-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="73d82-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="73d82-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="73d82-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="73d82-119">Order</span></span> | <span data-ttu-id="73d82-120">Путь</span><span class="sxs-lookup"><span data-stu-id="73d82-120">Path</span></span>                          | <span data-ttu-id="73d82-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="73d82-121">Disk Format</span></span> | <span data-ttu-id="73d82-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="73d82-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="73d82-123">1</span><span class="sxs-lookup"><span data-stu-id="73d82-123">1</span></span>     | <span data-ttu-id="73d82-124">/КСМП/ексиф: Гпсдестлонгитудереф</span><span class="sxs-lookup"><span data-stu-id="73d82-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="73d82-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="73d82-125">Unicode</span></span>     | <span data-ttu-id="73d82-126">Да</span><span class="sxs-lookup"><span data-stu-id="73d82-126">Yes</span></span>      |
| <span data-ttu-id="73d82-127">2</span><span class="sxs-lookup"><span data-stu-id="73d82-127">2</span></span>     | <span data-ttu-id="73d82-128">/APP1/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="73d82-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="73d82-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="73d82-129">ASCII</span></span>       | <span data-ttu-id="73d82-130">Нет</span><span class="sxs-lookup"><span data-stu-id="73d82-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="73d82-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="73d82-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="73d82-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="73d82-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="73d82-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="73d82-133">Order</span></span> | <span data-ttu-id="73d82-134">Путь</span><span class="sxs-lookup"><span data-stu-id="73d82-134">Path</span></span>                              | <span data-ttu-id="73d82-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="73d82-135">Disk Format</span></span> | <span data-ttu-id="73d82-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="73d82-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="73d82-137">1</span><span class="sxs-lookup"><span data-stu-id="73d82-137">1</span></span>     | <span data-ttu-id="73d82-138">/ИФД/КСМП/ексиф: Гпсдестлонгитудереф</span><span class="sxs-lookup"><span data-stu-id="73d82-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="73d82-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="73d82-139">Unicode</span></span>     | <span data-ttu-id="73d82-140">Да</span><span class="sxs-lookup"><span data-stu-id="73d82-140">Yes</span></span>      |
| <span data-ttu-id="73d82-141">2</span><span class="sxs-lookup"><span data-stu-id="73d82-141">2</span></span>     | <span data-ttu-id="73d82-142">/ИФД/ГПС/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="73d82-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="73d82-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="73d82-143">ASCII</span></span>       | <span data-ttu-id="73d82-144">Нет</span><span class="sxs-lookup"><span data-stu-id="73d82-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="73d82-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="73d82-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d82-146">См. также</span><span class="sxs-lookup"><span data-stu-id="73d82-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d82-147">System. GPS. Дестлонгитудереф</span><span class="sxs-lookup"><span data-stu-id="73d82-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
