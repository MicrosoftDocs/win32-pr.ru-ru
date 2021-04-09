---
title: Изменение политики повторной передачи
description: Реализация Microsoft WinSNMP обеспечивает поддержку политики повторной передачи, сохраняя значение времени ожидания и число повторных попыток для приложения WinSNMP в базе данных.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888424"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="d7fd3-103">Изменение политики повторной передачи</span><span class="sxs-lookup"><span data-stu-id="d7fd3-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="d7fd3-104">Реализация Microsoft WinSNMP обеспечивает поддержку политики повторной передачи, сохраняя значение времени ожидания и число повторных попыток для приложения WinSNMP в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="d7fd3-105">Реализация хранит значения для отдельных целевых сущностей.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="d7fd3-106">Реализация изначально предоставляет значения по умолчанию для этих элементов, но приложение может добавлять или изменять значения для отдельных сущностей.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="d7fd3-107">Вызов функций [**снмпжеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) и [**снмпжетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) возвращает значения времени ожидания и количества повторных попыток для определенной целевой сущности.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="d7fd3-108">Чтобы изменить значение времени ожидания, приложение WinSNMP должно вызвать функцию [**снмпсеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) .</span><span class="sxs-lookup"><span data-stu-id="d7fd3-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="d7fd3-109">Чтобы изменить значение счетчика повторных попыток, приложение должно вызвать функцию [**снмпсетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) .</span><span class="sxs-lookup"><span data-stu-id="d7fd3-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="d7fd3-110">Обновленные параметры влияют на новые запросы сообщений SNMP на целевую сущность.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




