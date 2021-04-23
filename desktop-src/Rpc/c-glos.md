---
title: C (RPC)
description: Слова, начинающиеся с C, в глоссарии удаленного вызова процедур (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: da1ee843-c33e-42a1-bcaf-6cdb4834e70b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15eb37af87fd36dd31f3e9e106904b4ce734c15
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103988131"
---
# <a name="c-rpc"></a><span data-ttu-id="622de-103">C (RPC)</span><span class="sxs-lookup"><span data-stu-id="622de-103">C (RPC)</span></span>

<span data-ttu-id="622de-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G р [. J](i-glos.md) K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="622de-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="622de-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Служба каталогов ячеек (компакт-диски)**</span><span class="sxs-lookup"><span data-stu-id="622de-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory Service (CDS)**</span></span>
</dt> <dd>

<span data-ttu-id="622de-106">Имя — поставщик службы для среды распределенных вычислений в среде Open Software Foundation.</span><span class="sxs-lookup"><span data-stu-id="622de-106">Name-service provider for the Open Software Foundation's Distributed Computing Environment.</span></span>

</dd> <dt>

<span data-ttu-id="622de-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**Заглушка клиента**</span><span class="sxs-lookup"><span data-stu-id="622de-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**client stub**</span></span>
</dt> <dd>

<span data-ttu-id="622de-108">Созданный MIDL исходный код на языке C.</span><span class="sxs-lookup"><span data-stu-id="622de-108">MIDL-generated C-language source code.</span></span> <span data-ttu-id="622de-109">Он содержит все функции, необходимые клиентскому приложению для выполнения удаленных вызовов процедур с использованием модели традиционного вызова функции в автономном приложении.</span><span class="sxs-lookup"><span data-stu-id="622de-109">It contains all the functions necessary for the client application to make remote procedure calls using the model of a traditional function call in a standalone application.</span></span> <span data-ttu-id="622de-110">Клиентская заглушка отвечает за упаковку входных параметров и распаковать выходные параметры.</span><span class="sxs-lookup"><span data-stu-id="622de-110">The client stub is responsible for marshaling input parameters and unmarshaling output parameters.</span></span> <span data-ttu-id="622de-111">См. также [*заглушку сервера*](s-glos.md), [*прокси-*](p-glos.md)сервер.</span><span class="sxs-lookup"><span data-stu-id="622de-111">See also [*server stub*](s-glos.md), [*proxy stub*](p-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="622de-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**согласованный массив**</span><span class="sxs-lookup"><span data-stu-id="622de-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**conformant array**</span></span>
</dt> <dd>

<span data-ttu-id="622de-113">Массив, размер которого определяется во время выполнения другим параметром, полем структуры или выражением.</span><span class="sxs-lookup"><span data-stu-id="622de-113">Array whose size is determined at run time by another parameter, structure field, or expression.</span></span>

</dd> <dt>

<span data-ttu-id="622de-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**с ориентацией на подключения**</span><span class="sxs-lookup"><span data-stu-id="622de-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**connection-oriented**</span></span>
</dt> <dd>

<span data-ttu-id="622de-115">Протокол связи или транспорт, предоставляющий виртуальный канал, через который пакеты данных получаются в том же порядке, в котором они были переданы.</span><span class="sxs-lookup"><span data-stu-id="622de-115">Communications protocol or transport that provides a virtual circuit through which data packets are received in the same order as they were transmitted.</span></span> <span data-ttu-id="622de-116">Если подключение между компьютерами завершается сбоем, приложение получает уведомления.</span><span class="sxs-lookup"><span data-stu-id="622de-116">If the connection between computers fails, the application is notified.</span></span> <span data-ttu-id="622de-117">Протоколы [*TCP*](t-glos.md) и [*SPX*](s-glos.md) являются примерами протоколов, ориентированных на подключения.</span><span class="sxs-lookup"><span data-stu-id="622de-117">[*TCP*](t-glos.md) and [*SPX*](s-glos.md) are examples of connection-oriented protocols.</span></span> <span data-ttu-id="622de-118">См. также [*датаграмма*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="622de-118">See also [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="622de-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**Служба**</span><span class="sxs-lookup"><span data-stu-id="622de-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connectionless**</span></span>
</dt> <dd>

<span data-ttu-id="622de-120">См. сведения о [*датаграмме*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="622de-120">See [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="622de-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**Очистка контекста**</span><span class="sxs-lookup"><span data-stu-id="622de-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**context rundown**</span></span>
</dt> <dd>

<span data-ttu-id="622de-122">Уведомление сервера, полученное в результате непредвиденного завершения привязки между клиентскими и серверными приложениями.</span><span class="sxs-lookup"><span data-stu-id="622de-122">Server notification that results from an unexpected termination of the binding between client and server applications.</span></span>

</dd> </dl>

 

 




