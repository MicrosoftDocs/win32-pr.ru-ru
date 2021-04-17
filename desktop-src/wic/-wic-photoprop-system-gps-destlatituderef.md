---
description: Политика метаданных фотографии для свойства System. GPS. Дестлатитудереф.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Политика метаданных фотографии System. GPS. Дестлатитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683779"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="4f952-103">Политика метаданных фотографии System. GPS. Дестлатитудереф</span><span class="sxs-lookup"><span data-stu-id="4f952-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="4f952-104">Политика метаданных фотографии для свойства [System. GPS. дестлатитудереф](../properties/props-system-gps-destlatituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="4f952-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4f952-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4f952-105">PKEY</span></span>

<span data-ttu-id="4f952-106">PKEY \_ GPS \_ дестлатитудереф</span><span class="sxs-lookup"><span data-stu-id="4f952-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="4f952-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="4f952-107">Containers</span></span>

<span data-ttu-id="4f952-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4f952-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4f952-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f952-109">Read-Only</span></span>

<span data-ttu-id="4f952-110">Нет</span><span class="sxs-lookup"><span data-stu-id="4f952-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4f952-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="4f952-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4f952-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4f952-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4f952-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="4f952-113">Input Type</span></span>

<span data-ttu-id="4f952-114">VT \_ LPWSTR является предпочтительным, но технология VT \_ LPSTR принимается.</span><span class="sxs-lookup"><span data-stu-id="4f952-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4f952-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="4f952-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4f952-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="4f952-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="4f952-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="4f952-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="4f952-118">Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="4f952-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="4f952-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="4f952-119">Order</span></span> | <span data-ttu-id="4f952-120">Путь</span><span class="sxs-lookup"><span data-stu-id="4f952-120">Path</span></span>                          | <span data-ttu-id="4f952-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4f952-121">Disk Format</span></span> | <span data-ttu-id="4f952-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4f952-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="4f952-123">1</span><span class="sxs-lookup"><span data-stu-id="4f952-123">1</span></span>     | <span data-ttu-id="4f952-124">/КСМП/ексиф: Гпсдестлатитудереф</span><span class="sxs-lookup"><span data-stu-id="4f952-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="4f952-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="4f952-125">Unicode</span></span>     | <span data-ttu-id="4f952-126">Да</span><span class="sxs-lookup"><span data-stu-id="4f952-126">Yes</span></span>      |
| <span data-ttu-id="4f952-127">2</span><span class="sxs-lookup"><span data-stu-id="4f952-127">2</span></span>     | <span data-ttu-id="4f952-128">/APP1/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="4f952-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="4f952-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="4f952-129">ASCII</span></span>       | <span data-ttu-id="4f952-130">Нет</span><span class="sxs-lookup"><span data-stu-id="4f952-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="4f952-131">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="4f952-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="4f952-132">Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="4f952-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="4f952-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="4f952-133">Order</span></span> | <span data-ttu-id="4f952-134">Путь</span><span class="sxs-lookup"><span data-stu-id="4f952-134">Path</span></span>                             | <span data-ttu-id="4f952-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4f952-135">Disk Format</span></span> | <span data-ttu-id="4f952-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4f952-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="4f952-137">1</span><span class="sxs-lookup"><span data-stu-id="4f952-137">1</span></span>     | <span data-ttu-id="4f952-138">/ИФД/КСМП/ексиф: Гпсдестлатитудереф</span><span class="sxs-lookup"><span data-stu-id="4f952-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="4f952-139">Юникод</span><span class="sxs-lookup"><span data-stu-id="4f952-139">Unicode</span></span>     | <span data-ttu-id="4f952-140">Да</span><span class="sxs-lookup"><span data-stu-id="4f952-140">Yes</span></span>      |
| <span data-ttu-id="4f952-141">2</span><span class="sxs-lookup"><span data-stu-id="4f952-141">2</span></span>     | <span data-ttu-id="4f952-142">/ИФД/ГПС/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="4f952-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="4f952-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="4f952-143">ASCII</span></span>       | <span data-ttu-id="4f952-144">Нет</span><span class="sxs-lookup"><span data-stu-id="4f952-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="4f952-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f952-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f952-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4f952-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f952-147">System. GPS. Дестлатитудереф</span><span class="sxs-lookup"><span data-stu-id="4f952-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
