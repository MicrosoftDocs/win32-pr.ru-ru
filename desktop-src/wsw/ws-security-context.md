---
title: WS_SECURITY_CONTEXT (WebService. h)
description: Непрозрачный тип, используемый для ссылки на объект контекста безопасности.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136271"
---
# <a name="ws_security_context"></a><span data-ttu-id="a56e2-104">\_контекст безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="a56e2-104">WS\_SECURITY\_CONTEXT</span></span>

<span data-ttu-id="a56e2-105">Непрозрачный тип, используемый для ссылки на [объект контекста безопасности](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="a56e2-105">An opaque type used to reference a [security context object](security-context.md).</span></span>


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a><span data-ttu-id="a56e2-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a56e2-106">Remarks</span></span>

<span data-ttu-id="a56e2-107">Этот объект не является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="a56e2-107">This object is not thread safe.</span></span> <span data-ttu-id="a56e2-108">Дополнительные сведения см. в статье [безопасность потоков](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="a56e2-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a56e2-109">Требования</span><span class="sxs-lookup"><span data-stu-id="a56e2-109">Requirements</span></span>



| <span data-ttu-id="a56e2-110">Требование</span><span class="sxs-lookup"><span data-stu-id="a56e2-110">Requirement</span></span> | <span data-ttu-id="a56e2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a56e2-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56e2-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a56e2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a56e2-113">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a56e2-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a56e2-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a56e2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a56e2-115">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="a56e2-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a56e2-116">Header</span><span class="sxs-lookup"><span data-stu-id="a56e2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a56e2-117"><dt>WebService. h</dt></span><span class="sxs-lookup"><span data-stu-id="a56e2-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a56e2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a56e2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56e2-119">Контекст безопасности</span><span class="sxs-lookup"><span data-stu-id="a56e2-119">Security Context</span></span>](security-context.md)
</dt> <dt>

[<span data-ttu-id="a56e2-120">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a56e2-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





