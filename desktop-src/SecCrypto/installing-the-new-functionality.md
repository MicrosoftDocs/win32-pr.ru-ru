---
description: Установка новых функций в память может повысить производительность. Функции CryptoAPI выполняют поиск функций в памяти перед поиском в реестре библиотеки DLL. Перед установкой функции необходимо загрузить библиотеку DLL.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Установка новых функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684339"
---
# <a name="installing-the-new-functionality"></a><span data-ttu-id="74bd6-105">Установка новых функций</span><span class="sxs-lookup"><span data-stu-id="74bd6-105">Installing the New Functionality</span></span>

<span data-ttu-id="74bd6-106">Установка новых функций в память может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="74bd6-106">Installing new functionality into memory can improve performance.</span></span> <span data-ttu-id="74bd6-107">Функции [*CryptoAPI*](../secgloss/c-gly.md) выполняют поиск функций в памяти перед поиском в реестре библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="74bd6-107">[*CryptoAPI*](../secgloss/c-gly.md) functions search memory for the functionality before searching the registry for the DLL.</span></span> <span data-ttu-id="74bd6-108">Перед установкой функции необходимо загрузить библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="74bd6-108">The DLL must be loaded before installing the functionality.</span></span>

<span data-ttu-id="74bd6-109">[**Криптинсталлоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) устанавливает адрес новой функциональности.</span><span class="sxs-lookup"><span data-stu-id="74bd6-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installs the address of the new functionality.</span></span> <span data-ttu-id="74bd6-110">Он должен быть помещен в функцию **DllMain** библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="74bd6-110">It should be placed in the **DllMain** function of the DLL.</span></span>

<span data-ttu-id="74bd6-111">Если *хмодуле* передается в [**криптинсталлоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), после установки библиотека DLL не выгружается до тех пор, пока не будет выгружена Crypt32.dll.</span><span class="sxs-lookup"><span data-stu-id="74bd6-111">If *hModule* is passed to [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), once installed, the DLL is not unloaded until the Crypt32.dll is unloaded.</span></span>

<span data-ttu-id="74bd6-112">В следующем примере вызывается функция [**криптинсталлоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) .</span><span class="sxs-lookup"><span data-stu-id="74bd6-112">The following example calls the [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
