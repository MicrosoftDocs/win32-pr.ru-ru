---
title: Создание PDU
description: Чтобы создать и инициализировать PDU, приложение WinSNMP вызывает функцию Снмпкреатепду.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009602"
---
# <a name="creating-a-pdu"></a>Создание PDU

Чтобы создать и инициализировать PDU, приложение WinSNMP вызывает функцию [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . Приложение должно вызвать **снмпкреатепду** перед вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) , чтобы запросить, что реализация Microsoft WinSNMP передает PDU. Приложение также должно вызывать [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) перед вызовом функции [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) для запроса кодирования SNMP-сообщения.

Приложение должно вызывать функцию [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) для освобождения ресурсов, выделяемых функцией [**Снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) для новых устройств PDU.

 

 




