---
title: Перевод ловушек с SNMPv2C
description: Когда реализация Microsoft WinSNMP получает ловушки из сущности, работающей в среде с платформой версии Майкрософт, она преобразует ловушки в формат SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887983"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="6134f-103">Перевод ловушек с SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="6134f-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="6134f-104">Когда реализация Microsoft WinSNMP получает ловушки из сущности, работающей в среде с платформой версии Майкрософт, она преобразует ловушки в формат SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6134f-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="6134f-105">Таким образом, когда [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) доставляет ловушку, она всегда находится в формате SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="6134f-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="6134f-106">RFC 1908, "сосуществование между версией 1 и версией 2 стандартной инфраструктуры управления сетью", определяет правила преобразования из стандарта в формат ловушек SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6134f-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="6134f-107">Приложение WinSNMP может проверить последнюю запись привязки переменной в списке привязок переменных, чтобы определить, является ли запись ловушкой, переведенной из неформатированного формата в формат SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6134f-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="6134f-108">Если да, Последняя привязка переменной всегда будет равна значению «Снмптрапентерприсеоид. 0».</span><span class="sxs-lookup"><span data-stu-id="6134f-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="6134f-109">Дополнительные сведения см. в разделе [Управление ловушками и уведомлениями](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6134f-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




