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
# <a name="creating-a-hash-with-cng"></a>Создание хэша с помощью CNG

[*Хэш*](/windows/desktop/SecGloss/h-gly) — это односторонняя операция, выполняемая на блоке данных для создания уникального хэш-значения, представляющего содержимое данных. Независимо от того, когда выполняется хэш, тот же самый хэш [*-алгоритм*](/windows/desktop/SecGloss/h-gly) , выполняемый на одних и тех же данных, всегда будет иметь то же значение хэша. Если какой-либо из данных изменится, значение хэша изменится соответствующим образом.

Хэши не используются для шифрования данных, так как они не предназначены для воспроизведения исходных данных из хэш-значения. Хэши наиболее полезны для проверки целостности данных при их использовании с алгоритмом асимметричной подписи. Например, если вы хэширует текстовое сообщение, подписали хэш и включили в исходное сообщение подписанное хэш-значение, получатель может проверить подписанный хэш, создать значение хэша для полученного сообщения, а затем сравнить это хэш-значение со знакомым хэшем, входящим в исходное сообщение. Если два хэш-значения идентичны, получатель может быть уверенным в том, что исходное сообщение не было изменено.

Размер хэш-значения фиксирован для конкретного алгоритма хэширования. Это означает, что независимо от того, насколько большой или маленький блок данных имеет значение, хэш всегда будет иметь одинаковый размер. В качестве примера алгоритм хэширования SHA256 имеет размер хэш-значения 256 бит.

-   [Создание объекта хэширования](#creating-a-hashing-object)
-   [Создание повторно используемого объекта хэширования](#creating-a-reusable-hashing-object)
-   [Дублирование хэш-объекта](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Создание объекта хэширования

Чтобы создать хэш с помощью CNG, выполните следующие действия.

1.  Откройте поставщик алгоритма, который поддерживает нужный алгоритм. К типичным алгоритмам хэширования относятся технологии MD2, MD4, MD5, SHA-1 и SHA256. Вызовите функцию [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) и укажите соответствующий идентификатор алгоритма в параметре *псзалгид* . Функция возвращает маркер поставщику.
2.  Чтобы создать объект хэширования, выполните следующие действия.

    1.  Получите размер объекта, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины объекта BCRYPT** .
    2.  Выделите память для хранения хэш-объекта.
    3.  Создайте объект, вызвав функцию [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .

3.  Хэширует данные. Это включает вызов функции [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) один или несколько раз. Каждый вызов добавляет указанные данные в хэш.
4.  Чтобы получить хэш-значение, выполните следующие действия.

    1.  Получите размер значения, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины хэша BCRYPT** .
    2.  Выделите память для хранения значения.
    3.  Получите хэш-значение, вызвав функцию [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) . После вызова этой функции хэш-объект больше не является допустимым.

5.  Для выполнения этой процедуры необходимо выполнить следующие действия по очистке:

    1.  Закройте хэш-объект, передав его в функцию [**бкриптдестройхаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Освободите память, выделенную для хэш-объекта.
    3.  Если вы не создадите никаких хэш-объектов, закройте поставщик алгоритма, передав его в функцию [**бкриптклосеалгорисмпровидер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .

        Если будут создаваться дополнительные хэш-объекты, мы рекомендуем повторно использовать поставщик алгоритма, а не создавать и уничтожать один и тот же тип поставщика алгоритма много раз.

    4.  По завершении использования памяти хэш-значения освободите ее.

В следующем примере показано, как создать хэш-значение с помощью CNG.


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



## <a name="creating-a-reusable-hashing-object"></a>Создание повторно используемого объекта хэширования

Начиная с Windows 8 и Windows Server 2012, можно создать многократно используемый объект хэширования для сценариев, требующих быстрого вычисления нескольких хэшей или кодов HMAC. Для этого укажите **\_ \_ \_ флаг повторного использования хэша BCRYPT** при вызове функции [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) . Этот флаг поддерживается всеми поставщиками хэш-алгоритма (Майкрософт). Объект хэширования, созданный с помощью этого флага, можно повторно использовать сразу после вызова [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) так же, как если бы он был создан с помощью вызова [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Чтобы создать повторно используемый объект хэширования, выполните следующие действия.

1.  Откройте поставщик алгоритма, который поддерживает требуемый алгоритм хэширования. Вызовите функцию [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) и укажите соответствующий идентификатор алгоритма в параметре *ПСЗАЛГИД* и **\_ \_ \_ флаг повторного использования хэша BCRYPT** в параметре *dwFlags* . Функция возвращает маркер поставщику.
2.  Чтобы создать объект хэширования, выполните следующие действия.

    1.  Получите размер объекта, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины объекта BCRYPT** .
    2.  Выделите память для хранения хэш-объекта.
    3.  Создайте объект, вызвав функцию [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Укажите **\_ \_ \_ флаг повторного использования хэша BCRYPT** в параметре *dwFlags* .

3.  Хэширует данные путем вызова функции [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .
4.  Чтобы получить хэш-значение, выполните следующие действия.

    1.  Получите размер хэш-значения, вызвав функцию [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) для получения свойства **\_ \_ длины хэша BCRYPT** .
    2.  Выделите память для хранения значения.
    3.  Получите хэш-значение, вызвав [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Чтобы повторно использовать объект хэширования с новыми данными, перейдите к шагу 3.
6.  Для выполнения этой процедуры необходимо выполнить следующие действия по очистке:

    1.  Закройте хэш-объект, передав его в функцию [**бкриптдестройхаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Освободите память, выделенную для хэш-объекта.
    3.  Если вы не создадите никаких хэш-объектов, закройте поставщик алгоритма, передав его в функцию [**бкриптклосеалгорисмпровидер**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .
    4.  По завершении использования памяти хэш-значения освободите ее.

## <a name="duplicating-a-hash-object"></a>Дублирование хэш-объекта

В некоторых случаях может быть полезно хэшировать некоторый объем общих данных, а затем создать два отдельных хэш-объекта из общих данных. Для этого не нужно создавать два отдельных хэш-объекта и дважды хэшировать общие данные. Можно создать один объект хэша и добавить все общие данные в хэш-объект. Затем можно использовать функцию [**бкриптдупликатехаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) для создания дубликата исходного хэш-объекта. Дублирующийся хэш-объект содержит все те же сведения о состоянии и хэшированные данные, что и исходный, но является полностью независимой хэш-объектом. Теперь можно добавить уникальные данные в каждый хэш-объект и получить хэш-значение, как показано в примере. Этот метод полезен при хэшировании потенциально большого объема общих данных. Для получения уникального хэш-объекта достаточно добавить только общие данные в исходный хэш, а затем скопировать хэш-объект.

 

 
