---
description: Требования к производительности для пользователей и администраторов приложений Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Требования к производительности: пользователи и администраторы'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072738"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="d392f-103">Требования к производительности: пользователи и администраторы</span><span class="sxs-lookup"><span data-stu-id="d392f-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="d392f-104">Пользователи изменяют производительность приложения по их опыту:</span><span class="sxs-lookup"><span data-stu-id="d392f-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="d392f-105">Приложение быстро отвечает на запросы?</span><span class="sxs-lookup"><span data-stu-id="d392f-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="d392f-106">Отображается ли значок песочных часов при выполнении фоновых операций?</span><span class="sxs-lookup"><span data-stu-id="d392f-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="d392f-107">Запускается ли приложение и быстро закрывается?</span><span class="sxs-lookup"><span data-stu-id="d392f-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="d392f-108">Обрабатываются ли ошибки понятным образом?</span><span class="sxs-lookup"><span data-stu-id="d392f-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="d392f-109">Для суммирования пользователи хотят, чтобы приложения были быстро и предсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="d392f-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="d392f-110">В отличие от этого, администраторы часто обоценивать производительность приложения на том, насколько эффективно он использует сетевые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d392f-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="d392f-111">Администраторы могут спросить:</span><span class="sxs-lookup"><span data-stu-id="d392f-111">Administrators may ask:</span></span>

