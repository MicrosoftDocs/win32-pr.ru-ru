---
description: Атрибут «завершение» задает время окончания объекта относительно родительского объекта.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Атрибут завершения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050175"
---
# <a name="stop-attribute"></a>Атрибут завершения

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`stop`Атрибут задает время окончания объекта относительно родительского объекта.

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

 

 



