---
description: '\_Тип данных Handle обработчика SCE является непрозрачным маркером, предоставляемым набором средств настройки безопасности. Он используется в ПФСЦЕ \_ запроса \_ info и \_ \_ функциях поддержки пфсце Set info для передачи информации между вложением и базой данных безопасности.'
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Сцесвк. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144437"
---
# <a name="sce_handle"></a><span data-ttu-id="96a12-104">\_обработчик SCE</span><span class="sxs-lookup"><span data-stu-id="96a12-104">SCE\_HANDLE</span></span>

<span data-ttu-id="96a12-105">Тип **данных \_ Handle обработчика SCE** является непрозрачным маркером, предоставляемым набором средств настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="96a12-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="96a12-106">Он используется в [**пфсце \_ запроса \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) и функциях поддержки [**пфсце \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) для передачи информации между вложением и базой данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="96a12-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="96a12-107">Требования</span><span class="sxs-lookup"><span data-stu-id="96a12-107">Requirements</span></span>



| <span data-ttu-id="96a12-108">Требование</span><span class="sxs-lookup"><span data-stu-id="96a12-108">Requirement</span></span> | <span data-ttu-id="96a12-109">Значение</span><span class="sxs-lookup"><span data-stu-id="96a12-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="96a12-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96a12-110">Minimum supported client</span></span><br/> | <span data-ttu-id="96a12-111">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96a12-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96a12-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96a12-112">Minimum supported server</span></span><br/> | <span data-ttu-id="96a12-113">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96a12-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="96a12-114">Header</span><span class="sxs-lookup"><span data-stu-id="96a12-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a12-115"><dt>Сцесвк. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a12-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a12-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96a12-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a12-117">**\_ \_ сведения о запросе пфсце**</span><span class="sxs-lookup"><span data-stu-id="96a12-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="96a12-118">**\_сведения о наборе пфсце \_**</span><span class="sxs-lookup"><span data-stu-id="96a12-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

