---
title: Отправка SNMP-сообщений
description: Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP. SNMP-сообщения включают в себя единицу данных протокола SNMP. Дополнительные сведения см. в разделе Работа с единицами данных протокола.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331347"
---
# <a name="sending-snmp-messages"></a>Отправка SNMP-сообщений

Ошибка WinSNMP-приложения инициирует запрос на передачу, отправляя сообщение SNMP. SNMP-сообщения включают в себя единицу данных протокола SNMP. Дополнительные сведения см. в разделе [Работа с единицами данных протокола](working-with-protocol-data-units.md).

Приложение WinSNMP должно вызывать функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) , чтобы запросить передачу PDU с помощью реализации Microsoft WinSNMP с другими необходимыми элементами сообщения, определенными соответствующим документом RFC. В дополнение к целевой сущности, приложение должно указать исходную сущность и контекст для запроса. Функция [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) выполняется асинхронно.

Для получения ответа на запрос **снмпсендмсг** в приложении WinSNMP необходимо вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

Реализация проверяет допустимость PDU и других элементов сообщения, когда приложение вызывает [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




