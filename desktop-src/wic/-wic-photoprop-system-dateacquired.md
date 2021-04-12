---
description: Политика метаданных фотографии для свойства System. Датеаккуиред.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Политика метаданных фотографии System. Датеаккуиред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272298"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="cfb3f-103">Политика метаданных фотографии System. Датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="cfb3f-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="cfb3f-104">Политика метаданных фотографии для свойства [System. датеаккуиред](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb3f-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cfb3f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cfb3f-105">PKEY</span></span>

<span data-ttu-id="cfb3f-106">PKEY \_ датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="cfb3f-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="cfb3f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="cfb3f-107">Containers</span></span>

<span data-ttu-id="cfb3f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cfb3f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cfb3f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfb3f-109">Read-Only</span></span>

<span data-ttu-id="cfb3f-110">Нет</span><span class="sxs-lookup"><span data-stu-id="cfb3f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cfb3f-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="cfb3f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cfb3f-112">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="cfb3f-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cfb3f-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="cfb3f-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cfb3f-114">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="cfb3f-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cfb3f-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="cfb3f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cfb3f-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="cfb3f-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="cfb3f-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="cfb3f-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="cfb3f-118">Если файл имеет формат JPEG, обработчик выполняет поиск данных в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cfb3f-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="cfb3f-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="cfb3f-119">Order</span></span> | <span data-ttu-id="cfb3f-120">Путь</span><span class="sxs-lookup"><span data-stu-id="cfb3f-120">Path</span></span>                             | <span data-ttu-id="cfb3f-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cfb3f-121">Disk Format</span></span>                        | <span data-ttu-id="cfb3f-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="cfb3f-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="cfb3f-123">1</span><span class="sxs-lookup"><span data-stu-id="cfb3f-123">1</span></span>     | <span data-ttu-id="cfb3f-124">/КСМП/микрософтфото: Датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="cfb3f-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="cfb3f-125">Строка Юникода в формате даты XMP.</span><span class="sxs-lookup"><span data-stu-id="cfb3f-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="cfb3f-126">Да</span><span class="sxs-lookup"><span data-stu-id="cfb3f-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="cfb3f-127">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="cfb3f-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="cfb3f-128">Если файл имеет формат TIFF, обработчик выполняет поиск данных в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cfb3f-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="cfb3f-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="cfb3f-129">Order</span></span> | <span data-ttu-id="cfb3f-130">Путь</span><span class="sxs-lookup"><span data-stu-id="cfb3f-130">Path</span></span>                                 | <span data-ttu-id="cfb3f-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cfb3f-131">Disk Format</span></span>                        | <span data-ttu-id="cfb3f-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="cfb3f-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="cfb3f-133">1</span><span class="sxs-lookup"><span data-stu-id="cfb3f-133">1</span></span>     | <span data-ttu-id="cfb3f-134">/ИФД/КСМП/микрософтфото: Датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="cfb3f-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="cfb3f-135">Строка Юникода в формате даты XMP.</span><span class="sxs-lookup"><span data-stu-id="cfb3f-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="cfb3f-136">Да</span><span class="sxs-lookup"><span data-stu-id="cfb3f-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="cfb3f-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfb3f-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfb3f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cfb3f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb3f-139">System. Датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="cfb3f-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
