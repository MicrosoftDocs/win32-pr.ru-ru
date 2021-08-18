---
title: Отправка SNMP-сообщений
description: Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP. SNMP-сообщения включают в себя единицу данных протокола SNMP. Дополнительные сведения см. в разделе Работа с единицами данных протокола.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009072"
---
# <a name="sending-snmp-messages"></a>Отправка SNMP-сообщений

Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP. SNMP-сообщения включают в себя единицу данных протокола SNMP. Дополнительные сведения см. в разделе [Работа с единицами данных протокола](working-with-protocol-data-units.md).

Приложение WinSNMP должно вызывать функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) , чтобы запросить передачу PDU с помощью реализации Microsoft WinSNMP с другими необходимыми элементами сообщения, определенными соответствующим документом RFC. В дополнение к целевой сущности, приложение должно указать исходную сущность и контекст для запроса. Функция [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) выполняется асинхронно.

Для получения ответа на запрос **снмпсендмсг** в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

Реализация проверяет допустимость PDU и других элементов сообщения, когда приложение вызывает [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




