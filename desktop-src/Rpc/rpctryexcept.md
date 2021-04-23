---
title: Рпктрексцепт (RPC. h)
description: Инструкция Рпктрексцепт обеспечивает структурированную обработку исключений для приложений RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- Рпктрексцепт RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136363"
---
# <a name="rpctryexcept"></a><span data-ttu-id="99586-104">рпктрексцепт</span><span class="sxs-lookup"><span data-stu-id="99586-104">RpcTryExcept</span></span>

<span data-ttu-id="99586-105">Инструкция **рпктрексцепт** обеспечивает структурированную обработку исключений для приложений RPC.</span><span class="sxs-lookup"><span data-stu-id="99586-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="99586-106">Если любая из инструкций программы в **рпктрексцепт** вызывает исключение, выполняются инструкции в блоке кода [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="99586-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="99586-107">Все инструкции **рпктрексцепт** должны завершаться инструкцией [**рпцендексцепт**](/previous-versions/aa375629(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="99586-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="99586-108">Дополнительные сведения см. в разделе [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="99586-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="99586-109">**Windows Vista и более поздние версии Windows:**  [**рпцексцептионфилтер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) рекомендуется для структурированной обработки исключений наиболее распространенных исключений в качестве альтернативы настраиваемым фильтрам с помощью [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="99586-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="99586-110">Требования</span><span class="sxs-lookup"><span data-stu-id="99586-110">Requirements</span></span>



| <span data-ttu-id="99586-111">Требование</span><span class="sxs-lookup"><span data-stu-id="99586-111">Requirement</span></span> | <span data-ttu-id="99586-112">Значение</span><span class="sxs-lookup"><span data-stu-id="99586-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="99586-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99586-113">Minimum supported client</span></span><br/> | <span data-ttu-id="99586-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99586-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="99586-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99586-115">Minimum supported server</span></span><br/> | <span data-ttu-id="99586-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99586-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99586-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="99586-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="99586-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="99586-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99586-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99586-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99586-120">**рпцексцепт**</span><span class="sxs-lookup"><span data-stu-id="99586-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="99586-121">**рпцексцептионфилтер**</span><span class="sxs-lookup"><span data-stu-id="99586-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="99586-122">**рпктрифиналли**</span><span class="sxs-lookup"><span data-stu-id="99586-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

