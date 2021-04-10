---
description: Атрибут Time указывает время, когда параметр принимает новое значение относительно начала перехода или воздействия.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Атрибут времени
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272965"
---
# <a name="time-attribute"></a>Атрибут времени

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`time`Атрибут задает время, когда параметр принимает новое значение относительно начала перехода или воздействия.

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="applies-to"></a>Применение

[**в**](at-element.md), [ **Линейная**](linear-element.md)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> </dl>

 

 



