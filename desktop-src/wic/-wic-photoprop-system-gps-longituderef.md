---
description: Политика метаданных фотографии для свойства System. GPS. Лонгитудереф.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Политика метаданных фотографии System. GPS. Лонгитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674274"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="2dd1b-103">Политика метаданных фотографии System. GPS. Лонгитудереф</span><span class="sxs-lookup"><span data-stu-id="2dd1b-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="2dd1b-104">Политика метаданных фотографии для свойства [System. GPS. лонгитудереф](../properties/props-system-gps-longituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd1b-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2dd1b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2dd1b-105">PKEY</span></span>

<span data-ttu-id="2dd1b-106">PKEY \_ GPS \_ лонгитудереф</span><span class="sxs-lookup"><span data-stu-id="2dd1b-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="2dd1b-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="2dd1b-107">Containers</span></span>

<span data-ttu-id="2dd1b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2dd1b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2dd1b-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2dd1b-109">Read-Only</span></span>

<span data-ttu-id="2dd1b-110">Нет</span><span class="sxs-lookup"><span data-stu-id="2dd1b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2dd1b-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="2dd1b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2dd1b-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="2dd1b-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="2dd1b-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="2dd1b-113">Input Type</span></span>

<span data-ttu-id="2dd1b-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2dd1b-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="2dd1b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2dd1b-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="2dd1b-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="2dd1b-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="2dd1b-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="2dd1b-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="2dd1b-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="2dd1b-119">Order</span></span> | <span data-ttu-id="2dd1b-120">Путь</span><span class="sxs-lookup"><span data-stu-id="2dd1b-120">Path</span></span>                         | <span data-ttu-id="2dd1b-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2dd1b-121">Disk Format</span></span> | <span data-ttu-id="2dd1b-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2dd1b-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="2dd1b-123">1</span><span class="sxs-lookup"><span data-stu-id="2dd1b-123">1</span></span>     | <span data-ttu-id="2dd1b-124">/КСМП/ексиф: Гпслонгитудереф</span><span class="sxs-lookup"><span data-stu-id="2dd1b-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="2dd1b-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="2dd1b-125">Unicode</span></span>     | <span data-ttu-id="2dd1b-126">Да</span><span class="sxs-lookup"><span data-stu-id="2dd1b-126">Yes</span></span>      |
| <span data-ttu-id="2dd1b-127">2</span><span class="sxs-lookup"><span data-stu-id="2dd1b-127">2</span></span>     | <span data-ttu-id="2dd1b-128">/APP1/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="2dd1b-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="2dd1b-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="2dd1b-129">ASCII</span></span>       | <span data-ttu-id="2dd1b-130">Нет</span><span class="sxs-lookup"><span data-stu-id="2dd1b-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="2dd1b-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="2dd1b-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="2dd1b-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="2dd1b-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="2dd1b-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="2dd1b-133">Order</span></span> | <span data-ttu-id="2dd1b-134">Путь</span><span class="sxs-lookup"><span data-stu-id="2dd1b-134">Path</span></span>                          | <span data-ttu-id="2dd1b-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2dd1b-135">Disk Format</span></span> | <span data-ttu-id="2dd1b-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2dd1b-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="2dd1b-137">1</span><span class="sxs-lookup"><span data-stu-id="2dd1b-137">1</span></span>     | <span data-ttu-id="2dd1b-138">/ИФД/КСМП/ексиф: Гпслонгитудереф</span><span class="sxs-lookup"><span data-stu-id="2dd1b-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="2dd1b-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="2dd1b-139">Unicode</span></span>     | <span data-ttu-id="2dd1b-140">Да</span><span class="sxs-lookup"><span data-stu-id="2dd1b-140">Yes</span></span>      |
| <span data-ttu-id="2dd1b-141">2</span><span class="sxs-lookup"><span data-stu-id="2dd1b-141">2</span></span>     | <span data-ttu-id="2dd1b-142">/ИФД/ГПС/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="2dd1b-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="2dd1b-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="2dd1b-143">ASCII</span></span>       | <span data-ttu-id="2dd1b-144">Нет</span><span class="sxs-lookup"><span data-stu-id="2dd1b-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="2dd1b-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="2dd1b-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dd1b-146">См. также</span><span class="sxs-lookup"><span data-stu-id="2dd1b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dd1b-147">System. GPS. Лонгитудереф</span><span class="sxs-lookup"><span data-stu-id="2dd1b-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
