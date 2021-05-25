---
description: В таблице ниже показано, какие слова зарезервированы и не должны использоваться.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Зарезервированные слова, заголовок и комментарии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343659"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="15e83-103">Зарезервированные слова, заголовок и комментарии</span><span class="sxs-lookup"><span data-stu-id="15e83-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="15e83-104">В таблице ниже показано, какие слова зарезервированы и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="15e83-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="15e83-105">Зарезервированные слова</span><span class="sxs-lookup"><span data-stu-id="15e83-105">Reserved Words</span></span> | <span data-ttu-id="15e83-106">Зарезервированные слова</span><span class="sxs-lookup"><span data-stu-id="15e83-106">Reserved Words</span></span> | <span data-ttu-id="15e83-107">Зарезервированные слова</span><span class="sxs-lookup"><span data-stu-id="15e83-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="15e83-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="15e83-108">ARRAY</span></span>            | <span data-ttu-id="15e83-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="15e83-109">DWORD</span></span>    | <span data-ttu-id="15e83-110">учар</span><span class="sxs-lookup"><span data-stu-id="15e83-110">UCHAR</span></span>     |
| <span data-ttu-id="15e83-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="15e83-111">BINARY</span></span>           | <span data-ttu-id="15e83-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="15e83-112">FLOAT</span></span>    | <span data-ttu-id="15e83-113">улонглонг</span><span class="sxs-lookup"><span data-stu-id="15e83-113">ULONGLONG</span></span> |
| <span data-ttu-id="15e83-114">ДВОИЧный \_ ресурс</span><span class="sxs-lookup"><span data-stu-id="15e83-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="15e83-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="15e83-115">SDWORD</span></span>   | <span data-ttu-id="15e83-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="15e83-116">UNICODE</span></span>   |
| <span data-ttu-id="15e83-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="15e83-117">CHAR</span></span>             | <span data-ttu-id="15e83-118">STRING</span><span class="sxs-lookup"><span data-stu-id="15e83-118">STRING</span></span>   | <span data-ttu-id="15e83-119">WORD</span><span class="sxs-lookup"><span data-stu-id="15e83-119">WORD</span></span>      |
| <span data-ttu-id="15e83-120">CSTRING</span><span class="sxs-lookup"><span data-stu-id="15e83-120">CSTRING</span></span>          | <span data-ttu-id="15e83-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="15e83-121">SWORD</span></span>    |           |
| <span data-ttu-id="15e83-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="15e83-122">DOUBLE</span></span>           | <span data-ttu-id="15e83-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="15e83-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="15e83-124">Заголовок переменной длины является принудительным и должен находиться в начале потока данных.</span><span class="sxs-lookup"><span data-stu-id="15e83-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="15e83-125">Заголовок содержит следующие данные.</span><span class="sxs-lookup"><span data-stu-id="15e83-125">The header contains the following data.</span></span>



