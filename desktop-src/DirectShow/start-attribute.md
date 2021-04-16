---
description: Атрибут start указывает время начала объекта относительно родительского объекта.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: начальный атрибут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684133"
---
# <a name="start-attribute"></a>начальный атрибут

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`start`Атрибут задает время начала объекта относительно родительского объекта.

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

 

 



