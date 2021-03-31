---
title: Распространение сведений об ошибках
description: Распространение расширенных сведений об ошибках позволяет серверам, получающих RPC \_ S \_ \ Error, или любому другому коду ошибки, чтобы разрешить время выполнения RPC распространить полученную информацию вызывающим объектам.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888904"
---
# <a name="propagating-error-information"></a><span data-ttu-id="1d6cb-103">Распространение сведений об ошибках</span><span class="sxs-lookup"><span data-stu-id="1d6cb-103">Propagating Error Information</span></span>

<span data-ttu-id="1d6cb-104">Распространение расширенных сведений об ошибках позволяет серверам, которые получают \_ ошибку RPC S \_ \* , или любому другому коду ошибки, чтобы разрешить время выполнения RPC распространить сведения, полученные им на вызывающие объекты.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="1d6cb-105">Все серверы должны выполнить вызов [**рпкраисиксцептион**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) или [**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) при возникновении неустранимой ошибки.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="1d6cb-106">Время выполнения RPC отвечает за создание цепочки расширенных сведений об ошибках (если таковые имеются), что приводит к тому, что Неустранимая ошибка сообщает о самой неустранимой ошибке, если код ошибки, заданный для **рпкраисиксцептион** или **рпкасинкаборткалл** , совпадает с кодом ошибки, вызвавшим неустранимую ошибку.</span><span class="sxs-lookup"><span data-stu-id="1d6cb-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




