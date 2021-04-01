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
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072357"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




