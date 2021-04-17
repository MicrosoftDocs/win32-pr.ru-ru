---
description: Является устаревшим и не должен использоваться.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Структура адреса (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663456"
---
# <a name="address-structure"></a>Структура адреса

Структура **адресов** устарела и не должна использоваться.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Тип адреса. Значением может быть одно из следующих.

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Представление данных, выраженное в виде необработанного MAC-адреса.

</dd> <dt>

**IPAddress**
</dt> <dd>

Представление данных, выраженное в виде необработанного IP-адреса.

</dd> <dt>

**ипксраваддресс**
</dt> <dd>

Представление данных, выраженное в виде необработанного IPX-адреса.

</dd> <dt>

**ипксаддресс**
</dt> <dd>

Представление данных, выраженное в виде декодированного значения IPX-адреса.

</dd> <dt>

**винесиправаддресс**
</dt> <dd>

Представление данных, выраженное в виде IP-адреса необработанных Vines.

</dd> <dt>

**винесипаддресс**
</dt> <dd>

Представление данных, выраженное в виде IP-адреса декодированных Vines.

</dd> <dt>

**есернетсркаддресс**
</dt> <dd>

Представление данных, выраженное в виде адреса источника Ethernet.

</dd> <dt>

**есернетдстаддресс**
</dt> <dd>

Представление данных, выраженное в виде адреса назначения Ethernet.

</dd> <dt>

**токенрингсркаддресс**
</dt> <dd>

Представление данных в виде адреса источника Token Ring.

</dd> <dt>

**токенрингдстаддресс**
</dt> <dd>

Представление данных в виде адреса назначения Token Ring.

</dd> <dt>

**фддисркаддресс**
</dt> <dd>

Представление данных, выраженное в виде исходного адреса FDDI.

</dd> <dt>

**фддидстаддресс**
</dt> <dd>

Представление данных, выраженное в виде адреса назначения FDDI.

</dd> <dt>

**Флаги**
</dt> <dd>

Набор флагов, которые изменяют свойства адреса.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




