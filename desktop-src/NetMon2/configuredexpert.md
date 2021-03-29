---
description: Структура КОНФИГУРЕДЕКСПЕРТ связывает эксперт с данными конфигурации.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Структура КОНФИГУРЕДЕКСПЕРТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264698"
---
# <a name="configuredexpert-structure"></a>Структура КОНФИГУРЕДЕКСПЕРТ

Структура **конфигуредексперт** связывает эксперт с данными конфигурации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Члены

<dl> <dt>

**хексперт**
</dt> <dd>

Обрабатывайте эксперта.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Значения флага запуска эксперта.

</dd> <dt>

**pConfig**
</dt> <dd>

Указатель на структуру [**експертконфиг**](expertconfig.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




