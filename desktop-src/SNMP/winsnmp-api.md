---
title: WinSNMP API
description: Интерфейс программирования приложений Microsoft Windows SNMP (WinSNMP API) версии 1.1 a и 2,0 позволяет разрабатывать приложения управления сетью на основе SNMP, выполняемые в среде Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070339"
---
# <a name="winsnmp-api"></a><span data-ttu-id="86447-104">WinSNMP API</span><span class="sxs-lookup"><span data-stu-id="86447-104">WinSNMP API</span></span>

<span data-ttu-id="86447-105">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="86447-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86447-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="86447-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="86447-107">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="86447-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="86447-108">Интерфейс программирования приложений Microsoft Windows SNMP (WinSNMP API) версии 1.1 a и 2,0 позволяет разрабатывать приложения управления сетью на основе SNMP, выполняемые в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="86447-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="86447-109">Протокол SNMP — это протокол запроса-ответа, который передает управляющие данные между сущностями протокола.</span><span class="sxs-lookup"><span data-stu-id="86447-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="86447-110">Ошибка WinSNMP была разработана совместно с совместным использованием, вводом и поддержкой из нескольких компаний, ассоциаций и отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="86447-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="86447-111">В первой части этого обзора содержатся сведения о дополнении WinSNMP 2,0, версиях SNMP и список соответствующих запросов на комментарии (RFC).</span><span class="sxs-lookup"><span data-stu-id="86447-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="86447-112">Кроме того, здесь описывается модель WinSNMP, а также компоненты и функции реализации Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="86447-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="86447-113">В нем также содержатся сведения о концепциях управления данными и связи, которые необходимо программировать в среде WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="86447-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="86447-114">Во втором разделе обсуждаются функции WinSNMP и следующие связанные задачи WinSNMP:</span><span class="sxs-lookup"><span data-stu-id="86447-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="86447-115">Открытие и закрытие WinSNMP приложения</span><span class="sxs-lookup"><span data-stu-id="86447-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="86447-116">Открытие и закрытие сеанса WinSNMP</span><span class="sxs-lookup"><span data-stu-id="86447-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="86447-117">Управление ловушками и уведомлениями</span><span class="sxs-lookup"><span data-stu-id="86447-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="86447-118">Работа с списками привязок переменных</span><span class="sxs-lookup"><span data-stu-id="86447-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="86447-119">Работа с единицами данных протокола</span><span class="sxs-lookup"><span data-stu-id="86447-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="86447-120">Отправка SNMP-сообщений</span><span class="sxs-lookup"><span data-stu-id="86447-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="86447-121">Получение сообщений SNMP</span><span class="sxs-lookup"><span data-stu-id="86447-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="86447-122">Управление идентификаторами объектов</span><span class="sxs-lookup"><span data-stu-id="86447-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="86447-123">Освобождение дескрипторов WinSNMP</span><span class="sxs-lookup"><span data-stu-id="86447-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="86447-124">Настройка режима преобразования объектов и контекста</span><span class="sxs-lookup"><span data-stu-id="86447-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="86447-125">Управление политикой повторной передачи</span><span class="sxs-lookup"><span data-stu-id="86447-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="86447-126">Создание WinSNMP Applications с несколькими потоками</span><span class="sxs-lookup"><span data-stu-id="86447-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="86447-127">Регистрация приложения агента SNMP</span><span class="sxs-lookup"><span data-stu-id="86447-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="86447-128">Прежде чем читать этот обзор, ознакомьтесь с основными понятиями по программированию SNMP и Windows.</span><span class="sxs-lookup"><span data-stu-id="86447-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="86447-129">Дополнительные сведения о протоколе SNMP см. в статьях об использовании [простого протокола управления сетью](simple-network-management-protocol-snmp-.md) и соответствующих запросов на комментарии (RFC), опубликованных в IETF.</span><span class="sxs-lookup"><span data-stu-id="86447-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 