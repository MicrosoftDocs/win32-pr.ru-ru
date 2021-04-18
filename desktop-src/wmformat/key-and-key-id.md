---
title: Ключ и идентификатор ключа
description: Ключ и идентификатор ключа
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Управление цифровыми правами (DRM), ключи
- DRM (Управление цифровыми правами), ключи
- Управление цифровыми правами (DRM), ребенок
- DRM (Управление цифровыми правами), ребенок
- Идентификатор ключа (ребенок)
- Детская (идентификатор ключа)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700541"
---
# <a name="key-and-key-id"></a><span data-ttu-id="a9d59-110">Ключ и идентификатор ключа</span><span class="sxs-lookup"><span data-stu-id="a9d59-110">Key and Key ID</span></span>

<span data-ttu-id="a9d59-111">При упаковке файла используется ключ.</span><span class="sxs-lookup"><span data-stu-id="a9d59-111">When you package a file, you use a key.</span></span> <span data-ttu-id="a9d59-112">Ключ — это фрагмент данных, используемых в алгоритмах шифрования, защищающих содержимое.</span><span class="sxs-lookup"><span data-stu-id="a9d59-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="a9d59-113">Каждый ключ состоит из двух частей: начальное значение лицензионного ключа и идентификатор ключа (часто сокращаются в виде детей).</span><span class="sxs-lookup"><span data-stu-id="a9d59-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="a9d59-114">Идентификатор ключа является общедоступным и хранится в заголовке файла в качестве способа идентификации ключа, необходимого для расшифровки файла.</span><span class="sxs-lookup"><span data-stu-id="a9d59-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="a9d59-115">Начальное значение лицензионного ключа является секретным значением, которое должно совместно использоваться диспетчером содержимого и издателем лицензии.</span><span class="sxs-lookup"><span data-stu-id="a9d59-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="a9d59-116">Идентификатор ключа идентифицирует защищенное содержимое с точки зрения лицензии.</span><span class="sxs-lookup"><span data-stu-id="a9d59-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="a9d59-117">Хотя один и тот же идентификатор ключа можно использовать для нескольких файлов, рекомендуется всегда использовать уникальный идентификатор ключа для каждого элемента защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a9d59-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="a9d59-118">Многие методы, описанные в этой документации, используют строки идентификатора ключа для выбора лицензий.</span><span class="sxs-lookup"><span data-stu-id="a9d59-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="a9d59-119">Эти строки содержат идентификатор ключа, закодированный в Base64.</span><span class="sxs-lookup"><span data-stu-id="a9d59-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9d59-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a9d59-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d59-121">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="a9d59-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