| <span data-ttu-id="15e83-126">Тип</span><span class="sxs-lookup"><span data-stu-id="15e83-126">Type</span></span>           | <span data-ttu-id="15e83-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="15e83-127">Required</span></span> | <span data-ttu-id="15e83-128">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="15e83-128">Size (in bytes)</span></span> | <span data-ttu-id="15e83-129">Значение</span><span class="sxs-lookup"><span data-stu-id="15e83-129">Value</span></span> | <span data-ttu-id="15e83-130">Описание</span><span class="sxs-lookup"><span data-stu-id="15e83-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="15e83-131">Магическое число</span><span class="sxs-lookup"><span data-stu-id="15e83-131">Magic Number</span></span>   | <span data-ttu-id="15e83-132">x</span><span class="sxs-lookup"><span data-stu-id="15e83-132">x</span></span>        | <span data-ttu-id="15e83-133">4</span><span class="sxs-lookup"><span data-stu-id="15e83-133">4</span></span>               | <span data-ttu-id="15e83-134">ксоф</span><span class="sxs-lookup"><span data-stu-id="15e83-134">xof</span></span>   |                              |
| <span data-ttu-id="15e83-135">Номер версии</span><span class="sxs-lookup"><span data-stu-id="15e83-135">Version Number</span></span> | <span data-ttu-id="15e83-136">x</span><span class="sxs-lookup"><span data-stu-id="15e83-136">x</span></span>        | <span data-ttu-id="15e83-137">2</span><span class="sxs-lookup"><span data-stu-id="15e83-137">2</span></span>               | <span data-ttu-id="15e83-138">03</span><span class="sxs-lookup"><span data-stu-id="15e83-138">03</span></span>    | <span data-ttu-id="15e83-139">Основной номер версии 3</span><span class="sxs-lookup"><span data-stu-id="15e83-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="15e83-140">03</span><span class="sxs-lookup"><span data-stu-id="15e83-140">03</span></span>    | <span data-ttu-id="15e83-141">Дополнительный номер версии 3</span><span class="sxs-lookup"><span data-stu-id="15e83-141">Minor version 3</span></span>              |
| <span data-ttu-id="15e83-142">Тип формата</span><span class="sxs-lookup"><span data-stu-id="15e83-142">Format Type</span></span>    | <span data-ttu-id="15e83-143">x</span><span class="sxs-lookup"><span data-stu-id="15e83-143">x</span></span>        | <span data-ttu-id="15e83-144">4</span><span class="sxs-lookup"><span data-stu-id="15e83-144">4</span></span>               | <span data-ttu-id="15e83-145">txt</span><span class="sxs-lookup"><span data-stu-id="15e83-145">txt</span></span>   | <span data-ttu-id="15e83-146">Текстовый файл</span><span class="sxs-lookup"><span data-stu-id="15e83-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="15e83-147">bin</span><span class="sxs-lookup"><span data-stu-id="15e83-147">bin</span></span>   | <span data-ttu-id="15e83-148">Двоичный файл</span><span class="sxs-lookup"><span data-stu-id="15e83-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="15e83-149">тзип</span><span class="sxs-lookup"><span data-stu-id="15e83-149">tzip</span></span>  | <span data-ttu-id="15e83-150">Сжатый текстовый файл MSZip</span><span class="sxs-lookup"><span data-stu-id="15e83-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="15e83-151">бзип</span><span class="sxs-lookup"><span data-stu-id="15e83-151">bzip</span></span>  | <span data-ttu-id="15e83-152">Сжатый двоичный файл MSZip</span><span class="sxs-lookup"><span data-stu-id="15e83-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="15e83-153">Размер float</span><span class="sxs-lookup"><span data-stu-id="15e83-153">Float Size</span></span>     | <span data-ttu-id="15e83-154">x</span><span class="sxs-lookup"><span data-stu-id="15e83-154">x</span></span>        | <span data-ttu-id="15e83-155">0064</span><span class="sxs-lookup"><span data-stu-id="15e83-155">0064</span></span>            |       | <span data-ttu-id="15e83-156">64-разрядное число с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="15e83-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="15e83-157">x</span><span class="sxs-lookup"><span data-stu-id="15e83-157">x</span></span>        | <span data-ttu-id="15e83-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="15e83-158">"0032"</span></span>          |       | <span data-ttu-id="15e83-159">32-разрядное число с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="15e83-159">32-bit floats</span></span>                |



 

<span data-ttu-id="15e83-160">Значения в таблице разделяются кавычками, чтобы привлечь внимание к числу символов в каждом значении.</span><span class="sxs-lookup"><span data-stu-id="15e83-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="15e83-161">В 4 байтах содержится четыре символа, длина которых состоит из двух символов.</span><span class="sxs-lookup"><span data-stu-id="15e83-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="15e83-162">Комментарии применимы только в текстовых файлах.</span><span class="sxs-lookup"><span data-stu-id="15e83-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="15e83-163">Комментарии могут находиться в любом месте потока данных.</span><span class="sxs-lookup"><span data-stu-id="15e83-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="15e83-164">Комментарий начинается с двойных косых черт в стиле C++ (//) или знака решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="15e83-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="15e83-165">Комментарий выполняется до следующей новой строки.</span><span class="sxs-lookup"><span data-stu-id="15e83-165">The comment runs to the next new line.</span></span> <span data-ttu-id="15e83-166">В следующем примере показаны допустимые комментарии.</span><span class="sxs-lookup"><span data-stu-id="15e83-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="15e83-167">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="15e83-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15e83-168">Кодировка текста</span><span class="sxs-lookup"><span data-stu-id="15e83-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



