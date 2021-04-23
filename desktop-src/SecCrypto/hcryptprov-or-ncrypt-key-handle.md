---
description: Используется в качестве маркера для поставщика служб шифрования CryptoAPI (CSP) или CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664116"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="f5d66-103">\_ \_ \_ маркер ключа хкриптпров или \_ NCRYPT</span><span class="sxs-lookup"><span data-stu-id="f5d66-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="f5d66-104">Тип **данных \_ \_ \_ \_ обработчика ключа хкриптпров или NCRYPT** используется в качестве маркера для поставщика служб [*шифрования*](../secgloss/c-gly.md) CryptoAPI (CSP) или CNG.</span><span class="sxs-lookup"><span data-stu-id="f5d66-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="f5d66-105">Этот обработчик должен быть обработчиком [**хкриптпров**](hcryptprov.md) , созданным с помощью функции [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) или обработчика **\_ ключей \_ NCRYPT** , созданного с помощью функции [**нкриптопенкэй**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="f5d66-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="f5d66-106">Новые приложения всегда должны передавать маркер **\_ \_ маркера ключа NCRYPT** в CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="f5d66-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="f5d66-107">Требования</span><span class="sxs-lookup"><span data-stu-id="f5d66-107">Requirements</span></span>



| <span data-ttu-id="f5d66-108">Требование</span><span class="sxs-lookup"><span data-stu-id="f5d66-108">Requirement</span></span> | <span data-ttu-id="f5d66-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f5d66-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d66-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5d66-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d66-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5d66-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5d66-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5d66-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d66-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5d66-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5d66-114">Header</span><span class="sxs-lookup"><span data-stu-id="f5d66-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d66-115"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d66-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
