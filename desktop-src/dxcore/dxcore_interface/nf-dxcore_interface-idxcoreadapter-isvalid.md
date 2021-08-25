---
title: IDXCoreAdapter::IsValid
description: Определяет, является ли этот объект адаптера Дкскоре допустимым.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6b8a0ccadb46f20db9c5f2a23ac8709b391254ee453f05424dadee309f33fc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842544"
---
# <a name="idxcoreadapterisvalid-method"></a>Метод Идкскореадаптер:: IsValid

Определяет, является ли этот объект адаптера Дкскоре допустимым. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Возвращаемое значение

Тип: **bool** .

Возвращает значение `true` , если объект адаптера дкскоре по-прежнему является допустимым. В противном случае возвращается `false`.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)