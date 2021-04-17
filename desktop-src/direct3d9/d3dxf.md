---
description: Параметры формата файла X, загрузки и сохранения.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691972"
---
# <a name="d3dxf"></a><span data-ttu-id="0ec9b-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="0ec9b-103">D3DXF</span></span>

<span data-ttu-id="0ec9b-104">Параметры формата файла X, загрузки и сохранения.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="0ec9b-105">Форматы файлов</span><span class="sxs-lookup"><span data-stu-id="0ec9b-105">File Formats</span></span>

<span data-ttu-id="0ec9b-106">В следующей таблице указаны типы файловых данных.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="0ec9b-107">\#Определяет формат файла</span><span class="sxs-lookup"><span data-stu-id="0ec9b-107">\#defines for File Format</span></span>     | <span data-ttu-id="0ec9b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0ec9b-108">Value</span></span> | <span data-ttu-id="0ec9b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0ec9b-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec9b-110">\_ \_ Двоичный FILEFORMAT D3DXF</span><span class="sxs-lookup"><span data-stu-id="0ec9b-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="0ec9b-111">0</span><span class="sxs-lookup"><span data-stu-id="0ec9b-111">0</span></span>     | <span data-ttu-id="0ec9b-112">Двоичный файл в старом формате.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-112">Legacy-format binary file.</span></span> <span data-ttu-id="0ec9b-113">См. раздел [Справочник по X (Legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="0ec9b-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="0ec9b-114">D3DXF \_ FILEFORMAT \_ текст</span><span class="sxs-lookup"><span data-stu-id="0ec9b-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="0ec9b-115">1</span><span class="sxs-lookup"><span data-stu-id="0ec9b-115">1</span></span>     | <span data-ttu-id="0ec9b-116">Текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="0ec9b-117">\_Сжатый D3DXF FILEFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="0ec9b-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="0ec9b-118">2</span><span class="sxs-lookup"><span data-stu-id="0ec9b-118">2</span></span>     | <span data-ttu-id="0ec9b-119">Сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-119">Compressed file.</span></span> <span data-ttu-id="0ec9b-120">С этим флагом необходимо также указать двоичный формат или текстовый формат.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="0ec9b-121">Параметры загрузки файлов</span><span class="sxs-lookup"><span data-stu-id="0ec9b-121">File Load Options</span></span>

<span data-ttu-id="0ec9b-122">В следующей таблице указаны параметры загрузки файлов с помощью x:</span><span class="sxs-lookup"><span data-stu-id="0ec9b-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="0ec9b-123">\#определенно</span><span class="sxs-lookup"><span data-stu-id="0ec9b-123">\#define</span></span>                      | <span data-ttu-id="0ec9b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0ec9b-124">Value</span></span> | <span data-ttu-id="0ec9b-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0ec9b-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="0ec9b-126">D3DXF \_ филелоад \_ фромфиле</span><span class="sxs-lookup"><span data-stu-id="0ec9b-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="0ec9b-127">0</span><span class="sxs-lookup"><span data-stu-id="0ec9b-127">0</span></span>     | <span data-ttu-id="0ec9b-128">Загрузка данных из файла.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-128">Load data from a file.</span></span>     |
| <span data-ttu-id="0ec9b-129">D3DXF \_ филелоад \_ фромвфиле</span><span class="sxs-lookup"><span data-stu-id="0ec9b-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="0ec9b-130">1</span><span class="sxs-lookup"><span data-stu-id="0ec9b-130">1</span></span>     | <span data-ttu-id="0ec9b-131">Загрузка данных из файла.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-131">Load data from a file.</span></span>     |
| <span data-ttu-id="0ec9b-132">D3DXF \_ филелоад \_ фромресаурце</span><span class="sxs-lookup"><span data-stu-id="0ec9b-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="0ec9b-133">2</span><span class="sxs-lookup"><span data-stu-id="0ec9b-133">2</span></span>     | <span data-ttu-id="0ec9b-134">Загрузка данных из ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-134">Load data from a resource.</span></span> |
| <span data-ttu-id="0ec9b-135">D3DXF \_ филелоад \_ фроммемори</span><span class="sxs-lookup"><span data-stu-id="0ec9b-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="0ec9b-136">3</span><span class="sxs-lookup"><span data-stu-id="0ec9b-136">3</span></span>     | <span data-ttu-id="0ec9b-137">Загрузка данных из памяти.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="0ec9b-138">Параметры сохранения файла</span><span class="sxs-lookup"><span data-stu-id="0ec9b-138">File Save Options</span></span>

<span data-ttu-id="0ec9b-139">В следующей таблице указаны параметры сохранения и загрузки файлов с расширением x.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="0ec9b-140">\#определенно</span><span class="sxs-lookup"><span data-stu-id="0ec9b-140">\#define</span></span>                 | <span data-ttu-id="0ec9b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="0ec9b-141">Value</span></span> | <span data-ttu-id="0ec9b-142">Описание</span><span class="sxs-lookup"><span data-stu-id="0ec9b-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="0ec9b-143">D3DXF \_ филесаве \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="0ec9b-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="0ec9b-144">0</span><span class="sxs-lookup"><span data-stu-id="0ec9b-144">0</span></span>     | <span data-ttu-id="0ec9b-145">Сохранить в файл.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-145">Save to a file.</span></span>                |
| <span data-ttu-id="0ec9b-146">D3DXF \_ филесаве \_ товфиле</span><span class="sxs-lookup"><span data-stu-id="0ec9b-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="0ec9b-147">1</span><span class="sxs-lookup"><span data-stu-id="0ec9b-147">1</span></span>     | <span data-ttu-id="0ec9b-148">Сохранить в файл расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="0ec9b-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="0ec9b-149">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="0ec9b-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="0ec9b-150">Header</span><span class="sxs-lookup"><span data-stu-id="0ec9b-150">Header</span></span>                   | <span data-ttu-id="0ec9b-151">d3dx9xof. h</span><span class="sxs-lookup"><span data-stu-id="0ec9b-151">d3dx9xof.h</span></span> |
| <span data-ttu-id="0ec9b-152">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="0ec9b-152">Minimum operating system</span></span> | <span data-ttu-id="0ec9b-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0ec9b-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0ec9b-154">См. также</span><span class="sxs-lookup"><span data-stu-id="0ec9b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ec9b-155">Константы файла D3DX X</span><span class="sxs-lookup"><span data-stu-id="0ec9b-155">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="0ec9b-156">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="0ec9b-156">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



