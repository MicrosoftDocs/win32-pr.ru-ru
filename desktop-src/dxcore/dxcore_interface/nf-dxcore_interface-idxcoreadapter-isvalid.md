---
title: IDXCoreAdapter::IsValid
description: Определяет, является ли этот объект адаптера Дкскоре допустимым.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070382"
---
# <a name="idxcoreadapterisvalid-method"></a>Метод Идкскореадаптер:: IsValid

Определяет, является ли этот объект адаптера Дкскоре допустимым. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает значение  `true`   , если объект адаптера дкскоре по-прежнему является допустимым. В противном случае возвращает  `false` .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)