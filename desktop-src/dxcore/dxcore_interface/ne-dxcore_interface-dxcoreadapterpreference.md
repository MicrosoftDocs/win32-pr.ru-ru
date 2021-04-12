---
title: DXCoreAdapterPreference
description: Определяет константы, указывающие параметры адаптера Дкскоре для использования в качестве критерия сортировки списка.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413390"
---
# <a name="dxcoreadapterpreference-enum"></a>Перечисление Дкскореадаптерпреференце

## <a name="description"></a>Описание

Определяет константы, указывающие параметры адаптера Дкскоре для использования в качестве критерия сортировки списка. Список адаптеров Дкскоре можно отсортировать, передав массив **дкскореадаптерпреференце** в [Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Синтаксис

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Поля перечислений

### <a name="hardware"></a>Оборудование

Задает предпочтения для аппаратных адаптеров (в отличие от программных адаптеров).

### <a name="minimumpower"></a>минимумповер

Указывает предпочитаемый для него графический процессор (например, встроенный графический процессор или ИГПУ).

### <a name="highperformance"></a>HighPerformance.

Задает предпочитаемый для высокопроизводительного графического процессора, например внешний графический процессор (Ксгпу), если он доступен, или дискретный графический процессор (ДГПУ), если он доступен.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)