---
title: Ошибки сетевого транспорта
description: Реализация Microsoft WinSNMP может обнаружить ошибку сетевого транспорта после передачи сообщения SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890957"
---
# <a name="network-transport-errors"></a>Ошибки сетевого транспорта

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Реализация Microsoft WinSNMP может обнаружить ошибку сетевого транспорта после передачи сообщения SNMP. В этом случае реализация отправляет уведомление о получении данных сеансу WinSNMP, который инициировал запрос на обмен данными. Реализация также возвращает СНМПАПИ \_ сбой при следующем вызове функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) для сеанса. Функция **снмпреквмсг** завершает работу с расширенным кодом ошибки, указывающим на ошибку транспортного уровня сети.

Список конкретных ошибок транспортного уровня см. на страницах справочника по функциям [**снмпрегистер**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)и [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 