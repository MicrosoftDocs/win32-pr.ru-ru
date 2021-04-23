---
title: Олицетворение и асинхронные вызовы
description: Олицетворение и асинхронные вызовы
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794160"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="04562-103">Олицетворение и асинхронные вызовы</span><span class="sxs-lookup"><span data-stu-id="04562-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="04562-104">Серверу не удается выполнить олицетворение клиента после вызова сервера [**исинчронизе:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) , даже если \_ метод Begin еще не завершен.</span><span class="sxs-lookup"><span data-stu-id="04562-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="04562-105">Например, предположим, что клиент вызывает метод Begin \_ , сервер немедленно обрабатывает вызов, а сервер вызывает **сигнал** , чтобы показать, что обработка завершена.</span><span class="sxs-lookup"><span data-stu-id="04562-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="04562-106">Даже если работа остается в \_ методе Begin, сервер не может олицетворять клиента после завершения вызова **сигнала** .</span><span class="sxs-lookup"><span data-stu-id="04562-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="04562-107">Если сервер олицетворяет клиента перед вызовом [**сигнала**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), маркер олицетворения не будет удален из потока, пока сервер не вызовет [**Исерверсекурити:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) или пока не выполнит вызов сервера, в зависимости от того \_ , что происходит первым.</span><span class="sxs-lookup"><span data-stu-id="04562-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04562-108">См. также</span><span class="sxs-lookup"><span data-stu-id="04562-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04562-109">Делегирование и олицетворение</span><span class="sxs-lookup"><span data-stu-id="04562-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="04562-110">Выполнение асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="04562-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 