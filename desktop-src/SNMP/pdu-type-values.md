---
title: Значения типа PDU (SNMP. h)
description: Значения типа PDU используются в поле типа PDU блока \_ распределения для описания его типа.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492324"
---
# <a name="pdu-type-values"></a>Значения типа PDU

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Значения типа PDU используются в поле **\_ типа PDU** блока распределения для описания его типа.



| Константа                                                                                                                                                                   | Описание                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**\_Получение PDU \_ SNMP**</dt> </dl>                | Поиск и получение значения из указанной переменной SNMP.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP- \_ PDU- \_ следующее**</dt> </dl>    | Найдите и получите значение переменной SNMP, не зная точное имя переменной.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**отклик SNMP- \_ PDU \_**</dt> </dl> | Ответьте на запрос на \_ Получение или прерывание SNMP-распределения SNMP \_ \_ \_ .<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_набор PDU \_ SNMP**</dt> </dl>                | Сохранение значения в указанной переменной SNMP.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**\_V1TRAP PDU \_ SNMP**</dt> </dl>       | Указывает, что ловушка PDU форматируется для обеспечения соответствия стандарту стандарта стандартизации.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**\_массив PDU \_ SNMP**</dt> </dl>    | Поиск и получение нескольких значений с помощью одного запроса.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**оповещения SNMP- \_ PDU \_**</dt> </dl>       | Указывает PDU запроса уведомления.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**\_ \_ ловушка PDU SNMP**</dt> </dl>             | Оповещает систему управления о непредвиденном событии в SNMPv2C.<br/>                             |



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

 

