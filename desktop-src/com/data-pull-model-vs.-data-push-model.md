---
title: Модель Data-Pull и модель Data-Push
description: Модель Data-Pull и модель Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413885"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="54c4e-103">Модель Data-Pull и модель Data-Push</span><span class="sxs-lookup"><span data-stu-id="54c4e-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="54c4e-104">Клиент асинхронного моникера может выбирать между моделью извлечения данных и принудительной отправкой данных для выполнения асинхронной операции [**IMoniker:: биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) и получения асинхронных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="54c4e-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="54c4e-105">В модели извлечения данных клиент выполняет операцию привязки, и моникер предоставляет клиенту данные только по мере их считывания.</span><span class="sxs-lookup"><span data-stu-id="54c4e-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="54c4e-106">Иными словами, после первого вызова [**метода интерфейса IBindStatusCallback:: ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))моникер не предоставляет клиенту никаких данных, если клиент не потребляет все данные, которые уже доступны.</span><span class="sxs-lookup"><span data-stu-id="54c4e-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="54c4e-107">Поскольку данные загружаются только по запросу, клиенты, которые выбирают модель извлечения данных, должны своевременно считывать эти данные.</span><span class="sxs-lookup"><span data-stu-id="54c4e-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="54c4e-108">В случае загрузки из Интернета с [моникерами URL-адресов](url-monikers.md)операция привязки может завершиться ошибкой, если клиент ожидает слишком долго перед запросом дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="54c4e-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="54c4e-109">В модели передачи данных моникер управляет асинхронной операцией привязки и постоянно уведомляет клиента каждый раз, когда новые данные доступны.</span><span class="sxs-lookup"><span data-stu-id="54c4e-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="54c4e-110">Клиент может выбрать, следует ли считывать данные в любой момент во время операции привязки, но моникер будет выполнять операцию привязки к завершению независимо.</span><span class="sxs-lookup"><span data-stu-id="54c4e-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="54c4e-111">Кроме того, необходимо следовать правилам COM для выделения памяти при использовании асинхронных моникеров, в частности следующих:</span><span class="sxs-lookup"><span data-stu-id="54c4e-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="54c4e-112">Всякий раз, когда COM-интерфейс или вызов функции возвращает буфер (строку или другой) клиенту, клиент несет ответственность за освобождение памяти путем вызова [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="54c4e-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="54c4e-113">Каждый раз, когда интерфейсу или функции COM требуется буфер от клиента, клиент должен выделить этот буфер с помощью метода [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) , и вызываемый объект должен освободить его.</span><span class="sxs-lookup"><span data-stu-id="54c4e-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="54c4e-114">Следует соблюдать эти правила при выделении строк или буферов, передаваемых в асинхронные моникеры, и не забывайте освобождать память, возвращенную асинхронными моникерами.</span><span class="sxs-lookup"><span data-stu-id="54c4e-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="54c4e-115">Подробные сведения см. в разделе [Управление выделением памяти](the-com-library.md) и связанными разделами.</span><span class="sxs-lookup"><span data-stu-id="54c4e-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54c4e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="54c4e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c4e-117">Асинхронные моникеры</span><span class="sxs-lookup"><span data-stu-id="54c4e-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 