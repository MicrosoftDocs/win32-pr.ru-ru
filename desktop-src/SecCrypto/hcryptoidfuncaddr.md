---
description: Представляет обработчик для устанавливаемой функции идентификатора объекта (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: ХКРИПТОИДФУНКАДДР (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664117"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="5516a-103">хкриптоидфункаддр</span><span class="sxs-lookup"><span data-stu-id="5516a-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="5516a-104">Тип данных **хкриптоидфункаддр** представляет собой описатель для устанавливаемой функции [*идентификатора объекта*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="5516a-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="5516a-105">Функции [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)и [**криптфриоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , а также [**\_ \_ \_ информационная структура хранилища сертификатов Prov**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) используют этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="5516a-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="5516a-106">Требования</span><span class="sxs-lookup"><span data-stu-id="5516a-106">Requirements</span></span>



| <span data-ttu-id="5516a-107">Требование</span><span class="sxs-lookup"><span data-stu-id="5516a-107">Requirement</span></span> | <span data-ttu-id="5516a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5516a-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5516a-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5516a-109">Minimum supported client</span></span><br/> | <span data-ttu-id="5516a-110">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5516a-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5516a-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5516a-111">Minimum supported server</span></span><br/> | <span data-ttu-id="5516a-112">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5516a-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5516a-113">Header</span><span class="sxs-lookup"><span data-stu-id="5516a-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="5516a-114"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="5516a-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
