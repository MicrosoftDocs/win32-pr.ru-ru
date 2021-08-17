---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Определяет, понимается ли заданное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) операционной системой.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502585"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>Метод Идкскореадаптерлист:: Исадаптерпреференцесуппортед

## <a name="description"></a>Описание

Определяет, понимается ли указанное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) текущей операционной системой (ОС). Можно вызвать **исадаптерпреференцесуппортед** перед вызовом [Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Синтаксис

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Параметры

### <a name="preference"></a>preference

Тип: **[дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) , которое будет проверяться на наличие поддержки операционной системы.

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает значение, `true` Если тип сортировки понимается текущей ОС. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)