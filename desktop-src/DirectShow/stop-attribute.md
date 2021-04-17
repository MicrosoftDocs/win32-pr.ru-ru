---
description: Атрибут «завершение» задает время окончания объекта относительно родительского объекта.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Атрибут завершения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684121"
---
# <a name="stop-attribute"></a>Атрибут завершения

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`stop`Атрибут задает время окончания объекта относительно родительского объекта.

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="applies-to"></a>Применение

[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинеобж:: Сетстартстоп**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



