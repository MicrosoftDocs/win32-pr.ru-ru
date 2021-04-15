---
description: Вспевентселект работает точно так же, как и Вспасинкселект, за исключением того, что вместо того, чтобы сообщение Windows отправлялось при возникновении любого назначенного \_ события сети демо-фильтра (например, для \_ чтения, \_ записи и т. д.), задается заданный объект события.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Сигнализация объекта события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701535"
---
# <a name="event-object-signaling"></a><span data-ttu-id="849fc-103">Сигнализация объекта события</span><span class="sxs-lookup"><span data-stu-id="849fc-103">Event Object Signaling</span></span>

<span data-ttu-id="849fc-104">[**Вспевентселект**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) работает точно так же, как и [**вспасинкселект**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , за исключением того, что вместо того, чтобы сообщение Windows отправлялось при возникновении любого назначенного \_ события сети демо-фильтра (например, для \_ чтения, \_ записи и т. д.), задается заданный объект события.</span><span class="sxs-lookup"><span data-stu-id="849fc-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="849fc-105">Кроме того, тот факт, что \_ произошло определенное сетевое событие демона "% XXX", запоминается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="849fc-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="849fc-106">Это необходимо, так как при возникновении всех заданных сетевых событий, а также при появления в нем одного объекта события будет получен сигнал.</span><span class="sxs-lookup"><span data-stu-id="849fc-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="849fc-107">Вызов [**вспенумнетворкевентс**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) приводит к тому, что текущее содержимое памяти сетевого события копируется в буфер, предоставляемый клиентом, и память сетевого события для очистки.</span><span class="sxs-lookup"><span data-stu-id="849fc-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="849fc-108">Клиент также может обозначать определенный объект события, который будет удаляться атомарно вместе с памятью сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="849fc-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
