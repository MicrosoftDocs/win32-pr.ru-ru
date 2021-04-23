---
title: Открытие и закрытие сеанса WinSNMP
description: Чтобы открыть сеанс, приложение вызывает функцию Снмпкреатесессион.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068298"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="444f0-103">Открытие и закрытие сеанса WinSNMP</span><span class="sxs-lookup"><span data-stu-id="444f0-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="444f0-104">Чтобы открыть сеанс, приложение вызывает функцию [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="444f0-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="444f0-105">Если функция завершается успешно, реализация Microsoft WinSNMP открывает сеанс, а функция возвращает идентификатор сеанса в виде **хснмп \_ сеанса** .</span><span class="sxs-lookup"><span data-stu-id="444f0-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="444f0-106">Все функции WinSNMP, которые возвращают переменные обработчика, включают идентификатор сеанса в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="444f0-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="444f0-107">Это позволяет реализации использовать этот обработчик для эффективного управления ресурсами на уровне сеанса.</span><span class="sxs-lookup"><span data-stu-id="444f0-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="444f0-108">В приложении может быть открыто несколько сеансов одновременно.</span><span class="sxs-lookup"><span data-stu-id="444f0-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="444f0-109">Несколько сеансов в приложении могут совместно использовать переменные управления.</span><span class="sxs-lookup"><span data-stu-id="444f0-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="444f0-110">Если реализация не может открыть сеанс из-за ограничений ресурсов, она возвращает СНМПАПИ \_ ошибку, когда приложение вызывает [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="444f0-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="444f0-111">Если приложение вызывает функцию [**снмпжетластеррор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , возвращается \_ Ошибка выделения снмпапи \_ .</span><span class="sxs-lookup"><span data-stu-id="444f0-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="444f0-112">Вызов функции [**снмпклосе**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) позволяет реализации освободить все оставшиеся ресурсы и закрыть сеанс.</span><span class="sxs-lookup"><span data-stu-id="444f0-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="444f0-113">Дополнительные сведения см. в разделе [объекты обработчика ресурсов](resource-handle-objects.md) и [WinSNMP Sessions](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="444f0-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




