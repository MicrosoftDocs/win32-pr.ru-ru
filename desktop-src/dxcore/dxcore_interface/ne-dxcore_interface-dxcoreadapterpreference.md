---
title: DXCoreAdapterPreference
description: Определяет константы, указывающие параметры адаптера Дкскоре для использования в качестве критерия сортировки списка.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117734"
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

## <a name="see-also"></a>См. также

[Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)