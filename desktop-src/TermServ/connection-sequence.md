---
title: Последовательность подключения
description: Иллюстрация, в которой показаны вызовы методов, выполняемые между службой службы удаленных рабочих столов и протоколом во время последовательности подключения клиента.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411297"
---
# <a name="connection-sequence"></a><span data-ttu-id="b3dcf-103">Последовательность подключения</span><span class="sxs-lookup"><span data-stu-id="b3dcf-103">Connection Sequence</span></span>

<span data-ttu-id="b3dcf-104">На следующем рисунке показаны вызовы методов, выполняемые между службой службы удаленных рабочих столов и протоколом во время последовательности подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="b3dcf-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="b3dcf-105">Действия, показанные здесь, следуют [начальной последовательности](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="b3dcf-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="b3dcf-106">Взаимодействие между службой и объектом [**иврдспротоколлиценсеконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) представляет собой подтверждение лицензирования для клиента.</span><span class="sxs-lookup"><span data-stu-id="b3dcf-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![последовательность клиентских подключений](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="b3dcf-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b3dcf-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3dcf-109">Последовательность вызовов методов</span><span class="sxs-lookup"><span data-stu-id="b3dcf-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="b3dcf-110">Повторно подключить последовательность</span><span class="sxs-lookup"><span data-stu-id="b3dcf-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="b3dcf-111">Начальная последовательность</span><span class="sxs-lookup"><span data-stu-id="b3dcf-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




