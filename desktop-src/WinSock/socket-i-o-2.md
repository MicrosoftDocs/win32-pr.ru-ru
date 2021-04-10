---
description: С помощью блокирующего ввода-вывода, неблокирующего ввода-вывода с асинхронным уведомлением о сетевых событиях и перекрывающихся операций ввода-вывода с указанием завершения в сокетах Windows 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: Ввод-вывод сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144953"
---
# <a name="socket-io"></a><span data-ttu-id="1200c-103">Ввод-вывод сокета</span><span class="sxs-lookup"><span data-stu-id="1200c-103">Socket I/O</span></span>

<span data-ttu-id="1200c-104">Существует три основных способа ввода-вывода в сокетах Windows 2:</span><span class="sxs-lookup"><span data-stu-id="1200c-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="1200c-105">Блокировка операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="1200c-105">Blocking I/O.</span></span>
-   <span data-ttu-id="1200c-106">Неблокирующий ввод-вывод и асинхронное уведомление о сетевых событиях.</span><span class="sxs-lookup"><span data-stu-id="1200c-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="1200c-107">Перекрывающиеся операции ввода-вывода с указанием завершения.</span><span class="sxs-lookup"><span data-stu-id="1200c-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="1200c-108">Мы описываем каждый метод в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="1200c-108">We describe each method in the following sections.</span></span> <span data-ttu-id="1200c-109">Блокирование ввода-вывода является поведением по умолчанию. неблокирующий режим можно использовать на любом сокете, который перемещается в неблокирующий режим, а перекрывающиеся операции ввода-вывода могут происходить только на сокетах, созданных с помощью атрибута OVERLAPPED.</span><span class="sxs-lookup"><span data-stu-id="1200c-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="1200c-110">Также интересно отметить, что два вызова для отправки: [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспсендто**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) и два вызова для получения: [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) и [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) каждый из них реализуют все три метода ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="1200c-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="1200c-111">Поставщики услуг определяют, как выполнять операции ввода-вывода на основе режимов сокета, атрибутов и значений входных параметров.</span><span class="sxs-lookup"><span data-stu-id="1200c-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
