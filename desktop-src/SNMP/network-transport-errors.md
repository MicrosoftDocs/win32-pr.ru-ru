---
title: Ошибки сетевого транспорта
description: Реализация Microsoft WinSNMP может обнаружить ошибку сетевого транспорта после передачи сообщения SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15284bba97f2dda8d2fb4224dc2c94bd14050afb9463c73b4d297c1647ec273f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009312"
---
# <a name="network-transport-errors"></a>Ошибки сетевого транспорта

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Реализация Microsoft WinSNMP может обнаружить ошибку сетевого транспорта после передачи сообщения SNMP. В этом случае реализация отправляет уведомление о получении данных сеансу WinSNMP, который инициировал запрос на обмен данными. Реализация также возвращает СНМПАПИ \_ сбой при следующем вызове функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) для сеанса. Функция **снмпреквмсг** завершает работу с расширенным кодом ошибки, указывающим на ошибку транспортного уровня сети.

Список конкретных ошибок транспортного уровня см. на страницах справочника по функциям [**снмпрегистер**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)и [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 