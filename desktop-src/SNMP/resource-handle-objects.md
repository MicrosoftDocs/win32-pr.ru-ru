---
title: Объекты «обработчик ресурсов»
description: Структура объекта ресурса ограничена реализацией Microsoft WinSNMP. Приложение WinSNMP может обращаться к объекту ресурса с помощью маркера.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b05702f0ad43e5b4b80a9b1a3cada471212dec3bc377bddcc95fe9a109ec78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009122"
---
# <a name="resource-handle-objects"></a>Объекты «обработчик ресурсов»

Структура объекта ресурса ограничена реализацией Microsoft WinSNMP. Приложение WinSNMP может обращаться к объекту ресурса с помощью маркера.

Реализация может выделить один из следующих типов дескрипторов ресурсов для приложения WinSNMP.

| Тип обработчика        | Описание                       |
|--------------------|-----------------------------------|
| **\_сеанс хснмп** | Обработчик для сеанса WinSNMP       |
| **\_сущность хснмп**  | Обработчик для объекта SNMP          |
| **\_контекст хснмп** | Обработку контекста WinSNMP       |
| **ХСНМП \_ PDU**     | Обработчик для единицы данных протокола    |
| **ХСНМП \_ вбл**     | Handle в список привязок переменных |



 

WinSNMP-приложение может запрашивать, что реализация создает или удаляет дескрипторы ресурсов, но реализация выполняет операцию. Дополнительные сведения об освобождении отдельных ресурсов см. в статье [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)и [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .

 

 




