---
description: Атрибут start указывает время начала объекта относительно родительского объекта.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: начальный атрибут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227b04a8cd7dc366a9cf10a4930233cd834e2bea7faa64bb59c248049b9e9abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650994"
---
# <a name="start-attribute"></a>начальный атрибут

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`start`Атрибут задает время начала объекта относительно родительского объекта.

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="applies-to"></a>Применяется к

[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)

## <a name="see-also"></a>См. также

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинеобж:: Сетстартстоп**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



