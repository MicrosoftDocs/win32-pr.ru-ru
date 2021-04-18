---
description: Политика метаданных фотографии для свойства System. GPS. Мапдатум.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Политика метаданных фотографии System. GPS. Мапдатум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674273"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="a0c32-103">Политика метаданных фотографии System. GPS. Мапдатум</span><span class="sxs-lookup"><span data-stu-id="a0c32-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="a0c32-104">Политика метаданных фотографии для свойства [System. GPS. мапдатум](../properties/props-system-gps-mapdatum.md) .</span><span class="sxs-lookup"><span data-stu-id="a0c32-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a0c32-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a0c32-105">PKEY</span></span>

<span data-ttu-id="a0c32-106">PKEY \_ GPS \_ мапдатум</span><span class="sxs-lookup"><span data-stu-id="a0c32-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="a0c32-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="a0c32-107">Containers</span></span>

<span data-ttu-id="a0c32-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a0c32-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a0c32-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0c32-109">Read-Only</span></span>

<span data-ttu-id="a0c32-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a0c32-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a0c32-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="a0c32-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a0c32-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a0c32-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a0c32-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="a0c32-113">Input Type</span></span>

<span data-ttu-id="a0c32-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR</span><span class="sxs-lookup"><span data-stu-id="a0c32-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a0c32-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="a0c32-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a0c32-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="a0c32-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="a0c32-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="a0c32-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="a0c32-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="a0c32-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="a0c32-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="a0c32-119">Order</span></span> | <span data-ttu-id="a0c32-120">Путь</span><span class="sxs-lookup"><span data-stu-id="a0c32-120">Path</span></span>                          | <span data-ttu-id="a0c32-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a0c32-121">Disk Format</span></span> | <span data-ttu-id="a0c32-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a0c32-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="a0c32-123">1</span><span class="sxs-lookup"><span data-stu-id="a0c32-123">1</span></span>     | <span data-ttu-id="a0c32-124">/КСМП/ексиф: Гпсмапдатум</span><span class="sxs-lookup"><span data-stu-id="a0c32-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="a0c32-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="a0c32-125">Unicode</span></span>     | <span data-ttu-id="a0c32-126">Да</span><span class="sxs-lookup"><span data-stu-id="a0c32-126">Yes</span></span>      |
| <span data-ttu-id="a0c32-127">2</span><span class="sxs-lookup"><span data-stu-id="a0c32-127">2</span></span>     | <span data-ttu-id="a0c32-128">/APP1/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="a0c32-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="a0c32-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="a0c32-129">ASCII</span></span>       | <span data-ttu-id="a0c32-130">Нет</span><span class="sxs-lookup"><span data-stu-id="a0c32-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="a0c32-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="a0c32-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="a0c32-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="a0c32-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="a0c32-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="a0c32-133">Order</span></span> | <span data-ttu-id="a0c32-134">Путь</span><span class="sxs-lookup"><span data-stu-id="a0c32-134">Path</span></span>                      | <span data-ttu-id="a0c32-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a0c32-135">Disk Format</span></span> | <span data-ttu-id="a0c32-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a0c32-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="a0c32-137">1</span><span class="sxs-lookup"><span data-stu-id="a0c32-137">1</span></span>     | <span data-ttu-id="a0c32-138">/ИФД/КСМП/ексиф: Гпсмапдатум</span><span class="sxs-lookup"><span data-stu-id="a0c32-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="a0c32-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="a0c32-139">Unicode</span></span>     | <span data-ttu-id="a0c32-140">Да</span><span class="sxs-lookup"><span data-stu-id="a0c32-140">Yes</span></span>      |
| <span data-ttu-id="a0c32-141">2</span><span class="sxs-lookup"><span data-stu-id="a0c32-141">2</span></span>     | <span data-ttu-id="a0c32-142">/ИФД/ГПС/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="a0c32-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="a0c32-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="a0c32-143">ASCII</span></span>       | <span data-ttu-id="a0c32-144">Нет</span><span class="sxs-lookup"><span data-stu-id="a0c32-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="a0c32-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="a0c32-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0c32-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a0c32-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0c32-147">System. GPS. Мапдатум</span><span class="sxs-lookup"><span data-stu-id="a0c32-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
