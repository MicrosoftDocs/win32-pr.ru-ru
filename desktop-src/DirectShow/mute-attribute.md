---
description: Атрибут «выкл.» указывает состояние отключения объекта.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: отключить атрибут
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140251"
---
# <a name="mute-attribute"></a>отключить атрибут

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`mute`Атрибут указывает состояние отключения объекта. Если значение равно **true**, то ни объект, ни его дочерние элементы не отображаются. Если значение равно **false**, объект визуализируется и его дочерние элементы отображаются в соответствии со своим состоянием отключения. Значение по умолчанию — **false**.

## <a name="possible-values"></a>Возможные значения

Следующие значения определены как TRUE: y, Y, t, T, 1. Следующие значения определены как FALSE: n, N, f, F, 0 (ноль).

## <a name="applies-to"></a>Применение

[**клип**](clip-element.md), [**составной**](composite-element.md), [**эффекты**](effect-element.md), [**Группа**](group-element.md), [**временная шкала**](timeline-element.md), [**Переход**](transition-element.md)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинеобж:: Сетмутед**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



