---
title: Получение сообщений SNMP
description: Для получения ответа на запрос Снмпсендмсг в приложении WinSNMP необходимо вызвать функцию Снмпреквмсг.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009182"
---
# <a name="receiving-snmp-messages"></a>Получение сообщений SNMP

Для получения ответа на запрос [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

Функция [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) передает в реализацию Microsoft WinSNMP маркер окна приложения и идентификатор сообщения уведомления. Когда окно приложения получает это сообщение, оно сообщает приложению о необходимости вызова функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) с помощью обработчика сеанса, возвращенного [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

Функция [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) возвращает два дескриптора сущности, дескриптор контекста и дескриптор PDU. Рекомендуется освобождать приложение WinSNMP с помощью функций [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)и [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Дополнительные сведения об управлении временем между вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) и получением соответствующего ответа см. в разделе о повторной [передаче](about-retransmission.md). Дополнительные сведения об использовании поля " **\_ идентификатор запроса** " PDU для сопоставления PDU ответа с соответствующим PDU запроса см. в разделе [сопоставление PDU и запросов распределения питания](matching-response-and-request-pdus.md).

 

 




