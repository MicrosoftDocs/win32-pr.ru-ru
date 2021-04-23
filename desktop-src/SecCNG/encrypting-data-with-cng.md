---
description: CNG позволяет шифровать данные с помощью минимального числа вызовов функций и позволяет выполнять все функции управления памятью.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Шифрование данных с помощью CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662123"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="2bdc7-103">Шифрование данных с помощью CNG</span><span class="sxs-lookup"><span data-stu-id="2bdc7-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="2bdc7-104">В основном используется любой криптографический API для шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="2bdc7-105">CNG позволяет шифровать данные с помощью минимального числа вызовов функций и позволяет выполнять все функции управления памятью.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="2bdc7-106">Хотя многие сведения о реализации протокола оставлены пользователю, CNG предоставляет примитивы, которые выполняют фактические задачи шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="2bdc7-107">Шифрование данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="2bdc7-108">Пример шифрования данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="2bdc7-109">Расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="2bdc7-110">Шифрование данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-110">Encrypting Data</span></span>

<span data-ttu-id="2bdc7-111">Чтобы зашифровать данные, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2bdc7-112">Откройте поставщик алгоритма, поддерживающий шифрование, например **, \_ \_ алгоритм BCRYPT des**.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2bdc7-113">Создайте ключ для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="2bdc7-114">Ключ можно создать с помощью любой из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="2bdc7-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="2bdc7-115">[**Бкриптженератекэйпаир**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) или [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) для асимметричных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="2bdc7-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) или [**бкриптимпорткэй**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) для симметричных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="2bdc7-117">Шифрование и расшифровка данных с помощью асимметричного ключа требуют значительного вычисления по сравнению с шифрованием с помощью симметричного ключа.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="2bdc7-118">Если необходимо зашифровать данные с помощью асимметричного ключа, следует зашифровать данные с помощью симметричного ключа, зашифровать симметричный ключ с помощью асимметричного ключа и включить в сообщение зашифрованный симметричный ключ.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="2bdc7-119">Затем получатель может расшифровать симметричный ключ и использовать симметричный ключ для расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="2bdc7-120">Получение размера зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="2bdc7-121">Это основано на алгоритме шифрования, схеме заполнения (при наличии) и размере данных для шифрования.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="2bdc7-122">Размер зашифрованных данных можно получить с помощью функции [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) , передав **значение NULL** для параметра *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2bdc7-123">Все остальные параметры должны быть такими же, как и при шифровании данных, за исключением параметра *пбинпут* , который не используется в этом случае.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2bdc7-124">Можно либо зашифровать данные на месте, используя один буфер, либо зашифровать данные в отдельный буфер.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2bdc7-125">Если требуется зашифровать данные на месте, передайте текстовый указатель буфера для параметров *пбинпут* и *Пбаутпут* в функции [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="2bdc7-126">Возможно, размер зашифрованных данных будет больше, чем размер незашифрованных данных, поэтому буфер открытого текста должен быть достаточно большим для хранения зашифрованных данных, а не только для простого текста.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="2bdc7-127">Для выделения буфера с открытым текстом можно использовать размер, полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="2bdc7-128">Если необходимо зашифровать данные в отдельный буфер, выделите буфер памяти для зашифрованных данных, используя размер, полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="2bdc7-129">Вызовите функцию [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="2bdc7-130">Эта функция будет записывать зашифрованные данные в расположение, указанное в параметре *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="2bdc7-131">При необходимости сохранимайте зашифрованные данные.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="2bdc7-132">Повторите шаги 5 и 6, пока не будут зашифрованы все данные.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="2bdc7-133">Пример шифрования данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-133">Encrypting Data Example</span></span>

<span data-ttu-id="2bdc7-134">В следующем примере показано, как зашифровать данные с помощью CNG с использованием алгоритма симметричного шифрования стандарта расширенного шифрования.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a><span data-ttu-id="2bdc7-135">Расшифровка данных</span><span class="sxs-lookup"><span data-stu-id="2bdc7-135">Decrypting Data</span></span>

<span data-ttu-id="2bdc7-136">Чтобы расшифровать данные, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2bdc7-137">Откройте поставщик алгоритма, поддерживающий шифрование, например **, \_ \_ алгоритм BCRYPT des**.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2bdc7-138">Получите ключ, с помощью которого были зашифрованы данные, и используйте этот ключ для получения маркера для ключа.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="2bdc7-139">Получение размера расшифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="2bdc7-140">Это основано на алгоритме шифрования, схеме заполнения (при наличии) и размере данных для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="2bdc7-141">Размер зашифрованных данных можно получить с помощью функции [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , передав **значение NULL** для параметра *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2bdc7-142">Параметры, задающих схему заполнения и [*вектор инициализации*](/windows/desktop/SecGloss/i-gly) (IV), должны быть такими же, как и при шифровании данных, за исключением параметра *пбинпут* , который не используется в этом случае.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2bdc7-143">Выделение буфера памяти для расшифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="2bdc7-144">Можно либо расшифровать данные на месте, используя один буфер, либо расшифровать данные в отдельный буфер.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2bdc7-145">Если вы хотите расшифровать данные на месте, передайте указатель буфера зашифрованных данных для параметров *пбинпут* и *Пбаутпут* в функции [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="2bdc7-146">Если вы хотите расшифровать данные в отдельный буфер, выделите буфер памяти для расшифрованных данных, используя размер, полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="2bdc7-147">Вызовите функцию [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) для расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="2bdc7-148">Параметры, задающих схему заполнения и вектор инициализации, должны быть такими же, как и при шифровании данных.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="2bdc7-149">Эта функция будет записывать расшифрованные данные в расположение, указанное в параметре *пбаутпут* .</span><span class="sxs-lookup"><span data-stu-id="2bdc7-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="2bdc7-150">При необходимости сохранимые расшифрованные данные.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="2bdc7-151">Повторите шаги 5 и 6, пока не будут расшифрованы все данные.</span><span class="sxs-lookup"><span data-stu-id="2bdc7-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 
