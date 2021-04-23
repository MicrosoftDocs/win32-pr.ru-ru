---
description: Политика метаданных фотографии для свойства System. photo. Флашмануфактурер.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Политика метаданных фото для System. photo. Флашмануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081445"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="5857a-103">Политика метаданных фото для System. photo. Флашмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5857a-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="5857a-104">Политика метаданных фотографии для свойства [System. photo. флашмануфактурер](../properties/props-system-photo-flashmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="5857a-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5857a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5857a-105">PKEY</span></span>

<span data-ttu-id="5857a-106">\_Флашмануфактурер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="5857a-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="5857a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="5857a-107">Containers</span></span>

<span data-ttu-id="5857a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5857a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5857a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5857a-109">Read-Only</span></span>

<span data-ttu-id="5857a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5857a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5857a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5857a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5857a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5857a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5857a-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="5857a-113">Input Type</span></span>

<span data-ttu-id="5857a-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="5857a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5857a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="5857a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5857a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="5857a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="5857a-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="5857a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="5857a-118">Если файл имеет формат JPEG, обработчик будет использовать следующий путь при чтении или записи данных.</span><span class="sxs-lookup"><span data-stu-id="5857a-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="5857a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="5857a-119">Order</span></span> | <span data-ttu-id="5857a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="5857a-120">Path</span></span>                                  | <span data-ttu-id="5857a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5857a-121">Disk Format</span></span> | <span data-ttu-id="5857a-122">Формат данных</span><span class="sxs-lookup"><span data-stu-id="5857a-122">Data Format</span></span> | <span data-ttu-id="5857a-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5857a-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="5857a-124">1</span><span class="sxs-lookup"><span data-stu-id="5857a-124">1</span></span>     | <span data-ttu-id="5857a-125">/КСМП/микрософтфото: Флашмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5857a-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="5857a-126">Юникод</span><span class="sxs-lookup"><span data-stu-id="5857a-126">Unicode</span></span>     |             | <span data-ttu-id="5857a-127">Да</span><span class="sxs-lookup"><span data-stu-id="5857a-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="5857a-128">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="5857a-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="5857a-129">Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.</span><span class="sxs-lookup"><span data-stu-id="5857a-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="5857a-130">Заказ</span><span class="sxs-lookup"><span data-stu-id="5857a-130">Order</span></span> | <span data-ttu-id="5857a-131">Путь</span><span class="sxs-lookup"><span data-stu-id="5857a-131">Path</span></span>                                      | <span data-ttu-id="5857a-132">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5857a-132">Disk Format</span></span> | <span data-ttu-id="5857a-133">Формат данных</span><span class="sxs-lookup"><span data-stu-id="5857a-133">Data Format</span></span> | <span data-ttu-id="5857a-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5857a-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="5857a-135">1</span><span class="sxs-lookup"><span data-stu-id="5857a-135">1</span></span>     | <span data-ttu-id="5857a-136">/ИФД/КСМП/микрософтфото: Флашмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5857a-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="5857a-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="5857a-137">Unicode</span></span>     |             | <span data-ttu-id="5857a-138">Да</span><span class="sxs-lookup"><span data-stu-id="5857a-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="5857a-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5857a-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5857a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="5857a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5857a-141">System. photo. Флашмануфактурер</span><span class="sxs-lookup"><span data-stu-id="5857a-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
