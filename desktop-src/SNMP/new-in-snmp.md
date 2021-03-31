---
title: Новые в SNMP
description: Протокол SNMP поддерживает использование IPv6, начиная с Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793488"
---
# <a name="new-in-snmp"></a>Новые в SNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Протокол SNMP поддерживает использование IPv6, начиная с Windows Vista. Однако протокол SNMP поддерживает IPv6 только для сетей под управлением Windows Server 2008 и Windows Vista. Это связано с тем, что для поддержки IPv6 протоколу SNMP требуется обновленный стек протокола, доступный в этих операционных системах.

Если сеть не является исключительно сетью Windows Server 2008, связь по протоколу IPv6 завершится сбоем, даже если на тех компьютерах, где работают предыдущие версии Windows, установлен стек протокола IPv6. Например, агенты SNMP, работающие на Windows Server 2003, Windows XP или Windows 2000, отвечают только на запросы, созданные для их IPv4-адресов.

 

 