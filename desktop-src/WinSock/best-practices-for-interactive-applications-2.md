---
description: При трансформации кода обновления жизненного цикла было обнаружено несколько рекомендаций по написанию высокопроизводительных сетевых приложений.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Рекомендации для интерактивных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711046"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="430a0-103">Рекомендации для интерактивных приложений</span><span class="sxs-lookup"><span data-stu-id="430a0-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="430a0-104">При трансформации кода обновления жизненного цикла было обнаружено несколько рекомендаций по написанию высокопроизводительных сетевых приложений.</span><span class="sxs-lookup"><span data-stu-id="430a0-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="430a0-105">Ниже приведены некоторые общие стратегии, которые следует применять при написании приложений следующих типов.</span><span class="sxs-lookup"><span data-stu-id="430a0-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="430a0-106">Сделайте поток данных максимально возможной, а не фрагментами.</span><span class="sxs-lookup"><span data-stu-id="430a0-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="430a0-107">Используйте несколько больших транзакций, а не много маленьких.</span><span class="sxs-lookup"><span data-stu-id="430a0-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="430a0-108">Большие транзакции также можно эффективно передавать в поток.</span><span class="sxs-lookup"><span data-stu-id="430a0-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="430a0-109">Распознают, что сеть является медленным, ненадежным ресурсом и разрабатывает каждое приложение, чтобы снизить его зависимость от сети.</span><span class="sxs-lookup"><span data-stu-id="430a0-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="430a0-110">Используйте четко спроектированное представление данных в сети.</span><span class="sxs-lookup"><span data-stu-id="430a0-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="430a0-111">Представление данных должно быть независимым от архитектуры компьютера, не должно содержать FAT и, возможно, сжато.</span><span class="sxs-lookup"><span data-stu-id="430a0-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="430a0-112">Во время инициализации и завершения работы пользователь не должен ждать, пока сеть не запустится или завершит работу.</span><span class="sxs-lookup"><span data-stu-id="430a0-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="430a0-113">Инициализация, связанная с сетью, может занять довольно много времени.</span><span class="sxs-lookup"><span data-stu-id="430a0-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="430a0-114">Разделите некритический сетевой код.</span><span class="sxs-lookup"><span data-stu-id="430a0-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="430a0-115">Обрабатывайте ошибки в соответствии с их влиянием.</span><span class="sxs-lookup"><span data-stu-id="430a0-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="430a0-116">Не все ошибки являются критически важными.</span><span class="sxs-lookup"><span data-stu-id="430a0-116">Not all errors are critical.</span></span> <span data-ttu-id="430a0-117">Реализуйте механизмы восстановления и предоставьте невмешательствные Отзывы пользователей.</span><span class="sxs-lookup"><span data-stu-id="430a0-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="430a0-118">Используйте удаленные вызовы процедур (RPC), только если это уместно.</span><span class="sxs-lookup"><span data-stu-id="430a0-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="430a0-119">RPC синхронно работает в Windows Me/98 и всегда приводит к небольшому числу протоколов FAT при использовании для отправки небольших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="430a0-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="430a0-120">Измерьте нагрузку на сеть с помощью программы netstat; возможно, вы удивлены тем, что откроете ваши измерения.</span><span class="sxs-lookup"><span data-stu-id="430a0-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="430a0-121">Протестируйте приложение в различных сетях, особенно в сетях с высокой скоростью или потерей данных.</span><span class="sxs-lookup"><span data-stu-id="430a0-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="430a0-122">Беспроводные локальные сети, модемы и виртуальные частные сети (VPN) через Интернет являются хорошими сетями для тестирования.</span><span class="sxs-lookup"><span data-stu-id="430a0-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="430a0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="430a0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="430a0-124">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="430a0-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



