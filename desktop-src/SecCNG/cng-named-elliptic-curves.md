---
description: Начиная с Windows 10 CNG поддерживает следующие именованные эллиптические кривые (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Именованные эллиптические кривые CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896741"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="4a313-103">CNG с именем "эллиптические кривые"</span><span class="sxs-lookup"><span data-stu-id="4a313-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="4a313-104">Начиная с Windows 10 CNG поддерживает следующие именованные эллиптические кривые (ANSI X 9.62, X 9.63, FIPS 186-2).</span><span class="sxs-lookup"><span data-stu-id="4a313-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="4a313-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**\_ \_ Кривая ECC BCRYPT \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-106">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-106">Requirement</span></span> | <span data-ttu-id="4a313-107">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="4a313-108">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-108">Name</span></span>              | <span data-ttu-id="4a313-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="4a313-109">curve25519</span></span>                                                  |
| <span data-ttu-id="4a313-110">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-110">Standard</span></span>          | [<span data-ttu-id="4a313-111">Кривая 25519</span><span class="sxs-lookup"><span data-stu-id="4a313-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="4a313-112">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-112">Key size (bits)</span></span>   | <span data-ttu-id="4a313-113">255</span><span class="sxs-lookup"><span data-stu-id="4a313-113">255</span></span>                                                         |
| <span data-ttu-id="4a313-114">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="4a313-115">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-115">Object identifier</span></span> | <span data-ttu-id="4a313-116">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-116">None</span></span>                                                        |



 

<span data-ttu-id="4a313-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_ \_ BRAINPOOLP160R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-118">Requirement</span></span> | <span data-ttu-id="4a313-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-120">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-120">Name</span></span>              | <span data-ttu-id="4a313-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="4a313-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-122">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-122">Standard</span></span>          | [<span data-ttu-id="4a313-123">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-124">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-124">Key size (bits)</span></span>   | <span data-ttu-id="4a313-125">160</span><span class="sxs-lookup"><span data-stu-id="4a313-125">160</span></span>                                                                                                               |
| <span data-ttu-id="4a313-126">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-126">TLS capable</span></span>       | <span data-ttu-id="4a313-127">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-127">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-128">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-128">Object identifier</span></span> | <span data-ttu-id="4a313-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="4a313-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="4a313-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-131">Requirement</span></span> | <span data-ttu-id="4a313-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-133">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-133">Name</span></span>              | <span data-ttu-id="4a313-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="4a313-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-135">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-135">Standard</span></span>          | [<span data-ttu-id="4a313-136">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-137">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-137">Key size (bits)</span></span>   | <span data-ttu-id="4a313-138">160</span><span class="sxs-lookup"><span data-stu-id="4a313-138">160</span></span>                                                                                                               |
| <span data-ttu-id="4a313-139">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-139">TLS capable</span></span>       | <span data-ttu-id="4a313-140">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-140">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-141">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-141">Object identifier</span></span> | <span data-ttu-id="4a313-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="4a313-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="4a313-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_ \_ BRAINPOOLP192R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-144">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-144">Requirement</span></span> | <span data-ttu-id="4a313-145">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-146">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-146">Name</span></span>              | <span data-ttu-id="4a313-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="4a313-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-148">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-148">Standard</span></span>          | [<span data-ttu-id="4a313-149">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-150">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-150">Key size (bits)</span></span>   | <span data-ttu-id="4a313-151">192</span><span class="sxs-lookup"><span data-stu-id="4a313-151">192</span></span>                                                                                                               |
| <span data-ttu-id="4a313-152">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-152">TLS capable</span></span>       | <span data-ttu-id="4a313-153">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-153">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-154">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-154">Object identifier</span></span> | <span data-ttu-id="4a313-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="4a313-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="4a313-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_ \_ BRAINPOOLP192T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-157">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-157">Requirement</span></span> | <span data-ttu-id="4a313-158">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-159">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-159">Name</span></span>              | <span data-ttu-id="4a313-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="4a313-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-161">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-161">Standard</span></span>          | [<span data-ttu-id="4a313-162">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-163">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-163">Key size (bits)</span></span>   | <span data-ttu-id="4a313-164">192</span><span class="sxs-lookup"><span data-stu-id="4a313-164">192</span></span>                                                                                                               |
| <span data-ttu-id="4a313-165">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-165">TLS capable</span></span>       | <span data-ttu-id="4a313-166">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-166">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-167">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-167">Object identifier</span></span> | <span data-ttu-id="4a313-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="4a313-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="4a313-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_ \_ BRAINPOOLP224R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-170">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-170">Requirement</span></span> | <span data-ttu-id="4a313-171">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-172">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-172">Name</span></span>              | <span data-ttu-id="4a313-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="4a313-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-174">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-174">Standard</span></span>          | [<span data-ttu-id="4a313-175">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-176">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-176">Key size (bits)</span></span>   | <span data-ttu-id="4a313-177">224</span><span class="sxs-lookup"><span data-stu-id="4a313-177">224</span></span>                                                                                                               |
| <span data-ttu-id="4a313-178">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-178">TLS capable</span></span>       | <span data-ttu-id="4a313-179">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-179">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-180">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-180">Object identifier</span></span> | <span data-ttu-id="4a313-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="4a313-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="4a313-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_ \_ BRAINPOOLP224T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-183">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-183">Requirement</span></span> | <span data-ttu-id="4a313-184">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-185">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-185">Name</span></span>              | <span data-ttu-id="4a313-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="4a313-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-187">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-187">Standard</span></span>          | [<span data-ttu-id="4a313-188">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-189">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-189">Key size (bits)</span></span>   | <span data-ttu-id="4a313-190">224</span><span class="sxs-lookup"><span data-stu-id="4a313-190">224</span></span>                                                                                                               |
| <span data-ttu-id="4a313-191">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-191">TLS capable</span></span>       | <span data-ttu-id="4a313-192">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-192">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-193">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-193">Object identifier</span></span> | <span data-ttu-id="4a313-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="4a313-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="4a313-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_ \_ BRAINPOOLP256R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-196">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-196">Requirement</span></span> | <span data-ttu-id="4a313-197">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-198">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-198">Name</span></span>              | <span data-ttu-id="4a313-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="4a313-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-200">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-200">Standard</span></span>          | [<span data-ttu-id="4a313-201">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-202">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-202">Key size (bits)</span></span>   | <span data-ttu-id="4a313-203">256</span><span class="sxs-lookup"><span data-stu-id="4a313-203">256</span></span>                                                                                                               |
| <span data-ttu-id="4a313-204">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-204">TLS capable</span></span>       | <span data-ttu-id="4a313-205">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="4a313-206">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-206">Object identifier</span></span> | <span data-ttu-id="4a313-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="4a313-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="4a313-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_ \_ BRAINPOOLP256T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-209">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-209">Requirement</span></span> | <span data-ttu-id="4a313-210">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-211">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-211">Name</span></span>              | <span data-ttu-id="4a313-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="4a313-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-213">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-213">Standard</span></span>          | [<span data-ttu-id="4a313-214">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-215">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-215">Key size (bits)</span></span>   | <span data-ttu-id="4a313-216">256</span><span class="sxs-lookup"><span data-stu-id="4a313-216">256</span></span>                                                                                                               |
| <span data-ttu-id="4a313-217">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-217">TLS capable</span></span>       | <span data-ttu-id="4a313-218">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-218">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-219">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-219">Object identifier</span></span> | <span data-ttu-id="4a313-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="4a313-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="4a313-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_ \_ BRAINPOOLP320R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-222">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-222">Requirement</span></span> | <span data-ttu-id="4a313-223">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-224">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-224">Name</span></span>              | <span data-ttu-id="4a313-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="4a313-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-226">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-226">Standard</span></span>          | [<span data-ttu-id="4a313-227">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-228">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-228">Key size (bits)</span></span>   | <span data-ttu-id="4a313-229">320</span><span class="sxs-lookup"><span data-stu-id="4a313-229">320</span></span>                                                                                                               |
| <span data-ttu-id="4a313-230">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-230">TLS capable</span></span>       | <span data-ttu-id="4a313-231">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-231">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-232">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-232">Object identifier</span></span> | <span data-ttu-id="4a313-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="4a313-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="4a313-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**\_ \_ Кривая ECC BCRYPT \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-235">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-235">Requirement</span></span> | <span data-ttu-id="4a313-236">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-237">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-237">Name</span></span>              | <span data-ttu-id="4a313-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="4a313-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-239">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-239">Standard</span></span>          | [<span data-ttu-id="4a313-240">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-241">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-241">Key size (bits)</span></span>   | <span data-ttu-id="4a313-242">320</span><span class="sxs-lookup"><span data-stu-id="4a313-242">320</span></span>                                                                                                               |
| <span data-ttu-id="4a313-243">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-243">TLS capable</span></span>       | <span data-ttu-id="4a313-244">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-244">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-245">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-245">Object identifier</span></span> | <span data-ttu-id="4a313-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="4a313-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="4a313-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-248">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-248">Requirement</span></span> | <span data-ttu-id="4a313-249">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-250">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-250">Name</span></span>              | <span data-ttu-id="4a313-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="4a313-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-252">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-252">Standard</span></span>          | [<span data-ttu-id="4a313-253">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-254">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-254">Key size (bits)</span></span>   | <span data-ttu-id="4a313-255">384</span><span class="sxs-lookup"><span data-stu-id="4a313-255">384</span></span>                                                                                                               |
| <span data-ttu-id="4a313-256">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-256">TLS capable</span></span>       | <span data-ttu-id="4a313-257">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="4a313-258">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-258">Object identifier</span></span> | <span data-ttu-id="4a313-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="4a313-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="4a313-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_ \_ BRAINPOOLP384T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-261">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-261">Requirement</span></span> | <span data-ttu-id="4a313-262">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-263">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-263">Name</span></span>              | <span data-ttu-id="4a313-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="4a313-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-265">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-265">Standard</span></span>          | [<span data-ttu-id="4a313-266">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-267">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-267">Key size (bits)</span></span>   | <span data-ttu-id="4a313-268">384</span><span class="sxs-lookup"><span data-stu-id="4a313-268">384</span></span>                                                                                                               |
| <span data-ttu-id="4a313-269">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-269">TLS capable</span></span>       | <span data-ttu-id="4a313-270">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-270">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-271">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-271">Object identifier</span></span> | <span data-ttu-id="4a313-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="4a313-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="4a313-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_ \_ BRAINPOOLP512R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-274">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-274">Requirement</span></span> | <span data-ttu-id="4a313-275">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-276">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-276">Name</span></span>              | <span data-ttu-id="4a313-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="4a313-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-278">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-278">Standard</span></span>          | [<span data-ttu-id="4a313-279">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-280">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-280">Key size (bits)</span></span>   | <span data-ttu-id="4a313-281">512</span><span class="sxs-lookup"><span data-stu-id="4a313-281">512</span></span>                                                                                                               |
| <span data-ttu-id="4a313-282">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-282">TLS capable</span></span>       | <span data-ttu-id="4a313-283">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="4a313-284">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-284">Object identifier</span></span> | <span data-ttu-id="4a313-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="4a313-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="4a313-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_ \_ BRAINPOOLP512T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-287">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-287">Requirement</span></span> | <span data-ttu-id="4a313-288">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-289">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-289">Name</span></span>              | <span data-ttu-id="4a313-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="4a313-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="4a313-291">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-291">Standard</span></span>          | [<span data-ttu-id="4a313-292">Генерирование кривых ECC Brainpool Standard и создание кривых</span><span class="sxs-lookup"><span data-stu-id="4a313-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="4a313-293">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-293">Key size (bits)</span></span>   | <span data-ttu-id="4a313-294">512</span><span class="sxs-lookup"><span data-stu-id="4a313-294">512</span></span>                                                                                                               |
| <span data-ttu-id="4a313-295">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-295">TLS capable</span></span>       | <span data-ttu-id="4a313-296">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-296">No</span></span>                                                                                                                |
| <span data-ttu-id="4a313-297">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-297">Object identifier</span></span> | <span data-ttu-id="4a313-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="4a313-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="4a313-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-300">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-300">Requirement</span></span> | <span data-ttu-id="4a313-301">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="4a313-302">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-302">Name</span></span>              | <span data-ttu-id="4a313-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="4a313-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="4a313-304">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-304">Standard</span></span>          | <span data-ttu-id="4a313-305">Китайский национальный стандарт для беспроводных локальных сетей (GB 15629.11-2003)</span><span class="sxs-lookup"><span data-stu-id="4a313-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="4a313-306">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-306">Key size (bits)</span></span>   | <span data-ttu-id="4a313-307">192</span><span class="sxs-lookup"><span data-stu-id="4a313-307">192</span></span>                                                            |
| <span data-ttu-id="4a313-308">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-308">TLS capable</span></span>       | <span data-ttu-id="4a313-309">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-309">No</span></span>                                                             |
| <span data-ttu-id="4a313-310">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-310">Object identifier</span></span> | <span data-ttu-id="4a313-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="4a313-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="4a313-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_ \_ NISTP192 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-313">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-313">Requirement</span></span> | <span data-ttu-id="4a313-314">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-315">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-315">Name</span></span>              | <span data-ttu-id="4a313-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="4a313-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="4a313-317">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-317">Standard</span></span>          | [<span data-ttu-id="4a313-318">Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений</span><span class="sxs-lookup"><span data-stu-id="4a313-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="4a313-319">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-319">Key size (bits)</span></span>   | <span data-ttu-id="4a313-320">192</span><span class="sxs-lookup"><span data-stu-id="4a313-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-321">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-321">TLS capable</span></span>       | <span data-ttu-id="4a313-322">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-323">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-323">Object identifier</span></span> | <span data-ttu-id="4a313-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="4a313-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="4a313-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-326">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-326">Requirement</span></span> | <span data-ttu-id="4a313-327">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-328">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-328">Name</span></span>              | <span data-ttu-id="4a313-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="4a313-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="4a313-330">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-330">Standard</span></span>          | [<span data-ttu-id="4a313-331">Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений</span><span class="sxs-lookup"><span data-stu-id="4a313-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="4a313-332">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-332">Key size (bits)</span></span>   | <span data-ttu-id="4a313-333">224</span><span class="sxs-lookup"><span data-stu-id="4a313-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-334">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-334">TLS capable</span></span>       | <span data-ttu-id="4a313-335">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-336">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-336">Object identifier</span></span> | <span data-ttu-id="4a313-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="4a313-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="4a313-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_ \_ NISTP256 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-339">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-339">Requirement</span></span> | <span data-ttu-id="4a313-340">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-341">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-341">Name</span></span>              | <span data-ttu-id="4a313-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="4a313-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="4a313-343">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-343">Standard</span></span>          | [<span data-ttu-id="4a313-344">Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений</span><span class="sxs-lookup"><span data-stu-id="4a313-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="4a313-345">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-345">Key size (bits)</span></span>   | <span data-ttu-id="4a313-346">256</span><span class="sxs-lookup"><span data-stu-id="4a313-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-347">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-347">TLS capable</span></span>       | <span data-ttu-id="4a313-348">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-349">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-349">Object identifier</span></span> | <span data-ttu-id="4a313-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="4a313-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="4a313-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-352">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-352">Requirement</span></span> | <span data-ttu-id="4a313-353">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-354">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-354">Name</span></span>              | <span data-ttu-id="4a313-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="4a313-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="4a313-356">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-356">Standard</span></span>          | [<span data-ttu-id="4a313-357">Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений</span><span class="sxs-lookup"><span data-stu-id="4a313-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="4a313-358">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-358">Key size (bits)</span></span>   | <span data-ttu-id="4a313-359">384</span><span class="sxs-lookup"><span data-stu-id="4a313-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-360">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-360">TLS capable</span></span>       | <span data-ttu-id="4a313-361">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-362">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-362">Object identifier</span></span> | <span data-ttu-id="4a313-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="4a313-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="4a313-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_ \_ NISTP521 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-365">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-365">Requirement</span></span> | <span data-ttu-id="4a313-366">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-367">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-367">Name</span></span>              | <span data-ttu-id="4a313-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="4a313-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="4a313-369">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-369">Standard</span></span>          | [<span data-ttu-id="4a313-370">Рекомендуемые эллиптические кривые для федерального использования правительственных учреждений</span><span class="sxs-lookup"><span data-stu-id="4a313-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="4a313-371">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-371">Key size (bits)</span></span>   | <span data-ttu-id="4a313-372">521</span><span class="sxs-lookup"><span data-stu-id="4a313-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-373">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-373">TLS capable</span></span>       | <span data-ttu-id="4a313-374">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="4a313-375">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-375">Object identifier</span></span> | <span data-ttu-id="4a313-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="4a313-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="4a313-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-378">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-378">Requirement</span></span> | <span data-ttu-id="4a313-379">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-380">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-380">Name</span></span>              | <span data-ttu-id="4a313-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="4a313-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="4a313-382">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-382">Standard</span></span>          | [<span data-ttu-id="4a313-383">Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб</span><span class="sxs-lookup"><span data-stu-id="4a313-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="4a313-384">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-384">Key size (bits)</span></span>   | <span data-ttu-id="4a313-385">256</span><span class="sxs-lookup"><span data-stu-id="4a313-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="4a313-386">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-386">TLS capable</span></span>       | <span data-ttu-id="4a313-387">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="4a313-388">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-388">Object identifier</span></span> | <span data-ttu-id="4a313-389">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="4a313-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-391">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-391">Requirement</span></span> | <span data-ttu-id="4a313-392">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-393">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-393">Name</span></span>              | <span data-ttu-id="4a313-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="4a313-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="4a313-395">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-395">Standard</span></span>          | [<span data-ttu-id="4a313-396">Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб</span><span class="sxs-lookup"><span data-stu-id="4a313-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="4a313-397">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-397">Key size (bits)</span></span>   | <span data-ttu-id="4a313-398">384</span><span class="sxs-lookup"><span data-stu-id="4a313-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="4a313-399">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-399">TLS capable</span></span>       | <span data-ttu-id="4a313-400">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="4a313-401">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-401">Object identifier</span></span> | <span data-ttu-id="4a313-402">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="4a313-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_ \_ NUMSP512T1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-404">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-404">Requirement</span></span> | <span data-ttu-id="4a313-405">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-406">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-406">Name</span></span>              | <span data-ttu-id="4a313-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="4a313-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="4a313-408">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-408">Standard</span></span>          | [<span data-ttu-id="4a313-409">Спецификация выбора кривой и поддерживаемые параметры кривой в MSR Екклиб</span><span class="sxs-lookup"><span data-stu-id="4a313-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="4a313-410">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-410">Key size (bits)</span></span>   | <span data-ttu-id="4a313-411">512</span><span class="sxs-lookup"><span data-stu-id="4a313-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="4a313-412">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-412">TLS capable</span></span>       | <span data-ttu-id="4a313-413">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="4a313-414">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-414">Object identifier</span></span> | <span data-ttu-id="4a313-415">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="4a313-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-417">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-417">Requirement</span></span> | <span data-ttu-id="4a313-418">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-419">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-419">Name</span></span>              | <span data-ttu-id="4a313-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="4a313-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="4a313-421">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-421">Standard</span></span>          | [<span data-ttu-id="4a313-422">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-423">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-423">Key size (bits)</span></span>   | <span data-ttu-id="4a313-424">160</span><span class="sxs-lookup"><span data-stu-id="4a313-424">160</span></span>                                                                             |
| <span data-ttu-id="4a313-425">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-425">TLS capable</span></span>       | <span data-ttu-id="4a313-426">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-426">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-427">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-427">Object identifier</span></span> | <span data-ttu-id="4a313-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="4a313-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="4a313-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-430">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-430">Requirement</span></span> | <span data-ttu-id="4a313-431">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-432">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-432">Name</span></span>              | <span data-ttu-id="4a313-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="4a313-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="4a313-434">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-434">Standard</span></span>          | [<span data-ttu-id="4a313-435">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-436">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-436">Key size (bits)</span></span>   | <span data-ttu-id="4a313-437">160</span><span class="sxs-lookup"><span data-stu-id="4a313-437">160</span></span>                                                                             |
| <span data-ttu-id="4a313-438">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-438">TLS capable</span></span>       | <span data-ttu-id="4a313-439">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-439">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-440">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-440">Object identifier</span></span> | <span data-ttu-id="4a313-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="4a313-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="4a313-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-443">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-443">Requirement</span></span> | <span data-ttu-id="4a313-444">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-445">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-445">Name</span></span>              | <span data-ttu-id="4a313-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="4a313-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="4a313-447">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-447">Standard</span></span>          | [<span data-ttu-id="4a313-448">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-449">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-449">Key size (bits)</span></span>   | <span data-ttu-id="4a313-450">160</span><span class="sxs-lookup"><span data-stu-id="4a313-450">160</span></span>                                                                             |
| <span data-ttu-id="4a313-451">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-451">TLS capable</span></span>       | <span data-ttu-id="4a313-452">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-452">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-453">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-453">Object identifier</span></span> | <span data-ttu-id="4a313-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="4a313-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="4a313-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_ \_ SECP192K1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-456">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-456">Requirement</span></span> | <span data-ttu-id="4a313-457">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-458">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-458">Name</span></span>              | <span data-ttu-id="4a313-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="4a313-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="4a313-460">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-460">Standard</span></span>          | [<span data-ttu-id="4a313-461">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-462">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-462">Key size (bits)</span></span>   | <span data-ttu-id="4a313-463">192</span><span class="sxs-lookup"><span data-stu-id="4a313-463">192</span></span>                                                                             |
| <span data-ttu-id="4a313-464">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-464">TLS capable</span></span>       | <span data-ttu-id="4a313-465">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-465">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-466">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-466">Object identifier</span></span> | <span data-ttu-id="4a313-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="4a313-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="4a313-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-469">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-469">Requirement</span></span> | <span data-ttu-id="4a313-470">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-471">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-471">Name</span></span>              | <span data-ttu-id="4a313-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="4a313-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="4a313-473">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-473">Standard</span></span>          | [<span data-ttu-id="4a313-474">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-475">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-475">Key size (bits)</span></span>   | <span data-ttu-id="4a313-476">192</span><span class="sxs-lookup"><span data-stu-id="4a313-476">192</span></span>                                                                             |
| <span data-ttu-id="4a313-477">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-477">TLS capable</span></span>       | <span data-ttu-id="4a313-478">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-478">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-479">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-479">Object identifier</span></span> | <span data-ttu-id="4a313-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="4a313-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="4a313-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_ \_ SECP224K1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-482">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-482">Requirement</span></span> | <span data-ttu-id="4a313-483">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-484">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-484">Name</span></span>              | <span data-ttu-id="4a313-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="4a313-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="4a313-486">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-486">Standard</span></span>          | [<span data-ttu-id="4a313-487">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-488">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-488">Key size (bits)</span></span>   | <span data-ttu-id="4a313-489">224</span><span class="sxs-lookup"><span data-stu-id="4a313-489">224</span></span>                                                                             |
| <span data-ttu-id="4a313-490">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-490">TLS capable</span></span>       | <span data-ttu-id="4a313-491">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-491">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-492">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-492">Object identifier</span></span> | <span data-ttu-id="4a313-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="4a313-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="4a313-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_ \_ SECP224R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-495">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-495">Requirement</span></span> | <span data-ttu-id="4a313-496">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-497">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-497">Name</span></span>              | <span data-ttu-id="4a313-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="4a313-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="4a313-499">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-499">Standard</span></span>          | [<span data-ttu-id="4a313-500">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-501">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-501">Key size (bits)</span></span>   | <span data-ttu-id="4a313-502">224</span><span class="sxs-lookup"><span data-stu-id="4a313-502">224</span></span>                                                                             |
| <span data-ttu-id="4a313-503">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-503">TLS capable</span></span>       | <span data-ttu-id="4a313-504">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-504">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-505">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-505">Object identifier</span></span> | <span data-ttu-id="4a313-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="4a313-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="4a313-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_ \_ SECP256K1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-508">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-508">Requirement</span></span> | <span data-ttu-id="4a313-509">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-510">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-510">Name</span></span>              | <span data-ttu-id="4a313-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="4a313-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="4a313-512">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-512">Standard</span></span>          | [<span data-ttu-id="4a313-513">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-514">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-514">Key size (bits)</span></span>   | <span data-ttu-id="4a313-515">256</span><span class="sxs-lookup"><span data-stu-id="4a313-515">256</span></span>                                                                             |
| <span data-ttu-id="4a313-516">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-516">TLS capable</span></span>       | <span data-ttu-id="4a313-517">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-517">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-518">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-518">Object identifier</span></span> | <span data-ttu-id="4a313-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="4a313-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="4a313-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_ \_ SECP256R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-521">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-521">Requirement</span></span> | <span data-ttu-id="4a313-522">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-523">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-523">Name</span></span>              | <span data-ttu-id="4a313-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="4a313-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="4a313-525">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-525">Standard</span></span>          | [<span data-ttu-id="4a313-526">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-527">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-527">Key size (bits)</span></span>   | <span data-ttu-id="4a313-528">256</span><span class="sxs-lookup"><span data-stu-id="4a313-528">256</span></span>                                                                             |
| <span data-ttu-id="4a313-529">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-529">TLS capable</span></span>       | <span data-ttu-id="4a313-530">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-530">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-531">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-531">Object identifier</span></span> | <span data-ttu-id="4a313-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="4a313-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="4a313-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-534">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-534">Requirement</span></span> | <span data-ttu-id="4a313-535">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-536">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-536">Name</span></span>              | <span data-ttu-id="4a313-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="4a313-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="4a313-538">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-538">Standard</span></span>          | [<span data-ttu-id="4a313-539">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-540">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-540">Key size (bits)</span></span>   | <span data-ttu-id="4a313-541">384</span><span class="sxs-lookup"><span data-stu-id="4a313-541">384</span></span>                                                                             |
| <span data-ttu-id="4a313-542">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-542">TLS capable</span></span>       | <span data-ttu-id="4a313-543">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-543">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-544">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-544">Object identifier</span></span> | <span data-ttu-id="4a313-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="4a313-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="4a313-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_ \_ SECP521R1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-547">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-547">Requirement</span></span> | <span data-ttu-id="4a313-548">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-549">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-549">Name</span></span>              | <span data-ttu-id="4a313-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="4a313-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="4a313-551">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-551">Standard</span></span>          | [<span data-ttu-id="4a313-552">Рекомендуемые параметры домена эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="4a313-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="4a313-553">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-553">Key size (bits)</span></span>   | <span data-ttu-id="4a313-554">521</span><span class="sxs-lookup"><span data-stu-id="4a313-554">521</span></span>                                                                             |
| <span data-ttu-id="4a313-555">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-555">TLS capable</span></span>       | <span data-ttu-id="4a313-556">Да</span><span class="sxs-lookup"><span data-stu-id="4a313-556">Yes</span></span>                                                                             |
| <span data-ttu-id="4a313-557">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-557">Object identifier</span></span> | <span data-ttu-id="4a313-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="4a313-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="4a313-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_ \_ WTLS12 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-560">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-560">Requirement</span></span> | <span data-ttu-id="4a313-561">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="4a313-562">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-562">Name</span></span>              | <span data-ttu-id="4a313-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="4a313-563">wtls12</span></span>       |
| <span data-ttu-id="4a313-564">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-564">Standard</span></span>          | <span data-ttu-id="4a313-565">втлс</span><span class="sxs-lookup"><span data-stu-id="4a313-565">WTLS</span></span>         |
| <span data-ttu-id="4a313-566">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-566">Key size (bits)</span></span>   | <span data-ttu-id="4a313-567">224</span><span class="sxs-lookup"><span data-stu-id="4a313-567">224</span></span>          |
| <span data-ttu-id="4a313-568">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-568">TLS capable</span></span>       | <span data-ttu-id="4a313-569">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-569">No</span></span>           |
| <span data-ttu-id="4a313-570">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-570">Object identifier</span></span> | <span data-ttu-id="4a313-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="4a313-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="4a313-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_ \_ WTLS7 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-573">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-573">Requirement</span></span> | <span data-ttu-id="4a313-574">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="4a313-575">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-575">Name</span></span>              | <span data-ttu-id="4a313-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="4a313-576">wtls7</span></span>        |
| <span data-ttu-id="4a313-577">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-577">Standard</span></span>          | <span data-ttu-id="4a313-578">втлс</span><span class="sxs-lookup"><span data-stu-id="4a313-578">WTLS</span></span>         |
| <span data-ttu-id="4a313-579">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-579">Key size (bits)</span></span>   | <span data-ttu-id="4a313-580">160</span><span class="sxs-lookup"><span data-stu-id="4a313-580">160</span></span>          |
| <span data-ttu-id="4a313-581">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-581">TLS capable</span></span>       | <span data-ttu-id="4a313-582">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-582">No</span></span>           |
| <span data-ttu-id="4a313-583">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-583">Object identifier</span></span> | <span data-ttu-id="4a313-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="4a313-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="4a313-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-586">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-586">Requirement</span></span> | <span data-ttu-id="4a313-587">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="4a313-588">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-588">Name</span></span>              | <span data-ttu-id="4a313-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="4a313-589">wtls9</span></span>         |
| <span data-ttu-id="4a313-590">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-590">Standard</span></span>          | <span data-ttu-id="4a313-591">втлс</span><span class="sxs-lookup"><span data-stu-id="4a313-591">WTLS</span></span>          |
| <span data-ttu-id="4a313-592">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-592">Key size (bits)</span></span>   | <span data-ttu-id="4a313-593">160</span><span class="sxs-lookup"><span data-stu-id="4a313-593">160</span></span>           |
| <span data-ttu-id="4a313-594">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-594">TLS capable</span></span>       | <span data-ttu-id="4a313-595">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-595">No</span></span>            |
| <span data-ttu-id="4a313-596">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-596">Object identifier</span></span> | <span data-ttu-id="4a313-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="4a313-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="4a313-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_ \_ X962P192V1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-599">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-599">Requirement</span></span> | <span data-ttu-id="4a313-600">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-601">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-601">Name</span></span>              | <span data-ttu-id="4a313-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="4a313-602">x962P192v1</span></span>          |
| <span data-ttu-id="4a313-603">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-603">Standard</span></span>          | <span data-ttu-id="4a313-604">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-605">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-605">Key size (bits)</span></span>   | <span data-ttu-id="4a313-606">192</span><span class="sxs-lookup"><span data-stu-id="4a313-606">192</span></span>                 |
| <span data-ttu-id="4a313-607">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-607">TLS capable</span></span>       | <span data-ttu-id="4a313-608">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-608">No</span></span>                  |
| <span data-ttu-id="4a313-609">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-609">Object identifier</span></span> | <span data-ttu-id="4a313-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="4a313-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="4a313-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-612">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-612">Requirement</span></span> | <span data-ttu-id="4a313-613">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-614">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-614">Name</span></span>              | <span data-ttu-id="4a313-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="4a313-615">x962P192v2</span></span>          |
| <span data-ttu-id="4a313-616">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-616">Standard</span></span>          | <span data-ttu-id="4a313-617">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-618">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-618">Key size (bits)</span></span>   | <span data-ttu-id="4a313-619">192</span><span class="sxs-lookup"><span data-stu-id="4a313-619">192</span></span>                 |
| <span data-ttu-id="4a313-620">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-620">TLS capable</span></span>       | <span data-ttu-id="4a313-621">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-621">No</span></span>                  |
| <span data-ttu-id="4a313-622">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-622">Object identifier</span></span> | <span data-ttu-id="4a313-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="4a313-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="4a313-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_ \_ X962P192V3 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-625">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-625">Requirement</span></span> | <span data-ttu-id="4a313-626">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-627">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-627">Name</span></span>              | <span data-ttu-id="4a313-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="4a313-628">x962P192v3</span></span>          |
| <span data-ttu-id="4a313-629">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-629">Standard</span></span>          | <span data-ttu-id="4a313-630">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-631">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-631">Key size (bits)</span></span>   | <span data-ttu-id="4a313-632">192</span><span class="sxs-lookup"><span data-stu-id="4a313-632">192</span></span>                 |
| <span data-ttu-id="4a313-633">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-633">TLS capable</span></span>       | <span data-ttu-id="4a313-634">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-634">No</span></span>                  |
| <span data-ttu-id="4a313-635">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-635">Object identifier</span></span> | <span data-ttu-id="4a313-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="4a313-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="4a313-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-638">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-638">Requirement</span></span> | <span data-ttu-id="4a313-639">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-640">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-640">Name</span></span>              | <span data-ttu-id="4a313-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="4a313-641">x962P239v1</span></span>          |
| <span data-ttu-id="4a313-642">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-642">Standard</span></span>          | <span data-ttu-id="4a313-643">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-644">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-644">Key size (bits)</span></span>   | <span data-ttu-id="4a313-645">239</span><span class="sxs-lookup"><span data-stu-id="4a313-645">239</span></span>                 |
| <span data-ttu-id="4a313-646">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-646">TLS capable</span></span>       | <span data-ttu-id="4a313-647">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-647">No</span></span>                  |
| <span data-ttu-id="4a313-648">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-648">Object identifier</span></span> | <span data-ttu-id="4a313-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="4a313-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="4a313-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-651">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-651">Requirement</span></span> | <span data-ttu-id="4a313-652">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-653">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-653">Name</span></span>              | <span data-ttu-id="4a313-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="4a313-654">x962P239v2</span></span>          |
| <span data-ttu-id="4a313-655">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-655">Standard</span></span>          | <span data-ttu-id="4a313-656">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-657">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-657">Key size (bits)</span></span>   | <span data-ttu-id="4a313-658">239</span><span class="sxs-lookup"><span data-stu-id="4a313-658">239</span></span>                 |
| <span data-ttu-id="4a313-659">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-659">TLS capable</span></span>       | <span data-ttu-id="4a313-660">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-660">No</span></span>                  |
| <span data-ttu-id="4a313-661">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-661">Object identifier</span></span> | <span data-ttu-id="4a313-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="4a313-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="4a313-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 кривой ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-664">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-664">Requirement</span></span> | <span data-ttu-id="4a313-665">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-666">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-666">Name</span></span>              | <span data-ttu-id="4a313-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="4a313-667">x962P239v3</span></span>          |
| <span data-ttu-id="4a313-668">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-668">Standard</span></span>          | <span data-ttu-id="4a313-669">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-670">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-670">Key size (bits)</span></span>   | <span data-ttu-id="4a313-671">239</span><span class="sxs-lookup"><span data-stu-id="4a313-671">239</span></span>                 |
| <span data-ttu-id="4a313-672">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-672">TLS capable</span></span>       | <span data-ttu-id="4a313-673">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-673">No</span></span>                  |
| <span data-ttu-id="4a313-674">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-674">Object identifier</span></span> | <span data-ttu-id="4a313-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="4a313-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="4a313-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_ \_ X962P256V1 кривая \_ ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="4a313-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="4a313-677">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-677">Requirement</span></span> | <span data-ttu-id="4a313-678">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="4a313-679">Имя</span><span class="sxs-lookup"><span data-stu-id="4a313-679">Name</span></span>              | <span data-ttu-id="4a313-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="4a313-680">x962P256v1</span></span>          |
| <span data-ttu-id="4a313-681">Standard</span><span class="sxs-lookup"><span data-stu-id="4a313-681">Standard</span></span>          | <span data-ttu-id="4a313-682">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="4a313-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="4a313-683">Размер ключа (в битах)</span><span class="sxs-lookup"><span data-stu-id="4a313-683">Key size (bits)</span></span>   | <span data-ttu-id="4a313-684">256</span><span class="sxs-lookup"><span data-stu-id="4a313-684">256</span></span>                 |
| <span data-ttu-id="4a313-685">Поддерживается TLS</span><span class="sxs-lookup"><span data-stu-id="4a313-685">TLS capable</span></span>       | <span data-ttu-id="4a313-686">Нет</span><span class="sxs-lookup"><span data-stu-id="4a313-686">No</span></span>                  |
| <span data-ttu-id="4a313-687">Идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="4a313-687">Object identifier</span></span> | <span data-ttu-id="4a313-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="4a313-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a313-689">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a313-689">Remarks</span></span>

<span data-ttu-id="4a313-690">Чтобы использовать именованную кривую, вызовите [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) , **используя \_ \_ алгоритм BCrypt ECDSA** или **BCrypt \_ ECDH \_** в качестве идентификатора алгоритма.</span><span class="sxs-lookup"><span data-stu-id="4a313-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="4a313-691">Затем вызовите [**бкриптсетпроперти**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) и задайте для свойства " **\_ \_ \_ название кривой с кодом коррекции ошибок** " одну из приведенных выше кривых или именованных кривых, зарегистрированных на компьютере, как показано в `certutil -displayEccCurve` команде.</span><span class="sxs-lookup"><span data-stu-id="4a313-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a313-692">Требования</span><span class="sxs-lookup"><span data-stu-id="4a313-692">Requirements</span></span>



| <span data-ttu-id="4a313-693">Требование</span><span class="sxs-lookup"><span data-stu-id="4a313-693">Requirement</span></span> | <span data-ttu-id="4a313-694">Значение</span><span class="sxs-lookup"><span data-stu-id="4a313-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a313-695">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a313-695">Minimum supported client</span></span><br/> | <span data-ttu-id="4a313-696">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4a313-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a313-697">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a313-697">Minimum supported server</span></span><br/> | <span data-ttu-id="4a313-698">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4a313-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a313-699">Header</span><span class="sxs-lookup"><span data-stu-id="4a313-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a313-700"><dt>BCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a313-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a313-701">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a313-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a313-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="4a313-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="4a313-703">**нкрипткреатеперсистедкэй**</span><span class="sxs-lookup"><span data-stu-id="4a313-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




