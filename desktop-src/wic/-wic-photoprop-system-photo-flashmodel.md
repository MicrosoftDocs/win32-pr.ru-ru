---
description: Политика метаданных фотографии для свойства System. photo. Флашмодел.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Политика метаданных фото для System. photo. Флашмодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712301"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="a5412-103">Политика метаданных фото для System. photo. Флашмодел</span><span class="sxs-lookup"><span data-stu-id="a5412-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="a5412-104">Политика метаданных фотографии для свойства [System. photo. флашмодел](../properties/props-system-photo-flashmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="a5412-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a5412-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a5412-105">PKEY</span></span>

<span data-ttu-id="a5412-106">\_Флашмодел фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="a5412-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="a5412-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="a5412-107">Containers</span></span>

<span data-ttu-id="a5412-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a5412-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a5412-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5412-109">Read-Only</span></span>

<span data-ttu-id="a5412-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a5412-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a5412-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="a5412-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a5412-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a5412-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a5412-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="a5412-113">Input Type</span></span>

<span data-ttu-id="a5412-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="a5412-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a5412-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="a5412-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a5412-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="a5412-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="a5412-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="a5412-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="a5412-118">Если файл имеет формат JPEG, обработчик будет использовать следующий путь при чтении или записи данных.</span><span class="sxs-lookup"><span data-stu-id="a5412-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="a5412-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="a5412-119">Order</span></span> | <span data-ttu-id="a5412-120">Путь</span><span class="sxs-lookup"><span data-stu-id="a5412-120">Path</span></span>                           | <span data-ttu-id="a5412-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a5412-121">Disk Format</span></span> | <span data-ttu-id="a5412-122">Формат данных</span><span class="sxs-lookup"><span data-stu-id="a5412-122">Data Format</span></span> | <span data-ttu-id="a5412-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a5412-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="a5412-124">1</span><span class="sxs-lookup"><span data-stu-id="a5412-124">1</span></span>     | <span data-ttu-id="a5412-125">/КСМП/микрософтфото: Флашмодел</span><span class="sxs-lookup"><span data-stu-id="a5412-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="a5412-126">Юникод</span><span class="sxs-lookup"><span data-stu-id="a5412-126">Unicode</span></span>     |             | <span data-ttu-id="a5412-127">Да</span><span class="sxs-lookup"><span data-stu-id="a5412-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="a5412-128">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="a5412-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="a5412-129">Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.</span><span class="sxs-lookup"><span data-stu-id="a5412-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="a5412-130">Заказ</span><span class="sxs-lookup"><span data-stu-id="a5412-130">Order</span></span> | <span data-ttu-id="a5412-131">Путь</span><span class="sxs-lookup"><span data-stu-id="a5412-131">Path</span></span>                               | <span data-ttu-id="a5412-132">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a5412-132">Disk Format</span></span> | <span data-ttu-id="a5412-133">Формат данных</span><span class="sxs-lookup"><span data-stu-id="a5412-133">Data Format</span></span> | <span data-ttu-id="a5412-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a5412-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="a5412-135">1</span><span class="sxs-lookup"><span data-stu-id="a5412-135">1</span></span>     | <span data-ttu-id="a5412-136">/ИФД/КСМП/микрософтфото: Флашмодел</span><span class="sxs-lookup"><span data-stu-id="a5412-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="a5412-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="a5412-137">Unicode</span></span>     |             | <span data-ttu-id="a5412-138">Да</span><span class="sxs-lookup"><span data-stu-id="a5412-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="a5412-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5412-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5412-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a5412-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5412-141">System. photo. Флашмодел</span><span class="sxs-lookup"><span data-stu-id="a5412-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
