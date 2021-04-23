---
description: Особое внимание должно быть уделено многосетевым отправителям или получателям PGM. На этой странице описываются рекомендации и приводятся рекомендации по оптимальным методикам программирования.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Многосайтовое и PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656117"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="19dd4-104">Многосайтовое и PGM</span><span class="sxs-lookup"><span data-stu-id="19dd4-104">Multihoming and PGM</span></span>

<span data-ttu-id="19dd4-105">Особое внимание должно быть уделено многосетевым отправителям или получателям PGM.</span><span class="sxs-lookup"><span data-stu-id="19dd4-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="19dd4-106">На этой странице описываются рекомендации и приводятся рекомендации по оптимальным методикам программирования.</span><span class="sxs-lookup"><span data-stu-id="19dd4-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="19dd4-107">Многосетевой отправитель PGM</span><span class="sxs-lookup"><span data-stu-id="19dd4-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="19dd4-108">Когда приложению не удается указать интерфейс при вызове функции [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , используется первый доступный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="19dd4-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="19dd4-109">Если интерфейс недоступен, **Подключение** не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19dd4-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="19dd4-110">Если приложение указывает интерфейс с помощью параметра [RM \_ Set \_ Send \_](socket-options.md) , то попытка [**привязки**](/windows/desktop/api/winsock/nf-winsock-bind) выполняется НЕЯВНО к этому интерфейсу с помощью TCP/IP и завершается ошибкой, если TCP/IP не может выполнить запрос на привязку.</span><span class="sxs-lookup"><span data-stu-id="19dd4-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="19dd4-111">Если интерфейс задается с помощью команды RM \_ Set \_ Send \_ несколько раз, применяется только последний набор интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="19dd4-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="19dd4-112">Сокеты Windows сохраняют, какой интерфейс задан, и если этот интерфейс исчезает, сеанс отключается.</span><span class="sxs-lookup"><span data-stu-id="19dd4-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="19dd4-113">Многосетевой приемник PGM</span><span class="sxs-lookup"><span data-stu-id="19dd4-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="19dd4-114">Когда приложению не удается указать интерфейс при вызове функции [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , используется интерфейс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19dd4-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="19dd4-115">Если интерфейс недоступен, произойдет сбой [**привязки**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="19dd4-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="19dd4-116">Если приложение указывает один или несколько интерфейсов для прослушивания, при помощи команды [RM \_ Add Receive, \_ \_ Если](socket-options.md)сокеты Windows пытаются выполнить привязку к запрошенному интерфейсу или интерфейсам с помощью TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="19dd4-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="19dd4-117">Любая ошибка из TCP/IP приводит к сбою запроса.</span><span class="sxs-lookup"><span data-stu-id="19dd4-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="19dd4-118">В отличие от случая отправителя PGM, Добавление интерфейса получения несколько раз приводит к тому, что прослушивает все успешно добавленные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="19dd4-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="19dd4-119">Используйте команду RM \_ Del \_ Receive, \_ Если сокет используется для прекращения прослушивания интерфейса.</span><span class="sxs-lookup"><span data-stu-id="19dd4-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="19dd4-120">Сокеты Windows не поддерживают состояние нескольких указанных интерфейсов прослушивания, а вместо этого используют TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="19dd4-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="19dd4-121">Однако после выполнения сеанса сокеты Windows отключают входящий интерфейс для этого сеанса и, если этот интерфейс исчезает, сокеты Windows отключает сеанс.</span><span class="sxs-lookup"><span data-stu-id="19dd4-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



