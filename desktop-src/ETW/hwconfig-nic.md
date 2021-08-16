---
description: '\_Класс NIC хвконфиг является классом типа событий для событий конфигурации сетевых интерфейсных карт. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Класс HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394728"
---
# <a name="hwconfig_nic-class"></a>\_Класс сетевого адаптера хвконфиг

Класс **\_ NIC хвконфиг** является классом типа событий для событий конфигурации сетевых интерфейсных карт.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Члены

Класс **\_ сетевого адаптера хвконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ сетевого адаптера хвконфиг** имеет следующие свойства.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя сетевой карты.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**хвконфиг**](hwconfig.md)
</dt> </dl>

 

 




