---
description: Представляет маркер для набора устанавливаемых функций идентификатора объекта (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: ХКРИПТОИДФУНКСЕТ (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664118"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="d8d35-103">хкриптоидфунксет</span><span class="sxs-lookup"><span data-stu-id="d8d35-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="d8d35-104">Тип данных **хкриптоидфунксет** представляет собой маркер набора устанавливаемых функций [*идентификатора объекта*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="d8d35-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="d8d35-105">Функции [**криптжетдефаултоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**криптжетоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**криптфриоидфунктионаддресс**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)и [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) используют этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="d8d35-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="d8d35-106">Требования</span><span class="sxs-lookup"><span data-stu-id="d8d35-106">Requirements</span></span>



| <span data-ttu-id="d8d35-107">Требование</span><span class="sxs-lookup"><span data-stu-id="d8d35-107">Requirement</span></span> | <span data-ttu-id="d8d35-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d8d35-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d35-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8d35-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d35-110">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d8d35-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d8d35-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8d35-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d35-112">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8d35-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8d35-113">Header</span><span class="sxs-lookup"><span data-stu-id="d8d35-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8d35-114"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d35-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
