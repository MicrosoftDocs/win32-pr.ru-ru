---
description: Самой простой формой ввода-вывода в Windows Sockets 2 является блокировка операций ввода-вывода.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Блокировка ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692311"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="e8389-103">Блокировка ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="e8389-103">Blocking Input/Output</span></span>

<span data-ttu-id="e8389-104">Самой простой формой ввода-вывода в Windows Sockets 2 является блокировка операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e8389-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="e8389-105">Как упоминалось в [флагах и режимах атрибутов сокета](socket-attribute-flags-and-modes-2.md), сокеты создаются в блокирующем режиме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8389-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="e8389-106">Любая операция ввода-вывода с блокирующим сокетом не будет возвращаться до полного завершения операции.</span><span class="sxs-lookup"><span data-stu-id="e8389-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="e8389-107">Таким же потоком в каждый момент времени может выполняться только одна операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e8389-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="e8389-108">Например, если поток выдает операцию Receive и в настоящее время нет доступных данных, поток блокируется до тех пор, пока данные не станут доступны и помещаются в буфер потока.</span><span class="sxs-lookup"><span data-stu-id="e8389-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="e8389-109">Хотя это и просто, это необязательно является самым эффективным способом ввода-вывода (см. сведения о [псевдолокализации и истинной блокировке](pseudo-vs--true-blocking-2.md) для получения дополнительных сведений).</span><span class="sxs-lookup"><span data-stu-id="e8389-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



