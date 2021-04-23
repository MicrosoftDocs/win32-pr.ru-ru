---
description: Сообщение о завершении будет отправлено сразу после сообщения Spec (изменение спецификации шифра), чтобы проверить успешность обмена ключами и процессов проверки подлинности.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Завершение сообщений в протоколе TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684098"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="bc152-103">Завершение сообщений в протоколе TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="bc152-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="bc152-104">Сообщение о завершении будет отправлено сразу после сообщения Spec (изменение спецификации шифра), чтобы проверить успешность обмена ключами и процессов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bc152-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="bc152-105">Сообщения о завершении в протоколе TLS 1,0 вычисляются с помощью [*функции псевдо-Random*](../secgloss/p-gly.md) (PRF) с [*главным ключом*](../secgloss/m-gly.md), меткой и начальным значением в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="bc152-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="bc152-106">PRF создает выходные данные произвольной длины.</span><span class="sxs-lookup"><span data-stu-id="bc152-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="bc152-107">Следующий метод используется для создания выходных данных PRF, используемых в сообщениях завершения TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="bc152-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="bc152-108">Для создания PRF [*-*](../secgloss/h-gly.md) обработчика используется [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) со значением **\_ идентификатора ALG** , установленным в калг \_ TLS1PRF, и маркером к главному ключу, переданному в параметре *hKey* .</span><span class="sxs-lookup"><span data-stu-id="bc152-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="bc152-109">Значения меток и начальных значений задаются для хэш-маркера с использованием значений HP \_ TLS1PRF \_ Label и HP \_ TLS1PRF \_ SEED соответственно в параметре *двпарам* с функцией [**криптсесашпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) .</span><span class="sxs-lookup"><span data-stu-id="bc152-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="bc152-110">Наконец, обработчик протокола вызывает функцию [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) со значением HP \_ хашвал в параметре *ДВПАРАМ* , чтобы извлечь PRF данные, включаемые в сообщение о завершении.</span><span class="sxs-lookup"><span data-stu-id="bc152-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="bc152-111">При вызове **CryptGetHashParam** механизм протокола должен указать, сколько байт данных PRF будет создавать.</span><span class="sxs-lookup"><span data-stu-id="bc152-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="bc152-112">Это делается в параметре *пдвдатален* , и результирующие данные помещаются в буфер, на который указывает параметр *pbData* .</span><span class="sxs-lookup"><span data-stu-id="bc152-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="bc152-113">Ниже приведен типичный исходный код для этой подсистемы протокола.</span><span class="sxs-lookup"><span data-stu-id="bc152-113">The following is typical source code for this protocol engine:</span></span>


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
