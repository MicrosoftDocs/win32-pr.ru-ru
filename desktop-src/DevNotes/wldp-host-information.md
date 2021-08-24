---
description: Структура, идентифицирующая узел и исходный файл для оценки.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Структура WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404073"
---
# <a name="wldp_host_information-structure"></a>\_ \_ Структура сведений о узле WLDP

Структура, идентифицирующая узел и исходный файл для оценки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**двревисион**
</dt> <dd>

Должна быть **WLDPа \_ \_ \_ версия сведений об узле**.

</dd> <dt>

**двхостид**
</dt> <dd>

Значение перечисления из [**\_ \_ идентификатора узла WLDP**](wldp-host-id.md) , описывающее идентификатор узла.

</dd> <dt>

**сзсаурце**
</dt> <dd>

Полный путь и имя скрипта с расширением. Значение NULL **для \_ \_ \_ глобального идентификатора узла WLDP** или выполнение скрипта вручную.

</dd> <dt>

**хсаурце**
</dt> <dd>

В дополнение к имени вызывающий объект может указать обработчик для файла, используемого для проверки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




