---
description: Политика метаданных фотографии для свойства System. photo. Камерасериалнумбер.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Политика метаданных фото для System. photo. Камерасериалнумбер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684290"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="dfb3f-103">Политика метаданных фото для System. photo. Камерасериалнумбер</span><span class="sxs-lookup"><span data-stu-id="dfb3f-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="dfb3f-104">Политика метаданных фотографии для свойства [System. photo. камерасериалнумбер](../properties/props-system-photo-cameraserialnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb3f-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="dfb3f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="dfb3f-105">PKEY</span></span>

<span data-ttu-id="dfb3f-106">\_Камерасериалнумбер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="dfb3f-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="dfb3f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="dfb3f-107">Containers</span></span>

<span data-ttu-id="dfb3f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="dfb3f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="dfb3f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfb3f-109">Read-Only</span></span>

<span data-ttu-id="dfb3f-110">Нет</span><span class="sxs-lookup"><span data-stu-id="dfb3f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="dfb3f-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="dfb3f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="dfb3f-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="dfb3f-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="dfb3f-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="dfb3f-113">Input Type</span></span>

<span data-ttu-id="dfb3f-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="dfb3f-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="dfb3f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="dfb3f-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="dfb3f-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="dfb3f-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="dfb3f-118">Если файл имеет формат JPEG, обработчик будет читать, записывать и удалять данные из следующего пути:</span><span class="sxs-lookup"><span data-stu-id="dfb3f-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="dfb3f-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="dfb3f-119">Order</span></span> | <span data-ttu-id="dfb3f-120">Путь</span><span class="sxs-lookup"><span data-stu-id="dfb3f-120">Path</span></span>                                   | <span data-ttu-id="dfb3f-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dfb3f-121">Disk Format</span></span> | <span data-ttu-id="dfb3f-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfb3f-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="dfb3f-123">1</span><span class="sxs-lookup"><span data-stu-id="dfb3f-123">1</span></span>     | <span data-ttu-id="dfb3f-124">/КСМП/микрософтфото: Камерасериалнумбер</span><span class="sxs-lookup"><span data-stu-id="dfb3f-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="dfb3f-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="dfb3f-125">Unicode</span></span>     | <span data-ttu-id="dfb3f-126">Да</span><span class="sxs-lookup"><span data-stu-id="dfb3f-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="dfb3f-127">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="dfb3f-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="dfb3f-128">Если файл имеет формат TIFF, обработчик будет читать, записывать и удалять данные из следующего пути.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="dfb3f-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="dfb3f-129">Order</span></span> | <span data-ttu-id="dfb3f-130">Путь</span><span class="sxs-lookup"><span data-stu-id="dfb3f-130">Path</span></span>                                       | <span data-ttu-id="dfb3f-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dfb3f-131">Disk Format</span></span> | <span data-ttu-id="dfb3f-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfb3f-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="dfb3f-133">1</span><span class="sxs-lookup"><span data-stu-id="dfb3f-133">1</span></span>     | <span data-ttu-id="dfb3f-134">/ИФД/КСМП/микрософтфото: Камерасериалнумбер</span><span class="sxs-lookup"><span data-stu-id="dfb3f-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="dfb3f-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="dfb3f-135">Unicode</span></span>     | <span data-ttu-id="dfb3f-136">Да</span><span class="sxs-lookup"><span data-stu-id="dfb3f-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="dfb3f-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfb3f-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfb3f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="dfb3f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb3f-139">System. photo. Камерасериалнумбер</span><span class="sxs-lookup"><span data-stu-id="dfb3f-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
