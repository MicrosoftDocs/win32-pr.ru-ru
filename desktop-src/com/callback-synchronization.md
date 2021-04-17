---
title: Синхронизация обратного вызова
description: Синхронизация обратного вызова
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710376"
---
# <a name="callback-synchronization"></a><span data-ttu-id="92f47-103">Синхронизация обратного вызова</span><span class="sxs-lookup"><span data-stu-id="92f47-103">Callback Synchronization</span></span>

<span data-ttu-id="92f47-104">Асинхронный [API-интерфейс WinInet](/windows/desktop/WinInet/portal) (используемый для наиболее распространенных протоколов) оставляет синхронизацию механизма обратного вызова и вызывающего приложения в качестве упражнения для клиента.</span><span class="sxs-lookup"><span data-stu-id="92f47-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="92f47-105">Это сделано намеренно, так как оно обеспечивает максимальную степень гибкости.</span><span class="sxs-lookup"><span data-stu-id="92f47-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="92f47-106">Протоколы по умолчанию и реализация моникера URL выполняют эту синхронизацию и гарантируют, что приложения с одним потоком и потоковыми потоками никогда не должны справляться с состязаниями в стиле свободной цепочки.</span><span class="sxs-lookup"><span data-stu-id="92f47-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="92f47-107">То есть интерфейсы [**иенумформатетк**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) и [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) клиента вызываются только в соответствующих потоках.</span><span class="sxs-lookup"><span data-stu-id="92f47-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="92f47-108">Эта функция прозрачна для пользователя URL-адреса Ммоникер, если каждый поток, вызывающий [**IMoniker:: биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) и [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , имеет очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="92f47-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="92f47-109">Для асинхронной спецификации моникера требуется более точный контроль определения приоритетов и управления загрузкой, чем разрешено для WinSock или WinInet.</span><span class="sxs-lookup"><span data-stu-id="92f47-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="92f47-110">Соответственно, моникер URL-адреса управляет всеми загружаемыми файлами для любого потока вызывающего объекта, используя (в рамках синхронизации) схему приоритета на основе спецификации [**ибиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="92f47-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92f47-111">См. также</span><span class="sxs-lookup"><span data-stu-id="92f47-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f47-112">Моникеры URL-адресов</span><span class="sxs-lookup"><span data-stu-id="92f47-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 