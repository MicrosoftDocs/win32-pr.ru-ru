---
description: Хэши наиболее полезны для проверки целостности данных при их использовании с алгоритмом асимметричной подписи.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Создание хэша с помощью CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662125"
---
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="fb8fa-103">Создание хэша с помощью CNG</span><span class="sxs-lookup"><span data-stu-id="fb8fa-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="fb8fa-104">[*Хэш*](/windows/desktop/SecGloss/h-gly) — это односторонняя операция, выполняемая на блоке данных для создания уникального хэш-значения, представляющего содержимое данных.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="fb8fa-105">Независимо от того, когда выполняется хэш, тот же самый хэш [*-алгоритм*](/windows/desktop/SecGloss/h-gly) , выполняемый на одних и тех же данных, всегда будет иметь то же значение хэша.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="fb8fa-106">Если какой-либо из данных изменится, значение хэша изменится соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="fb8fa-107">Хэши не используются для шифрования данных, так как они не предназначены для воспроизведения исходных данных из хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="fb8fa-108">Хэши наиболее полезны для проверки целостности данных при их использовании с алгоритмом асимметричной подписи.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="fb8fa-109">Например, если вы хэширует текстовое сообщение, подписали хэш и включили в исходное сообщение подписанное хэш-значение, получатель может проверить подписанный хэш, создать значение хэша для полученного сообщения, а затем сравнить это хэш-значение со знакомым хэшем, входящим в исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="fb8fa-110">Если два хэш-значения идентичны, получатель может быть уверенным в том, что исходное сообщение не было изменено.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="fb8fa-111">Размер хэш-значения фиксирован для конкретного алгоритма хэширования.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="fb8fa-112">Это означает, что независимо от того, насколько большой или маленький блок данных имеет значение, хэш всегда будет иметь одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="fb8fa-113">В качестве примера алгоритм хэширования SHA256 имеет размер хэш-значения 256 бит.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="fb8fa-114">Создание объекта хэширования</span><span class="sxs-lookup"><span data-stu-id="fb8fa-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="fb8fa-115">Создание повторно используемого объекта хэширования</span><span class="sxs-lookup"><span data-stu-id="fb8fa-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="fb8fa-116">Дублирование хэш-объекта</span><span class="sxs-lookup"><span data-stu-id="fb8fa-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="fb8fa-117">Создание объекта хэширования</span><span class="sxs-lookup"><span data-stu-id="fb8fa-117">Creating a Hashing Object</span></span>

