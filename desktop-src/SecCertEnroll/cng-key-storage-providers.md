---
description: 'В отличие от криптографических API (CryptoAPI), API шифрования: следующее поколение (CNG) отделяет поставщиков служб шифрования от поставщиков хранилища ключей (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Поставщики хранилища ключей CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423670"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="4adf8-103">Поставщики хранилища ключей CNG</span><span class="sxs-lookup"><span data-stu-id="4adf8-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="4adf8-104">В отличие от криптографических API (CryptoAPI), API шифрования: следующее поколение (CNG) отделяет поставщиков служб шифрования от поставщиков хранилища ключей (KSP).</span><span class="sxs-lookup"><span data-stu-id="4adf8-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="4adf8-105">KSP можно использовать для создания, удаления, экспорта, импорта, открытия и сохранения ключей.</span><span class="sxs-lookup"><span data-stu-id="4adf8-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="4adf8-106">В зависимости от реализации они также могут использоваться для асимметричного шифрования, секретного соглашения и подписывания.</span><span class="sxs-lookup"><span data-stu-id="4adf8-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="4adf8-107">Корпорация Майкрософт устанавливает следующие KSP, начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4adf8-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="4adf8-108">Поставщики могут создавать и устанавливать другие поставщики.</span><span class="sxs-lookup"><span data-stu-id="4adf8-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="4adf8-109">Поставщик хранилища ключей программного обеспечения Майкрософт</span><span class="sxs-lookup"><span data-stu-id="4adf8-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="4adf8-110">Поддерживает создание и хранение ключей программного обеспечения, а также следующие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="4adf8-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="4adf8-111">Алгоритм</span><span class="sxs-lookup"><span data-stu-id="4adf8-111">Algorithm</span></span>                                          | <span data-ttu-id="4adf8-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="4adf8-112">Purpose</span></span>                           | <span data-ttu-id="4adf8-113">Длина ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4adf8-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="4adf8-114">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="4adf8-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="4adf8-115">Секретное соглашение и обмен ключами</span><span class="sxs-lookup"><span data-stu-id="4adf8-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="4adf8-116">от 512 до 4096 в 64-разрядных шагах</span><span class="sxs-lookup"><span data-stu-id="4adf8-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="4adf8-117">Алгоритм цифровых подписей (DSA)</span><span class="sxs-lookup"><span data-stu-id="4adf8-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="4adf8-118">Сигнатуры</span><span class="sxs-lookup"><span data-stu-id="4adf8-118">Signatures</span></span>                        | <span data-ttu-id="4adf8-119">от 512 до 1024 в 64-разрядных шагах</span><span class="sxs-lookup"><span data-stu-id="4adf8-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="4adf8-120">Diffie-Hellman на эллиптических кривых (ECDH)</span><span class="sxs-lookup"><span data-stu-id="4adf8-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="4adf8-121">Секретное соглашение и обмен ключами</span><span class="sxs-lookup"><span data-stu-id="4adf8-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="4adf8-122">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="4adf8-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="4adf8-123">Алгоритм цифровых подписей на основе эллиптических кривых (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="4adf8-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="4adf8-124">Сигнатуры</span><span class="sxs-lookup"><span data-stu-id="4adf8-124">Signatures</span></span>                        | <span data-ttu-id="4adf8-125">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="4adf8-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="4adf8-126">RSA</span><span class="sxs-lookup"><span data-stu-id="4adf8-126">RSA</span></span>                                                | <span data-ttu-id="4adf8-127">Асимметричное шифрование и подписывание</span><span class="sxs-lookup"><span data-stu-id="4adf8-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="4adf8-128">от 512 до 16384 в 64-разрядных шагах</span><span class="sxs-lookup"><span data-stu-id="4adf8-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="4adf8-129">Поставщик хранилища ключей смарт-карт (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4adf8-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="4adf8-130">Поддерживает создание и хранение ключей смарт-карт, а также следующие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="4adf8-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="4adf8-131">Алгоритм</span><span class="sxs-lookup"><span data-stu-id="4adf8-131">Algorithm</span></span>                                          | <span data-ttu-id="4adf8-132">Назначение</span><span class="sxs-lookup"><span data-stu-id="4adf8-132">Purpose</span></span>                           | <span data-ttu-id="4adf8-133">Длина ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4adf8-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="4adf8-134">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="4adf8-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="4adf8-135">Секретное соглашение и обмен ключами</span><span class="sxs-lookup"><span data-stu-id="4adf8-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="4adf8-136">от 512 до 4096 в 64-разрядных шагах</span><span class="sxs-lookup"><span data-stu-id="4adf8-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="4adf8-137">Diffie-Hellman на эллиптических кривых (ECDH)</span><span class="sxs-lookup"><span data-stu-id="4adf8-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="4adf8-138">Секретное соглашение и обмен ключами</span><span class="sxs-lookup"><span data-stu-id="4adf8-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="4adf8-139">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="4adf8-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="4adf8-140">Алгоритм цифровых подписей на основе эллиптических кривых (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="4adf8-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="4adf8-141">Сигнатуры</span><span class="sxs-lookup"><span data-stu-id="4adf8-141">Signatures</span></span>                        | <span data-ttu-id="4adf8-142">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="4adf8-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="4adf8-143">RSA</span><span class="sxs-lookup"><span data-stu-id="4adf8-143">RSA</span></span>                                                | <span data-ttu-id="4adf8-144">Асимметричное шифрование и подписывание</span><span class="sxs-lookup"><span data-stu-id="4adf8-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="4adf8-145">от 512 до 16384 в 64-разрядных шагах</span><span class="sxs-lookup"><span data-stu-id="4adf8-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4adf8-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4adf8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adf8-147">**Идентификаторы алгоритма CNG**</span><span class="sxs-lookup"><span data-stu-id="4adf8-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="4adf8-148">Функции хранилища ключей CNG</span><span class="sxs-lookup"><span data-stu-id="4adf8-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="4adf8-149">Общие сведения о поставщиках служб шифрования</span><span class="sxs-lookup"><span data-stu-id="4adf8-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
