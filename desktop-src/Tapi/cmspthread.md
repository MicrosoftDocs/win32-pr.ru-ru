---
description: Класс Кмспсреад реализует рабочий поток MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: кмспсреад
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674268"
---
# <a name="cmspthread"></a><span data-ttu-id="603d0-103">кмспсреад</span><span class="sxs-lookup"><span data-stu-id="603d0-103">CMSPThread</span></span>

<span data-ttu-id="603d0-104">Класс **кмспсреад** реализует рабочий поток MSP.</span><span class="sxs-lookup"><span data-stu-id="603d0-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="603d0-105">Базовые классы используют этот рабочий поток для выполнения нескольких задач.</span><span class="sxs-lookup"><span data-stu-id="603d0-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="603d0-106">Универсальный и упрощенный механизм рабочих элементов позволяет производному MSP использовать этот поток для собственных синхронных или асинхронных рабочих элементов, независимо от того, что они могут быть.</span><span class="sxs-lookup"><span data-stu-id="603d0-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="603d0-107">Поток также переносит сообщения и поддерживает обработку APC (хотя APC не используются в базовых классах).</span><span class="sxs-lookup"><span data-stu-id="603d0-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="603d0-108">При наличии нескольких подобных адресов (то есть при многократном создании одной и той же реализации MSP из одной и той же библиотеки DLL) класс потока обеспечивает масштабируемость, автоматически используя один поток для всех адресов.</span><span class="sxs-lookup"><span data-stu-id="603d0-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="603d0-109">Интерфейс к классу потока состоит в том, что реализация MSP может представлять класс потока как частный поток и не требует от вас других адресов, которые могут совместно использовать его.</span><span class="sxs-lookup"><span data-stu-id="603d0-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="603d0-110">Определен в Мспсрд. h.</span><span class="sxs-lookup"><span data-stu-id="603d0-110">Defined in MSPthrd.h.</span></span>

 

 



