---
description: Тип адреса определяет формат адреса, например Стандартный номер телефона или адрес электронной почты. Только приложения, которые согласовывают TAPI версии 3,0 или выше, могут использовать типы адресов.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Константы LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6555ff934ffb8c1b40b8f35d279a2071cad32b80b754af19672108f5e318a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873340"
---
# <a name="lineaddresstype_-constants"></a>\_Константы линеаддресстипе

Тип адреса определяет формат адреса, например Стандартный номер телефона или адрес электронной почты. Только приложения, которые согласовывают TAPI версии 3,0 или выше, могут использовать типы адресов.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Тип адреса — это стандартный номер телефона.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**ЛИНЕАДДРЕССТИПЕ \_ SDP**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Тип адреса — конференция "Протокол описания сеанса (SDP)".


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**ЛИНЕАДДРЕССТИПЕ \_ емаилнаме**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Тип адреса — это имя электронной почты.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**ЛИНЕАДДРЕССТИПЕ \_ имя_домена**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Тип адреса — имя домена.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**\_IP-адрес линеаддресстипе**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Тип адреса — это IP-адрес.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




