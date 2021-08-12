---
title: IDXCoreAdapter
description: Интерфейс **идкскореадаптер** реализует методы для получения сведений об элементе адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278791"
---
# <a name="idxcoreadapter-interface"></a>Интерфейс Идкскореадаптер

Интерфейс **идкскореадаптер** реализует методы для получения сведений об элементе адаптера. **Идкскореадаптер** наследует от интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Remarks

Свойства адаптера устанавливаются во время запуска адаптера и становятся неизменяемыми в течение времени существования адаптера. Это отличается от состояния адаптера, которое можно запрашивать или задавать, а значения, которые могут меняться со временем.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)