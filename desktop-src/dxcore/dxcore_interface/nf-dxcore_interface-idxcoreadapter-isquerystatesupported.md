---
title: IDXCoreAdapter::IsQueryStateSupported
description: Определяет, будет ли этот объект адаптера Дкскоре и текущая поддержка операционной системы (ОС) запрашивать значение указанного состояния адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8ae77c308cb251982947d91e23eaef8f6d828c1233df442cb013bf9737e3c57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279225"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Метод Идкскореадаптер:: Искуеристатесуппортед

Определяет, будет ли этот объект адаптера Дкскоре и текущая поддержка операционной системы (ОС) запрашивать значение указанного состояния адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="state"></a>state

Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**

Тип элемента состояния, для которого запрашиваются сведения о поддержке. Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает значение, `true` Если данный объект адаптера дкскоре и текущая поддержка операционной системы (ОС) запрашивают заданное состояние адаптера. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)