---
title: Создание PDU
description: Чтобы создать и инициализировать PDU, приложение WinSNMP вызывает функцию Снмпкреатепду.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888423"
---
# <a name="creating-a-pdu"></a>Создание PDU

Чтобы создать и инициализировать PDU, приложение WinSNMP вызывает функцию [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . Приложение должно вызвать **снмпкреатепду** перед вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) , чтобы запросить, что реализация Microsoft WinSNMP передает PDU. Приложение также должно вызывать [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) перед вызовом функции [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) для запроса кодирования SNMP-сообщения.

Приложение должно вызывать функцию [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) для освобождения ресурсов, выделяемых функцией [**Снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) для новых устройств PDU.

 

 




