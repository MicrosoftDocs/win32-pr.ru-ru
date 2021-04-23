---
title: Многопоточные проблемы
description: Многопоточные проблемы
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411462"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="c1912-103">Многопоточные проблемы</span><span class="sxs-lookup"><span data-stu-id="c1912-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="c1912-104">Технология OLE обеспечивает поддержку многопоточных приложений, позволяя приложениям выполнять вызовы OLE из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="c1912-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="c1912-105">Эта Многопотоковая поддержка называется моделью подразделения, поэтому важно, чтобы все компоненты OLE, использующие несколько потоков, следовали этой модели.</span><span class="sxs-lookup"><span data-stu-id="c1912-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="c1912-106">Для модели апартамента необходимо, чтобы указатели интерфейса были упакованы (с использованием [**комаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)и [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) при передаче между потоками.</span><span class="sxs-lookup"><span data-stu-id="c1912-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1912-107">См. также</span><span class="sxs-lookup"><span data-stu-id="c1912-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1912-108">Процессы, потоки и подразделения</span><span class="sxs-lookup"><span data-stu-id="c1912-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




