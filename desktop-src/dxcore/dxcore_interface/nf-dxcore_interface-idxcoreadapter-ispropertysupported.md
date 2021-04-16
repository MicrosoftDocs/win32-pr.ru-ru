---
title: IDXCoreAdapter::IsPropertySupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) указанное свойство адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719140"
---
# <a name="idxcoreadapterispropertysupported-method"></a>Метод Идкскореадаптер:: Испропертисуппортед

Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) указанное свойство адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="property"></a>свойство;

Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Тип свойства, для которого запрашиваются сведения о поддержке. Дополнительные сведения о каждом свойстве адаптера см. в таблице в [дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md) .

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает значение  `true`   , если этот объект адаптера дкскоре и текущая операционная система (ОС) поддерживают указанное свойство адаптера. В противном случае возвращает  `false` .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)