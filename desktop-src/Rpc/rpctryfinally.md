---
title: Рпктрифиналли (RPC. h)
description: Инструкция Рпктрифиналли обеспечивает структурированную обработку завершения.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- Рпктрифиналли RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491397"
---
# <a name="rpctryfinally"></a><span data-ttu-id="ad733-104">рпктрифиналли</span><span class="sxs-lookup"><span data-stu-id="ad733-104">RpcTryFinally</span></span>

<span data-ttu-id="ad733-105">Инструкция **рпктрифиналли** обеспечивает структурированную обработку завершения.</span><span class="sxs-lookup"><span data-stu-id="ad733-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="ad733-106">Это исключение возникает во время выполнения инструкций блока кода, связанного с инструкцией **рпктрифиналли** , для выполнения инструкций в блоке кода, связанного с инструкцией [**рпкфиналли**](/previous-versions/aa375699(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="ad733-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="ad733-107">Все инструкции **рпктрифиналли** должны завершаться инструкцией [**рпцендфиналли**](/previous-versions/aa375634(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="ad733-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="ad733-108">Дополнительные сведения см. в разделе [**рпкфиналли**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="ad733-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad733-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ad733-109">Requirements</span></span>



| <span data-ttu-id="ad733-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ad733-110">Requirement</span></span> | <span data-ttu-id="ad733-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ad733-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ad733-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad733-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ad733-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad733-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ad733-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad733-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ad733-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad733-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ad733-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ad733-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad733-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad733-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad733-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad733-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad733-119">[**рпкфиналли**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="ad733-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="ad733-120">[**рпцендфиналли**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="ad733-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

