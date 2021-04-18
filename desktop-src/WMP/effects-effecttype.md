---
title: EFFECTs. Еффекттипе
description: Метод Еффекттипе извлекает имя реестра визуализации с указанным индексом реестра. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- Effect. Еффекттипе Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695036"
---
# <a name="effectseffecttype"></a>EFFECTs. Еффекттипе

Метод **еффекттипе** извлекает имя реестра визуализации с указанным индексом реестра. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*номер*
</dt> <dd>

**Число** (**Long**), содержащее индекс реестра визуализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Этот метод полезен для переключения между визуализациями в скрипте. Пользовательский интерфейс может отображать набор заголовков, но когда пользователь выбирает его, скрипт должен использовать **куррентеффекттипе** для переключения визуализаций.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EFFECTs, элемент**](effects-element.md)
</dt> <dt>

[**EFFECTs. Куррентеффекттипе**](effects-currenteffecttype.md)
</dt> </dl>

 

 





