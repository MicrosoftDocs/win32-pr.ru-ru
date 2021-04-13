---
title: Регистрация диспетчера протокола
description: Необходимо создать хотя бы одну запись значения реестра для диспетчера протоколов, чтобы служба службы удаленных рабочих столов могла создать ее экземпляр.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410770"
---
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="48003-103">Регистрация диспетчера протокола</span><span class="sxs-lookup"><span data-stu-id="48003-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="48003-104">Необходимо создать хотя бы одну запись значения реестра для диспетчера протоколов, чтобы служба службы удаленных рабочих столов могла создать ее экземпляр.</span><span class="sxs-lookup"><span data-stu-id="48003-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="48003-105">Расположение реестра</span><span class="sxs-lookup"><span data-stu-id="48003-105">Registry Location</span></span>

<span data-ttu-id="48003-106">Создайте раздел реестра в следующем расположении для каждого прослушивателя ([**иврдспротоколлистенер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)), используемого протоколом.</span><span class="sxs-lookup"><span data-stu-id="48003-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="48003-107">В этом примере новые ключи прослушивателя называются *MyListener1* и *MyListener2*.</span><span class="sxs-lookup"><span data-stu-id="48003-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

<span data-ttu-id="48003-108">Для справки можно просмотреть записи значений в разделе по умолчанию ключа прослушивателя **RDP-TCP** в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="48003-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="48003-109">Записи значений реестра</span><span class="sxs-lookup"><span data-stu-id="48003-109">Registry Value Entries</span></span>

<span data-ttu-id="48003-110">Ключ прослушивателя для протокола должен иметь запись значения с именем **лоадаблепротокол \_ Object** .</span><span class="sxs-lookup"><span data-stu-id="48003-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="48003-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="48003-111">Data type</span></span>
</dt> <dd><span data-ttu-id="48003-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="48003-112">REG_SZ</span></span></dd> <span data-ttu-id="48003-113">Интерфейс </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**иврдспротоколманажер**</a> .) Служба службы удаленных рабочих столов использует этот идентификатор CLSID для создания экземпляра диспетчера протоколов для этого прослушивателя после того, как обнаружит прослушиватель в реестре.</span><span class="sxs-lookup"><span data-stu-id="48003-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="48003-114">Если поставщик протокола использует более одного прослушивателя, то служба службы удаленных рабочих столов создает только один экземпляр диспетчера протокола и использует его для вызова [**креателистенер**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) один раз для каждого прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="48003-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48003-115">См. также</span><span class="sxs-lookup"><span data-stu-id="48003-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48003-116">Создание поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="48003-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="48003-117">Последовательность вызовов методов</span><span class="sxs-lookup"><span data-stu-id="48003-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




