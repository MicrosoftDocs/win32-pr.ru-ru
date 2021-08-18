---
title: Сопоставление устройств распределения питания и запросов
description: Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009323"
---
# <a name="matching-response-and-request-pdus"></a>Сопоставление устройств распределения питания и запросов

Порядок, в котором WinSNMP-приложение получает SNMP-ответы, может не соответствовать порядку, в котором приложение отправляет запросы операции SNMP. Чтобы сопоставить ответ с запросом, приложение должно использовать поле идентификатора запроса ( **\_ идентификатор запроса**) ответа.

Поле **\_ идентификатора запроса** — это уникальное числовое значение, идентифицирующее PDU. Приложения могут назначать идентификаторы запросов путем вызова функции [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) или функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Вызовите функцию [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) , чтобы получить **\_ идентификатор запроса** PDU.

 

 




