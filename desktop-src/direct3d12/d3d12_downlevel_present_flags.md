---
title: Перечисление D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Флаги, передаваемые методу ID3D12CommandQueueDownlevel::P повторной попытке.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 98ff4f1c82c5f44c16a926e900d6eea7d5395138bb9418d9bdba6115d4fbfd88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807594"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>\_ \_ \_ Перечисление флагов предыдущих версий D3D12

Флаги, передаваемые в функцию повторной отправки [**ID3D12CommandQueueDownlevel::P**](id3d12commandqueuedownlevel-present.md) для изменения поведения.

## <a name="syntax"></a>Синтаксис

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Константы

**\_Флаг D3D12 нижнего уровня \_ отсутствует \_ \_**

Параметры не выбраны.

**D3D12ный \_ \_ флаг представления предыдущих версий \_ \_ ожидает \_ \_ вбланк**

**Текущая** операция не будет выполнена до тех пор, пока не вертикальной синхронизации с момента последнего выполнения **ED.**

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------|------------------|
| Заголовок | d3d12downlevel. h |
| DLL    | D3D12.dll (только Windows 7) |

## <a name="see-also"></a>См. также
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Перечисления Direct3D 12 в Windows 7](direct3d-12on7-enumerations.md)
* [справочник по Direct3D 12 на Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
