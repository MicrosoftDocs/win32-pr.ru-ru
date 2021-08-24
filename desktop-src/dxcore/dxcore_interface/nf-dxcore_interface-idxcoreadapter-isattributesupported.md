---
title: IDXCoreAdapter::IsAttributeSupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре указанный атрибут адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787084"
---
# <a name="idxcoreadapterisattributesupported-method"></a>Метод Идкскореадаптер:: Исаттрибутесуппортед

Определяет, поддерживает ли этот объект адаптера Дкскоре указанный атрибут адаптера.

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="attributeguid"></a>аттрибутегуид

Тип: **рефгуид**

Ссылка на GUID атрибута адаптера. Список идентификаторов GUID атрибутов см. в разделе [идентификаторы GUID атрибута адаптера дкскоре](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает `true` , если этот объект адаптера дкскоре поддерживает указанный атрибут адаптера. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)