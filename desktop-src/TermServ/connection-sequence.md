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
# <a name="connection-sequence"></a>Последовательность подключения

На следующем рисунке показаны вызовы методов, выполняемые между службой службы удаленных рабочих столов и протоколом во время последовательности подключения клиента. Действия, показанные здесь, следуют [начальной последовательности](start-sequence.md). Взаимодействие между службой и объектом [**иврдспротоколлиценсеконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) представляет собой подтверждение лицензирования для клиента.

![последовательность клиентских подключений](images/protocol-connectionsequence.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Последовательность вызовов методов](method-call-sequence.md)
</dt> <dt>

[Повторно подключить последовательность](reconnect-sequence.md)
</dt> <dt>

[Начальная последовательность](start-sequence.md)
</dt> </dl>

 

 




