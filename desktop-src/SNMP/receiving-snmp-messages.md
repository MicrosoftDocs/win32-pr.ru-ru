---
title: Получение сообщений SNMP
description: Для получения ответа на запрос Снмпсендмсг в приложении WinSNMP необходимо вызвать функцию Снмпреквмсг.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778599"
---
# <a name="receiving-snmp-messages"></a>Получение сообщений SNMP

Для получения ответа на запрос [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

Функция [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) передает в реализацию Microsoft WinSNMP маркер окна приложения и идентификатор сообщения уведомления. Когда окно приложения получает это сообщение, оно сообщает приложению о необходимости вызова функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) с помощью обработчика сеанса, возвращенного [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

Функция [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) возвращает два дескриптора сущности, дескриптор контекста и дескриптор PDU. Рекомендуется освобождать приложение WinSNMP с помощью функций [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)и [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Дополнительные сведения об управлении временем между вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) и получением соответствующего ответа см. в разделе о повторной [передаче](about-retransmission.md). Дополнительные сведения об использовании поля " **\_ идентификатор запроса** " PDU для сопоставления PDU ответа с соответствующим PDU запроса см. в разделе [сопоставление PDU и запросов распределения питания](matching-response-and-request-pdus.md).

 

 




