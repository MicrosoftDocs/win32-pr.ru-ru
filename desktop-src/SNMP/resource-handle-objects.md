---
title: Объекты «обработчик ресурсов»
description: Структура объекта ресурса ограничена реализацией Microsoft WinSNMP. Приложение WinSNMP может обращаться к объекту ресурса с помощью маркера.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778596"
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

 

 




