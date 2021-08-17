---
title: Типы запросов SNMP (SNMP. h)
description: Типы запросов SNMP используются для описания операции, которую служба SNMP запрашивает для выполнения агентом расширения.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c4dfdfc6d65e63b8cd00956627eef9e831c46c6979e44634067b1e29defc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142997"
---
# <a name="snmp-request-types"></a>Типы запросов SNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Типы запросов SNMP используются для описания операции, которую служба SNMP запрашивает для выполнения агентом расширения.



| Константа/значение                                                                                                                                                                                                                                                          | Описание                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**Протокол SNMP \_ получение \_ расширения**</dt> <dt> \_ PDU SNMP \_ Get</dt> </dl>                       | Получение значений указанных переменных.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**Протокол SNMP \_ \_Get \_**</dt> -следующий <dt>SNMP- \_ \_ PDU</dt> расширения </dl>   | Получение значения или значений последователя лексикографическим порядком заданных переменных.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**Протокол SNMP \_ РАСШИРЕНИЕ \_ " \_ получить**</dt> многоблочный <dt> \_ \_ PDU SNMP</dt> " </dl>   | Поиск и получение нескольких значений с помощью одного запроса.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**\_ \_ Проверка набора расширения \_ SNMP**</dt> </dl>                                                                           | Проверьте значения указанных переменных. Эта операция увеличивает вероятность успешной операции записи во время запроса на ФИКСАЦИю. Дополнительные сведения см. в описании функции [**снмпекстенсионкуерекс**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**Протокол SNMP \_ набор расширения " \_ \_ фиксация**</dt> <dt>SNMP- \_ \_ распределения</dt> " </dl> | Запишите новые значения в указанные переменные.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**\_расширение SNMP \_ Set \_ Undo**</dt> </dl>                                                                           | Сбросьте значения указанных переменных до запроса ФИКСАЦИи.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**\_ \_ Очистка набора расширений \_ SNMP**</dt> </dl>                                                                  | Освободите ресурсы, выделенные в предыдущих запросах и операциях.<br/>                                                                                                                                                                             |



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

 

