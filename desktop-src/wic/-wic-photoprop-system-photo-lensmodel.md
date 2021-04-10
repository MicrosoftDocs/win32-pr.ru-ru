---
description: Политика метаданных фотографии для свойства System. photo. Ленсмодел.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Политика метаданных фото для System. photo. Ленсмодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081306"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="abede-103">Политика метаданных фото для System. photo. Ленсмодел</span><span class="sxs-lookup"><span data-stu-id="abede-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="abede-104">Политика метаданных фотографии для свойства [System. photo. ленсмодел](../properties/props-system-photo-lensmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="abede-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="abede-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="abede-105">PKEY</span></span>

<span data-ttu-id="abede-106">\_Ленсмодел фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="abede-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="abede-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="abede-107">Containers</span></span>

<span data-ttu-id="abede-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="abede-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="abede-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="abede-109">Read-Only</span></span>

<span data-ttu-id="abede-110">Нет</span><span class="sxs-lookup"><span data-stu-id="abede-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="abede-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="abede-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="abede-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="abede-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="abede-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="abede-113">Input Type</span></span>

<span data-ttu-id="abede-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="abede-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="abede-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="abede-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="abede-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="abede-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="abede-117">Приоритет путей (JPEG)</span><span class="sxs-lookup"><span data-stu-id="abede-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="abede-118">Если файл имеет формат JPEG, обработчик будет использовать следующий путь при чтении или записи данных.</span><span class="sxs-lookup"><span data-stu-id="abede-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="abede-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="abede-119">Order</span></span> | <span data-ttu-id="abede-120">Путь</span><span class="sxs-lookup"><span data-stu-id="abede-120">Path</span></span>                          | <span data-ttu-id="abede-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="abede-121">Disk Format</span></span> | <span data-ttu-id="abede-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="abede-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="abede-123">1</span><span class="sxs-lookup"><span data-stu-id="abede-123">1</span></span>     | <span data-ttu-id="abede-124">/КСМП/микрософтфото: Ленсмодел</span><span class="sxs-lookup"><span data-stu-id="abede-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="abede-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="abede-125">Unicode</span></span>     | <span data-ttu-id="abede-126">Да</span><span class="sxs-lookup"><span data-stu-id="abede-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="abede-127">Приоритет путей (TIFF)</span><span class="sxs-lookup"><span data-stu-id="abede-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="abede-128">Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.</span><span class="sxs-lookup"><span data-stu-id="abede-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="abede-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="abede-129">Order</span></span> | <span data-ttu-id="abede-130">Путь</span><span class="sxs-lookup"><span data-stu-id="abede-130">Path</span></span>                              | <span data-ttu-id="abede-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="abede-131">Disk Format</span></span> | <span data-ttu-id="abede-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="abede-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="abede-133">1</span><span class="sxs-lookup"><span data-stu-id="abede-133">1</span></span>     | <span data-ttu-id="abede-134">/ИФД/КСМП/микрософтфото: Ленсмодел</span><span class="sxs-lookup"><span data-stu-id="abede-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="abede-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="abede-135">Unicode</span></span>     | <span data-ttu-id="abede-136">Да</span><span class="sxs-lookup"><span data-stu-id="abede-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="abede-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abede-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="abede-138">См. также</span><span class="sxs-lookup"><span data-stu-id="abede-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abede-139">System. photo. Ленсмодел</span><span class="sxs-lookup"><span data-stu-id="abede-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
