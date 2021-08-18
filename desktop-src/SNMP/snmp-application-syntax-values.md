---
title: Значения синтаксиса приложения SNMP (SNMP. h)
description: Значения синтаксиса приложения SNMP используются приложениями управления, которые используют API управления Microsoft SNMP.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009032"
---
# <a name="snmp-application-syntax-values"></a>Значения синтаксиса приложения SNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Значения синтаксиса приложения SNMP используются приложениями управления, которые используют API управления Microsoft SNMP.



| Константа                                                                                                                                                                                  | Описание                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**ASN \_ IPAddress**</dt> </dl>                             | Указывает переменную IP-адреса.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**ASN \_ COUNTER32**</dt> </dl>                             | Указывает переменную счетчика.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**ASN \_ значение Gauge32**</dt> </dl>                                   | Указывает переменную датчика. Эта переменная описывает тип Unsigned32 в согласовании с RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**ASN \_ значение TIMETICKS**</dt> </dl>                             | Указывает переменную значение TIMETICKS.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**непрозрачный ASN \_**</dt> </dl>                                      | Указывает непрозрачную переменную.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**ASN \_ COUNTER64**</dt> </dl>                             | Указывает переменную счетчика, которая увеличивается до достижения максимального значения (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**ASN \_ UINTEGER32**</dt> </dl>                          | Указывает на 32-разрядную переменную целых чисел без знака. Эта переменная описывает тип UInteger32 в согласовании с RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | См. раздел ASN \_ значение Gauge32.<br/>                                                                                                     |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Протокол SNMP. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обзор протокола SNMP](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Справочник по SNMP](snmp-reference.md)
</dt> <dt>

[Константы SNMP](snmp-constants.md)
</dt> </dl>

 

