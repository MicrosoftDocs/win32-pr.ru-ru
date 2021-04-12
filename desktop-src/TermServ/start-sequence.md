---
title: Начальная последовательность
description: Действия по запуску настраиваемого протокола.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252863"
---
# <a name="start-sequence"></a><span data-ttu-id="4a64e-103">Начальная последовательность</span><span class="sxs-lookup"><span data-stu-id="4a64e-103">Start Sequence</span></span>

<span data-ttu-id="4a64e-104">Чтобы запустить поставщик протокола, служба службы удаленных рабочих столов:</span><span class="sxs-lookup"><span data-stu-id="4a64e-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="4a64e-105">Извлекает имя прослушивателя и CLSID объекта диспетчера протоколов ([**иврдспротоколманажер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) из реестра.</span><span class="sxs-lookup"><span data-stu-id="4a64e-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="4a64e-106">Дополнительные сведения см. [в разделе Регистрация диспетчера протоколов](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="4a64e-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="4a64e-107">Вызывает метод [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) для инициализации диспетчера протоколов.</span><span class="sxs-lookup"><span data-stu-id="4a64e-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="4a64e-108">Создает объект диспетчера протокола с помощью идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="4a64e-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="4a64e-109">Даже если для одного поставщика протокола зарегистрировано несколько прослушивателей, служба создает только один объект диспетчера протокола.</span><span class="sxs-lookup"><span data-stu-id="4a64e-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="4a64e-110">Вызывает [**креателистенер**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) , чтобы указать объекту диспетчера протокола создать объект прослушивателя [**иврдспротоколлистенер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) и вернуть его в службу.</span><span class="sxs-lookup"><span data-stu-id="4a64e-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="4a64e-111">Объект диспетчера протоколов должен добавить ссылку на объект прослушивателя, прежде чем возвратить его службе.</span><span class="sxs-lookup"><span data-stu-id="4a64e-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="4a64e-112">Служба освободит объект при остановке службы или удалении прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="4a64e-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="4a64e-113">Вызывает [**стартлистен**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) для объекта прослушивателя, чтобы прослушиватель мог начать прослушивание входящих подключений.</span><span class="sxs-lookup"><span data-stu-id="4a64e-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="4a64e-114">Вызывает [**стоплистен**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) , чтобы предотвратить прослушивание объекта прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="4a64e-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="4a64e-115">Вызывает [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) , чтобы отменить инициализацию диспетчера протокола.</span><span class="sxs-lookup"><span data-stu-id="4a64e-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="4a64e-116">Прослушиватель создает объект [**иврдспротоколконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) , когда клиент пытается подключиться.</span><span class="sxs-lookup"><span data-stu-id="4a64e-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="4a64e-117">Объект Listener вызывает [**Onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) для уведомления службы Службы удаленных рабочих столов о том, что новый клиент пытается подключиться или повторно подключиться, и передает объект **иврдспротоколконнектион** в этом вызове.</span><span class="sxs-lookup"><span data-stu-id="4a64e-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="4a64e-118">Служба службы удаленных рабочих столов, в свою очередь, возвращает объект [**иврдспротоколконнектионкаллбакк**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) в этом вызове, чтобы протокол мог взаимодействовать со службой Службы удаленных рабочих столов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4a64e-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="4a64e-119">Служба добавляет ссылку на объект обратного вызова перед возвратом, и протокол должен освободить эту ссылку при закрытии соединения.</span><span class="sxs-lookup"><span data-stu-id="4a64e-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="4a64e-120">На следующем рисунке показано взаимодействие между различными объектами во время запуска.</span><span class="sxs-lookup"><span data-stu-id="4a64e-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![RCM начальная последовательность](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="4a64e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4a64e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a64e-123">Последовательность вызовов методов</span><span class="sxs-lookup"><span data-stu-id="4a64e-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="4a64e-124">Последовательность подключения</span><span class="sxs-lookup"><span data-stu-id="4a64e-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




