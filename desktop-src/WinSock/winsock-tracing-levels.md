---
description: Дополнительные сведения см. в статье уровни трассировки Winsock.
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Уровни трассировки Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712533"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="5c801-103">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="5c801-104">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="5c801-105">В трассировке Winsock возможны два уровня ведения журнала:</span><span class="sxs-lookup"><span data-stu-id="5c801-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="5c801-106">Сведения</span><span class="sxs-lookup"><span data-stu-id="5c801-106">Information</span></span>
-   <span data-ttu-id="5c801-107">Подробный</span><span class="sxs-lookup"><span data-stu-id="5c801-107">Verbose</span></span>

<span data-ttu-id="5c801-108">Информационный уровень отслеживает события создания и закрытия сокета, а также любые ошибки, возникающие на сокете.</span><span class="sxs-lookup"><span data-stu-id="5c801-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="5c801-109">Уровень подробных данных включает события уровня информации и добавляет дополнительную трассировку для событий отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="5c801-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="5c801-110">Подробное ведение журнала используется для перехвата проблем с повреждением буфера, а также для плохо написанных приложений.</span><span class="sxs-lookup"><span data-stu-id="5c801-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="5c801-111">Уровень Information или verbose можно использовать с трассировкой событий сети Winsock.</span><span class="sxs-lookup"><span data-stu-id="5c801-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="5c801-112">Трассировка изменений каталога Winsock поддерживает только уровень информации.</span><span class="sxs-lookup"><span data-stu-id="5c801-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="5c801-113">Трассировка информационных событий</span><span class="sxs-lookup"><span data-stu-id="5c801-113">Information Event Tracing</span></span>

<span data-ttu-id="5c801-114">В следующем списке приведены сведения об операциях сокета сетевых событий Winsock, которые отслеживаются на уровне информации:</span><span class="sxs-lookup"><span data-stu-id="5c801-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="5c801-115">Создание сокета</span><span class="sxs-lookup"><span data-stu-id="5c801-115">Socket creation</span></span>

    <span data-ttu-id="5c801-116">Событие заносится в журнал при создании сокета, который может использоваться для трассировки времени существования сокета.</span><span class="sxs-lookup"><span data-stu-id="5c801-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="5c801-117">Эти события также включают сокеты, созданные с помощью приема соединений на сокете прослушивания.</span><span class="sxs-lookup"><span data-stu-id="5c801-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="5c801-118">Bind</span><span class="sxs-lookup"><span data-stu-id="5c801-118">Bind</span></span>

    <span data-ttu-id="5c801-119">Локальный IP-адрес заносится в журнал, чтобы помочь сопоставлять данные трассировки Winsock с вызовами сокета приложения.</span><span class="sxs-lookup"><span data-stu-id="5c801-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="5c801-120">Подключение</span><span class="sxs-lookup"><span data-stu-id="5c801-120">Connect</span></span>

    <span data-ttu-id="5c801-121">Удаленный IP-адрес подключенного сокета заносится в журнал, чтобы помочь сопоставить данные трассировки Winsock с вызовами сокета приложения.</span><span class="sxs-lookup"><span data-stu-id="5c801-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="5c801-122">Winsock — инициированные прерывания и отмены</span><span class="sxs-lookup"><span data-stu-id="5c801-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="5c801-123">Когда Winsock активно прерывает или отменяет запрос, событие заносится в журнал.</span><span class="sxs-lookup"><span data-stu-id="5c801-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="5c801-124">Сброс инициированного транспорта</span><span class="sxs-lookup"><span data-stu-id="5c801-124">Transport initiated resets</span></span>

    <span data-ttu-id="5c801-125">Когда базовый транспорт указывает, что подключение сброшено, событие заносится в журнал.</span><span class="sxs-lookup"><span data-stu-id="5c801-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="5c801-126">Ошибки отправки и получения</span><span class="sxs-lookup"><span data-stu-id="5c801-126">Send and receive errors</span></span>

    <span data-ttu-id="5c801-127">При сбое вызова Send или Receive к базовому транспорту событие регистрируется в журнале.</span><span class="sxs-lookup"><span data-stu-id="5c801-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="5c801-128">Отключение сокета и закрытие</span><span class="sxs-lookup"><span data-stu-id="5c801-128">Socket disconnect and close</span></span>

    <span data-ttu-id="5c801-129">Событие регистрируется при закрытии маркера сокета.</span><span class="sxs-lookup"><span data-stu-id="5c801-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="5c801-130">Подробная трассировка событий</span><span class="sxs-lookup"><span data-stu-id="5c801-130">Verbose Event Tracing</span></span>

<span data-ttu-id="5c801-131">Все информационные события отслеживаются на уровне подробных данных.</span><span class="sxs-lookup"><span data-stu-id="5c801-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="5c801-132">В следующем списке приведены дополнительные операции сокета событий сети Winsock, которые отслеживаются на уровне подробных данных.</span><span class="sxs-lookup"><span data-stu-id="5c801-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="5c801-133">Буферы отправки и получения</span><span class="sxs-lookup"><span data-stu-id="5c801-133">Send and receive buffers</span></span>

    <span data-ttu-id="5c801-134">События записываются в журнал для адресов буфера пользователя и длины, когда вызовы Send и Receive публикуются в Winsock, а также после завершения этих вызовов.</span><span class="sxs-lookup"><span data-stu-id="5c801-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="5c801-135">Это полезно для диагностики проблем повторного использования буфера, а также для неэффективного использования буферов.</span><span class="sxs-lookup"><span data-stu-id="5c801-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="5c801-136">Параметры сокета</span><span class="sxs-lookup"><span data-stu-id="5c801-136">Socket options</span></span>

    <span data-ttu-id="5c801-137">Событие регистрируется, когда приложение изменяет определенные значения параметров сокета.</span><span class="sxs-lookup"><span data-stu-id="5c801-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="5c801-138">Некоторые из параметров в журнале включают \_ сндбуф, поэтому \_ РКВБУФ, SIO \_ \_ \_ и фионбио.</span><span class="sxs-lookup"><span data-stu-id="5c801-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="5c801-139">Всаполл и выберите</span><span class="sxs-lookup"><span data-stu-id="5c801-139">WSAPoll and select</span></span>

    <span data-ttu-id="5c801-140">Событие заносится в журнал использования [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) и вызовов [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) , которые можно использовать для поиска узких мест производительности.</span><span class="sxs-lookup"><span data-stu-id="5c801-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="5c801-141">Winsock — инициированные прерывания и отмены</span><span class="sxs-lookup"><span data-stu-id="5c801-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="5c801-142">Когда Winsock активно прерывает или отменяет запрос, событие заносится в журнал.</span><span class="sxs-lookup"><span data-stu-id="5c801-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="5c801-143">Маска события</span><span class="sxs-lookup"><span data-stu-id="5c801-143">Event mask</span></span>

    <span data-ttu-id="5c801-144">Событие заносится в журнал для маски событий, регистрируемой приложением при помощи функции [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="5c801-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="5c801-145">Datagram</span><span class="sxs-lookup"><span data-stu-id="5c801-145">Datagram</span></span>

    <span data-ttu-id="5c801-146">Событие регистрируется каждый раз, когда происходит датаграмма, и нет буферного пространства для его копирования.</span><span class="sxs-lookup"><span data-stu-id="5c801-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c801-147">См. также</span><span class="sxs-lookup"><span data-stu-id="5c801-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c801-148">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5c801-149">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5c801-150">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="5c801-151">Сведения о трассировке событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="5c801-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
