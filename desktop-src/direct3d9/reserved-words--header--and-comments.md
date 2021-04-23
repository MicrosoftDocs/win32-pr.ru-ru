---
description: В таблице ниже показано, какие слова зарезервированы и не должны использоваться.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Зарезервированные слова, заголовок и комментарии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536818"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="530eb-103">Зарезервированные слова, заголовок и комментарии</span><span class="sxs-lookup"><span data-stu-id="530eb-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="530eb-104">В таблице ниже показано, какие слова зарезервированы и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="530eb-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="530eb-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="530eb-105">ARRAY</span></span>            | <span data-ttu-id="530eb-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="530eb-106">DWORD</span></span>    | <span data-ttu-id="530eb-107">учар</span><span class="sxs-lookup"><span data-stu-id="530eb-107">UCHAR</span></span>     |
| <span data-ttu-id="530eb-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="530eb-108">BINARY</span></span>           | <span data-ttu-id="530eb-109">FLOAT</span><span class="sxs-lookup"><span data-stu-id="530eb-109">FLOAT</span></span>    | <span data-ttu-id="530eb-110">улонглонг</span><span class="sxs-lookup"><span data-stu-id="530eb-110">ULONGLONG</span></span> |
| <span data-ttu-id="530eb-111">ДВОИЧный \_ ресурс</span><span class="sxs-lookup"><span data-stu-id="530eb-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="530eb-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="530eb-112">SDWORD</span></span>   | <span data-ttu-id="530eb-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="530eb-113">UNICODE</span></span>   |
| <span data-ttu-id="530eb-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="530eb-114">CHAR</span></span>             | <span data-ttu-id="530eb-115">STRING</span><span class="sxs-lookup"><span data-stu-id="530eb-115">STRING</span></span>   | <span data-ttu-id="530eb-116">WORD</span><span class="sxs-lookup"><span data-stu-id="530eb-116">WORD</span></span>      |
| <span data-ttu-id="530eb-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="530eb-117">CSTRING</span></span>          | <span data-ttu-id="530eb-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="530eb-118">SWORD</span></span>    |           |
| <span data-ttu-id="530eb-119">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="530eb-119">DOUBLE</span></span>           | <span data-ttu-id="530eb-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="530eb-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="530eb-121">Заголовок переменной длины является принудительным и должен находиться в начале потока данных.</span><span class="sxs-lookup"><span data-stu-id="530eb-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="530eb-122">Заголовок содержит следующие данные.</span><span class="sxs-lookup"><span data-stu-id="530eb-122">The header contains the following data.</span></span>



