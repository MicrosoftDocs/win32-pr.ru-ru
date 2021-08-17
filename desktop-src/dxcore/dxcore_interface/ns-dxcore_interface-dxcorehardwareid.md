---
title: DXCoreHardwareID
description: Представляет компоненты идентификатора оборудования PnP для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118631"
---
# <a name="dxcorehardwareid-structure"></a>Структура Дкскорехардвареид

Представляет компоненты идентификатора оборудования PnP для адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Члены

### <a name="vendorid"></a>Поставщика

Тип: **uint32_t \***

Идентификатор PCI поставщика оборудования адаптера.

### <a name="deviceid"></a>deviceId

Тип: **uint32_t \***

Идентификатор PCI аппаратного устройства адаптера.

### <a name="subsysid"></a>субсисид

Тип: **uint32_t \***

Идентификатор PCI аппаратной подсистемы адаптера.

### <a name="revision"></a>revision

Тип: **uint32_t \***

Идентификатор PCI для номера редакции адаптера.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)