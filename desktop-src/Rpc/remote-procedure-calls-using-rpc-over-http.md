---
title: Удаленные вызовы процедур с помощью RPC через HTTP
description: Программы Интернет-браузера обычно используют протокол HTTP в качестве основного средства просмотра в Интернете.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Удаленный вызов процедур RPC, задачи, использование RPC/HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986071"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="e23f7-104">Удаленные вызовы процедур с помощью RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="e23f7-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="e23f7-105">Программы Интернет-браузера обычно используют протокол HTTP в качестве основного средства просмотра в Интернете.</span><span class="sxs-lookup"><span data-stu-id="e23f7-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="e23f7-106">Поэтому в настоящее время протокол HTTP видит широкое использование на большинстве компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e23f7-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="e23f7-107">Корпорация Майкрософт расширила возможности сервера IIS для предоставления служб удаленного вызова процедур по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="e23f7-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="e23f7-108">Реализация Microsoft RPC-over-HTTP (RPC через HTTP) позволяет клиентам RPC безопасно и эффективно подключаться через Интернет к программам сервера RPC и выполнять удаленные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="e23f7-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="e23f7-109">Это достигается за счет использования промежуточного посредника, известного как прокси RPC-over-HTTP, или просто прокси RPC.</span><span class="sxs-lookup"><span data-stu-id="e23f7-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="e23f7-110">Прокси-сервер RPC работает на компьютере IIS.</span><span class="sxs-lookup"><span data-stu-id="e23f7-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="e23f7-111">Он принимает запросы RPC, поступающие из Интернета, выполняет проверку подлинности, проверку и проверку доступа для этих запросов. Если запрос проходит все тесты, прокси-сервер RPC перенаправляет запрос серверу RPC, который выполняет фактическую обработку.</span><span class="sxs-lookup"><span data-stu-id="e23f7-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="e23f7-112">При использовании RPC через HTTP клиент RPC и сервер не обмениваются данными напрямую; Вместо этого они используют прокси-сервер RPC в качестве посредника.</span><span class="sxs-lookup"><span data-stu-id="e23f7-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="e23f7-113">Эта модель была выбрана по многим причинам.</span><span class="sxs-lookup"><span data-stu-id="e23f7-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="e23f7-114">Дополнительные сведения см. в разделе [RPC over HTTP Security](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="e23f7-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="e23f7-115">В этом разделе приводится обзор RPC через HTTP в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e23f7-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="e23f7-116">Использование HTTP в качестве транспорта RPC</span><span class="sxs-lookup"><span data-stu-id="e23f7-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="e23f7-117">Безопасность RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="e23f7-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="e23f7-118">Требования к системе и взаимодействие для RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="e23f7-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="e23f7-119">Настройка компьютеров для RPC через HTTP</span><span class="sxs-lookup"><span data-stu-id="e23f7-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="e23f7-120">Рекомендации по развертыванию RPC по HTTP</span><span class="sxs-lookup"><span data-stu-id="e23f7-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="e23f7-121">Сведения о сценариях RPC по протоколу HTTP для большого объема см. в [статье балансировка нагрузки Microsoft RPC](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="e23f7-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




