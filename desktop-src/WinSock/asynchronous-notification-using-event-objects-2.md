---
description: Функции Всаевентселект и Всаенумнетворкевентс предоставляются для размещения приложений, таких как управляющие программы и службы, которые не имеют пользовательского интерфейса (и поэтому не используют дескрипторы Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Асинхронное уведомление с помощью объектов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897358"
---
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="104bd-103">Асинхронное уведомление с помощью объектов событий</span><span class="sxs-lookup"><span data-stu-id="104bd-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="104bd-104">Функции [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) и [**всаенумнетворкевентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) предоставляются для размещения приложений, таких как управляющие программы и службы, которые не имеют пользовательского интерфейса (и поэтому не используют дескрипторы Windows).</span><span class="sxs-lookup"><span data-stu-id="104bd-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="104bd-105">Функция **всаевентселект** работает точно так же, как функция [**всаасинкселект**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) .</span><span class="sxs-lookup"><span data-stu-id="104bd-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="104bd-106">Однако вместо того, чтобы сообщение Windows отправлялось при возникновении \_ события сети «демон-приложение» (например, «Демон \_ чтения» и «демон записи» \_ ), задается объект события, назначенный приложению.</span><span class="sxs-lookup"><span data-stu-id="104bd-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="104bd-107">Кроме того, тот факт, что \_ произошло определенное сетевое событие демона "% XXX", запоминается поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="104bd-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="104bd-108">Приложение может вызвать [**всаенумнетворкевентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , чтобы текущее содержимое памяти сетевого события копировалось в буфер, предоставленный приложением, и автоматически очищать память сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="104bd-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="104bd-109">При необходимости приложение может также обозначать определенный объект события, который удаляется вместе с памятью сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="104bd-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