-   <span data-ttu-id="d392f-112">Есть ли у приложения низкая нагрузка и эффективное использование сети?</span><span class="sxs-lookup"><span data-stu-id="d392f-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="d392f-113">Используется ли минимальное количество подключений, так что мой сервер может обслуживать как можно больше пользователей одновременно?</span><span class="sxs-lookup"><span data-stu-id="d392f-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="d392f-114">Вы постоянно вызываете службу технической поддержки?</span><span class="sxs-lookup"><span data-stu-id="d392f-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="d392f-115">Вкратце, администраторы хотят масштабировать приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="d392f-116">Рекомендации по повышению производительности</span><span class="sxs-lookup"><span data-stu-id="d392f-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="d392f-117">При разработке приложения Windows Sockets эти требования к производительности преобразуются в полезные правила.</span><span class="sxs-lookup"><span data-stu-id="d392f-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="d392f-118">Быстро инициализируйте сетевые приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="d392f-119">Пользовательский интерфейс не должен ждать ответов сети.</span><span class="sxs-lookup"><span data-stu-id="d392f-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="d392f-120">Некоторые задачи могут быть выполнены до того, как сеть будет доступна или без сети.</span><span class="sxs-lookup"><span data-stu-id="d392f-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="d392f-121">Если сеть не отвечает, пользователю может потребоваться пользовательский интерфейс для выполнения простых операций, таких как закрытие приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="d392f-122">Не дожидаться завершения работы сети.</span><span class="sxs-lookup"><span data-stu-id="d392f-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="d392f-123">Правильно написанные клиент-серверные приложения обрабатывали аварийные отключения.</span><span class="sxs-lookup"><span data-stu-id="d392f-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="d392f-124">Не инициируйте потенциально длительную операцию, например синхронизацию файлов или папок с сервером, которые не могут быть прерваны при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="d392f-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="d392f-125">Сети не отвечают постоянно, поэтому даже небольшие операции могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="d392f-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="d392f-126">Предоставьте положительный отзыв пользователям, включая указание хода выполнения и предполагаемое время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d392f-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="d392f-127">Обеспечьте реагирование пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d392f-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="d392f-128">Скорость реагирования приложения помогает устранить ненужные вызовы службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="d392f-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="d392f-129">Хорошей рекомендацией для интерактивного ответа является 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="d392f-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="d392f-130">Пользователи воспринимают паузы дольше 500 миллисекунд в качестве задержки в производительности.</span><span class="sxs-lookup"><span data-stu-id="d392f-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="d392f-131">Приложения должны быть достаточно быстро реагировать на то, чтобы пользователь уверен в наличии приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="d392f-132">Сопротивляются сетевые ошибки.</span><span class="sxs-lookup"><span data-stu-id="d392f-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="d392f-133">Не все сетевые ошибки являются критически важными.</span><span class="sxs-lookup"><span data-stu-id="d392f-133">Not all network errors are critical.</span></span> <span data-ttu-id="d392f-134">Например, приложение, которое получило или разместило все данные, скорее всего, может игнорировать ошибки при закрытии соединения.</span><span class="sxs-lookup"><span data-stu-id="d392f-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="d392f-135">Не следует считать сеть или пользователя доступной; либо обрабатывайте ошибки без вмешательства пользователя, либо Проигнорируйте их, если ошибки некритически.</span><span class="sxs-lookup"><span data-stu-id="d392f-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="d392f-136">Приложение должно определить свое разумное время ожидания.</span><span class="sxs-lookup"><span data-stu-id="d392f-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="d392f-137">Например, запрос Connect () Windows Sockets () может блокироваться в некоторых условиях в течение 21 секунды.</span><span class="sxs-lookup"><span data-stu-id="d392f-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="d392f-138">Приложениям может потребоваться ввести собственные интервалы времени, соответствующие пользователям.</span><span class="sxs-lookup"><span data-stu-id="d392f-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="d392f-139">Сократите нагрузку на протокол.</span><span class="sxs-lookup"><span data-stu-id="d392f-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="d392f-140">Экономия пропускной способности сети частично снижает нагрузку на протокол, вызванную приложением.</span><span class="sxs-lookup"><span data-stu-id="d392f-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="d392f-141">Кроме того, он устраняет ненужный сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="d392f-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="d392f-142">Протоколы с более низкими издержками заголовков можно использовать для перемещения данных приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="d392f-143">Например, при отправке меньших объемов некритических или повторяемых данных используйте UDP в отличие от протокола TCP, чтобы уменьшить издержки, связанные с установлением соединения и обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="d392f-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="d392f-144">Если одни и те же данные должны быть отправлены нескольким получателям, рассмотрите возможность многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d392f-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="d392f-145">Имейте в виду, что приложения UDP не управляются потоком — передача данных за пределы доступной пропускной способности может привести к катастрофному сбою сети.</span><span class="sxs-lookup"><span data-stu-id="d392f-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="d392f-146">Служебную программу netstat можно использовать с параметрами **-e** и **-s** для вывода статистики по различным протоколам.</span><span class="sxs-lookup"><span data-stu-id="d392f-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="d392f-147">Экономия системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d392f-147">Conserve system resources.</span></span>

    <span data-ttu-id="d392f-148">Системные ресурсы можно быстро потреблять, если не используется правильное ограничения.</span><span class="sxs-lookup"><span data-stu-id="d392f-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="d392f-149">Например, сокеты и TCP-подключения потребляют ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d392f-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="d392f-150">Не используйте для каждого клиента несколько TCP-подключений, где один будет обслуживать назначение приложения.</span><span class="sxs-lookup"><span data-stu-id="d392f-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="d392f-151">Для транзакционных приложений хорошее взаимодействие с пользователем и низкая загрузка сети не конфликтуют с целями.</span><span class="sxs-lookup"><span data-stu-id="d392f-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="d392f-152">Сеть является узким местом.</span><span class="sxs-lookup"><span data-stu-id="d392f-152">The network is a bottleneck.</span></span> <span data-ttu-id="d392f-153">Ресурсоемкие приложения тратят больше времени на ожидание, а написанные сетевые приложения предназначены для снижения ненужного времени ожидания, как для пользовательского интерфейса, так и для передачи данных в сети.</span><span class="sxs-lookup"><span data-stu-id="d392f-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d392f-154">См. также</span><span class="sxs-lookup"><span data-stu-id="d392f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d392f-155">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d392f-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="d392f-156">Измерения производительности</span><span class="sxs-lookup"><span data-stu-id="d392f-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



