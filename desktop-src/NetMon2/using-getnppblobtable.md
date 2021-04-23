---
description: В следующем примере показано, как использовать функцию Жетнппблобтабле для получения таблицы больших двоичных объектов НПП, представляющей зарегистрированные сетевые адаптеры на локальном компьютере.
ms.assetid: 7267f658-103d-4290-8ebf-b78866bd1fe8
title: Использование Жетнппблобтабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8432f0f3c2cb23056eee4a94b75da5de85cd6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673864"
---
# <a name="using-getnppblobtable"></a><span data-ttu-id="205be-103">Использование Жетнппблобтабле</span><span class="sxs-lookup"><span data-stu-id="205be-103">Using GetNPPBlobTable</span></span>

<span data-ttu-id="205be-104">В следующем примере показано, как использовать функцию [**жетнппблобтабле**](getnppblobtable.md) для получения таблицы больших двоичных объектов НПП, представляющей зарегистрированные сетевые адаптеры на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="205be-104">The following example shows how to use the [**GetNPPBlobTable**](getnppblobtable.md) function to retrieve a NPP BLOB table that represents the registered network interface cards on the local computer.</span></span>


```C++
DWORD rc;
PBLOB_TABLE pBlobTable;
// Create the filter blob
HBLOB hFilterBlob;
if (NMERR_SUCCESS != (rc = CreateBlob(&hFilterBlob)))
    return FALSE;

// Set test criteria
// To obtain delayed capture interface
if (NMERR_SUCCESS != (rc = SetBoolInBlob (
                             hFilterBlob,
                             OWNER_NPP,
                             CATEGORY_CONFIG,
                             TAG_INTERFACE_DELAYED_CAPTURE,
                             TRUE)))
    return FALSE;

// Only obtain Ethernet cards
if (NMERR_SUCCESS != (rc = SetStringInBlob(hBlob,
                             OWNER_NPP,
                             CATEGORY_NETWORKINFO,
                             TAG_MACTYPE,
                             PROTOCOL_STRING_ETHERNET_TXT)))
    return FALSE;

// To get SpecialBlobs back
if (NMERR_SUCCESS != (rc = SetBoolInBlob(hBlob,
                             OWNER_NPP,
                             CATEGORY_FINDER,
                             TAG_GET_SPECIAL_BLOBS,
                             TRUE)))
    return FALSE;

// Make the call to the finder
rc = GetNPPBlobTable( hFilterBlob, &pBlobTable );

// Did we get anything?
if (rc != NMERR_SUCCESS)
    return FALSE;


//  To obtain a "special" blob.
//  Should have set
//  the filter blob to include the TAG_INTERFACE_REMOTE
//  interface &#8211; then only a TAG_INTERFACE_REMOTE interface
//  would return.

HBLOB OurBlob = NULL;
DWORD index;
for (index = 0; index < pBlobTable->dwNumBlobs; index++)
{
    // Here is the test for a special blob
    if (NMERR_SUCCESS == 
       (rc = GetStringFromBlob(pBlobTable->Blobs[index],
                               OWNER_NPP,
                               CATEGORY_FINDER,
                               TAG_DLL_FILENAME,
                               &DLLFileName)))
    {
        // This is a special blob.
        // Check to see if it is supports the remote interface.
        BOOL bGoesRemote;
        rc = GetBoolFromBlob( hBlob,
                              OWNER_NPP,
                              CATEGORY_CONFIG,
                              TAG_INTERFACE_DELAYED_CAPTURE,
                              &bGoesRemote);
        if (rc == NMERR_SUCCESS && bGoesRemote)
        {
            // This is the one we want. Save it off
            OurBlob = pBlobTable->Blobs[index];
            break;
        }
    }
}

if (OurBlob == NULL)
    return FALSE;

// Set the computer name in our special blob.
rc = SetStringInBlob(OurBlob,
                     OWNER_NPP,
                     CATEGORY_LOCATION,
                     TAG_REMOTE_MACHINE_NAME,
                     "mycomputer");

PBLOB_TABLE pSecondBlobTable;
// Call the finder again.
rc = GetNPPBlobTable( OurBlob, &pSecondBlobTable );

// Did we get anything?
if (rc != NMERR_SUCCESS)
    return FALSE;

// A Blob is now on mycomputer.
// Use the blob as shown in the previous example.
```



 

 



