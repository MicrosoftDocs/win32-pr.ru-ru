---
title: Последовательность подключения
description: Иллюстрация, в которой показаны вызовы методов, выполняемые между службой службы удаленных рабочих столов и протоколом во время последовательности подключения клиента.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8a159dcc61b3d748b7d2570891e270e53e9f08e70fe884c71949425f6c08be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942216"
---
# <a name="connection-sequence"></a>Последовательность подключения

На следующем рисунке показаны вызовы методов, выполняемые между службой службы удаленных рабочих столов и протоколом во время последовательности подключения клиента. Действия, показанные здесь, следуют [начальной последовательности](start-sequence.md). Взаимодействие между службой и объектом [**иврдспротоколлиценсеконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) представляет собой подтверждение лицензирования для клиента.

![последовательность клиентских подключений](images/protocol-connectionsequence.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Последовательность вызовов методов](method-call-sequence.md)
</dt> <dt>

[Повторно подключить последовательность](reconnect-sequence.md)
</dt> <dt>

[Начальная последовательность](start-sequence.md)
</dt> </dl>

 

 




