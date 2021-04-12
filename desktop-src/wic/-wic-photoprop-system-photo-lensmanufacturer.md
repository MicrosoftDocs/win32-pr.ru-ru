---
description: Политика метаданных фотографии для свойства System. photo. Ленсмануфактурер.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Политика метаданных фото для System. photo. Ленсмануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265861"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="5573d-103">Политика метаданных фото для System. photo. Ленсмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5573d-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="5573d-104">Политика метаданных фотографии для свойства [System. photo. ленсмануфактурер](../properties/props-system-photo-lensmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="5573d-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5573d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5573d-105">PKEY</span></span>

<span data-ttu-id="5573d-106">\_Ленсмануфактурер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="5573d-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="5573d-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="5573d-107">Containers</span></span>

<span data-ttu-id="5573d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5573d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5573d-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5573d-109">Read-Only</span></span>

<span data-ttu-id="5573d-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5573d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5573d-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5573d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5573d-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5573d-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5573d-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="5573d-113">Input Type</span></span>

<span data-ttu-id="5573d-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="5573d-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5573d-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="5573d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5573d-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="5573d-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="5573d-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="5573d-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="5573d-118">Если файл имеет формат JPEG, обработчик будет использовать следующий путь при чтении или записи данных.</span><span class="sxs-lookup"><span data-stu-id="5573d-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="5573d-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="5573d-119">Order</span></span> | <span data-ttu-id="5573d-120">Путь</span><span class="sxs-lookup"><span data-stu-id="5573d-120">Path</span></span>                                 | <span data-ttu-id="5573d-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5573d-121">Disk Format</span></span> | <span data-ttu-id="5573d-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5573d-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="5573d-123">1</span><span class="sxs-lookup"><span data-stu-id="5573d-123">1</span></span>     | <span data-ttu-id="5573d-124">/КСМП/микрософтфото: Ленсмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5573d-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="5573d-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="5573d-125">Unicode</span></span>     | <span data-ttu-id="5573d-126">Да</span><span class="sxs-lookup"><span data-stu-id="5573d-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="5573d-127">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="5573d-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="5573d-128">Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.</span><span class="sxs-lookup"><span data-stu-id="5573d-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="5573d-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="5573d-129">Order</span></span> | <span data-ttu-id="5573d-130">Путь</span><span class="sxs-lookup"><span data-stu-id="5573d-130">Path</span></span>                                     | <span data-ttu-id="5573d-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5573d-131">Disk Format</span></span> | <span data-ttu-id="5573d-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5573d-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="5573d-133">1</span><span class="sxs-lookup"><span data-stu-id="5573d-133">1</span></span>     | <span data-ttu-id="5573d-134">/ИФД/КСМП/микрософтфото: Ленсмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5573d-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="5573d-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="5573d-135">Unicode</span></span>     | <span data-ttu-id="5573d-136">Да</span><span class="sxs-lookup"><span data-stu-id="5573d-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="5573d-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5573d-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5573d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5573d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5573d-139">System. photo. Ленсмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5573d-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
