---
title: Типы ловушек в нестандартные (SNMP. h)
description: Типы ловушек в спецификации "Стандартный" описывают предопределенный набор универсальных типов ловушек, которые отформатированы в соответствии со стандартом PDU ловушек стандарта.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892678"
---
# <a name="snmpv1-trap-types"></a>Типы ловушек в нестандартные

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Типы ловушек в спецификации "Стандартный" описывают предопределенный набор универсальных типов ловушек, которые отформатированы в соответствии со стандартом PDU ловушек стандарта.



| Константа                                                                                                                                                                                                          | Описание                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**\_COLDSTART SNMP женериктрап \_**</dt> </dl>             | Указывает ловушку холодного запуска. Агент инициализирует сущности протокола в управляемом режиме. Он может изменять объекты в своем представлении.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**\_WARMSTART SNMP женериктрап \_**</dt> </dl>             | Указывает на ловушку горячий запуск. Выполняется повторная инициализация агента, но объекты в его представлении не будут изменены.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**\_ЛИНКДОВН SNMP женериктрап \_**</dt> </dl>                | Обозначает ловушку связи. Состояние подключенного интерфейса изменилось на "отключено". Первая переменная в списке привязок переменных определяет интерфейс.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**\_ЛИНКУП SNMP женериктрап \_**</dt> </dl>                      | Указывает ловушку связи. Подключенный интерфейс изменился с начала до состояния up. Первая переменная в списке привязок переменных определяет интерфейс.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**\_АУСФАИЛУРЕ SNMP женериктрап \_**</dt> </dl>       | Указывает ловушку сбоя проверки подлинности. Сущность SNMP отправила SNMP-сообщение, но оно неверно запросило отнести его к известному сообществу.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**\_ЕГПНЕИГХЛОСС SNMP женериктрап \_**</dt> </dl>    | Указывает ловушку потери соседей ЕГП. Одноранговый узел ЕГП изменился на состояние down. Первая переменная в списке привязок переменных определяет IP-адрес однорангового узла ЕГП.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**\_ЕНТЕРСПЕЦИФИК SNMP женериктрап \_**</dt> </dl> | Указывает ловушку для конкретного предприятия. Произошло непредвиденное событие. Он определяется в параметре *спеЦификтрап* с использованием значения, зависящего от Организации.<br/>               |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Протокол SNMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор протокола SNMP](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Справочник по SNMP](snmp-reference.md)
</dt> <dt>

[Константы SNMP](snmp-constants.md)
</dt> </dl>

 

