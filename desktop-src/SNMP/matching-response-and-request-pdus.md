---
title: Сопоставление устройств распределения питания и запросов
description: Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986653"
---
# <a name="matching-response-and-request-pdus"></a>Сопоставление устройств распределения питания и запросов

Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP. Чтобы сопоставить ответ с запросом, приложение должно использовать поле идентификатора запроса ( **\_ идентификатор запроса**) ответа.

Поле **\_ идентификатора запроса** — это уникальное числовое значение, идентифицирующее PDU. Приложения могут назначать идентификаторы запросов путем вызова функции [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) или функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Вызовите функцию [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) , чтобы получить **\_ идентификатор запроса** PDU.

 

 




