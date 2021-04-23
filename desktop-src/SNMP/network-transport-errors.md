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
# <a name="network-transport-errors"></a><span data-ttu-id="3c340-103">Ошибки сетевого транспорта</span><span class="sxs-lookup"><span data-stu-id="3c340-103">Network Transport Errors</span></span>

<span data-ttu-id="3c340-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3c340-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3c340-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="3c340-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3c340-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="3c340-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="3c340-107">Реализация Microsoft WinSNMP может обнаружить ошибку сетевого транспорта после передачи сообщения SNMP.</span><span class="sxs-lookup"><span data-stu-id="3c340-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="3c340-108">В этом случае реализация отправляет уведомление о получении данных сеансу WinSNMP, который инициировал запрос на обмен данными.</span><span class="sxs-lookup"><span data-stu-id="3c340-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="3c340-109">Реализация также возвращает СНМПАПИ \_ сбой при следующем вызове функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="3c340-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="3c340-110">Функция **снмпреквмсг** завершает работу с расширенным кодом ошибки, указывающим на ошибку транспортного уровня сети.</span><span class="sxs-lookup"><span data-stu-id="3c340-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="3c340-111">Список конкретных ошибок транспортного уровня см. на страницах справочника по функциям [**снмпрегистер**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)и [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="3c340-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 