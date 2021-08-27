---
title: Задачи WinSNMP программирования
description: В следующей таблице перечислены основные процедуры программирования, которые необходимо выполнить для создания кода для приложения WinSNMP, а также разделы, содержащие сведения об этих задачах.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb83d6d61311866ddb84d3980f5742f82f51405
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479400"
---
# <a name="winsnmp-programming-tasks"></a>Задачи WinSNMP программирования

В следующей таблице перечислены основные процедуры программирования, которые необходимо выполнить для создания кода для приложения WinSNMP, а также разделы, содержащие сведения об этих задачах.




| Задача программирования | Функции и разделы, связанные с задачами | 
|------------------|----------------------------------|
| Откройте приложение WinSNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>снмпстартуп</strong></a>. См. раздел <a href="opening-and-closing-a-winsnmp-application.md">Открытие и закрытие приложения WinSNMP</a>.<br /> | 
| Откройте один или несколько сеансов WinSNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a>. См. раздел <a href="opening-and-closing-a-winsnmp-session.md">Открытие и закрытие сеанса WinSNMP</a>.<br /> | 
| Зарегистрируйтесь для получения ловушек или уведомлений. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>снмпрегистер</strong></a>. См. раздел <a href="managing-traps-and-notifications.md">Управление ловушками и уведомлениями</a>.<br /> | 
| Создайте один или несколько списков привязок переменных для Организации в PDU. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>снмпкреатевбл</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>снмпдупликатевбл</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>снмпсетвб</strong></a>. См. раздел <a href="working-with-variable-binding-lists.md">Работа с списками привязок переменных</a>.<br /><blockquote>[!Note]<br />Приложению может потребоваться вызвать другие <a href="winsnmp-functions.md">функции привязки переменных</a> для создания списка привязок переменных.</blockquote><br /> | 
| Создайте одно или несколько устройств PDU для передачи и обработки. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>снмпкреатепду</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>снмпсетпдудата</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>снмпдупликатепду</strong></a>. См. раздел <a href="working-with-protocol-data-units.md">Работа с единицами данных протокола</a>.<br /><blockquote>[!Note]<br />Приложению может потребоваться вызвать другие <a href="winsnmp-functions.md">функции PDU</a> и <a href="winsnmp-functions.md">функции WinSNMP Utility</a> для создания PDU.</blockquote><br /> | 
| Отправьте один или несколько запросов на операции SNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>снмпсендмсг</strong></a>. См. раздел <a href="sending-snmp-messages.md">Отправка SNMP-сообщений</a>.<br /> | 
| Получите ответ на запрос операции SNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>снмпреквмсг</strong></a>. См. раздел <a href="receiving-snmp-messages.md">Получение SNMP-сообщений</a>.<br /> | 
| Обработка ответа на запрос. | Используйте логику конкретного приложения. | 
| Закройте каждый сеанс WinSNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>снмпклосе</strong></a>. См. раздел <a href="opening-and-closing-a-winsnmp-session.md">Открытие и закрытие сеанса WinSNMP</a>.<br /> | 
| Закройте приложение WinSNMP. | Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>снмпклеануп</strong></a>. См. раздел <a href="opening-and-closing-a-winsnmp-application.md">Открытие и закрытие приложения WinSNMP</a>.<br /> | 




 

Следующие разделы содержат дополнительные сведения о других общих концепциях программирования, характерных для среды WinSNMP.



| Раздел                                                              | Основные понятия                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Общие задачи программирования](general-winsnmp-programming-tasks.md) | [Управление идентификаторами объектов](managing-object-identifiers.md)[освобождение дескрипторов WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Настройка режима преобразования объектов и контекста](setting-the-entity-and-context-translation-mode.md)<br/> [Управление политикой повторной передачи](managing-the-retransmission-policy.md)<br/> [Создание WinSNMP Applications с несколькими потоками](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Регистрация приложения агента SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Кроме того, приложению WinSNMP может потребоваться включить вызовы следующих функций WinSNMP: [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)и [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Это позволяет реализации Microsoft WinSNMP освобождать объекты WinSNMP Memory. Как правило, приложение WinSNMP должно освобождать все ресурсы, выделенные в результате вызова функции WinSNMP. Дополнительные сведения о освобождении ресурсов см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).

 

 





