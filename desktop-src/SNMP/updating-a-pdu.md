---
title: Обновление PDU
description: Приложение WinSNMP может извлекать и обновлять выбранные поля PDU с помощью функций Снмпжетпдудата и Снмпсетпдудата.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778872"
---
# <a name="updating-a-pdu"></a>Обновление PDU

Приложение WinSNMP может извлекать и обновлять выбранные поля PDU с помощью функций [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) и [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

Приложение может получить поля типа PDU, идентификатора запроса, состояния ошибки и индекса ошибок из определенного PDU. Он также может получить маркер для списка привязок переменных. Приложение может обновлять поля **\_ типа PDU** и **\_ идентификатора запроса** .

Если тип PDU равен числу PDU SNMP \_ \_ , то приложение также может обновлять **\_ неповторяющиеся** значения и поля **максимального числа \_ повторений** PDU.

 

 




