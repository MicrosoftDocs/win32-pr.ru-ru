---
description: Следующие флаги используются для указания каналов текстуры для обработки. Не рекомендуется.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Константы ДКСФИЛЕ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42b20ca9934b9a4203e05f477ea8c40853a0a836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997301"
---
# <a name="dxfile-constants"></a><span data-ttu-id="9cb43-104">Константы ДКСФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="9cb43-104">DXFILE Constants</span></span>

<span data-ttu-id="9cb43-105">Следующие флаги используются для указания каналов текстуры для обработки.</span><span class="sxs-lookup"><span data-stu-id="9cb43-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="9cb43-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9cb43-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="9cb43-107">дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="9cb43-107">DXFILEFORMAT</span></span>



| <span data-ttu-id="9cb43-108">\#определенно</span><span class="sxs-lookup"><span data-stu-id="9cb43-108">\#define</span></span>                 | <span data-ttu-id="9cb43-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9cb43-109">Value</span></span> | <span data-ttu-id="9cb43-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9cb43-110">Description</span></span>      |
|--------------------------|-------|------------------|
| <span data-ttu-id="9cb43-111">\_двоичный файл дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="9cb43-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="9cb43-112">0</span><span class="sxs-lookup"><span data-stu-id="9cb43-112">0</span></span>     | <span data-ttu-id="9cb43-113">Двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="9cb43-113">Binary file.</span></span>     |
| <span data-ttu-id="9cb43-114">ДКСФИЛЕФОРМАТ \_ текст</span><span class="sxs-lookup"><span data-stu-id="9cb43-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="9cb43-115">1</span><span class="sxs-lookup"><span data-stu-id="9cb43-115">1</span></span>     | <span data-ttu-id="9cb43-116">Текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="9cb43-116">Text file.</span></span>       |
| <span data-ttu-id="9cb43-117">\_сжатый дксфилеформат</span><span class="sxs-lookup"><span data-stu-id="9cb43-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="9cb43-118">2</span><span class="sxs-lookup"><span data-stu-id="9cb43-118">2</span></span>     | <span data-ttu-id="9cb43-119">Сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="9cb43-119">Compressed file.</span></span> |



 

<span data-ttu-id="9cb43-120">Эти \# определения объявляются в дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="9cb43-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="9cb43-121">дксфилелоадоптионс</span><span class="sxs-lookup"><span data-stu-id="9cb43-121">DXFILELOADOPTIONS</span></span>



| <span data-ttu-id="9cb43-122">\#определенно</span><span class="sxs-lookup"><span data-stu-id="9cb43-122">\#define</span></span>                 | <span data-ttu-id="9cb43-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9cb43-123">Value</span></span> | <span data-ttu-id="9cb43-124">Описание</span><span class="sxs-lookup"><span data-stu-id="9cb43-124">Description</span></span>                  |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="9cb43-125">ДКСФИЛЕЛОАД \_ фромфиле</span><span class="sxs-lookup"><span data-stu-id="9cb43-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="9cb43-126">0x00</span><span class="sxs-lookup"><span data-stu-id="9cb43-126">0x00L</span></span> | <span data-ttu-id="9cb43-127">Загрузить файл из файла.</span><span class="sxs-lookup"><span data-stu-id="9cb43-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="9cb43-128">ДКСФИЛЕЛОАД \_ фромресаурце</span><span class="sxs-lookup"><span data-stu-id="9cb43-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="9cb43-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="9cb43-129">0x01L</span></span> | <span data-ttu-id="9cb43-130">Загрузка файла из ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cb43-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="9cb43-131">ДКСФИЛЕЛОАД \_ фроммемори</span><span class="sxs-lookup"><span data-stu-id="9cb43-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="9cb43-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="9cb43-132">0x02L</span></span> | <span data-ttu-id="9cb43-133">Загрузка файла из памяти.</span><span class="sxs-lookup"><span data-stu-id="9cb43-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="9cb43-134">ДКСФИЛЕЛОАД \_ фромстреам</span><span class="sxs-lookup"><span data-stu-id="9cb43-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="9cb43-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="9cb43-135">0x04L</span></span> | <span data-ttu-id="9cb43-136">Загрузить файл из потока.</span><span class="sxs-lookup"><span data-stu-id="9cb43-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="9cb43-137">ДКСФИЛЕЛОАД \_ фромурл</span><span class="sxs-lookup"><span data-stu-id="9cb43-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="9cb43-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="9cb43-138">0x08L</span></span> | <span data-ttu-id="9cb43-139">Загрузка файла из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="9cb43-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="9cb43-140">Эти \# определения объявляются в дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="9cb43-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cb43-141">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9cb43-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb43-142">Ссылка на X-файл (устаревшая)</span><span class="sxs-lookup"><span data-stu-id="9cb43-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



