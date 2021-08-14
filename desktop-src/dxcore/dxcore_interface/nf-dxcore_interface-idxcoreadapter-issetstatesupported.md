---
title: IDXCoreAdapter::IsSetStateSupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) установку значения указанного состояния адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: dc63b541a552f1b01792e9f503acc7aeee03ce5ac6cc92e7b70e271ae62a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278982"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>Метод Идкскореадаптер:: Иссетстатесуппортед

Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) установку значения указанного состояния адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="state"></a>state

Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**

Тип элемента состояния, для которого запрашиваются сведения о поддержке. Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает `true` значение, если этот объект адаптера дкскоре и текущая операционная система (ОС) поддерживают задание указанного состояния адаптера. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)