---
title: Структура CB_TARGET_INFO (Кбклиент. h)
description: Содержит сведения о целевом компьютере и IP-адресах, на которые должны перенаправляться входящие подключения.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO структуры службы удаленных рабочих столов
- PCB_TARGET_INFO службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e7c00e1997ee36b42b21b833942597d9b43f393b2bcdfcee1aa0ee18e3a4548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001612"
---
# <a name="cb_target_info-structure"></a>\_ \_ Структура сведений о целевом объекте CB

Содержит сведения о целевом компьютере и IP-адресах, на которые должны перенаправляться входящие подключения. Эта структура используется с методом [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**ServerName**
</dt> <dd>

Представляет полное доменное имя целевого сервера. Для сценария удаленный рабочий стол Virtualization (RDV) этот член имеет **значение NULL**. Для сценария узла удаленный рабочий стол сеансов (узлов сеансов удаленных рабочих столов) этот член содержит имя сервера, на котором перенаправляется входящее подключение.

</dd> <dt>

**аддресскаунт**
</dt> <dd>

Количество допустимых записей в массиве **addresses** .

</dd> <dt>

**Адреса**
</dt> <dd>

Массив строк, содержащий IP-адреса, на которые перенаправляются входящие подключения. Число допустимых элементов в этом массиве указано в элементе **аддресскаунт** .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иконнектионброкерклиент:: Жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





