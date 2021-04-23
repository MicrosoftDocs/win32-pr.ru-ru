---
description: Непрозрачный тип данных.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Нтсекпкг. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264686"
---
# <a name="plsa_client_request"></a><span data-ttu-id="bed59-103">\_запрос клиента \_ плса</span><span class="sxs-lookup"><span data-stu-id="bed59-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="bed59-104">Тип **данных \_ \_ запроса клиента плса** является непрозрачным типом данных.</span><span class="sxs-lookup"><span data-stu-id="bed59-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="bed59-105">[*Локальный центр безопасности*](../secgloss/l-gly.md) (LSA) использует его для внутренних целей, чтобы поддерживать клиентскую информацию, относящуюся к отдельным запросам.</span><span class="sxs-lookup"><span data-stu-id="bed59-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="bed59-106">Требования</span><span class="sxs-lookup"><span data-stu-id="bed59-106">Requirements</span></span>



| <span data-ttu-id="bed59-107">Требование</span><span class="sxs-lookup"><span data-stu-id="bed59-107">Requirement</span></span> | <span data-ttu-id="bed59-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bed59-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bed59-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bed59-109">Minimum supported client</span></span><br/> | <span data-ttu-id="bed59-110">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bed59-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bed59-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bed59-111">Minimum supported server</span></span><br/> | <span data-ttu-id="bed59-112">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bed59-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bed59-113">Header</span><span class="sxs-lookup"><span data-stu-id="bed59-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed59-114"><dt>Нтсекпкг. h</dt></span><span class="sxs-lookup"><span data-stu-id="bed59-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
