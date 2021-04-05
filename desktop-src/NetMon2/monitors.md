---
description: Монитор — это библиотека динамической компоновки (DLL), которая анализирует записи сетевого трафика в режиме реального времени.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Мониторы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991203"
---
# <a name="monitors"></a><span data-ttu-id="7080f-103">Мониторы</span><span class="sxs-lookup"><span data-stu-id="7080f-103">Monitors</span></span>

<span data-ttu-id="7080f-104">Монитор — это библиотека динамической компоновки (DLL), которая анализирует записи сетевого трафика в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="7080f-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="7080f-105">Он выполняет поиск предварительно определенных условий, а затем создает события при обнаружении этих условий.</span><span class="sxs-lookup"><span data-stu-id="7080f-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="7080f-106">Например, событие может быть вызвано при попытке перезапуска сети, когда фальшивая Рабочая станция передает IP-адреса или происходит сбой маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="7080f-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="7080f-107">Если необходимо выполнить подробный анализ сетевых данных, для которых требуется анализ после записи, необходимо использовать приложения [*эксперта*](e.md) и [*анализатора*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="7080f-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="7080f-108">[*Служба управления монитором*](m.md) (мксвк) предоставляет платформу для управления мониторами.</span><span class="sxs-lookup"><span data-stu-id="7080f-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="7080f-109">Он предоставляет функции для загрузки библиотек DLL монитора и интерфейс связи с инструментом управления монитором, позволяющий создавать, настраивать, запускать, прекращать и отключать несколько экземпляров мониторов.</span><span class="sxs-lookup"><span data-stu-id="7080f-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="7080f-110">Мониторы запускаются в двух потоках выполнения.</span><span class="sxs-lookup"><span data-stu-id="7080f-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="7080f-111">МКСВК предоставляет первый поток, который обеспечивает прямое управление монитором.</span><span class="sxs-lookup"><span data-stu-id="7080f-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="7080f-112">Второй поток предоставляется [*поставщиком сетевых пакетов*](n.md) (НПП), который предоставляет способ передачи захваченных данных сети, статистики и состояния записи из НПП обратно в монитор.</span><span class="sxs-lookup"><span data-stu-id="7080f-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="7080f-113">Для каждого интерфейса НПП времени выполнения, используемого для сбора данных, может существовать более одного экземпляра одного монитора.</span><span class="sxs-lookup"><span data-stu-id="7080f-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



