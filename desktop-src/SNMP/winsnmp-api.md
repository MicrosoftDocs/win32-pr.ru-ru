---
title: WinSNMP API
description: интерфейс программирования приложений Microsoft Windows SNMP (WinSNMP API) версий 1.1 a и 2,0 позволяет разрабатывать приложения управления сетью на основе snmp, выполняемые в среде Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142987"
---
# <a name="winsnmp-api"></a>WinSNMP API

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

интерфейс программирования приложений Microsoft Windows SNMP (WinSNMP API) версий 1.1 a и 2,0 позволяет разрабатывать приложения управления сетью на основе snmp, выполняемые в среде Windows. Протокол SNMP — это протокол запроса-ответа, который передает управляющие данные между сущностями протокола.

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

прежде чем читать этот обзор, ознакомьтесь с основными концепциями SNMP и Windowsного программирования. Дополнительные сведения о протоколе SNMP см. в статьях об использовании [простого протокола управления сетью](simple-network-management-protocol-snmp-.md) и соответствующих запросов на комментарии (RFC), опубликованных в IETF.

 

 