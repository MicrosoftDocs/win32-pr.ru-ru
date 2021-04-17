---
title: Справочник по функциям
description: В этом разделе описываются функции времени выполнения удаленного вызова процедур (RPC), поддерживаемые в Microsoft RPC.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486821"
---
# <a name="function-reference"></a><span data-ttu-id="3d47c-103">Справочник по функциям</span><span class="sxs-lookup"><span data-stu-id="3d47c-103">Function Reference</span></span>

<span data-ttu-id="3d47c-104">В этом разделе описываются функции времени выполнения удаленного вызова процедур (RPC), поддерживаемые в Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="3d47c-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="3d47c-105">В этом разделе описывается назначение функции, синтаксис, входные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="3d47c-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="3d47c-106">В нем также содержатся дополнительные сведения, помогающие использовать функции RPC в приложении.</span><span class="sxs-lookup"><span data-stu-id="3d47c-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="3d47c-107">Все указатели, передаваемые в функции RPC, должны включать атрибут **\_ \_ RPC \_ FAR** .</span><span class="sxs-lookup"><span data-stu-id="3d47c-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="3d47c-108">Например, **\_ \_ маркер \* привязки RPC** в указателе преобразуется в **RPC- \_ \_ \_ \_ вызов \_ \* обработчика привязки** RPC, а **char \* \*** *ptr*  **\_ \_ \_ \* \_ \_ \_ \* — в дальнем** времени RPC типа RPC.</span><span class="sxs-lookup"><span data-stu-id="3d47c-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="3d47c-109">В этом разделе представлены ссылки на функции в следующих группах:</span><span class="sxs-lookup"><span data-stu-id="3d47c-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="3d47c-110">Функции RPC</span><span class="sxs-lookup"><span data-stu-id="3d47c-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="3d47c-111">Функции обратного вызова и уведомления RPC</span><span class="sxs-lookup"><span data-stu-id="3d47c-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




