---
title: Делегирование QueryInterface
description: Делегирование QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134634"
---
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="23c55-103">Делегирование QueryInterface</span><span class="sxs-lookup"><span data-stu-id="23c55-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="23c55-104">Обработчики, которым требуется доступ к некоторым внутренним интерфейсам в диспетчере прокси-сервера, должны проходить через интерфейс [**иинтерналункновн**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) .</span><span class="sxs-lookup"><span data-stu-id="23c55-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="23c55-105">Это предотвращает появление обработчиками скрытого делегирования и доступа к внутренним интерфейсам агрегата за пределами статистической функции.</span><span class="sxs-lookup"><span data-stu-id="23c55-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="23c55-106">К этим интерфейсам относятся [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) и [**имултики**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="23c55-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="23c55-107">Если обработчик хочет предоставить **иклиентсекурити** или **имултики**, он должен реализовать их сами.</span><span class="sxs-lookup"><span data-stu-id="23c55-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="23c55-108">В случае с [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), если клиент пытается установить безопасность интерфейса, предоставленного обработчиком, обработчик должен установить безопасность на базовом прокси-сервере сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="23c55-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="23c55-109">В случае с [**имултики**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)обработчик должен заполнить интерфейсы, о которых он знает, а затем перенаправить вызов диспетчеру прокси-сервера для получения остальных интерфейсов, заполненных.</span><span class="sxs-lookup"><span data-stu-id="23c55-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23c55-110">См. также</span><span class="sxs-lookup"><span data-stu-id="23c55-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c55-111">Упрощенный обработчик Client-Side</span><span class="sxs-lookup"><span data-stu-id="23c55-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 