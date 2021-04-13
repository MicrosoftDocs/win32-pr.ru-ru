---
title: WS_SECURITY_TOKEN (WebService. h)
description: Непрозрачный маркер, представляющий маркер безопасности.
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52e69a46f206f1def7cc2e7e2d03c2e5f1369f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491241"
---
# <a name="ws_security_token"></a><span data-ttu-id="ee027-104">\_токен безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="ee027-104">WS\_SECURITY\_TOKEN</span></span>

<span data-ttu-id="ee027-105">Непрозрачный маркер, представляющий [маркер безопасности](security-processing-results.md).</span><span class="sxs-lookup"><span data-stu-id="ee027-105">The opaque handle representing a [security token](security-processing-results.md).</span></span>


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
```



## <a name="remarks"></a><span data-ttu-id="ee027-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee027-106">Remarks</span></span>

<span data-ttu-id="ee027-107">Этот объект не является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="ee027-107">This object is not thread safe.</span></span> <span data-ttu-id="ee027-108">Дополнительные сведения см. в статье [безопасность потоков](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="ee027-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee027-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ee027-109">Requirements</span></span>



| <span data-ttu-id="ee027-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ee027-110">Requirement</span></span> | <span data-ttu-id="ee027-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ee027-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee027-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee027-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ee027-113">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ee027-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ee027-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee027-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ee027-115">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ee027-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ee027-116">Header</span><span class="sxs-lookup"><span data-stu-id="ee027-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee027-117"><dt>WebService. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee027-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee027-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee027-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee027-119">Результаты обработки безопасности</span><span class="sxs-lookup"><span data-stu-id="ee027-119">Security Processing Results</span></span>](security-processing-results.md)
</dt> <dt>

[<span data-ttu-id="ee027-120">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ee027-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





