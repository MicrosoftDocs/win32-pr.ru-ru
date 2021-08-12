---
title: IDXCoreAdapter::IsPropertySupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) указанное свойство адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ddee6bea5af8fb64dfa2bfc15392e92239e7326b34cbd93cbd112559a6027912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279235"
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

Возвращает значение `true` , если этот объект адаптера дкскоре и текущая операционная система (ОС) поддерживают указанное свойство адаптера. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)