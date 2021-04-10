---
description: Шифрование — это процесс преобразования текстовых данных (открытого текста) в то, что кажется случайным и бессмысленным (зашифрованным текстом). Расшифровка — это процесс преобразования зашифрованного текста обратно в обычный текст.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Шифрование и расшифровка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144464"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="a40ae-104">Шифрование и расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="a40ae-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="a40ae-105">Шифрование — это процесс преобразования текстовых данных ([*открытого*](../secgloss/p-gly.md)текста) в то, что кажется случайным и бессмысленным ([*зашифрованным*](../secgloss/c-gly.md)текстом).</span><span class="sxs-lookup"><span data-stu-id="a40ae-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="a40ae-106">Расшифровка — это процесс преобразования зашифрованного текста обратно в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="a40ae-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="a40ae-107">Для шифрования более чем небольшого объема данных используется [*симметричное шифрование*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a40ae-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="a40ae-108">[*Симметричный ключ*](../secgloss/s-gly.md) используется в процессах шифрования и расшифровки.</span><span class="sxs-lookup"><span data-stu-id="a40ae-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="a40ae-109">Для расшифровки определенного фрагмента зашифрованного текста необходимо использовать ключ, который использовался для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="a40ae-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="a40ae-110">Цель каждого алгоритма шифрования состоит в том, чтобы сделать его как можно более сложным для расшифровки сгенерированного зашифрованного текста без использования ключа.</span><span class="sxs-lookup"><span data-stu-id="a40ae-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="a40ae-111">Если используется действительно хороший алгоритм шифрования, не существует методики, которая значительно лучше, чем методичное, пытаясь каждый возможного ключа.</span><span class="sxs-lookup"><span data-stu-id="a40ae-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="a40ae-112">Для такого алгоритма чем длиннее ключ, тем сложнее расшифровывает фрагмент зашифрованного текста без использования ключа.</span><span class="sxs-lookup"><span data-stu-id="a40ae-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="a40ae-113">Трудно определить качество алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="a40ae-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="a40ae-114">Алгоритмы, которые выглядят в расчете, иногда пребывают легко прерывать, учитывая правильную атаку.</span><span class="sxs-lookup"><span data-stu-id="a40ae-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="a40ae-115">При выборе алгоритма шифрования рекомендуется выбрать тот, который уже использовался в течение нескольких лет и успешно вызвал все атаки.</span><span class="sxs-lookup"><span data-stu-id="a40ae-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="a40ae-116">Дополнительные сведения см. в разделе [функции шифрования и расшифровки данных](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a40ae-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
