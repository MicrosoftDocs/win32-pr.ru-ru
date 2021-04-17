---
description: Подпрограммы Вспсенд, Вспсендто, Вспрекв и Вспреквфром принимают массив буферов клиента в качестве входных параметров и, таким образом, могут использоваться для точечной/собираемой (или векторной) операции ввода-вывода.
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Поддержка точечных или собираемых входных и выходных данных в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711760"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a><span data-ttu-id="e3827-103">Поддержка точечных или собираемых входных и выходных данных в SPI</span><span class="sxs-lookup"><span data-stu-id="e3827-103">Support for Scatter/Gather Input/Output in the SPI</span></span>

<span data-ttu-id="e3827-104">Подпрограммы [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**вспсендто**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))и [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) принимают массив буферов клиента в качестве входных параметров и, таким образом, могут использоваться для точечной/собираемой (или векторной) операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e3827-104">The [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)), and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) routines all take an array of client buffers as input parameters and thus may be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="e3827-105">Это может быть очень полезно в случаях, когда части каждого передаваемого сообщения состоят из одного или нескольких компонентов заголовка фиксированной длины в дополнение к тексту сообщения.</span><span class="sxs-lookup"><span data-stu-id="e3827-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed length header components in addition to a message body.</span></span> <span data-ttu-id="e3827-106">Такие компоненты заголовков не нужно объединять в один непрерывный буфер перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="e3827-106">Such header components need not be concatenated into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="e3827-107">Как и при получении, компоненты заголовка можно автоматически разбивать на отдельные буферы, при этом текст сообщения остается чистым.</span><span class="sxs-lookup"><span data-stu-id="e3827-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body pure.</span></span>

<span data-ttu-id="e3827-108">Использование списков буферов вместо одного буфера не влияет на границы, применяемые к операциям получения.</span><span class="sxs-lookup"><span data-stu-id="e3827-108">Utilizing lists of buffers instead of a single buffer does not change the boundaries that apply to receive operations.</span></span> <span data-ttu-id="e3827-109">Для протоколов, ориентированных на сообщения, операция получения завершается при получении одного сообщения, независимо от того, сколько из предоставленных буферов было использовано.</span><span class="sxs-lookup"><span data-stu-id="e3827-109">For message-oriented protocols, a receive operation completes whenever a single message has been received, regardless of how many or few of the supplied buffers were used.</span></span> <span data-ttu-id="e3827-110">Аналогично для протоколов, ориентированных на поток, получение завершается, когда неопределенное количество байтов передается по сети, а не обязательно, когда все указанные буферы заполнены.</span><span class="sxs-lookup"><span data-stu-id="e3827-110">Likewise for stream-oriented protocols, a receive completes when an unspecified quantity of bytes arrives over the network, not necessarily when all of the supplied buffers are full.</span></span>

 

 
