---
title: Асинхронное и синхронное хранилище
description: Асинхронное и синхронное хранилище
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533545"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="1f82b-103">Асинхронное и синхронное хранилище</span><span class="sxs-lookup"><span data-stu-id="1f82b-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="1f82b-104">Асинхронные моникеры также могут возвращать [асинхронный объект хранилища](/windows/desktop/Stg/asynchronous-storage) в уведомлении [**метода интерфейса IBindStatusCallback:: ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1f82b-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="1f82b-105">Этот объект хранилища может разрешить доступ к некоторым из постоянных данных объекта, пока привязка еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f82b-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="1f82b-106">Клиент может выбрать один из двух режимов хранения: Блокировка и неблокировка.</span><span class="sxs-lookup"><span data-stu-id="1f82b-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="1f82b-107">В режиме блокировки, который совместим с текущими реализациями объектов хранилища, если данные недоступны, вызов блокируется до поступления данных.</span><span class="sxs-lookup"><span data-stu-id="1f82b-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="1f82b-108">В неблокирующем режиме, вместо того чтобы блокировать вызов, объект хранилища возвращает новую ошибку E Pending, \_ когда данные недоступны.</span><span class="sxs-lookup"><span data-stu-id="1f82b-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="1f82b-109">Клиент, осведомленный о асинхронной привязке и хранилище, задерживает эту ошибку и ожидает дальнейших уведомлений ([**ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))), чтобы повторить операцию.</span><span class="sxs-lookup"><span data-stu-id="1f82b-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="1f82b-110">Клиент может выбрать между синхронным (блокирующее) и асинхронным (неблочным) хранилищем, выбрав, следует ли установить \_ флаг биндф асинкстораже в значении *грфбиндф* , возвращаемом в [**метода интерфейса IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f82b-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f82b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1f82b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f82b-112">Асинхронные моникеры</span><span class="sxs-lookup"><span data-stu-id="1f82b-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 