---
description: Следующие флаги используются для указания каналов текстуры для обработки. Не рекомендуется.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Константы ДКСФИЛЕ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072251"
---
# <a name="dxfile-constants"></a><span data-ttu-id="7a527-104">Константы ДКСФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="7a527-104">DXFILE Constants</span></span>

<span data-ttu-id="7a527-105">Следующие флаги используются для указания каналов текстуры для обработки.</span><span class="sxs-lookup"><span data-stu-id="7a527-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="7a527-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7a527-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="7a527-107">дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="7a527-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="7a527-108">\#определенно</span><span class="sxs-lookup"><span data-stu-id="7a527-108">\#define</span></span>                 | <span data-ttu-id="7a527-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7a527-109">Value</span></span> | <span data-ttu-id="7a527-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7a527-110">Description</span></span>      |
| <span data-ttu-id="7a527-111">\_двоичный файл дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="7a527-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="7a527-112">0</span><span class="sxs-lookup"><span data-stu-id="7a527-112">0</span></span>     | <span data-ttu-id="7a527-113">Двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="7a527-113">Binary file.</span></span>     |
| <span data-ttu-id="7a527-114">ДКСФИЛЕФОРМАТ \_ текст</span><span class="sxs-lookup"><span data-stu-id="7a527-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="7a527-115">1</span><span class="sxs-lookup"><span data-stu-id="7a527-115">1</span></span>     | <span data-ttu-id="7a527-116">Текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="7a527-116">Text file.</span></span>       |
| <span data-ttu-id="7a527-117">\_сжатый дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="7a527-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="7a527-118">2</span><span class="sxs-lookup"><span data-stu-id="7a527-118">2</span></span>     | <span data-ttu-id="7a527-119">Сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="7a527-119">Compressed file.</span></span> |



 

<span data-ttu-id="7a527-120">Эти \# определения объявляются в дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="7a527-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="7a527-121">дксфилелоадоптионс</span><span class="sxs-lookup"><span data-stu-id="7a527-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="7a527-122">\#определенно</span><span class="sxs-lookup"><span data-stu-id="7a527-122">\#define</span></span>                 | <span data-ttu-id="7a527-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7a527-123">Value</span></span> | <span data-ttu-id="7a527-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7a527-124">Description</span></span>                  |
| <span data-ttu-id="7a527-125">ДКСФИЛЕЛОАД \_ фромфиле</span><span class="sxs-lookup"><span data-stu-id="7a527-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="7a527-126">0x00</span><span class="sxs-lookup"><span data-stu-id="7a527-126">0x00L</span></span> | <span data-ttu-id="7a527-127">Загрузить файл из файла.</span><span class="sxs-lookup"><span data-stu-id="7a527-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="7a527-128">ДКСФИЛЕЛОАД \_ фромресаурце</span><span class="sxs-lookup"><span data-stu-id="7a527-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="7a527-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="7a527-129">0x01L</span></span> | <span data-ttu-id="7a527-130">Загрузка файла из ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a527-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="7a527-131">ДКСФИЛЕЛОАД \_ фроммемори</span><span class="sxs-lookup"><span data-stu-id="7a527-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="7a527-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="7a527-132">0x02L</span></span> | <span data-ttu-id="7a527-133">Загрузка файла из памяти.</span><span class="sxs-lookup"><span data-stu-id="7a527-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="7a527-134">ДКСФИЛЕЛОАД \_ фромстреам</span><span class="sxs-lookup"><span data-stu-id="7a527-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="7a527-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="7a527-135">0x04L</span></span> | <span data-ttu-id="7a527-136">Загрузить файл из потока.</span><span class="sxs-lookup"><span data-stu-id="7a527-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="7a527-137">ДКСФИЛЕЛОАД \_ фромурл</span><span class="sxs-lookup"><span data-stu-id="7a527-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="7a527-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="7a527-138">0x08L</span></span> | <span data-ttu-id="7a527-139">Загрузка файла из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7a527-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="7a527-140">Эти \# определения объявляются в дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="7a527-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a527-141">См. также</span><span class="sxs-lookup"><span data-stu-id="7a527-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a527-142">Ссылка на X-файл (устаревшая)</span><span class="sxs-lookup"><span data-stu-id="7a527-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



