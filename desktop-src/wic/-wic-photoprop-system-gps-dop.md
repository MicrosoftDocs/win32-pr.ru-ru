---
description: Политика метаданных фотографии для свойства System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Политика метаданных фотографии System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999420"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="ad540-103">Политика метаданных фотографии System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="ad540-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="ad540-104">Политика метаданных фотографии для свойства [System. GPS. DOP](../properties/props-system-gps-dop.md) .</span><span class="sxs-lookup"><span data-stu-id="ad540-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ad540-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ad540-105">PKEY</span></span>

<span data-ttu-id="ad540-106">PKEY \_ GPS \_ DOP</span><span class="sxs-lookup"><span data-stu-id="ad540-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="ad540-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="ad540-107">Containers</span></span>

<span data-ttu-id="ad540-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ad540-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ad540-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad540-109">Read-Only</span></span>

<span data-ttu-id="ad540-110">Да</span><span class="sxs-lookup"><span data-stu-id="ad540-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ad540-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="ad540-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ad540-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ad540-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ad540-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="ad540-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="ad540-114">Это значение можно записать с помощью записи в System. GPS. Допнумератор и System. GPS. Допденоминатор.</span><span class="sxs-lookup"><span data-stu-id="ad540-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="ad540-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="ad540-115">It cannot be written directly.</span></span> <span data-ttu-id="ad540-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="ad540-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="ad540-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="ad540-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="ad540-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="ad540-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="ad540-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="ad540-119">Order</span></span> | <span data-ttu-id="ad540-120">Путь</span><span class="sxs-lookup"><span data-stu-id="ad540-120">Path</span></span>                          | <span data-ttu-id="ad540-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ad540-121">Disk Format</span></span>   | <span data-ttu-id="ad540-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ad540-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="ad540-123">1</span><span class="sxs-lookup"><span data-stu-id="ad540-123">1</span></span>     | <span data-ttu-id="ad540-124">/КСМП/ексиф: ГПСДОП</span><span class="sxs-lookup"><span data-stu-id="ad540-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="ad540-125">Рациональное XMP</span><span class="sxs-lookup"><span data-stu-id="ad540-125">XMP rational</span></span>  | <span data-ttu-id="ad540-126">Да</span><span class="sxs-lookup"><span data-stu-id="ad540-126">Yes</span></span>      |
| <span data-ttu-id="ad540-127">2</span><span class="sxs-lookup"><span data-stu-id="ad540-127">2</span></span>     | <span data-ttu-id="ad540-128">/APP1/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="ad540-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="ad540-129">Рациональное воссебе EXIF</span><span class="sxs-lookup"><span data-stu-id="ad540-129">EXIF rational</span></span> | <span data-ttu-id="ad540-130">Нет</span><span class="sxs-lookup"><span data-stu-id="ad540-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="ad540-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="ad540-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="ad540-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="ad540-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="ad540-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="ad540-133">Order</span></span> | <span data-ttu-id="ad540-134">Путь</span><span class="sxs-lookup"><span data-stu-id="ad540-134">Path</span></span>                     | <span data-ttu-id="ad540-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ad540-135">Disk Format</span></span>   | <span data-ttu-id="ad540-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ad540-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="ad540-137">1</span><span class="sxs-lookup"><span data-stu-id="ad540-137">1</span></span>     | <span data-ttu-id="ad540-138">/ИФД/КСМП/ексиф: Гпсдоп</span><span class="sxs-lookup"><span data-stu-id="ad540-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="ad540-139">Рациональное XMP</span><span class="sxs-lookup"><span data-stu-id="ad540-139">XMP rational</span></span>  | <span data-ttu-id="ad540-140">Да</span><span class="sxs-lookup"><span data-stu-id="ad540-140">Yes</span></span>      |
| <span data-ttu-id="ad540-141">2</span><span class="sxs-lookup"><span data-stu-id="ad540-141">2</span></span>     | <span data-ttu-id="ad540-142">/ИФД/ГПС/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="ad540-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="ad540-143">Рациональное воссебе EXIF</span><span class="sxs-lookup"><span data-stu-id="ad540-143">EXIF rational</span></span> | <span data-ttu-id="ad540-144">Нет</span><span class="sxs-lookup"><span data-stu-id="ad540-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="ad540-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="ad540-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad540-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ad540-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad540-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="ad540-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
