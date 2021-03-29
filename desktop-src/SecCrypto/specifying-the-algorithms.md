---
description: После создания или импорта главного ключа оба алгоритма (RSA/SChannel и Диффи-Хелмана/Schannel) сообщают CSP о типе ключей неполного шифрования и ключах MAC, которые будут получены из главного ключа.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Указание алгоритмов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647193"
---
# <a name="specifying-the-algorithms"></a>Указание алгоритмов

После создания или импорта [*главного ключа*](../secgloss/m-gly.md) как [*RSA*](../secgloss/r-gly.md)/Счаннел, так и [*Диффи-Хелмана*](../secgloss/d-gly.md)/счаннел сообщают [*CSP*](../secgloss/c-gly.md) о типе [*ключей шифрования*](../secgloss/b-gly.md) и [*ключах Mac*](../secgloss/m-gly.md) , которые будут получены из главного ключа. В следующем примере задаются эти алгоритмы. Один и тот же код используется как для клиента, так и для сервера.


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> Механизм протокола [*SChannel*](../secgloss/s-gly.md) не должен указывать алгоритмы и размеры ключей, не поддерживаемые CSP. Дополнительные сведения см. в разделе [перечисление поддерживаемых протоколов](enumerating-supported-protocols.md). Если указаны неподдерживаемые алгоритмы или размеры ключей, функция CSP должна завершиться ошибкой и возвращать код ошибки "не разрешено" \_ \_ .

 

 

 
