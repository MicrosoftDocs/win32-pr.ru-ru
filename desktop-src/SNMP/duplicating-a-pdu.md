---
title: Дублирование PDU
description: Функция Снмпдупликатепду дублирует PDU, выделяя любой необходимый объем памяти. Чтобы освободить ресурсы, выделенные Снмпдупликатепду для нового PDU, приложение WinSNMP должно вызывать функцию Снмпфрипду.
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9f9fdecd41ce8ad0d430f5ddc61748b365bd2e0a647067cd2bcf39d050599a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009562"
---
# <a name="duplicating-a-pdu"></a>Дублирование PDU

Функция [**снмпдупликатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) дублирует PDU, выделяя любой необходимый объем памяти. Чтобы освободить ресурсы, выделенные **снмпдупликатепду** для нового PDU, приложение WinSNMP должно вызывать функцию [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

 

 




