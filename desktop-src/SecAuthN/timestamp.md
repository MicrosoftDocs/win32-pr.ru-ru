---
description: Тип данных TimeStamp содержит сведения о допустимости времени маркеров безопасности. Формат значения типа данных TimeStamp совпадает со значением структуры FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Метка времени (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647275"
---
# <a name="timestamp"></a><span data-ttu-id="86d4b-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="86d4b-104">TimeStamp</span></span>

<span data-ttu-id="86d4b-105">Тип данных **timestamp** содержит сведения о допустимости времени маркеров безопасности.</span><span class="sxs-lookup"><span data-stu-id="86d4b-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="86d4b-106">Формат значения типа данных **timestamp** совпадает со значением структуры [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="86d4b-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="86d4b-107">Требования</span><span class="sxs-lookup"><span data-stu-id="86d4b-107">Requirements</span></span>



| <span data-ttu-id="86d4b-108">Требование</span><span class="sxs-lookup"><span data-stu-id="86d4b-108">Requirement</span></span> | <span data-ttu-id="86d4b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="86d4b-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86d4b-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86d4b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="86d4b-111">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="86d4b-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="86d4b-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86d4b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="86d4b-113">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86d4b-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="86d4b-114">Header</span><span class="sxs-lookup"><span data-stu-id="86d4b-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="86d4b-115"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86d4b-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 
