---
description: '\_ \_ Тип данных context перечисления SCE является непрозрачным маркером, предоставляемым набором средств настройки безопасности. Он используется \_ функцией пфсце запроса \_ info для навигации по базе данных безопасности.'
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Сцесвк. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343115"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="36d24-104">\_контекст ПЕРЕЧИСЛЕНИЯ \_ SCE</span><span class="sxs-lookup"><span data-stu-id="36d24-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="36d24-105">Тип **данных \_ \_ context перечисления SCE** является непрозрачным маркером, предоставляемым набором средств настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="36d24-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="36d24-106">Он используется функцией [**пфсце \_ запроса \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) для навигации по базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="36d24-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="36d24-107">Требования</span><span class="sxs-lookup"><span data-stu-id="36d24-107">Requirements</span></span>



| <span data-ttu-id="36d24-108">Требование</span><span class="sxs-lookup"><span data-stu-id="36d24-108">Requirement</span></span> | <span data-ttu-id="36d24-109">Значение</span><span class="sxs-lookup"><span data-stu-id="36d24-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36d24-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36d24-110">Minimum supported client</span></span><br/> | <span data-ttu-id="36d24-111">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="36d24-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36d24-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36d24-112">Minimum supported server</span></span><br/> | <span data-ttu-id="36d24-113">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36d24-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36d24-114">Header</span><span class="sxs-lookup"><span data-stu-id="36d24-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="36d24-115"><dt>Сцесвк. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d24-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d24-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36d24-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d24-117">**\_ \_ сведения о запросе пфсце**</span><span class="sxs-lookup"><span data-stu-id="36d24-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

