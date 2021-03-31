---
title: Перечисление CB_RESOURCE_TYPE (Кбклиент. h)
description: Указывает тип ресурса, к которому подключается входящее подключение.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Перечисление CB_RESOURCE_TYPE службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801588"
---
# <a name="cb_resource_type-enumeration"></a>\_ \_ Перечисление типов ресурсов CB

Указывает тип ресурса, к которому подключается входящее подключение. Это перечисление используется со структурой [**\_ \_ сведений о соединении CB**](cb-connection-info.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**ресурс CB не \_ \_ определен**
</dt> <dd>

Тип ресурса не определен.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_сеанс ресурсов \_ CB**
</dt> <dd>

Ресурс является удаленным сеансом.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_ \_ Виртуальная машина ресурса CB**
</dt> <dd>

Ресурс является виртуальной машиной.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ сведения о подключении CB**](cb-connection-info.md)
</dt> </dl>

 

 





