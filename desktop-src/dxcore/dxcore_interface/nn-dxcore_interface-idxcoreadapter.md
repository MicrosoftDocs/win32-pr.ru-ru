---
title: IDXCoreAdapter
description: Интерфейс **идкскореадаптер**   реализует методы для получения сведений об элементе адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134427"
---
# <a name="idxcoreadapter-interface"></a>Интерфейс Идкскореадаптер

Интерфейс **идкскореадаптер**   реализует методы для получения сведений об элементе адаптера. **Идкскореадаптер** наследует от интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Комментарии

Свойства адаптера устанавливаются во время запуска адаптера и становятся неизменяемыми в течение времени существования адаптера. Это отличается от состояния адаптера, которое можно запрашивать или задавать, а значения, которые могут меняться со временем.

## <a name="see-also"></a>См. также раздел

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)