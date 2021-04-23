---
title: Отмена асинхронного вызова
description: Клиент может отменить асинхронный вызов, который выполняется, если объект вызова реализует интерфейс Иканцелмесодкаллс.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134658"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="dd833-103">Отмена асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="dd833-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="dd833-104">Клиент может отменить асинхронный вызов, который выполняется, если объект вызова реализует интерфейс [**иканцелмесодкаллс**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="dd833-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="dd833-105">Для объектов, использующих стандартный маршалирование, **иканцелмесодкаллс** всегда доступен для упакованных вызовов.</span><span class="sxs-lookup"><span data-stu-id="dd833-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="dd833-106">Для объектов, использующих настраиваемое маршалирование или для вызовов к серверным объектам в пределах одного подразделения, эта функция доступна, только если объект вызова реализует **иканцелмесодкаллс**.</span><span class="sxs-lookup"><span data-stu-id="dd833-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="dd833-107">Клиент может в любое время отменить вызов, от момента \_ вызова метода Begin до \_ возврата методом Finish.</span><span class="sxs-lookup"><span data-stu-id="dd833-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="dd833-108">Если клиент отменяет вызов до вызова \_ метода Finish, он должен вызвать метод Finish, \_ чтобы очистить состояние объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="dd833-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="dd833-109">Пока клиент не закончит работу, любые вызовы любого метода Begin \_ в объекте Call будут возвращать вызов RPC \_ E \_ Call \_ .</span><span class="sxs-lookup"><span data-stu-id="dd833-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="dd833-110">**Отмена асинхронного вызова**</span><span class="sxs-lookup"><span data-stu-id="dd833-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="dd833-111">Запросите объект Call для [**иканцелмесодкаллс**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span><span class="sxs-lookup"><span data-stu-id="dd833-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="dd833-112">Вызовите метод [**иканцелмесодкаллс:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), а затем вызовите метод [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить указатель, полученный вызовом [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="dd833-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="dd833-113">Если клиент еще не вызвал \_ метод Finish, вызовите его сейчас.</span><span class="sxs-lookup"><span data-stu-id="dd833-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="dd833-114">Нет никакой гарантии, что сервер фактически остановил выполнение вызова.</span><span class="sxs-lookup"><span data-stu-id="dd833-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="dd833-115">Если работа клиента зависит от состояния сервера, которое вызов может измениться, клиент должен определить это состояние перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="dd833-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd833-116">См. также</span><span class="sxs-lookup"><span data-stu-id="dd833-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd833-117">Выполнение асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="dd833-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 