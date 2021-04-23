---
title: Управление ловушками и уведомлениями
description: Для получения ловушек и уведомлений приложение WinSNMP должно быть зарегистрировано, вызвав функцию Снмпрегистер с параметром СНМПАПИ \_ On. Приложение может отменить регистрацию и отключить ловушки и уведомления, вызвав функцию с параметром СНМПАПИ \_ Off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888868"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="fc33e-104">Управление ловушками и уведомлениями</span><span class="sxs-lookup"><span data-stu-id="fc33e-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="fc33e-105">Для получения ловушек и уведомлений приложение WinSNMP должно быть зарегистрировано, вызвав функцию [**снмпрегистер**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) с параметром снмпапи \_ On.</span><span class="sxs-lookup"><span data-stu-id="fc33e-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="fc33e-106">Приложение может отменить регистрацию и отключить ловушки и уведомления, вызвав функцию с параметром СНМПАПИ \_ Off.</span><span class="sxs-lookup"><span data-stu-id="fc33e-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="fc33e-107">Если приложение вызывает **снмпрегистер**, доступны несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="fc33e-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="fc33e-108">Приложение может регистрироваться или отменять регистрацию для следующих ловушек и уведомлений:</span><span class="sxs-lookup"><span data-stu-id="fc33e-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="fc33e-109">Один тип ловушки или уведомления</span><span class="sxs-lookup"><span data-stu-id="fc33e-109">One type of trap or notification</span></span>
-   <span data-ttu-id="fc33e-110">Все ловушки и уведомления</span><span class="sxs-lookup"><span data-stu-id="fc33e-110">All traps and notifications</span></span>
-   <span data-ttu-id="fc33e-111">Все источники запросов на ловушки и уведомления</span><span class="sxs-lookup"><span data-stu-id="fc33e-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="fc33e-112">Ловушки и уведомления из всех сущностей управления</span><span class="sxs-lookup"><span data-stu-id="fc33e-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="fc33e-113">Ловушки и уведомления для каждого контекста</span><span class="sxs-lookup"><span data-stu-id="fc33e-113">Traps and notifications for every context</span></span>

<span data-ttu-id="fc33e-114">Чтобы зарегистрировать и получить предопределенную ловушку или тип уведомления, приложение должно определить идентификатор объекта (структуру [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) для каждого предопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="fc33e-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="fc33e-115">Структура должна содержать последовательность сопоставления шаблонов для типа ловушки или уведомления.</span><span class="sxs-lookup"><span data-stu-id="fc33e-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="fc33e-116">RFC 1907, «база данных управления для версии 2 протокола простого сетевого управления (SNMPv2)», определяет идентификаторы объектов Trap и Notification.</span><span class="sxs-lookup"><span data-stu-id="fc33e-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="fc33e-117">Чтобы получить необработанные данные и уведомления о ловушках для сеанса WinSNMP, приложение WinSNMP должно вызвать функцию [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) с помощью обработчика сеанса, возвращенного функцией [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="fc33e-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="fc33e-118">Дополнительные сведения см. в разделе [Отправка SNMP-сообщений](sending-snmp-messages.md) и [Получение сообщений SNMP](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="fc33e-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="fc33e-119">Дополнительные сведения о выделении и освобождении ресурсов для ловушек и уведомлений см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fc33e-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