<span data-ttu-id="fb8fa-118">Чтобы создать хэш с помощью CNG, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="fb8fa-119">Откройте поставщик алгоритма, который поддерживает нужный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="fb8fa-120">К типичным алгоритмам хэширования относятся технологии MD2, MD4, MD5, SHA-1 и SHA256.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="fb8fa-121">Вызовите функцию [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) и укажите соответствующий идентификатор алгоритма в параметре *псзалгид* .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="fb8fa-122">Функция возвращает маркер поставщику.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="fb8fa-123">Чтобы создать объект хэширования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="fb8fa-124">Получите размер объекта, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины объекта BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="fb8fa-125">Выделите память для хранения хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="fb8fa-126">Создайте объект, вызвав функцию [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="fb8fa-127">Хэширует данные.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-127">Hash the data.</span></span> <span data-ttu-id="fb8fa-128">Это включает вызов функции [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) один или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="fb8fa-129">Каждый вызов добавляет указанные данные в хэш.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="fb8fa-130">Чтобы получить хэш-значение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="fb8fa-131">Получите размер значения, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины хэша BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="fb8fa-132">Выделите память для хранения значения.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="fb8fa-133">Получите хэш-значение, вызвав функцию [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="fb8fa-134">После вызова этой функции хэш-объект больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="fb8fa-135">Для выполнения этой процедуры необходимо выполнить следующие действия по очистке:</span><span class="sxs-lookup"><span data-stu-id="fb8fa-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="fb8fa-136">Закройте хэш-объект, передав его в функцию [**бкриптдестройхаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="fb8fa-137">Освободите память, выделенную для хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="fb8fa-138">Если вы не создадите никаких хэш-объектов, закройте поставщик алгоритма, передав его в функцию [**бкриптклосеалгорисмпровидер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="fb8fa-139">Если будут создаваться дополнительные хэш-объекты, мы рекомендуем повторно использовать поставщик алгоритма, а не создавать и уничтожать один и тот же тип поставщика алгоритма много раз.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="fb8fa-140">По завершении использования памяти хэш-значения освободите ее.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="fb8fa-141">В следующем примере показано, как создать хэш-значение с помощью CNG.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-141">The following example shows how to create a hash value by using CNG.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

}

```



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="fb8fa-142">Создание повторно используемого объекта хэширования</span><span class="sxs-lookup"><span data-stu-id="fb8fa-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="fb8fa-143">Начиная с Windows 8 и Windows Server 2012, можно создать многократно используемый объект хэширования для сценариев, требующих быстрого вычисления нескольких хэшей или кодов HMAC.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="fb8fa-144">Для этого укажите **\_ \_ \_ флаг повторного использования хэша BCRYPT** при вызове функции [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="fb8fa-145">Этот флаг поддерживается всеми поставщиками хэш-алгоритма (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="fb8fa-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="fb8fa-146">Объект хэширования, созданный с помощью этого флага, можно повторно использовать сразу после вызова [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) так же, как если бы он был создан с помощью вызова [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="fb8fa-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="fb8fa-147">Чтобы создать повторно используемый объект хэширования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="fb8fa-148">Откройте поставщик алгоритма, который поддерживает требуемый алгоритм хэширования.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="fb8fa-149">Вызовите функцию [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) и укажите соответствующий идентификатор алгоритма в параметре *ПСЗАЛГИД* и **\_ \_ \_ флаг повторного использования хэша BCRYPT** в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="fb8fa-150">Функция возвращает маркер поставщику.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="fb8fa-151">Чтобы создать объект хэширования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="fb8fa-152">Получите размер объекта, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины объекта BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="fb8fa-153">Выделите память для хранения хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="fb8fa-154">Создайте объект, вызвав функцию [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="fb8fa-155">Укажите **\_ \_ \_ флаг повторного использования хэша BCRYPT** в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="fb8fa-156">Хэширует данные путем вызова функции [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="fb8fa-157">Чтобы получить хэш-значение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="fb8fa-158">Получите размер хэш-значения, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины хэша BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="fb8fa-159">Выделите память для хранения значения.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="fb8fa-160">Получите хэш-значение, вызвав [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span><span class="sxs-lookup"><span data-stu-id="fb8fa-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="fb8fa-161">Чтобы повторно использовать объект хэширования с новыми данными, перейдите к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="fb8fa-162">Для выполнения этой процедуры необходимо выполнить следующие действия по очистке:</span><span class="sxs-lookup"><span data-stu-id="fb8fa-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="fb8fa-163">Закройте хэш-объект, передав его в функцию [**бкриптдестройхаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="fb8fa-164">Освободите память, выделенную для хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="fb8fa-165">Если вы не создадите никаких хэш-объектов, закройте поставщик алгоритма, передав его в функцию [**бкриптклосеалгорисмпровидер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="fb8fa-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="fb8fa-166">По завершении использования памяти хэш-значения освободите ее.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="fb8fa-167">Дублирование хэш-объекта</span><span class="sxs-lookup"><span data-stu-id="fb8fa-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="fb8fa-168">В некоторых случаях может быть полезно хэшировать некоторый объем общих данных, а затем создать два отдельных хэш-объекта из общих данных.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="fb8fa-169">Для этого не нужно создавать два отдельных хэш-объекта и дважды хэшировать общие данные.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="fb8fa-170">Можно создать один объект хэша и добавить все общие данные в хэш-объект.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="fb8fa-171">Затем можно использовать функцию [**бкриптдупликатехаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) для создания дубликата исходного хэш-объекта.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="fb8fa-172">Дублирующийся хэш-объект содержит все те же сведения о состоянии и хэшированные данные, что и исходный, но является полностью независимой хэш-объектом.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="fb8fa-173">Теперь можно добавить уникальные данные в каждый хэш-объект и получить хэш-значение, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="fb8fa-174">Этот метод полезен при хэшировании потенциально большого объема общих данных.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="fb8fa-175">Для получения уникального хэш-объекта достаточно добавить только общие данные в исходный хэш, а затем скопировать хэш-объект.</span><span class="sxs-lookup"><span data-stu-id="fb8fa-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 
