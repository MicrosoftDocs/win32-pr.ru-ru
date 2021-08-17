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
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139117"
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

 

 





