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
# <a name="winsnmp-api"></a>WinSNMP API

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Интерфейс программирования приложений Microsoft Windows SNMP (WinSNMP API) версии 1.1 a и 2,0 позволяет разрабатывать приложения управления сетью на основе SNMP, выполняемые в среде Windows. Протокол SNMP — это протокол запроса-ответа, который передает управляющие данные между сущностями протокола.

Ошибка WinSNMP была разработана совместно с совместным использованием, вводом и поддержкой из нескольких компаний, ассоциаций и отдельных пользователей.

В первой части этого обзора содержатся сведения о дополнении WinSNMP 2,0, версиях SNMP и список соответствующих запросов на комментарии (RFC). Кроме того, здесь описывается модель WinSNMP, а также компоненты и функции реализации Microsoft WinSNMP. В нем также содержатся сведения о концепциях управления данными и связи, которые необходимо программировать в среде WinSNMP.

Во втором разделе обсуждаются функции WinSNMP и следующие связанные задачи WinSNMP:

-   [Открытие и закрытие WinSNMP приложения](opening-and-closing-a-winsnmp-application.md)
-   [Открытие и закрытие сеанса WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Управление ловушками и уведомлениями](managing-traps-and-notifications.md)
-   [Работа с списками привязок переменных](working-with-variable-binding-lists.md)
-   [Работа с единицами данных протокола](working-with-protocol-data-units.md)
-   [Отправка SNMP-сообщений](sending-snmp-messages.md)
-   [Получение сообщений SNMP](receiving-snmp-messages.md)
-   [Управление идентификаторами объектов](managing-object-identifiers.md)
-   [Освобождение дескрипторов WinSNMP](freeing-winsnmp-descriptors.md)
-   [Настройка режима преобразования объектов и контекста](setting-the-entity-and-context-translation-mode.md)
-   [Управление политикой повторной передачи](managing-the-retransmission-policy.md)
-   [Создание WinSNMP Applications с несколькими потоками](writing-winsnmp-applications-with-multiple-threads.md)
-   [Регистрация приложения агента SNMP](registering-an-snmp-agent-application.md)

Прежде чем читать этот обзор, ознакомьтесь с основными понятиями по программированию SNMP и Windows. Дополнительные сведения о протоколе SNMP см. в статьях об использовании [простого протокола управления сетью](simple-network-management-protocol-snmp-.md) и соответствующих запросов на комментарии (RFC), опубликованных в IETF.

 

 