| <span data-ttu-id="530eb-123">Тип</span><span class="sxs-lookup"><span data-stu-id="530eb-123">Type</span></span>           | <span data-ttu-id="530eb-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="530eb-124">Required</span></span> | <span data-ttu-id="530eb-125">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="530eb-125">Size (in bytes)</span></span> | <span data-ttu-id="530eb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="530eb-126">Value</span></span> | <span data-ttu-id="530eb-127">Описание</span><span class="sxs-lookup"><span data-stu-id="530eb-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="530eb-128">Магическое число</span><span class="sxs-lookup"><span data-stu-id="530eb-128">Magic Number</span></span>   | <span data-ttu-id="530eb-129">x</span><span class="sxs-lookup"><span data-stu-id="530eb-129">x</span></span>        | <span data-ttu-id="530eb-130">4</span><span class="sxs-lookup"><span data-stu-id="530eb-130">4</span></span>               | <span data-ttu-id="530eb-131">ксоф</span><span class="sxs-lookup"><span data-stu-id="530eb-131">xof</span></span>   |                              |
| <span data-ttu-id="530eb-132">Номер версии</span><span class="sxs-lookup"><span data-stu-id="530eb-132">Version Number</span></span> | <span data-ttu-id="530eb-133">x</span><span class="sxs-lookup"><span data-stu-id="530eb-133">x</span></span>        | <span data-ttu-id="530eb-134">2</span><span class="sxs-lookup"><span data-stu-id="530eb-134">2</span></span>               | <span data-ttu-id="530eb-135">03</span><span class="sxs-lookup"><span data-stu-id="530eb-135">03</span></span>    | <span data-ttu-id="530eb-136">Основной номер версии 3</span><span class="sxs-lookup"><span data-stu-id="530eb-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="530eb-137">03</span><span class="sxs-lookup"><span data-stu-id="530eb-137">03</span></span>    | <span data-ttu-id="530eb-138">Дополнительный номер версии 3</span><span class="sxs-lookup"><span data-stu-id="530eb-138">Minor version 3</span></span>              |
| <span data-ttu-id="530eb-139">Тип формата</span><span class="sxs-lookup"><span data-stu-id="530eb-139">Format Type</span></span>    | <span data-ttu-id="530eb-140">x</span><span class="sxs-lookup"><span data-stu-id="530eb-140">x</span></span>        | <span data-ttu-id="530eb-141">4</span><span class="sxs-lookup"><span data-stu-id="530eb-141">4</span></span>               | <span data-ttu-id="530eb-142">txt</span><span class="sxs-lookup"><span data-stu-id="530eb-142">txt</span></span>   | <span data-ttu-id="530eb-143">Текстовый файл</span><span class="sxs-lookup"><span data-stu-id="530eb-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="530eb-144">bin</span><span class="sxs-lookup"><span data-stu-id="530eb-144">bin</span></span>   | <span data-ttu-id="530eb-145">Двоичный файл</span><span class="sxs-lookup"><span data-stu-id="530eb-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="530eb-146">тзип</span><span class="sxs-lookup"><span data-stu-id="530eb-146">tzip</span></span>  | <span data-ttu-id="530eb-147">Сжатый текстовый файл MSZip</span><span class="sxs-lookup"><span data-stu-id="530eb-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="530eb-148">бзип</span><span class="sxs-lookup"><span data-stu-id="530eb-148">bzip</span></span>  | <span data-ttu-id="530eb-149">Сжатый двоичный файл MSZip</span><span class="sxs-lookup"><span data-stu-id="530eb-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="530eb-150">Размер float</span><span class="sxs-lookup"><span data-stu-id="530eb-150">Float Size</span></span>     | <span data-ttu-id="530eb-151">x</span><span class="sxs-lookup"><span data-stu-id="530eb-151">x</span></span>        | <span data-ttu-id="530eb-152">0064</span><span class="sxs-lookup"><span data-stu-id="530eb-152">0064</span></span>            |       | <span data-ttu-id="530eb-153">64-разрядное число с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="530eb-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="530eb-154">x</span><span class="sxs-lookup"><span data-stu-id="530eb-154">x</span></span>        | <span data-ttu-id="530eb-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="530eb-155">"0032"</span></span>          |       | <span data-ttu-id="530eb-156">32-разрядное число с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="530eb-156">32-bit floats</span></span>                |



 

<span data-ttu-id="530eb-157">Значения в таблице разделяются кавычками, чтобы привлечь внимание к числу символов в каждом значении.</span><span class="sxs-lookup"><span data-stu-id="530eb-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="530eb-158">В 4 байтах содержится четыре символа, длина которых состоит из двух символов.</span><span class="sxs-lookup"><span data-stu-id="530eb-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="530eb-159">Комментарии применимы только в текстовых файлах.</span><span class="sxs-lookup"><span data-stu-id="530eb-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="530eb-160">Комментарии могут находиться в любом месте потока данных.</span><span class="sxs-lookup"><span data-stu-id="530eb-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="530eb-161">Комментарий начинается с двойных косых черт в стиле C++ (//) или знака решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="530eb-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="530eb-162">Комментарий выполняется до следующей новой строки.</span><span class="sxs-lookup"><span data-stu-id="530eb-162">The comment runs to the next new line.</span></span> <span data-ttu-id="530eb-163">В следующем примере показаны допустимые комментарии.</span><span class="sxs-lookup"><span data-stu-id="530eb-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="530eb-164">См. также</span><span class="sxs-lookup"><span data-stu-id="530eb-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="530eb-165">Кодировка текста</span><span class="sxs-lookup"><span data-stu-id="530eb-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



