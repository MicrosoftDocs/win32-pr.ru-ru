---
title: IDXCoreAdapter::IsAttributeSupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре указанный атрибут адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413106"
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

Возвращает  `true`   , если этот объект адаптера дкскоре поддерживает указанный атрибут адаптера. В противном случае возвращает  `false` .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)